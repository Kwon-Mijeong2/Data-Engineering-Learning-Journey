# Glossary (용어 정리)

데이터 엔지니어링 학습 및 면접 대비를 위한 주요 용어 정리입니다.  
카테고리별로 핵심 개념을 정리하고, **간단한 정의 + 예시** 중심으로 기록합니다.  

---

## 1. Database & SQL

- **RDBMS (관계형 데이터베이스)**  
  데이터를 행(Row)과 열(Column)로 구성된 테이블 형태로 관리하는 DBMS.  
  👉 예: MySQL, PostgreSQL  

- **NoSQL (Document, Key-Value, Column, Graph DB)**  
  비정형 데이터 처리에 적합한 비관계형 DBMS.  
  👉 예: MongoDB(Document), Redis(Key-Value), Cassandra(Column), Neo4j(Graph)  

- **Index / Clustered vs Non-clustered Index**  
  데이터를 빠르게 검색하기 위한 자료 구조.  
  - Clustered: 데이터 자체가 정렬되어 저장됨 (테이블 = 인덱스)  
  - Non-clustered: 별도 인덱스 구조가 생성됨 (책의 목차 역할)  

- **Transaction / ACID**  
  DB의 일련의 작업 단위. 원자성(Atomicity), 일관성(Consistency), 고립성(Isolation), 지속성(Durability) 보장.  

- **Normalization / Denormalization**  
  - 정규화: 데이터 중복 최소화 → 저장 효율성 ↑  
  - 반정규화: 성능 최적화를 위해 의도적으로 중복 허용  

- **Stored Procedure / Trigger**  
  - Stored Procedure: DB에 저장된 재사용 가능한 SQL 코드 블록  
  - Trigger: 특정 이벤트(INSERT/UPDATE/DELETE) 발생 시 자동 실행되는 SQL  

- **Partitioning / Sharding**  
  - Partitioning: 하나의 DB 테이블을 여러 파티션으로 나누어 저장  
  - Sharding: DB 자체를 여러 서버(샤드)로 분산  

- **Query Optimization**  
  실행 계획을 개선하여 쿼리 성능을 높이는 기법.  
  👉 예: 인덱스 활용, JOIN 순서 조정  

---

## 2. Data Engineering

- **ETL / ELT**  
  - ETL: Extract → Transform → Load (전통적 DW 방식)  
  - ELT: Extract → Load → Transform (BigQuery, Snowflake 같은 MPP DB 활용)  

- **Data Pipeline**  
  데이터를 수집, 변환, 저장, 분석까지 이어주는 자동화된 데이터 흐름.  

- **Batch Processing vs Stream Processing**  
  - Batch: 일정량 데이터를 모아 일괄 처리 (예: 하루 단위 리포트)  
  - Stream: 데이터가 들어오는 즉시 처리 (예: 실시간 알림)  

- **Orchestration (Airflow, Step Functions 등)**  
  여러 작업(Job)을 순서와 조건에 따라 자동 실행/관리하는 것.  

- **Data Lake / Data Warehouse**  
  - Data Lake: 원천 데이터를 가공 없이 저장 (S3, HDFS)  
  - Data Warehouse: 분석용으로 정제된 데이터 저장소 (Redshift, BigQuery)  

- **Schema on Write vs Schema on Read**  
  - Write: 저장 시 스키마 적용 (DW)  
  - Read: 읽을 때 스키마 적용 (Data Lake)  

- **Data Quality / Data Governance**  
  - Data Quality: 결측치, 중복, 오류 없는 신뢰성 높은 데이터 확보  
  - Governance: 권한, 보안, 데이터 정책 관리  

---

## 3. Distributed Systems

- **MapReduce**  
  분산 환경에서 데이터를 Map(분할) → Reduce(집계) 단계로 처리하는 방식. (Hadoop 기본 구조)  

- **Spark (RDD, DataFrame, Catalyst Optimizer)**  
  대규모 데이터를 메모리 기반으로 빠르게 처리하는 분산 프레임워크.  
  👉 RDD(저수준 API), DataFrame(고수준 API), Catalyst(쿼리 최적화 엔진)  

- **Hadoop Ecosystem**  
  HDFS(저장소) + YARN(자원 관리) + Hive/Impala(SQL 인터페이스) 등  

- **Kafka (Topic, Partition, Consumer Group)**  
  - Topic: 데이터 스트림의 카테고리  
  - Partition: 병렬 처리 단위  
  - Consumer Group: 메시지를 병렬 소비하는 단위  

- **Message Queue vs Pub/Sub**  
  - MQ: 메시지를 FIFO 방식으로 소비 (RabbitMQ)  
  - Pub/Sub: 발행/구독 구조 (Kafka, GCP Pub/Sub)  

- **Event-driven Architecture**  
  이벤트(상태 변화)가 발생하면 즉시 트리거되는 시스템 설계 패턴.  

- **CAP Theorem**  
  분산 시스템은 **Consistency / Availability / Partition Tolerance** 중 2개만 보장 가능.  

---

## 4. Cloud & Infra

- **IaaS / PaaS / SaaS**  
  - IaaS: 가상머신/스토리지 제공 (AWS EC2)  
  - PaaS: 앱 실행 환경 제공 (Heroku, GCP App Engine)  
  - SaaS: 소프트웨어 서비스 (Google Docs, Slack)  

- **Serverless**  
  서버 관리 없이 코드만 배포 (AWS Lambda)  

- **VPC, Subnet, Security Group**  
  클라우드 네트워크 보안 구조.  
  👉 VPC(가상 네트워크), Subnet(IP 블록), SG(방화벽 규칙)  

- **IAM (Identity and Access Management)**  
  사용자/서비스 권한 관리 (AWS IAM Role, Policy)  

- **Object Storage vs Block Storage**  
  - Object: 파일 단위 저장 (S3)  
  - Block: 디스크 블록 단위 저장 (EBS)  

- **Auto Scaling**  
  트래픽 변화에 따라 인스턴스 자동 증가/감소  

- **Infrastructure as Code (Terraform, CloudFormation)**  
  인프라 환경을 코드로 정의 → 버전 관리 가능  

- **Containerization (Docker)**  
  앱과 실행 환경을 이미지로 묶어 실행 → 이식성 강화  

- **Kubernetes (Pod, Node, Deployment, Service)**  
  컨테이너 오케스트레이션 도구.  
  👉 Pod(최소 실행 단위), Node(서버), Deployment(배포 관리), Service(네트워크 연결)  

---

## 5. DevOps & Monitoring

- **CI/CD**  
  지속적 통합/배포 → 코드 변경을 자동으로 테스트/배포  

- **GitOps**  
  Git 저장소를 단일 진실 소스로 활용하는 DevOps 방법론  

- **Observability vs Monitoring**  
  - Monitoring: 미리 정의된 지표를 관찰  
  - Observability: 시스템 내부 상태를 추론할 수 있도록 설계  

- **Metrics, Logs, Traces**  
  - Metrics: 수치형 지표 (CPU, 메모리)  
  - Logs: 이벤트 기록  
  - Traces: 요청 단위 흐름 추적  

- **Prometheus / Grafana**  
  모니터링 & 시각화 도구 (Prometheus = 데이터 수집, Grafana = 대시보드)  

- **CloudWatch**  
  AWS 모니터링 서비스  

- **SLA / SLO / SLI**  
  - SLA: 고객과 맺는 서비스 수준 계약  
  - SLO: 서비스 제공자가 목표로 삼는 지표  
  - SLI: 실제 측정되는 지표 값  

---

## 6. BI & Visualization

- **OLTP vs OLAP**  
  - OLTP: 온라인 거래 처리 (실시간 CRUD)  
  - OLAP: 분석 쿼리 처리 (집계, 통계)  

- **Star Schema / Snowflake Schema**  
  - Star: Fact 테이블 중심 + Dimension 테이블 단순 구조  
  - Snowflake: Dimension이 정규화된 복잡한 구조  

- **Dashboard vs Report**  
  - Dashboard: 실시간 모니터링 뷰  
  - Report: 정기적 보고서  

- **Data Modeling**  
  데이터 구조를 설계하는 과정 (ERD, Fact/Dimension 설계 포함)  

- **Drill-down / Roll-up**  
  OLAP 분석 기법.  
  👉 Drill-down: 세부 데이터로 내려가기  
  👉 Roll-up: 집계 수준을 올리기  

- **KPI (Key Performance Indicator)**  
  성과 측정을 위한 핵심 지표.  

---

## 7. General CS / Interview Basics

- **Time Complexity (Big-O, Big-Theta, Big-Omega)**  
  알고리즘 성능을 입력 크기에 따라 분석하는 방법.  
  👉 Big-O(상한), Big-Theta(평균), Big-Omega(하한)  

- **Network Protocols (TCP/IP, HTTP, gRPC)**  
  - TCP/IP: 인터넷 기본 전송 계층  
  - HTTP: 요청-응답 기반 프로토콜  
  - gRPC: 구글의 경량 고성능 RPC 프레임워크  

- **REST API vs GraphQL**  
  - REST: 엔드포인트별 리소스 CRUD  
  - GraphQL: 단일 엔드포인트, 클라이언트가 원하는 데이터만 요청  

- **Serialization (JSON, Avro, Parquet, ORC)**  
  데이터를 전송/저장을 위해 구조화하는 포맷.  
  👉 JSON(텍스트), Avro/Parquet/ORC(컬럼 기반 바이너리, 빅데이터 친화적)  

- **Caching (Redis, Memcached)**  
  자주 쓰는 데이터를 메모리에 저장 → 성능 향상  

- **Consistency Models (Strong, Eventual)**  
  - Strong: 즉시 일관성 보장  
  - Eventual: 지연 후 최종적으로 일관성 수렴  

- **Idempotency**  
  같은 요청을 여러 번 보내도 결과가 동일하게 유지되는 성질.  
  👉 예: "결제 취소" 요청  
