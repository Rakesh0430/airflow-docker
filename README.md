your_project_folder/
├── dags/
│   ├── hello_world.py
├── setup.ps1
└── docker-compose.yaml  (downloaded manually or via the script)

setup.ps1 file
 # Download Docker Compose file
powershell Invoke-WebRequest -Uri 'https://airflow.apache.org/docs/apache-airflow/stable/docker-compose.yaml' -OutFile 'docker-compose.yaml'

# Initialize Airflow database
docker-compose up airflow-init

# Start Airflow
docker-compose up -d

2) hello_world.py DAG

3) Set-ExecutionPolicy RemoteSigned -Scope CurrentUser

4) .\setup.ps1 ## for running and getting compose into local


docker-compose down --volumes --rmi all
docker-compose build --no-cache
docker-compose up airflow-init
docker-compose up -d


docker-compose down
docker-compose build 
docker-compose up -d
