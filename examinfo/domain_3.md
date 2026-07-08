

# 콘텐츠 도메인 3: 고성능 아키텍처 설계
<a name="solutions-architect-associate-03-domain3"></a>

**Topics**
+ [작업 3.1: 고성능 및/또는 확장 가능한 스토리지 솔루션 결정](#solutions-architect-associate-03-domain3-task1)
+ [작업 3.2: 고성능의 탄력적인 컴퓨팅 솔루션 설계](#solutions-architect-associate-03-domain3-task2)
+ [작업 3.3: 고성능 데이터베이스 솔루션 결정](#solutions-architect-associate-03-domain3-task3)
+ [작업 3.4: 고성능 및/또는 확장 가능한 네트워크 아키텍처 결정](#solutions-architect-associate-03-domain3-task4)
+ [작업 3.5: 고성능 데이터 수집 및 변환 솔루션 결정](#solutions-architect-associate-03-domain3-task5)

## 작업 3.1: 고성능 및/또는 확장 가능한 스토리지 솔루션 결정
<a name="solutions-architect-associate-03-domain3-task1"></a>

관련 지식:
+ 비즈니스 요구 사항을 충족하는 하이브리드 스토리지 솔루션
+ 스토리지 서비스와 적합한 사용 사례(예: Amazon S3, Amazon EFS, Amazon EBS)
+ 연관된 특성이 있는 스토리지 유형(예: 객체, 파일, 블록)

관련 기술:
+ 성능 요구 사항을 충족하는 스토리지 서비스 및 구성 결정
+ 향후 요구 사항을 수용하도록 규모 조정 가능한 스토리지 서비스 결정

## 작업 3.2: 고성능의 탄력적인 컴퓨팅 솔루션 설계
<a name="solutions-architect-associate-03-domain3-task2"></a>

관련 지식:
+ AWS 컴퓨팅 서비스와 적합한 사용 사례(예: AWS Batch, Amazon EMR, AWS Fargate)
+ AWS 글로벌 인프라 및 엣지 서비스에서 지원하는 분산 컴퓨팅 개념
+ 대기열 및 메시징 개념(예: 게시/구독)
+ 확장성 기능과 적합한 사용 사례(예: Amazon EC2 Auto Scaling, AWS Auto Scaling)
+ 서버리스 기술 및 패턴(예: AWS Lambda, Fargate)
+ 컨테이너의 오케스트레이션(예: Amazon ECS, Amazon EKS)

관련 기술:
+ 구성 요소 크기를 독립적으로 규모를 조정할 수 있도록 워크로드 분리
+ 스케일링 작업을 수행하기 위한 지표 및 조건 파악
+ 비즈니스 요구 사항을 충족하는 적합한 컴퓨팅 옵션 및 기능 선택(예: EC2 인스턴스 유형)
+ 비즈니스 요구 사항을 충족하는 적합한 리소스 유형 및 크기 선택(예: Lambda 메모리 양)

## 작업 3.3: 고성능 데이터베이스 솔루션 결정
<a name="solutions-architect-associate-03-domain3-task3"></a>

관련 지식:
+ AWS 글로벌 인프라(예: 가용 영역, AWS 리전)
+ 캐싱 전략 및 서비스(예: Amazon ElastiCache)
+ 데이터 액세스 패턴(예: 읽기 집약적 패턴과 쓰기 집약적 패턴 비교)
+ 데이터베이스 용량 계획(예: 용량 단위, 인스턴스 유형, 프로비저닝된 IOPS)
+ 데이터베이스 연결 및 프록시
+ 데이터베이스 엔진과 적합한 사용 사례(예: 이기종 마이그레이션, 동종 마이그레이션)
+ 데이터베이스 복제(예: 읽기 전용 복제본)
+ 데이터베이스 유형 및 서비스(예: 서버리스, 관계형과 비관계형 비교, 인 메모리)

관련 기술:
+ 비즈니스 요구 사항을 충족하도록 읽기 전용 복제본 구성
+ 데이터베이스 아키텍처 설계
+ 적합한 데이터베이스 엔진 결정(예: MySQL과 PostgreSQL 비교)
+ 적합한 데이터베이스 유형 결정(예: Amazon Aurora, Amazon DynamoDB)
+ 비즈니스 요구 사항을 충족하도록 캐싱 통합

## 작업 3.4: 고성능 및/또는 확장 가능한 네트워크 아키텍처 결정
<a name="solutions-architect-associate-03-domain3-task4"></a>

관련 지식:
+ 엣지 네트워킹 서비스와 적합한 사용 사례(예: Amazon CloudFront, AWS Global Accelerator)
+ 네트워크 아키텍처 설계 방법(예: 서브넷 티어, 라우팅, IP 주소 지정)
+ 로드 밸런싱 개념(예: Application Load Balancer)
+ 네트워크 연결 옵션(예: AWS VPN, AWS Direct Connect, AWS PrivateLink)

관련 기술:
+ 다양한 아키텍처에 대한 네트워크 토폴로지 만들기(예: 글로벌, 하이브리드, 멀티 티어)
+ 향후 요구 사항을 수용하도록 규모 조정 가능한 네트워크 구성 결정
+ 비즈니스 요구 사항을 충족하는 적합한 리소스 배치 결정
+ 적합한 로드 밸런싱 전략 선택

## 작업 3.5: 고성능 데이터 수집 및 변환 솔루션 결정
<a name="solutions-architect-associate-03-domain3-task5"></a>

관련 지식:
+ 데이터 분석 및 시각화 서비스와 적합한 사용 사례(예: Amazon Athena, AWS Lake Formation, Amazon QuickSuite)
+ 데이터 수집 패턴(예: 빈도)
+ 데이터 전송 서비스와 적합한 사용 사례(예: AWS DataSync, AWS Storage Gateway)
+ 데이터 변환 서비스와 적합한 사용 사례(예: AWS Glue)
+ 수집 액세스 포인트에 대한 보안 액세스
+ 비즈니스 요구 사항을 충족하는 데 필요한 크기 및 속도
+ 스트리밍 데이터 서비스와 적합한 사용 사례(예: Amazon Kinesis)

관련 기술:
+ 데이터 레이크 구축 및 보호
+ 데이터 스트리밍 아키텍처 설계
+ 데이터 전송 솔루션 설계
+ 시각화 전략 구현
+ 데이터 처리에 적합한 컴퓨팅 옵션 선택(예: Amazon EMR)
+ 수집에 적합한 구성 선택
+ 데이터 형식 변환(예: .csv에서.parquet으로 변환)
