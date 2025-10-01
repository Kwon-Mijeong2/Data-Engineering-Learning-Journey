# 🗺️ Data Engineering Learning Roadmap (2025.11 ~ 2026.05)

본 문서는 데이터 엔지니어 신입 취업을 목표로 한 7개월 학습 로드맵입니다.  
SQL·Python 기초 이후, 데이터 엔지니어링 전반의 기술 스택을 단계별로 학습하고 프로젝트로 연결합니다.  

---

## 🔹 2025년 11월 — 필수 스킬 & 협업 기초

### 🎯 학습 목표
- Git & GitHub 협업 (브랜치 전략, Pull Request, Merge)
- Python 객체지향 & 모듈화
- 데이터 품질 기초: Pytest, Unit Test
- Docker 기초 (단일 컨테이너 → Docker Compose)
- 파이썬 logging
- 용어/개념 정리: Neo4j, Flink, Terraform

### 🛠️ 미니 프로젝트
- GitHub 협업 시뮬레이션 (branch → PR → merge)
- Python 모듈/패키지 작성 + Pytest 적용
- Dockerfile 작성 → DB + 앱 환경 Docker Compose로 실행

### 🔍 추가 학습/보완
- Great Expectations 맛보기

---

## 🔹 2025년 12월 — 워크플로우 & 배치 ETL

### 🎯 학습 목표
- Apache Airflow (DAG 작성, 스케줄링)
- GitHub Actions (CI/CD 기초)
- 데이터 품질 검증 (Great Expectations)
- BI 툴 학습 (QuickSight or Looker Studio 중 1개 집중)

### 🚀 프로젝트
**Batch ETL 파이프라인 구축**
- Airflow DAG → 매일 S3 Raw Data 업로드
- PostgreSQL 적재
- dbt 변환 (Fact/Dimension 테이블)
- Great Expectations 품질 검증
- BI 도구로 대시보드 구성

### 🔍 추가 학습/보완
- Airflow: XCom, Operator, Sensor 기초
- GitHub Actions: pytest + flake8 자동 실행
- 프로젝트: GitHub Repo + 아키텍처 다이어그램 + Airflow Task 로그 기록 포함

---

## 🔹 2026년 1월 — 분산 처리 기초

### 🎯 학습 목표
- Apache Spark (로컬 → AWS EMR)
- 대용량 데이터셋 처리 (CSV/Parquet)

### 🛠️ 미니 프로젝트
- Spark로 수백 MB 데이터 처리 → S3 저장
- Spark SQL vs Pandas 성능 비교

### 🔍 추가 학습/보완
- 1GB~10GB 이상 데이터 실험 → 분산 처리 체감
- Spark DataFrame API & SQL 병행
- UDF 작성 및 성능 차이 확인

---

## 🔹 2026년 2월 — 실시간 데이터 파이프라인

### 🎯 학습 목표
- Apache Kafka, AWS SQS/SNS
- Spark Streaming (Structured Streaming 중심)
- Flink 기초
- Redis (캐시 & 메시지 큐 활용)

### 🛠️ 미니 프로젝트
- Kafka 토픽 생성 → 트위터/로그 API 스트리밍 → PostgreSQL 저장
- AWS SQS → Lambda → DynamoDB 파이프라인
- Redis 캐싱/큐 처리 실습

### 🔍 추가 학습/보완
- Kafka Connect + Schema Registry 기본 실습
- Redis: 캐싱 예제 + Pub/Sub 알림 시스템 두 가지 활용

---

## 🔹 2026년 3월 — 데이터 웨어하우스 & 모니터링

### 🎯 학습 목표
- Redshift, BigQuery
- 데이터 품질 관리 심화 (Great Expectations 고급)
- 모니터링: Prometheus, Grafana, CloudWatch
- 데이터 거버넌스 & GDPR
- Neo4j (Graph DB 기초)

### 🛠️ 미니 프로젝트
- Redshift 적재 후 BI 툴 연결
- Prometheus + Grafana로 Airflow 모니터링
- Neo4j 실습 (추천/소셜 네트워크 모델링)

### 🔍 추가 학습/보완
- DW: 분산 키, Sort Key, Partition 최적화
- 모니터링: Airflow DAG 실패 시 Slack/Discord 알림
- 데이터 카탈로그: AWS Glue Data Catalog or DataHub

---

## 🔹 2026년 4월 — 자동화 & 테스트

### 🎯 학습 목표
- Terraform / AWS CDK (IaC)
- Pytest & Unit Test (Airflow/Spark 코드 테스트)

### 🛠️ 미니 프로젝트
- Terraform으로 S3 + RDS 자동 배포
- Airflow DAG 테스트 코드 작성

### 🔍 추가 학습/보완
- IaC: Airflow 클러스터 + S3 + RDS 통합 배포
- Unit Test + 통합 테스트 + 데이터 품질 테스트 포함

---

## 🔹 2026년 5월 — 종합 프로젝트 & 마무리

### 🎯 학습 목표
- 전체 복습 및 포트폴리오 정리
- 협업 문서화 + 발표 준비
- 기초 통계 & 머신러닝 개념 (분포, 샘플링, 피처 엔지니어링)

### 🚀 최종 프로젝트
**실시간 뉴스 트렌드 분석 시스템**
- Kafka → 실시간 데이터 수집
- Spark Streaming → 클렌징 & 집계
- DynamoDB or Cassandra 적재
- Grafana/QuickSight 시각화

### 🔍 추가 학습/보완
- 오픈 API(뉴스API, 트위터 API) 활용
- DynamoDB와 Cassandra 중 1개 깊게 학습 (AWS 환경이면 DynamoDB 추천)

---

# ✅ 최종 정리

- **11월~12월**: 기초 스킬, 배치 ETL 파이프라인 완성  
- **1월~2월**: Spark & 실시간 파이프라인 경험  
- **3월~4월**: DW, 모니터링, IaC 자동화  
- **5월**: 종합 프로젝트 & 포트폴리오 정리  
