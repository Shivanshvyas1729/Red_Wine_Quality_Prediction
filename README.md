# 🍷 Red Wine Quality Prediction — End-to-End MLOps

An end-to-end machine learning project for predicting **red wine quality scores** from physicochemical properties.

The project is designed as a **production-oriented MLOps pipeline**, with modular components, configuration-driven development, structured logging, model evaluation, and deployment-ready architecture.

---

## 🚀 Overview

This project demonstrates how to build and organize a complete machine learning system beyond simply training a model.

### ML Pipeline

```text
Raw Dataset
     │
     ▼
Data Ingestion
     │
     ▼
Data Validation
     │
     ▼
Data Transformation
     │
     ▼
Model Training
     │
     ▼
Model Evaluation
     │
     ▼
Model Artifact
     │
     ▼
API / Deployment
```

The pipeline is designed to be **reproducible, modular, configurable, and extensible**.

---

## 🧠 Problem Statement

The objective is to predict the **quality score of red wine** using physicochemical characteristics of the wine.

The target variable represents wine quality, with observed values in the **3–8 range**.

This problem is formulated as a **regression task**.

### Example Features

* Fixed acidity
* Volatile acidity
* Citric acid
* Residual sugar
* Chlorides
* Free sulfur dioxide
* Total sulfur dioxide
* Density
* pH
* Sulphates
* Alcohol

---

## 🏗️ Project Architecture

The project follows a modular ML pipeline architecture.

```text
                 ┌──────────────────┐
                 │   Raw Dataset    │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Data Ingestion   │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Data Validation  │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Data             │
                 │ Transformation   │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Model Training   │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Model Evaluation │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ Trained Model    │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ API / Deployment │
                 └──────────────────┘
```

---

## 📂 Project Structure

```text
Red_Wine_Quality_Prediction/
│
├── .github/
│   └── workflows/
│       └── main.yml
│
├── artifacts/
│   ├── data_ingestion/
│   ├── data_validation/
│   ├── data_transformation/
│   └── model_trainer/
│
├── config/
│   └── config.yaml
│
├── research/
│   └── experiments.ipynb
│
├── src/
│   └── mlProject/
│       ├── components/
│       │   ├── data_ingestion.py
│       │   ├── data_validation.py
│       │   ├── data_transformation.py
│       │   ├── mo
```
