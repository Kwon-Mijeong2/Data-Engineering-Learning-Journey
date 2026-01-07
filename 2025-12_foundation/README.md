# 2025-12_foundation

12월 안에 Airflow + dbt + RDS + S3 기반의 실무형 배치 파이프라인을 직접 구축하고 포트폴리오 프로젝트 완성하기.
```
├── README.md
├── web_crawling/
│ ├── references/
│ ├── notes.md
│ └── exercises/
├── airflow/
│ ├── dags/
│ ├── docker-compose.yml
│ ├── notes.md
│ └── exercises/
├── dbt/
│ ├── dbt_project/
│ ├── seeds/
│ ├── models/
│ ├── tests/
│ └── notes.md
├── rds_s3_parquet/
│ ├── s3_scripts/
│ ├── parquet_examples/
│ ├── sql/
│ └── notes.md
├── batch_pipeline/
│ ├── airflow_dags/
│ ├── dbt/
│ ├── ci/
│ └── notes.md
└── portfolio/
├── architecture.png
├── README.md
└── screenshots/
```

# 📁 폴더 구조 설명


| 폴더 | 설명 |
|------|------|
| web_crawling | 웹 크롤러 만들기 |
| airflow | Airflow 설치, 기본 DAG, XCom, Variables, 연습 DAG 포함 |
| dbt | dbt 프로젝트 전체 구조 및 모델링 파일 |
| rds_s3_parquet | RDS, S3, Parquet 관련 실습 코드/스크립트 |
| batch_pipeline | 최종 파이프라인 DAG + CI 구성 |
| portfolio | 최종 포트폴리오 문서 및 이미지 |


---


# 🏁 최종 결과물
- Airflow 전체 파이프라인 1개
- marts 모델 2~3개
- RDS-S3 연동
- GitHub Actions CI
- 포트폴리오 README
