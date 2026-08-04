# I. 기본 사항


  * 공동 책임 모델

  * AWS 글로벌 인프라

  * AWS 서비스 복원력

  * AWS 리소스에 대한 액세스 보안

  * 퍼블릭 / 하이브리드 / 프라이빗 / 멀티 클라우드의 차이

  * 계정


# II. IAM 및 인증 / 인가


  1. IAM User

    * AWS 계정이 생성할 수 있는 사용자. Root 사용자 계정을 직접 사용하는 것은 위험하므로 일부 권한만 주어진 하위 계정을 만든다.

	* AWS는 ARN을 이용해 IAM User를 식별한다.

	* IAM Name: AWS Managenent Console 등에서 볼 수 있는 친근한 이름. 같은 AWS 계정 내에서만 식별 가능하다.


	* ARN: Amazon Resource Name. 전체 AWS 영역 내에서 고유한 식별자를 가진다.

	* 표준 ARN 구조: `arn:partition:service:region:account-id:resource`

	* partition: aws (일반 리전), aws-cn (중국), aws-us-gov (미국 정부) etc.

	* service: AWS 서비스 종류. s3, iam, lambda etc.

	* region: 리소스가 위치한 region 이름. ex: ap-northeast-2

	* account-id: 전체 AWS 내에서 고유한 ID. 12자리로 구성

	* resource: 리소스 ID 또는 경로

	* 표준 ARN 예시: `arn:aws:iam::123456789012:user/oscar` (IAM은 전역 서비스이기 때문에 region이 비어있음)


	* IAM 계정에 접근하는 방법

	* 콘솔 패스워드

	* Access Key: 자격이 계속 유효하기 때문에 보안상의 이유로 다른 대안을 추천함

	* SSH Key: ssh-rsa 또는 PEM 형식으로 된 OpsnSSH Format

	* Server Certificates: AWS Certificate Manager(ACM)를 이용하는 것을 추천. 공식 문서에서는 ACM을 지원하지 않는 리전에서는 IAM만 이용하도록 조언함.

	
	* 새로운 IAM User를 생성할 때는 콘솔 패스워드, 액세스 키 중 하나 이상을 반드시 포함해야 함.

	* 기본적으로 AWS CLI, AWS API에 대해서는 어떠한 자격 증명도 없음

	
	* 권한: 기본적으로는 아무 권한도 없음. 최소 권한을 부여한 여러 IAM 계정을 생성하는 방식을 사용

	* IAM User는 오직 하나의 Account에만 소속됨

	
	* 서비스 계정으로서의 IAM User

	* IAM User는 AWS 서비스를 요청하기 위해 자격 증명을 이용하는 애플리케이션에 사용될 수 있음

	* 장기간 유효한 자격증명을 이용할 경우 애플리케이션에 하드코딩하면 안 됨

	* 정해진 위치에서 자격 증명을 주입하기 위해 AWS SDK, AWS CLI를 이용할 수 있음


  2. IAM User Group

    * IAM 사용자의 집합

	* 여러 사용자에게 일괄적으로 권한을 부여하기 위해 사용함

	* User Group과 User는 M : N 관계

	* 단, User Group은 다른 User Group을 포함할 수 없음

	* AWS User를 기본적으로 포함하는 User Group은 없음


  3. Policy

    * 권한을 정의하는 객체

	* 대부분의 정책은 JSON 형식으로 AWS에 저장됨

	
	* 지원하는 정책 종류

	* Identity-Based

	* 예를 들어, 사용자 John이 특정 EC2 리소스를 이용할 수 있는 권한을 John User에게 할당할 수 있다.

	* Resource-Based

	* 예를 들어, 특정 S3 Bucket에 User A, User B가 적혀있는 AllowList를 할당할 수 있다.

	* VPC Endpoint

	* VPC Endpoint를 생성하면 기본적으로 전체 액세스가 허용되지만, 사용자 지정 정책을 연결하여 특정 보안 경계를 구축할 수 있음

	* Permissions Boundaries

	* Identity-Based Policy에서 최대한의 권한을 정의해놓는 기능

	* AWS Organizations Service Control Policies(SCP)

	* 조직 또는 조직 단위 내 모든 Account의 IAM User에게(Root 포함) 일괄적으로 적용할 수 있는 정책

	* 단, Organization을 생성한 Management Account는 영향을 받지 않는다.

	* AWS Organizations Resource Control Policies(RCP)

	* 조직 내부 Account들이 소유한 모든 리소스의 최대 권한을 강제할 때 사용됨

	* 실수로 외부 계정에 외부로 노출해서는 안 되는 리소스를 명시적으로 허용하는 Identity-Based Policy를 설정하더라도, RCP에서 Implicit Deny 또는 Explicit Deny 되었으면 접근이 거부되어 안전장치 역할을 한다.

	* ACL

	* Resource-Based Ploicy와 유사, JSON 형식을 사용하지 않음

	* Resource Access Manager Shares(RAMS)

	* 다른 계정과, 또는 한 Organizations 내에서 리소스를 공유할 수 있다.

	* Session

	* AWS STS에서 생성된 임시 세션에 부여할 수 있는 최대 권한


  4. Permission Boundaries

    * 자격 증명 정책에서 허용할 수 있는 최대한의 권한을 정의해놓는 기능

	
	* 주의사항

    * 권한의 최대 범위를 지정하지만 권한 자체를 부여하지는 않는다.

    * 예를 들어 최대 권한을 s3, Cloudwatch, ec2만 지정하면 IAM에 대한 권한을 부여하더라도 작업이 거부된다.


  5. IAM Identity Center

    * 개별 계정을 IAM으로 따로 관리하지 않고, 여러 AWS 계정과 클라우드 애플리케이션에 대한 접근 권한을 중앙에서 관리할 수 있다.

	* 여러 계정에 일괄적으로 권한을 할당할 수 있다.


  6. Cross Account Access

    * 다른 계정의 리소스에 접근할 수 있도록 하는 서비스

	* 리소스를 직접 공유하려면 해당 리소스가 Resource-Based Policy를 지원해야 한다.

	* Role을 이용할 수도 있다.

	* Identity-Based Policy와 Resource-Based Policy 둘 중 하나만 있으면 된다.


  7. Federation

    * 외부의 인증 시스템을 활용해 별도의 IAM 사용자 생성 없이 AWS 리소스에 안전하게 임시 접근하도록 지원하는 보안 메커니즘
