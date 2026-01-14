# 🍷 End-to-End Wine Quality Prediction (MLOps)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![MLflow](https://img.shields.io/badge/MLflow-Tracking-green)
![Docker](https://img.shields.io/badge/Docker-Enabled-blue)
![Flask](https://img.shields.io/badge/Flask-Web%20App-red)
![CI/CD](https://img.shields.io/badge/GitHub%20Actions-CI%2FCD-grey)

## 📋 Project Overview
This project is an **End-to-End Machine Learning pipeline** designed to predict the quality of wine based on physicochemical tests. It demonstrates a robust MLOps workflow, integrating data validation, modular coding, experiment tracking, and containerized deployment.

The system allows users to input wine characteristics via a Web UI and receive a quality rating, while the backend handles model versioning and artifact logging.

## 🚀 Key Features
* **Modular Codebase:** Organized structure with separate components for data ingestion, validation, transformation, and model training.
* **Data Validation:** Automated schema checks using `schema.yaml` to ensure data integrity (e.g., checking for columns like `fixed acidity`, `chlorides`, `alcohol`).
* **Experiment Tracking:** integrated **MLflow** to track model parameters, metrics, and artifacts.
* **CI/CD Pipelines:** Automated workflows using GitHub Actions for continuous integration.
* **Containerization:** Fully Dockerized application for consistent deployment across environments.
* **Prediction API:** A Flask-based web application for real-time predictions.

## 🛠️ Tech Stack
* **Language:** Python
* **Frameworks:** Flask, Scikit-learn, Pandas
* **MLOps Tools:** MLflow, DVC (Data Version Control)
* **DevOps:** Docker, GitHub Actions
* **Configuration:** YAML-based configuration (`config.yaml`, `params.yaml`, `schema.yaml`)

  
## 📊 Dataset Details
**The model is trained on a Wine Quality dataset. The schema validation ensures the following input features:**
* Physicochemical features: Fixed acidity, Volatile acidity, Citric acid, Residual sugar, Chlorides, Free sulfur dioxide, Total sulfur dioxide, Density, pH, Sulphates,     Alcohol.
* Target: Quality (Score between 0 and 10).

## 📂 Project Structure
```text
├── .github/workflows/      # CI/CD Workflows
├── config/                 # Configuration files
│   └── config.yaml         # Main project paths and settings
├── research/               # Jupyter notebooks for experimentation
├── src/
│   └── datascience/        # Source code for the pipeline
│       ├── components/     # Data ingestion, validation, trainer modules
│       ├── pipeline/       # Orchestration of components
│       ├── entity/         # Dataclasses for configuration
│       └── config/         # Configuration managers
├── templates/              # HTML templates for the Flask UI
├── app.py                  # Flask application entry point
├── main.py                 # Main pipeline execution script
├── Dockerfile              # Docker configuration
├── params.yaml             # Model hyperparameters
├── schema.yaml             # Data validation schema
├── requirements.txt        # Python dependencies
└── setup.py                # Package setup
```

** ⚙️ Installation & Usage**
1. Clone the Repository
```Bash

git clone [https://github.com/Tushar973/End-to-End-Quality-Prediction-MLOps](https://github.com/Tushar973/End-to-End-Quality-Prediction-MLOps)
cd End-to-End-Quality-Prediction-MLOps
```
2. Create a Virtual Environment
```Bash

conda create -n wine-ml python=3.8 -y
conda activate wine-ml
```
3. Install Dependencies
```Bash

pip install -r requirements.txt
```
4. Run the Pipeline
* To run the data ingestion, validation, and training pipeline:

```Bash

python main.py
```
5. Launch the Web Application
```Bash

python app.py
```
Open your browser and navigate to http://localhost:5000 (or the port specified in the terminal).


**📈 MLflow Integration**

```Bash

mlflow ui
```
