# 2025-12_foundation

Spark로 대용량 로그를 처리하고, Parquet 최적화 + Airflow 자동화 + RDS 적재까지 이어지는 실무형 파이프라인 완성.
```
├── README.md
├── week1_spark_basics/
│ ├── notebooks/
│ ├── scripts/
│ ├── data/
│ └── notes.md
├── week2_shuffle_join/
│ ├── experiments/
│ ├── broadcast_examples/
│ ├── skew_tests/
│ └── notes.md
├── week3_rds_airflow/
│ ├── spark_jobs/
│ ├── airflow_dags/
│ ├── screenshots/
│ └── notes.md
├── week4_biglog_project/
│ ├── generator/
│ ├── spark_etl/
│ ├── parquet/
│ ├── airflow/
│ ├── rds/
│ └── notes.md
└── portfolio/
├── architecture.png
├── performance_report.md
├── screenshots/
└── README.md
```
# 📅 전체 커리큘럼


## **1주차 — Spark 기초 정복**
- SparkSession 생성
- CSV/JSON 로드
- DataFrame 연산
- explain()으로 실행 계획 해석


🎯 **성과:** Spark DataFrame으로 데이터 가공 가능


---


## **2주차 — Join & Shuffle 핵심**
- narrow vs wide
- shuffle 발생 위치 이해
- broadcast join
- skew 데이터 처리
- partition 조정


🎯 **성과:** Spark 병목 구조 설명 가능


---


## **3주차 — Spark + RDS + Airflow**
- `.write.jdbc()` 적재
- batchsize 비교
- Airflow SparkSubmitOperator
- Spark UI 병목 분석


🎯 **성과:** Spark 파이프라인 자동 실행


---


## **4주차 — 대용량 로그 ETL 프로젝트**
- 100만~500만 로그 생성
- Spark ETL 가공
- Partition 전략 적용
- Parquet 저장 + 성능 비교
- Airflow 전체 연결
- RDS 최종 적재


🎯 **성과:** 실무형 Spark ETL 포트폴리오 1개 완성


---


# 📁 폴더 구조 설명


| 폴더 | 설명 |
|------|------|
| week1_spark_basics | Spark 기초 연습, 노트북, 기본 스크립트 |
| week2_shuffle_join | shuffle/broadcast/skew 실험 코드 |
| week3_rds_airflow | RDS 적재 + Airflow 연동 실습 |
| week4_biglog_project | 대용량 로그 생성 + Spark ETL + Parquet + Airflow + RDS |
| portfolio | 최종 포트폴리오 및 리포트 |


---


# 🚀 실행 방법


## Spark 실행
```
pyspark --packages org.postgresql:postgresql:42.7.1
```


---


## Spark 스크립트 실행
```
python week1_spark_basics/scripts/basic_etl.py
```


---


## Airflow + SparkSubmitOperator
```
cd week3_rds_airflow/airflow_dags
```
(Docker 기반 airflow 설치 후 DAG 자동 인식)


---


# 🏁 최종 결과물
- 대용량 로그 ETL 파이프라인 (Spark → Parquet → RDS)
- Shuffle / Join / Partition 튜닝 실험 결과
- Airflow SparkSubmit 자동 실행
- 포트폴리오 문서 완성
