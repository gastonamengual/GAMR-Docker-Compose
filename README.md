## Access the deployed APP here! https://gamr-image-recognition.streamlit.app

This repository is part of the GAMR MLOps project and handles the deployment of the architecture using Docker Compose. It also includes an MLflow tracking server with a PostgreSQL backend and artifact storage.

## Architecture

The architecture consists of the following repos:

* [Client UI](https://github.com/gastonamengual/GAMR-Client-Streamlit)
* [Backend Service API](https://github.com/gastonamengual/GAMR-Backend-Service-Vercel)
* [Model Service API](https://github.com/gastonamengual/GAMR-Model-Registry-MLFlow)
* [MLFlow Server](https://github.com/gastonamengual/GAMR-MLFlow-Server)

## Setup Instructions

1. Create a Project Folder

``mkdir mlflow_project && cd mlflow_project``

2. Clone or Add Docker Compose File

Place the docker-compose.yml file at the root of your project:

```bash
mlflow_project/
├── docker-compose.yml
├── MLFlow_Server/
├── Another_Service/
└── ...
```

3. Create Folders for Each Service

Clone each service (e.g., MLflow, API, UI) inside the project folder. Each repo must have it's own folder.

4. Run the Services

To build and start the services, run on the root:

`docker-compose up --build`

5. Access the services

Once running, the UI can be accessed at http://localhost:8501 and the MLflow server can be accessed at http://localhost:5005.

## Next Steps

* Enhance CI/CD: Automate deployment workflows.
* Integrate Kubernetes: Improve scalability and reliability.
* Add multi-environment functions.
