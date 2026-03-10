# End-to-End Machine Learning Project with MLflow

Production-ready End-to-End Machine Learning pipeline with experiment tracking, model management, and deployment using **MLflow**, **FastAPI**, **Docker**, and **CI/CD**.

This project demonstrates how to design and implement a scalable ML system following **MLOps best practices**.

---

## Project Overview

The goal of this project is to build a complete machine learning pipeline that covers the entire lifecycle of an ML model:

- Data ingestion
- Data validation
- Data transformation
- Model training
- Model evaluation
- Experiment tracking with MLflow
- Model deployment via API

The system is designed to be **modular, configurable, and production-ready**.

---

## Key Features

- Modular ML pipeline architecture
- Experiment tracking using **MLflow**
- Configuration-driven pipeline using YAML files
- REST API for inference
- Docker containerization
- CI/CD with GitHub Actions
- Cloud deployment ready (AWS EC2 + ECR)
- Scalable project structure following MLOps practices

---

## Tech Stack

**Programming Language**

- Python

**Machine Learning**

- Scikit-learn
- Pandas
- NumPy

**MLOps**

- MLflow
- Docker
- GitHub Actions

**API**

- FastAPI / Flask

**Cloud**

- AWS EC2
- AWS ECR

---

## Project Architecture

```
.
├── config
│   ├── config.yaml
│   ├── params.yaml
│   └── schema.yaml
│
├── src
│   ├── components
│   │   ├── data_ingestion.py
│   │   ├── data_validation.py
│   │   ├── data_transformation.py
│   │   ├── model_trainer.py
│   │   └── model_evaluation.py
│   │
│   ├── pipeline
│   │   ├── training_pipeline.py
│   │   └── prediction_pipeline.py
│   │
│   ├── entity
│   └── config
│
├── artifacts
├── notebooks
├── app.py
├── main.py
├── requirements.txt
├── Dockerfile
└── README.md
```

---

## ML Pipeline Workflow

The ML pipeline consists of the following stages:

1. **Data Ingestion**
   - Load raw dataset
   - Store data artifacts

2. **Data Validation**
   - Schema validation
   - Data integrity checks

3. **Data Transformation**
   - Feature engineering
   - Feature scaling
   - Data preprocessing

4. **Model Training**
   - Train machine learning model
   - Hyperparameter configuration

5. **Model Evaluation**
   - Evaluate performance metrics
   - Compare experiments

6. **Experiment Tracking**
   - Log experiments with MLflow
   - Track parameters, metrics, and artifacts

---

## MLflow Tracking

MLflow is used for:

- Experiment tracking
- Parameter logging
- Metric logging
- Model artifact storage
- Model versioning

Run MLflow UI locally:

```bash
mlflow ui
```

Then open:

```
http://localhost:5000
```

---

## Installation

### Clone the repository

```bash
git clone https://github.com/yourusername/mlflow-ml-project.git
cd mlflow-ml-project
```

---

### Create a virtual environment

Using **conda**

```bash
conda create -n mlproj python=3.8 -y
conda activate mlproj
```

or using **venv**

```bash
python -m venv venv
source venv/bin/activate
```

---

### Install dependencies

```bash
pip install -r requirements.txt
```

---

## Run the Application

Start the application:

```bash
python app.py
```

Then open your browser:

```
http://localhost:5000
```

---

## Running ML Pipeline

To run the training pipeline:

```bash
python main.py
```

This will execute the entire pipeline including:

- Data ingestion
- Data transformation
- Model training
- Model evaluation
- MLflow experiment logging

---

## Docker Support

Build Docker image:

```bash
docker build -t ml-project .
```

Run container:

```bash
docker run -p 5000:5000 ml-project
```

---

## CI/CD Pipeline

The project includes **GitHub Actions CI/CD pipeline** that performs:

- Build Docker image
- Push image to AWS ECR
- Deploy container to AWS EC2

Workflow:

```
GitHub → Build Docker Image → Push to ECR → Deploy to EC2
```

---

## AWS Deployment Architecture

Deployment pipeline:

1. Build Docker image
2. Push Docker image to **AWS ECR**
3. Launch **EC2 instance**
4. Pull image from ECR
5. Run Docker container

Services used:

- AWS EC2
- AWS ECR
- GitHub Actions

---

## Example API Request

Prediction endpoint:

```
POST /predict
```

Example JSON request:

```json
{
  "feature_1": 10,
  "feature_2": 5.5,
  "feature_3": 2
}
```

Example response:

```json
{
  "prediction": 1
}
```

---

## Future Improvements

- Add model monitoring
- Add automated retraining pipeline
- Integrate with Kubernetes
- Add feature store
- Implement advanced hyperparameter tuning

---

## Author

Machine Learning / MLOps Portfolio Project.

Designed to demonstrate real-world **production ML system design**.

---

## License

This project is licensed under the MIT License.
