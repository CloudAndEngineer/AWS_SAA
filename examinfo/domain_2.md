

# 콘텐츠 도메인 2: 복원력을 갖춘 아키텍처 설계
<a name="solutions-architect-associate-03-domain2"></a>

**Topics**
+ [작업 2.1: 확장 가능하고 느슨하게 결합된 아키텍처 설계](#solutions-architect-associate-03-domain2-task1)
+ [작업 2.2: 고가용성 및/또는 내결함성 아키텍처 설계](#solutions-architect-associate-03-domain2-task2)

## 작업 2.1: 확장 가능하고 느슨하게 결합된 아키텍처 설계
<a name="solutions-architect-associate-03-domain2-task1"></a>

관련 지식:
+ API 만들기 및 관리(예: Amazon API Gateway, REST API)
+ AWS Managed Services와 적합한 사용 사례(예: AWS Transfer Family, Amazon SQS, AWS Secrets Manager)
+ 캐싱 전략
+ 마이크로서비스의 설계 원칙(예: 스테이트리스 워크로드와 스테이트풀 워크로드 비교)
+ 이벤트 기반 아키텍처
+ 수평적 스케일링 및 수직적 스케일링
+ 엣지 액셀러레이터를 적절하게 사용하는 방법(예: 콘텐츠 전송 네트워크(CDN))
+ 애플리케이션을 컨테이너로 마이그레이션하는 방법
+ 로드 밸런싱 개념(예: Application Load Balancer(ALB))
+ 멀티 티어 아키텍처
+ 대기열 및 메시징 개념(예: 게시/구독)
+ 서버리스 기술 및 패턴(예: AWS Fargate, AWS Lambda)
+ 연관된 특성이 있는 스토리지 유형(예: 객체, 파일, 블록)
+ 컨테이너의 오케스트레이션(예: Amazon ECS, Amazon EKS)
+ 읽기 전용 복제본 사용 시기
+ 워크플로 오케스트레이션(예: AWS Step Functions)

관련 기술:
+ 요구 사항에 따라 이벤트 기반, 마이크로서비스 및/또는 멀티 티어 아키텍처 설계
+ 아키텍처 설계에 사용되는 구성 요소의 스케일링 전략 결정
+ 요구 사항에 따라 느슨한 결합을 달성하는 데 필요한 AWS 서비스 결정
+ 컨테이너 사용 시기 결정
+ 서버리스 기술 및 패턴 사용 시기 결정
+ 요구 사항에 따라 적합한 컴퓨팅, 스토리지, 네트워킹 및 데이터베이스 기술 권장
+ 워크로드에 맞춰 특별히 구축된 AWS 서비스 사용

## 작업 2.2: 고가용성 및/또는 내결함성 아키텍처 설계
<a name="solutions-architect-associate-03-domain2-task2"></a>

관련 지식:
+ AWS 글로벌 인프라(예: 가용 영역, AWS 리전, Amazon Route 53)
+ AWS Managed Services와 적합한 사용 사례(예: Amazon Comprehend, Amazon Polly)
+ 기본 네트워킹 개념(예: 라우팅 테이블)
+ 재해 복구(DR) 전략(예: 백업 및 복원, 파일럿 라이트, 예열 대기 방식, 활성/활성 장애 조치, RPO(복구 시점 목표), RTO(복구 시간 목표))
+ 분산 설계 패턴
+ 장애 조치 전략
+ 변경 불가능한 인프라
+ 로드 밸런싱 개념(예: ALB)
+ 프록시 개념(예: Amazon RDS Proxy)
+ Service Quotas 및 제한(예: 대기 환경에서 워크로드에 대한 Service Quotas를 구성하는 방법)
+ 스토리지 옵션 및 특성(예: 내구성, 복제)
+ 워크로드 가시성(예: AWS X-Ray)

관련 기술:
+ 인프라 무결성을 보장하기 위한 자동화 전략 결정
+ AWS 리전 또는 가용 영역 전체에서 고가용성 및/또는 내결함성 아키텍처를 제공하는 데 필요한 AWS 서비스 결정
+ 비즈니스 요구 사항에 따라 지표를 파악하여 고가용성 솔루션 제공
+ 단일 실패 지점을 완화하기 위한 설계 구현
+ 데이터의 내구성과 가용성을 보장하기 위한 전략 구현(예: 백업)
+ 비즈니스 요구 사항을 충족하는 적합한 DR 전략 선택
+ 레거시 애플리케이션과 클라우드용으로 구축되지 않은 애플리케이션의 신뢰성을 개선하는 AWS 서비스 사용(예: 애플리케이션 변경이 불가능한 경우)
+ 워크로드에 맞춰 특별히 구축된 AWS 서비스 사용
