# airflow-transaction-analyzer

### Prerequisites: -
- A running Kubernetes cluster
- Helm v3.12.2 or higher
- GitSync v4.3.0 or higher

### Major Components: -
- Airflow
- One application to parse the CSV data and stream it to Airflow
- A DAG to run mathematical models on the data and stream results to Airflow
- Another application to read data from airflow and visualize it

### How to replicate this project: -
1. Clone this repository
2. Navigate to airflow directory and follow the readme steps
3. Navigate to DAG directory and follow the readme steps
4. Navigate to app directory and follow the readme steps
