# 2026-03_lakehouse-warehouse

```
├── README.md
├── 01_lakehouse/
│ ├── lake_vs_warehouse.md
│ ├── lakehouse_summary.md
│ ├── etl_to_elt.md
│ ├── iceberg_vs_delta.md
│ ├── iceberg_internals.md
│ ├── delta_internals.md
│ ├── s3_iceberg_setup.md
│ └── iceberg_table_example/
│ ├── create_table.py
│ ├── insert_data.py
│ └── query_time_travel.py
├── 02_warehouse/
│ ├── warehouse_intro.md
│ ├── redshift_architecture.md
│ ├── redshift_table_design.sql
│ ├── bigquery_intro.md
│ ├── bigquery_table_design.sql
│ └── redshift_vs_bigquery.md
├── 03_data_quality/
│ ├── data_quality_concepts.md
│ ├── ge_structure.md
│ ├── ge_profiling.md
│ ├── ge_custom_rules.md
│ ├── airflow_ge_integration_dag.py
│ └── alert_strategy.md
└── 04_architecture_portfolio/
├── star_schema.md
├── star_schema_design.md
├── lakehouse_vs_warehouse.md
├── final_architecture_diagram.png
├── tech_stack_choices.md
├── portfolio_document.md
├── github_finalization.md
├── blog_draft.md
└── interview_questions.md
```

📌 README.md
📦 2026년 3월 — Lakehouse & Warehouse 기본기

이 레포는 2026년 3월에 진행한 Lakehouse / Warehouse / Data Quality / 아키텍처 설계 학습 및 실습 결과물을 정리한 저장소입니다.

3월은 "회복 구간"이면서도 데이터 엔지니어링의 핵심 개념을 단단히 정리하는 달로 설계되었습니다.

🎯 최종 산출물

✔️ Lakehouse & Warehouse 비교 문서

✔️ Iceberg 실습 1개 (S3 + Iceberg ACID 테이블)

✔️ Redshift or BigQuery 테이블 설계 1개

✔️ 데이터 품질 체크 파이프라인 1개 (Airflow + GE)

✔️ 데이터 플랫폼 아키텍처 포트폴리오 1개

📚 학습 구성

레포는 총 4개의 큰 파트로 구성되어 있습니다.

1️⃣ Lakehouse 기초

Lake vs Warehouse

Lakehouse 등장 배경

Iceberg / Delta 비교

Iceberg Internals (Snapshot, Manifest, Partition Evolution)

S3 + Iceberg 실습 (create_table.py, insert_data.py, query_time_travel.py)

📁 폴더: /01_lakehouse/

2️⃣ Warehouse 기본기

OLTP vs OLAP

Redshift 구조: Leader / Compute / Dist / Sort

BigQuery Partition & Clustering

비용 구조 및 성능 비교

📁 폴더: /02_warehouse/

3️⃣ 데이터 품질(Data Quality)

Accuracy / Completeness / Freshness

Great Expectations 구조

프로파일링 → 룰 작성 → Airflow DAG 연동

Slack 알람 전략, 재처리 전략

📁 폴더: /03_data_quality/

4️⃣ 아키텍처 설계 포트폴리오

스타 스키마(Fact / Dimension)

Kafka → Spark → Iceberg → Redshift/BigQuery → Airflow → GE 전체 데이터 파이프라인

기술 스택 선택 이유

기술 블로그 초안

면접 질문 정리

📁 폴더: /04_architecture_portfolio/

🏗️ 전체 아키텍처 (요약)
Kafka → Spark Streaming → Iceberg(Lakehouse)
           ↓
     Redshift / BigQuery (Warehouse)
           ↓
   Airflow → Great Expectations
• 실시간 수집: Kafka
• 처리 엔진: Spark
• 저장: Iceberg (ACID & Time Travel)
• 분석: Redshift / BigQuery
• 품질 검증: Great Expectations
• 스케줄링 & 오케스트레이션: Airflow
📝 기술 포트폴리오

최종 산출물은 /04_architecture_portfolio/portfolio_document.md 에 정리되어 있으며, 데이터 엔지니어 포트폴리오 및 면접 대비에 최적화된 형태로 구성했습니다.
