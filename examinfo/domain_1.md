

# 콘텐츠 도메인 1: 보안 아키텍처 설계
<a name="solutions-architect-associate-03-domain1"></a>

**Topics**
+ [작업 1.1: AWS 리소스에 대한 보안 액세스 설계](#solutions-architect-associate-03-domain1-task1)
+ [작업 1.2: 안전한 워크로드 및 애플리케이션 설계](#solutions-architect-associate-03-domain1-task2)
+ [작업 1.3: 적합한 데이터 보안 제어 결정](#solutions-architect-associate-03-domain1-task3)

## 작업 1.1: AWS 리소스에 대한 보안 액세스 설계
<a name="solutions-architect-associate-03-domain1-task1"></a>

관련 지식:
+ 여러 계정에 대한 액세스 제어 및 관리
+ AWS 페더레이션된 액세스 및 ID 서비스(예: IAM, AWS IAM Identity Center)
+ AWS 글로벌 인프라(예: 가용 영역, AWS 리전)
+ AWS 보안 모범 사례(예: 최소 권한의 원칙)
+ AWS 공동 책임 모델

관련 기술:
+ IAM 사용자 및 루트 사용자에게 AWS 보안 모범 사례 적용(예: 다중 인증(MFA))
+ IAM 사용자, 그룹, 역할 및 정책을 포함하는 유연한 권한 부여 모델 설계
+ 역할 기반 액세스 제어 전략 설계(예: AWS STS, 역할 전환, 크로스 계정 액세스)
+ 여러 AWS 계정에 대한 보안 전략 설계(예: AWS Control Tower, 서비스 제어 정책(SCP))
+ AWS 서비스에 적합한 리소스 정책 사용 결정
+ 디렉터리 서비스를 IAM 역할과 연동할 시기 결정

## 작업 1.2: 안전한 워크로드 및 애플리케이션 설계
<a name="solutions-architect-associate-03-domain1-task2"></a>

관련 지식:
+ 애플리케이션 구성 및 보안 인증 정보의 보안
+ AWS 서비스 엔드포인트
+ AWS에서 포트, 프로토콜 및 네트워크 트래픽 제어
+ 안전한 애플리케이션 액세스
+ 적절한 사용 사례를 갖춘 보안 서비스(예: AWS Cognito, AWS GuardDuty, AWS Macie)
+ AWS 외부의 위협 벡터(예: DDoS, SQL 인젝션)

관련 기술:
+ 보안 구성 요소(예: 보안 그룹, 라우팅 테이블, 네트워크 ACL, NAT 게이트웨이)로 VPC 아키텍처 설계
+ 네트워크 분할 전략 결정(예: 퍼블릭 서브넷 및 프라이빗 서브넷 사용)
+ 보안 애플리케이션에 AWS 서비스 통합(예: AWS Shield, AWS WAF, IAM Identity Center, AWS Secrets Manager)
+ AWS 클라우드와의 외부 네트워크 연결 보호(예: VPN, AWS Direct Connect)

## 작업 1.3: 적합한 데이터 보안 제어 결정
<a name="solutions-architect-associate-03-domain1-task3"></a>

관련 지식:
+ 데이터 액세스 및 거버넌스
+ 데이터 복구
+ 데이터 보존 및 분류
+ 암호화 및 적합한 키 관리

관련 기술:
+ 규정 준수 요구 사항을 충족하도록 AWS 기술 조율
+ 저장된 데이터 암호화(예: AWS KMS)
+ 전송 중 데이터 암호화(예: TLS를 사용하는 AWS Certificate Manager(ACM))
+ 암호화 키에 대한 액세스 정책 구현
+ 데이터 백업 및 복제 구현
+ 데이터 액세스, 수명 주기 및 보호를 위한 정책 구현
+ 암호화 키 교체 및 인증서 갱신
