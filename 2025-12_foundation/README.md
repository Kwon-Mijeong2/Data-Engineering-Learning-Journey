# 2025-12_foundation

12월 안에 Airflow + dbt + RDS + S3 기반의 실무형 배치 파이프라인을 직접 구축하고 포트폴리오 프로젝트 완성하기.
```
├── README.md
├── week1_airflow/
│ ├── dags/
│ ├── docker-compose.yml
│ ├── notes.md
│ └── exercises/
├── week2_dbt/
│ ├── dbt_project/
│ ├── seeds/
│ ├── models/
│ ├── tests/
│ └── notes.md
├── week3_rds_s3_parquet/
│ ├── s3_scripts/
│ ├── parquet_examples/
│ ├── sql/
│ └── notes.md
├── week4_batch_pipeline/
│ ├── airflow_dags/
│ ├── dbt/
│ ├── ci/
│ └── notes.md
└── portfolio/
├── architecture.png
├── README.md
└── screenshots/
---


# 📅 전체 커리큘럼


## **1주차 — Airflow 기초**
- Airflow 설치(Docker)
- DAG 작성(PythonOperator, BashOperator)
- schedule_interval · start_date · retry
- XCom
- Variables / Connections


🎯 **성과**: DAG 3개 이상 작성 + ETL 미니 파이프라인 완성


---


## **2주차 — dbt 기초**
- staging → mart 모델 구성
- seed / source / ref
- 테스트/문서화
- Jinja


🎯 **성과**: marts 2~3개 구성 + docs 페이지 생성


---


## **3주차 — RDS + S3 + Parquet**
- RDS(PostgreSQL) 생성 및 연동
- S3 업로드·다운로드
- CSV → Parquet 변환
- 간단한 성능 비교


🎯 **성과**: RDS-S3-Parquet 연동 이해


---


## **4주차 — 배치 파이프라인 프로젝트**
- API → S3 → RDS → dbt mart 전체 DAG
- GitHub Actions CI
- 문서화 + README


🎯 **최종 성과**: 실무형 포트폴리오 프로젝트 1개 완성


---


# 📁 폴더 구조 설명


| 폴더 | 설명 |
|------|------|
| week1_airflow | Airflow 설치, 기본 DAG, XCom, Variables, 연습 DAG 포함 |
| week2_dbt | dbt 프로젝트 전체 구조 및 모델링 파일 |
| week3_rds_s3_parquet | RDS, S3, Parquet 관련 실습 코드/스크립트 |
| week4_batch_pipeline | 최종 파이프라인 DAG + CI 구성 |
| portfolio | 최종 포트폴리오 문서 및 이미지 |


---


# 🚀 실행 방법


## Airflow 시작하기
```
cd week1_airflow
docker-compose up -d
```
→ http://localhost:8080 접속


---


## dbt 실행
```
cd week2_dbt/dbt_project
~/.dbt/profiles.yml 설정 후


dbt run
dbt test
dbt docs generate
dbt docs serve
```


---


## S3 업로드 테스트
```
python week3_rds_s3_parquet/s3_scripts/upload.py
```


---


## 전체 파이프라인 실행(Airflow)
```
week4_batch_pipeline/airflow_dags/pipeline_dag.py
```


---


# 🏁 최종 결과물
- Airflow 전체 파이프라인 1개
- marts 모델 2~3개
- RDS-S3 연동
- GitHub Actions CI
- 포트폴리오 README
