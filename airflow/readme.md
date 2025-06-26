### How to install this airflow helm chart


#### Step 1 : Initial airflow setup
```
helm repo add apache-airflow https://airflow.apache.org;
kubectl create ns airflow;
helm upgrade --install airflow apache-airflow/airflow -n airflow;
```

#### Step 2 : Create GH sync secret to pull dags from github repo
```
apiVersion: v1
kind: Secret
metadata:
  name: git-credentials
data:
  GIT_SYNC_USERNAME: <base64_encoded_git_username>
  GIT_SYNC_PASSWORD: <base64_encoded_git_pat>
  GITSYNC_USERNAME: <base64_encoded_git_username>
  GITSYNC_PASSWORD: <base64_encoded_git_pat>
```

#### Step 3 : Update helm chart to enable gitsync
```
helm upgrade --install airflow apache-airflow/airflow -n airflow -f airflow/values.yaml;
```
