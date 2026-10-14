# Spotify End-to-End ETL Data Pipeline

An automated data engineering pipeline that extracts listening history from the Spotify Web API, performs data quality checks and transformations, and loads clean analytical records into a PostgreSQL database. The entire workflow is containerized using Docker and scheduled via Apache Airflow.

## 🛠 Tech Stack
- **Language:** Python (Pandas, Requests, SQLAlchemy)
- **Orchestration:** Apache Airflow
- **Database:** PostgreSQL
- **Containerization:** Docker & Docker Compose
- **Source API:** Spotify Web API (OAuth 2.0)

## 🚀 Key Features
- **Automated Ingestion:** Regularly fetches tracks from Spotify's `recently-played` endpoint using OAuth 2.0 authorization.
- **Data Validation & Quality Checks:** Enforces primary key constraints (`played_at`), verifies non-null fields, and handles duplicate track instances.
- **Data Transformation:** Aggregates listening trends by artist and playback timestamps.
- **Pipeline Orchestration:** Modular Airflow DAG handling automated table creation, task dependency mapping, and scheduled database loading.
- **Containerized Environment:** Fully reproducible multi-container Airflow and Postgres stack managed via Docker Compose.
