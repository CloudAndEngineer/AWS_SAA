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

  3. IAM Policy

    * 권한을 정의하는 객체

	* 대부분의 정책은 JSON 형식으로 AWS에 저장됨

	
	* 지원하는 정책 종류

	* Identity-Based

	* Resource-Based

	* VPC Endpoint

	* Permissions Boundaries

	* AWS Organizations Service Control Policies(SCP)

	* AWS Organizations Resource Control Policies(RCP)

	* ACL

	* Resource Access Manager Shares(RAMS)

	* Session
