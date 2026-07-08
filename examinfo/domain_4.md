

# 콘텐츠 도메인 4: 비용에 최적화된 아키텍처 설계
<a name="solutions-architect-associate-03-domain4"></a>

**Topics**
+ [작업 4.1: 비용에 최적화된 스토리지 솔루션 설계](#solutions-architect-associate-03-domain4-task1)
+ [작업 4.2: 비용에 최적화된 컴퓨팅 솔루션 설계](#solutions-architect-associate-03-domain4-task2)
+ [작업 4.3: 비용에 최적화된 데이터베이스 솔루션 설계](#solutions-architect-associate-03-domain4-task3)
+ [작업 4.4: 비용에 최적화된 네트워크 아키텍처 설계](#solutions-architect-associate-03-domain4-task4)

## 작업 4.1: 비용에 최적화된 스토리지 솔루션 설계
<a name="solutions-architect-associate-03-domain4-task1"></a>

관련 지식:
+ 액세스 옵션(예: 요청자 지불 객체 스토리지가 포함된 S3 버킷)
+ AWS 비용 관리 서비스 기능(예: 비용 할당 태그, 다중 계정 결제)
+ AWS 비용 관리 도구와 적합한 사용 사례(예: AWS Cost Explorer, AWS Budgets, AWS Cost and Usage Report)
+ AWS 스토리지 서비스와 적합한 사용 사례(예: Amazon FSx, Amazon EFS, Amazon S3, Amazon EBS)
+ 백업 전략
+ 블록 스토리지 옵션(예: 하드 디스크 드라이브(HDD) 볼륨 유형, 솔리드 스테이트 드라이브(SSD) 볼륨 유형)
+ 데이터 수명 주기
+ 하이브리드 스토리지 옵션(예: AWS DataSync, AWS Transfer Family, AWS Storage Gateway)
+ 스토리지 액세스 패턴
+ 스토리지 계층화(예: 객체 스토리지의 콜드 계층화)
+ 연관된 특성이 있는 스토리지 유형(예: 객체, 파일, 블록)

관련 기술:
+ 적합한 스토리지 전략 설계(예: Amazon S3에 배치 업로드와 개별 업로드 비교)
+ 워크로드에 올바른 스토리지 크기 결정
+ 워크로드에 대한 데이터를 AWS 스토리지로 전송하는 가장 저렴한 방법 결정
+ 스토리지 오토 스케일링이 필요한 시점 결정
+ S3 객체 수명 주기 관리
+ 적합한 백업 및/또는 아카이브 솔루션 선택
+ 스토리지 서비스로의 데이터 마이그레이션에 적합한 서비스 선택
+ 적합한 스토리지 티어 선택
+ 스토리지에 올바른 데이터 수명 주기 선택
+ 워크로드에 가장 비용 효율적인 스토리지 서비스 선택

## 작업 4.2: 비용에 최적화된 컴퓨팅 솔루션 설계
<a name="solutions-architect-associate-03-domain4-task2"></a>

관련 지식:
+ AWS 비용 관리 서비스 기능(예: 비용 할당 태그, 다중 계정 결제)
+ AWS 비용 관리 도구와 적합한 사용 사례(예: AWS Cost Explorer, AWS Budgets, AWS Cost and Usage Report)
+ AWS 글로벌 인프라(예: 가용 영역, AWS 리전)
+ AWS 구매 옵션(예: 스팟 인스턴스, 예약 인스턴스, 절감형 플랜)
+ 분산 컴퓨팅 전략(예: 엣지 프로세싱)
+ 하이브리드 컴퓨팅 옵션(예: AWS Outposts)
+ 인스턴스 유형, 패밀리 및 크기(예: 메모리 최적화, 컴퓨팅 최적화, 가상화)
+ 컴퓨팅 사용률 최적화(예: 컨테이너, 서버리스 컴퓨팅, 마이크로서비스)
+ 크기 조정 전략(예: 오토 스케일링, 최대 절전 모드)

관련 기술:
+ 적합한 로드 밸런싱 전략 결정(예: Application Load Balancer(계층 7)와 Network Load Balancer(계층 4)와 Gateway Load Balancer 비교)
+ 탄력적인 워크로드에 적합한 스케일링 방법 및 전략 결정(예: 수평과 수직 비교, EC2 최대 절전 모드)
+ 적합한 사용 사례로 비용 효율적인 AWS 컴퓨팅 서비스 결정(예: AWS Lambda, Amazon EC2, AWS Fargate)
+ 다양한 워크로드 클래스에 필요한 가용성 결정(예: 프로덕션 워크로드, 비프로덕션 워크로드)
+ 워크로드에 적합한 인스턴스 패밀리 선택
+ 워크로드에 적합한 인스턴스 크기 선택

## 작업 4.3: 비용에 최적화된 데이터베이스 솔루션 설계
<a name="solutions-architect-associate-03-domain4-task3"></a>

관련 지식:
+ AWS 비용 관리 서비스 기능(예: 비용 할당 태그, 다중 계정 결제)
+ AWS 비용 관리 도구와 적합한 사용 사례(예: AWS Cost Explorer, AWS Budgets, AWS Cost and Usage Report)
+ 캐싱 전략
+ 데이터 보존 정책
+ 데이터베이스 용량 계획(예: 용량 단위)
+ 데이터베이스 연결 및 프록시
+ 데이터베이스 엔진과 적합한 사용 사례(예: 이기종 마이그레이션, 동종 마이그레이션)
+ 데이터베이스 복제(예: 읽기 전용 복제본)
+ 데이터베이스 유형 및 서비스(예: 관계형과 비관계형 비교, Amazon Aurora, Amazon DynamoDB)

관련 기술:
+ 적합한 백업 및 보존 정책 설계(예: 스냅샷 빈도)
+ 적합한 데이터베이스 엔진 결정(예: MySQL과 PostgreSQL 비교)
+ 적합한 사용 사례로 비용 효율적인 AWS 데이터베이스 서비스 결정(예: DynamoDB와 Amazon RDS 비교, 서버리스)
+ 비용 효율적인 AWS 데이터베이스 유형 결정(예: 시계열 형식, 열 형식)
+ 데이터베이스 스키마와 데이터를 다른 위치 및/또는 다른 데이터베이스 엔진으로 마이그레이션

## 작업 4.4: 비용에 최적화된 네트워크 아키텍처 설계
<a name="solutions-architect-associate-03-domain4-task4"></a>

관련 지식:
+ AWS 비용 관리 서비스 기능(예: 비용 할당 태그, 다중 계정 결제)
+ AWS 비용 관리 도구와 적합한 사용 사례(예: AWS Cost Explorer, AWS Budgets, AWS Cost and Usage Report)
+ 로드 밸런싱 개념(예: Application Load Balancer)
+ NAT 게이트웨이(예: NAT 인스턴스 비용과 NAT 게이트웨이 비용 비교)
+ 네트워크 연결(예: 프라이빗 회선, 전용 회선, VPN)
+ 네트워크 라우팅, 토폴로지 및 피어링(예: AWS Transit Gateway, VPC 피어링)
+ 네트워크 서비스와 적합한 사용 사례(예: DNS)

관련 기술:
+ 네트워크에 적합한 NAT 게이트웨이 유형 구성(예: 단일 공유 NAT 게이트웨이와 각 가용 영역의 NAT 게이트웨이 비교)
+ 적합한 네트워크 연결 구성(예: AWS Direct Connect와 VPN과 인터넷 비교)
+ 네트워크 전송 비용을 최소화하는 데 적합한 네트워크 경로 구성(예: 리전 간, 가용 영역 간, 프라이빗과 퍼블릭 간, AWS Global Accelerator, VPC 엔드포인트)
+ 콘텐츠 전송 네트워크(CDN) 및 엣지 캐싱에 대한 전략적 요구 사항 결정
+ 네트워크 최적화를 위한 기존 워크로드 검토
+ 적합한 제한 전략 선택
+ 네트워크 디바이스에 적합한 대역폭 할당 선택(예: 단일 VPN과 복수 VPN 비교, Direct Connect 속도)
