```
├── terraform/
│ ├── backend/
│ │ ├── main.tf
│ │ ├── variables.tf
│ │ └── outputs.tf
│ ├── s3/
│ │ ├── main.tf
│ │ ├── variables.tf
│ │ └── outputs.tf
│ ├── iam/
│ │ ├── main.tf
│ │ ├── variables.tf
│ │ └── outputs.tf
│ ├── rds/
│ │ ├── main.tf
│ │ ├── variables.tf
│ │ └── outputs.tf
│ ├── dev.tfvars
│ ├── prod.tfvars (참고용)
│ └── main.tf
│
├── airflow/
│ ├── dags/
│ │ ├── sample_dag.py
│ │ └── __init__.py
│ ├── tests/
│ │ ├── test_dag_structure.py
│ │ └── conftest.py
│ └── README.md
│
├── spark/
│ ├── transform.py
│ ├── tests/
│ │ ├── test_transform.py
│ │ └── conftest.py
│ └── README.md
│
├── ci/
│ ├── python-ci.yml
│ ├── dbt-ci.yml
│ └── terraform-ci.yml
│
├── README.md
└── docs/
├── infra-architecture.png
├── ci-flow.png
└── testing-guide.md
```

📘 README.md (초안)
1. Overview

이 레포는 신입 데이터 엔지니어 포트폴리오용으로 구성된 실제형 미니 프로젝트입니다.

포함된 구성 요소는 다음과 같습니다:

Terraform: S3, IAM, RDS, Backend(State), Variable 관리

Airflow DAG 테스트: DagBag 기반 구조 검증

Spark Transform 테스트: Schema & Row 비교

GitHub Actions 기반 CI

Python lint + pytest

dbt test

terraform validate + plan

2. Terraform (Infra-as-Code)
구성

S3 버킷 생성

DynamoDB 기반 remote backend

최소 권한 IAM 생성

PostgreSQL RDS 생성

dev/prod 환경 변수 분리

실행 방법
cd terraform
tf init --backend=true
tf plan -var-file=dev.tfvars
tf apply -var-file=dev.tfvars
tf destroy -var-file=dev.tfvars
제공되는 모듈

backend

s3

iam

rds

3. Airflow Test

Airflow DAG 테스트는 아래를 검증합니다.

DAG이 정상 로딩되는지

task 개수가 맞는지

schedule_interval이 올바른지

예시 코드: airflow/tests/test_dag_structure.py

4. Spark Transform Test

SparkSession을 테스트용으로 생성해 아래를 검증:

변환 로직이 schema를 정확히 생성하는지

값이 의도한 대로 바뀌는지

예시: spark/tests/test_transform.py

5. CI Pipelines (GitHub Actions)
제공되는 CI

Python: lint + pytest

dbt test

terraform validate + plan

CI 흐름

Pull Request 발생

자동 테스트 실행

terraform plan 출력

6. Docs

/docs/infra-architecture.png: 전체 Infra 구조도

/docs/ci-flow.png: CI 흐름도

/docs/testing-guide.md: 테스트가 왜 필요한지 설명

7. 결과물

이 레포는 다음 역량을 보여줍니다:

IaC로 인프라 구성

데이터 엔지니어링 테스트 능력

CI/CD 적용 능력

정리된 문서화 및 구조적 설계
