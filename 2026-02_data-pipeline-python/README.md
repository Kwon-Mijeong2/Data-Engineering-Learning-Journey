# 2026-02_data-pipeline-python

실시간 로그 → Kafka → Spark Streaming → S3 → Athena → QuickSight로 이어지는 엔드투엔드 실시간 데이터 파이프라인 구축.

```
kafka-realtime-2026/
├── README.md
├── week1_kafka_basics/
│ ├── docker-compose.yml
│ ├── cli_commands.md
│ ├── python_producer/
│ │ ├── producer.py
│ │ └── generator.py
│ ├── python_consumer/
│ │ └── consumer.py
│ └── notes.md
├── week2_spark_streaming/
│ ├── spark_streaming_kafka.py
│ ├── schema.json
│ ├── checkpoint/
│ └── notes.md
├── week3_s3_athena/
│ ├── s3_config.md
│ ├── glue_crawler.md
│ ├── athena_queries.sql
│ └── notes.md
├── week4_realtime_dashboard/
│ ├── architecture.png
│ ├── quicksight_guide.md
│ ├── performance_test.md
│ └── notes.md
└── portfolio/
├── final_report.md
├── diagrams/
└── screenshots/
```

# 📅 전체 커리큘럼


## **1주차 — Kafka 기초 완전 정복**
- Kafka 로컬 실행 (Docker)
- Topic / Partition / Replication
- CLI Producer/Consumer
- Python Producer & Consumer 구현


🎯 **성과:** 메시지를 Kafka에 생산/소비하는 전체 구조 이해


---


## **2주차 — Spark Structured Streaming**
- Kafka → Spark Streaming 연동
- JSON 파싱 & 스키마 정의
- Parquet 실시간 저장
- Trigger / Checkpoint / Watermark


🎯 **성과:** 실시간 ETL 파이프라인 구축


---


## **3주차 — S3 + Glue + Athena 리얼타임 분석**
- 웹 로그 시뮬레이터 Producer 개발
- Spark Streaming → S3 실시간 적재
- Glue Catalog 자동 테이블 생성
- Athena 실시간 분석 쿼리 작성


🎯 **성과:** 실시간 데이터 레이크 + 웨어하우스 구축


---


## **4주차 — QuickSight 대시보드 + 문서화**
- 전체 파이프라인 아키텍처 정리
- QuickSight 실시간 시각화 구성
- 장애 테스트 & checkpoint 복구 검증
- 면접 질문 정리 + 포트폴리오 완성


🎯 **성과:** 완전한 실시간 데이터 플랫폼 포트폴리오 완성


---


# 🏗 기술 스택
- **Kafka / KRaft 모드**
- **Python Producer & Consumer**
- **Spark Structured Streaming**
- **S3 / Parquet / Glue / Athena**
- **QuickSight 시각화**
- **Docker 기반 개발환경**


---


# 🔧 실행 방법


## Kafka 실행
```
docker compose up -d
```


## Python Producer 실행
```
python week1_kafka_basics/python_producer/producer.py
```


## Spark Streaming 실행
```
spark-submit \
--packages org.apache.spark:spark-sql-kafka-0-10_2.12:3.5.0 \
week2_spark_streaming/spark_streaming_kafka.py
```


---


# 🏁 최종 결과물
- **실시간 로그 처리 시스템 전체 구성**
- Kafka → Spark Streaming → S3 파이프라인
- Athena 기반 분석 쿼리
- QuickSight 실시간 대시보드
- 포트폴리오 문서
