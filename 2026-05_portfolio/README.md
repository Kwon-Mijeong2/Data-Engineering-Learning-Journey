```
2026-04-ops-monitoring/
│
├── airflow-ops/
│ ├── docs/
│ │ ├── airflow-architecture.md
│ │ ├── retries-sla-timeout.md
│ │ ├── backfill-catchup.md
│ │ ├── idempotency.md
│ │ └── ops-rules-10.md
│ ├── failure-scenarios/
│ │ ├── api_failure.md
│ │ ├── db_failure.md
│ │ ├── file_missing.md
│ │ └── recovery-guide.md
│ └── configs/
│ ├── connections-example.json
│ └── variables-example.json
│
├── metrics-logging/
│ ├── logs-vs-metrics-vs-tracing.md
│ ├── airflow-logs-structure.md
│ ├── system-metrics.md
│ ├── cloudwatch-basics.md
│ ├── spark-metrics.md
│ └── troubleshooting-report.md
│
├── monitoring-dashboard/
│ ├── grafana-overview.md
│ ├── prometheus-concept.md
│ ├── cloudwatch-dashboard.md
│ ├── airflow-success-dashboard.md
│ └── daily-ops-dashboard.md
│
├── incident-response/
│ ├── incident-types.md
│ ├── reprocessing-strategy.md
│ ├── data-loss-prevention.md
│ ├── cost-optimization.md
│ ├── midnight-incident.md
│ ├── log-volume-explosion.md
│ └── final-portfolio.md
│
├── interview/
│ ├── airflow-failure-questions.md
│ ├── spark-performance-questions.md
│ ├── cost-questions.md
│ └── general-de-ops-questions.md
│
├── README.md
└── .gitignore
```

📝 README (초안)
📌 2026년 4월 — 운영 안정화 & 모니터링 프로젝트

데이터 엔지니어 실무 전환을 위해 운영 중심 역량을 강화하는 한 달 프로젝트입니다. Airflow 운영, 모니터링 구축, 장애 대응 전략을 모두 포함하여 실무 투입 가능한 운영 능력을 목표로 합니다.

📆 월간 계획 요약
🟦 1주차 — Airflow 운영 실전

운영 중심 관점에서 Airflow 구조, Retry/SLA, Backfill, Idempotency 등을 정리합니다.

포함 파일

airflow-ops/docs/*.md

airflow-ops/failure-scenarios/*.md

airflow-ops/configs/*

🟩 2주차 — 로그 & 메트릭 수집

로그/메트릭/트레이싱 개념부터 CloudWatch/Spark 메트릭 분석까지 실습 중심으로 정리합니다.

포함 파일

metrics-logging/*.md

🟨 3주차 — Grafana & CloudWatch 운영 대시보드

Prometheus 기본 개념 파악 후, CloudWatch & Airflow 운영 대시보드를 구축합니다.

포함 파일

monitoring-dashboard/*.md

🟥 4주차 — 장애 대응 & 운영 포트폴리오 완료

재처리, 장애 대응, 비용 최적화, 데이터 유실 방지 전략 등을 정리하고 운영 포트폴리오 제작.

포함 파일

incident-response/*.md

interview/*.md

🎁 최종 산출물

Airflow 운영 가이드

로그/메트릭 분석 문서

운영 대시보드 스크린샷 & 설명

장애 대응 시나리오 5종

재처리 전략 문서

비용 폭탄 방지 전략 문서

실무형 운영 포트폴리오 완성본
