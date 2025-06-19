# 🏗️ Airflow ETL Pipeline – Olympic Athlete Data
This project implements an **Apache Airflow** ETL pipeline using **Docker**, designed to extract, transform, and load Olympic athlete data from CSV files using `pandas`.

---

## 📁 Project Structure
airflow-etl-project/
├── dags/
│ └── etlpandas.py # Main ETL DAG using pandas
├── data/
│ ├── athlete_events.csv # Raw input data
│ └── athlete_cleaned.csv # Cleaned output data
├── config/
│ └── airflow.cfg # Optional custom Airflow config
├── .env # Environment variables (credentials/secrets)
├── docker-compose.yaml # Dockerized Airflow stack
├── .gitignore
└── README.md


---

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/airflow-etl-project.git
cd airflow-etl-project
```

2. Setup Environment
Copy .env.example to .env (if used for secrets or configs):
```bash
cp .env.example .env
```
3. Start Airflow (via Docker)
```bash
docker-compose up airflow-init  # Initializes Airflow DB and user
docker-compose up               # Starts all services
```
Visit the Airflow web UI at:

👉 http://localhost:8080
Login: airflow / airflow
