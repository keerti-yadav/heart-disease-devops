# ❤️ Heart Disease Prediction System using MLOps

## 📌 Project Overview

This project demonstrates an **end-to-end MLOps (Machine Learning + DevOps) pipeline** for predicting heart disease.
It integrates machine learning model development with deployment and automation using modern DevOps practices.

The system allows users to send input features via an API and receive predictions, while the entire workflow is automated using CI/CD.

---

## 🚀 Key Features

* 🧠 Machine Learning model for disease prediction
* 🌐 REST API using Flask
* 🐳 Docker containerization for portability
* ⚡ CI/CD automation using GitHub Actions
* 🔁 Automated model training and build pipeline

---

## 🧠 Tech Stack

| Category         | Tools Used     |
| ---------------- | -------------- |
| Programming      | Python         |
| ML Library       | Scikit-learn   |
| API Framework    | Flask          |
| Containerization | Docker         |
| CI/CD            | GitHub Actions |

---

## 📊 Dataset

The project uses a built-in dataset from **Scikit-learn**:

* 30 numerical features
* Binary classification problem

| Label | Meaning         |
| ----- | --------------- |
| 0     | No disease      |
| 1     | Disease present |

---

## 🏗️ Project Structure

```
heart-disease-devops/
│
├── app.py                  # Flask API
├── model.py                # Model training script
├── model.pkl               # Trained model
├── requirements.txt        # Dependencies
├── Dockerfile              # Docker configuration
│
└── .github/
    └── workflows/
        └── ci.yml          # CI/CD pipeline
```

---

## ⚙️ Working Pipeline

### 🔁 End-to-End Flow

```
Data → Model Training → Save Model → API → Docker → CI/CD Automation
```

### 🔍 Explanation

1. `model.py` trains the ML model
2. Model is saved as `model.pkl`
3. `app.py` loads the model and serves predictions
4. Docker container runs the application
5. GitHub Actions automates the pipeline

---

## 🌐 API Endpoints

### 1️⃣ Home Route

```
GET /
```

**Response:**

```
API Running
```

---

### 2️⃣ Prediction Route

```
POST /predict
```

#### 📥 Request Body

```json
{
  "features": [14.5, 20.1, 90.2, 600, ...]
}
```

#### 📤 Response

```json
{
  "prediction": 0
}
```

---

## 🐳 Docker Setup

### Build Docker Image

```bash
docker build -t heart-api .
```

### Run Container

```bash
docker run -p 5000:5000 heart-api
```

---

## ⚡ CI/CD Pipeline (GitHub Actions)

This project uses GitHub Actions to automate the workflow.

### 🔄 Trigger

* Runs automatically on every push to `main` branch

### ⚙️ Pipeline Steps

1. Checkout code
2. Setup Python
3. Install dependencies
4. Train model
5. Build Docker image

---

## 🧠 DevOps for AI Explanation

This project demonstrates DevOps principles applied to Machine Learning:

* ✅ Automated workflows using CI/CD
* ✅ Environment consistency using Docker
* ✅ Reproducibility of results
* ✅ Seamless deployment pipeline

---

## 🎯 Key Learnings

* Machine Learning model deployment
* API development using Flask
* Docker containerization
* CI/CD pipeline automation
* MLOps fundamentals

---

