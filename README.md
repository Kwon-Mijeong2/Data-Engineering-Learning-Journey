# 🚀 Data Engineering Learning Journey

데이터 엔지니어 신입 취업을 목표로 진행한 **8개월 학습 로드맵 & 프로젝트 기록**입니다.  
Python, SQL, ETL, 데이터 파이프라인, 분산처리, 스트리밍, 클라우드, 인프라 자동화 등  
데이터 엔지니어링 필수 역량을 학습하고 실습했습니다.  

---

## 📌 학습 로드맵 (2025.10 ~ 2026.05)

| 기간 | 학습 내용 |
|------|-----------|
| 2025.10 | Python / SQL 문제풀이 (백준, LeetCode, Programmers) |
| 2025.11 | SQL 심화, ETL 기초, Pandas, 크롤링, AWS 기초, Git/GitHub 협업 |
| 2025.12 | Airflow, dbt, ERD, 데이터 품질, Docker, AWS RDS, BI 도구 |
| 2026.01 | Spark (Batch), Pandas vs Spark 성능 비교 |
| 2026.02 | Kafka / SQS, Spark Streaming, Flink, 실시간 데이터 처리 |
| 2026.03 | DWH (Redshift/BigQuery), 모니터링 (Grafana, CloudWatch), Governance |
| 2026.04 | IaC (Terraform), CI/CD, 데이터 품질 테스트, 자동화 배포 |
| 2026.05 | 최종 프로젝트 (실시간 뉴스 트렌드 분석 시스템) + 포트폴리오 정리 |

---

## 📂 Repository Structure

> 각 디렉토리별 상세 내용은 내부 README에서 확인할 수 있습니다.

- 01_sql_etl_basics/ → SQL 고급, ETL 기초, dbt
- 02_ingest/ → 데이터 수집 (API, 크롤링, 파일 적재)
- 03_sql_database/ → MySQL, PostgreSQL, SQLite, AWS RDS
- 04_data_engineering/ → 파이프라인, Airflow, Docker, Spark, Kafka, Flink
- 05_cloud/ → AWS, GCP, Azure, 멀티클라우드 비교
- 06_infra_ops/ → IaC(Terraform), CI/CD, 모니터링/Observability
- 07_visualization_bi/ → BI 툴 (Looker, Quicksight, Tableau, PowerBI)
- 08_projects/ → 프로젝트 모음 (배치, 스트리밍, DWH, 최종 프로젝트)
- 10_docs/ → 문서, 로드맵, 면접 대비, 용어 정리

---

## 🛠️ 기술 스택

- **언어 & 쿼리**: Python, SQL (MySQL, PostgreSQL, SQLite)
- **데이터 수집 & 처리**: Pandas, BeautifulSoup, Selenium, dbt
- **워크플로우 & 파이프라인**: Apache Airflow, Docker
- **분산/스트리밍 처리**: Apache Spark, Kafka, Flink
- **클라우드 & 인프라**: AWS (S3, RDS, EC2, Lambda, Glue, IAM, VPC), Terraform
- **모니터링 & 품질 관리**: Great Expectations, Prometheus, Grafana, CloudWatch
- **시각화 & BI**: Quicksight, Tableau, PowerBI, Looker Studio

---

## 📊 주요 프로젝트

| 기간 | 프로젝트 | 설명 |
|------|-----------|------|
| 2025.09 | [CSV 파이프라인](Mini_projects/2025_09_kaggle_csv_pipeline/) | Kaggle CSV → Pandas → SQLite/MySQL |
| 2025.10 | [API → dbt 모델링](./08_projects/2025_10_api_to_dbt) | API 수집 → MySQL/Postgres → dbt 모델링 |
| 2025.12 | [배치 ETL 파이프라인](./08_projects/2025_12_batch_etl) | Airflow + dbt + GE → BI 시각화 |
| 2026.01 | [Spark 성능 비교](./08_projects/2026_01_spark_perf) | Spark vs Pandas 대용량 처리 성능 분석 |
| 2026.02 | [스트리밍 파이프라인](./08_projects/2026_02_streaming_pipeline) | Kafka/SQS → Streaming → DB 적재 |
| 2026.03 | [DWH & 모니터링](./08_projects/2026_03_dw_monitoring) | Redshift/BigQuery + Grafana |
| 2026.05 | [최종 프로젝트](./08_projects/2026_05_final_project) | 실시간 뉴스 트렌드 분석 (Kafka → Spark Streaming → DynamoDB → Grafana) |

---

## 📝 문서 & 면접 대비

- [roadmap.md](./10_docs/roadmap.md) : 학습 로드맵 정리  
- [interview_preparation.md](./10_docs/interview_preparation.md) : 면접 대비 Q&A 모음  
- [terminology.md](./10_docs/terminology.md) : 데이터 엔지니어링 용어 정리  
- [references.md](./10_docs/references.md) : 참고 자료 (Docs, 블로그, 논문 등)  

---

## 🌱 목표

1. **데이터 엔지니어 신입 취업**을 위한 전 과정 정리  
2. **실무 수준 프로젝트 경험** (Batch, Streaming, DWH, Infra) 확보  
3. 오픈소스 친화적 포트폴리오로 깃허브에 공개  

---
