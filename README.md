🍷 End-to-End Wine Quality Prediction (MLOps)

This project implements a production-style end-to-end machine learning pipeline for predicting red wine quality using physicochemical properties.
It follows industry-standard MLOps practices, including modular pipelines, configuration-driven development, logging, and CI/CD-ready structure.

🚀 Project Overview

The pipeline covers the complete ML lifecycle:

Data Ingestion

Data Validation

Data Transformation

Model Training

Model Evaluation

Model Serving (API-ready)

CI/CD & Cloud Deployment Ready

The goal is to build a reproducible, scalable, and maintainable ML system, not just a model.

🧠 Problem Statement

Predict the quality score (3–8) of red wine samples based on physicochemical features such as acidity, alcohol, sulphates, etc.

This is treated as a regression problem.

📂 Project Workflow (How to Extend / Modify)

Whenever you add a new pipeline stage or change logic, follow this order:

Update config.yaml

Update schema.yaml

Update params.yaml

Update entity (dataclass) definitions

Update ConfigurationManager

Update components

Update pipeline stages

Update main.py

Update app.py (if serving logic changes)

This ensures clean dependency flow and avoids runtime errors.

🗂️ Project Structure (High-Level)
├── config/
│   ├── config.yaml
│   ├── schema.yaml
│
├── src/Red_Wine_Prediction/
│   ├── components/
│   ├── config/
│   ├── constants/
│   ├── entity/
│   ├── pipeline/
│   ├── utils/
│
├── artifacts/
│   ├── data_ingestion/
│   ├── data_validation/
│   ├── data_transformation/
│   ├── model_trainer/
│
├── main.py
├── app.py
├── params.yaml
├── requirements.txt
├── setup.py

⚙️ Configuration-Driven Design

config.yaml → Paths & pipeline settings

schema.yaml → Data validation rules

params.yaml → Model hyperparameters

No hardcoded values inside pipeline logic.

🧪 Model Used

ElasticNet Regression

Handles multicollinearity

Controlled via alpha and l1_ratio from params.yaml

📊 Evaluation

Evaluation metrics include:

MAE

RMSE

R² Score

Predictions are optionally clipped to valid quality range (3–8).

🛠️ How to Run Locally
1️⃣ Clone the Repository
git clone https://github.com/your-username/End-to-End-Wine-Quality-Prediction.git
cd End-to-End-Wine-Quality-Prediction

2️⃣ Create Environment
conda create -n wine_ml python=3.9 -y
conda activate wine_ml

3️⃣ Install Dependencies
pip install -r requirements.txt

4️⃣ Run Pipeline
python main.py

☁️ Deployment Ready (AWS CI/CD)

The project is structured to support:

Docker

AWS ECR

EC2

GitHub Actions (CI/CD)

Deployment flow:

Build Docker image

Push to AWS ECR

Pull image on EC2

Run container