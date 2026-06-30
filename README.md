# 🚀 Parth Mhatre — Software Developer & ML Engineer

<div align="center">

### Building Production-Ready AI Systems That Solve Real-World Problems

**[🌐 Portfolio](https://parth-s-mhatre.netlify.app/) • [💼 LinkedIn](https://linkedin.com/in/parthmhatre41) • [📧 Email](mailto:parth.mhatre4141@gmail.com) • [🎓 Resume](./RESUME.pdf)**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-ff6b35?style=for-the-badge)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)

</div>

---

## 📊 Quick Stats

| Metric | Value |
|--------|-------|
| **Projects Shipped** | 4 production systems |
| **ML Model R²** | 99%+ (LoadIQ ensemble) |
| **MAPE Accuracy** | < 1.5% (time-series forecasting) |
| **Users Reached** | 500+ monthly active (LoadIQ) |
| **API Response Time** | Optimized from 2.3s → 380ms |
| **Data Processed** | 6 years of half-hourly grid data |
| **GitHub Stars** | 50+ across repositories |
| **Certifications** | 15+ (Deep Learning, AI, Backend, Cloud) |

---

## 🌟 Featured Project: LoadIQ

### AI-Powered Electricity Load Forecasting Platform

<div align="center">
  <a href="https://github.com/Parth-S-Mhatre/LoadIQ">
    <img src="https://img.shields.io/badge/View%20Repository-GitHub-181717?style=for-the-badge&logo=github" />
  </a>
  <a href="https://loadiq-smart-ai.web.app/">
    <img src="https://img.shields.io/badge/Live%20Demo-Firebase%20Hosting-FFCA28?style=for-the-badge&logo=firebase" />
  </a>
</div>

#### Project Overview
LoadIQ predicts real-time electricity demand across **4 countries (UK, USA, Germany, India)** using advanced ML ensemble methods trained on **6 years of half-hourly transmission-level grid data** (180K+ data points, zero null values).

#### 🎯 Key Achievements

| Achievement | Details |
|-------------|---------|
| **ML Model Performance** | R² > 99% • MAPE < 1.5% • Chronological train/test split |
| **Ensemble Architecture** | LightGBM (60%) + XGBoost (40%) • Ridge regression fallback |
| **Feature Engineering** | 43-55 features • Lag windows (1h-168h) • Rolling statistics |
| **API Optimization** | Response time: 2.3s → 380ms (83% reduction) • Batch prediction support |
| **Frontend UX** | Lazy loading • Skeleton screens • Three.js WebGL globe |
| **Deployment** | Docker containerization • Nginx reverse proxy • Firebase Hosting |
| **Reliability** | Connection-refused guard • WebGL context recovery • Error fallback system |

#### 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                   LoadIQ Platform                            │
├─────────────────────────────────────────────────────────────┤
│                                                               │
│  Frontend (React 18 + TypeScript)                            │
│  ├─ Lazy-loaded pages (code splitting)                       │
│  ├─ Skeleton-first UI (instant perceived load)               │
│  ├─ Three.js WebGL globe (4-country visualization)           │
│  └─ Recharts forecasting dashboard                           │
│                                                               │
│  ↓ Unified API Layer (Connection Guard)                      │
│                                                               │
│  Backend (FastAPI + Uvicorn)                                 │
│  ├─ Model1.py (Port 8001: DE+LU Load Prediction)             │
│  ├─ Model2.py (Port 8002: GB Load Prediction)                │
│  ├─ Health checks & request validation                       │
│  └─ Batch prediction (24-168 steps ahead)                    │
│                                                               │
│  ML Inference Layer                                          │
│  ├─ LightGBM Model (primary, 60% weight)                     │
│  ├─ XGBoost Model (secondary, 40% weight)                    │
│  ├─ Ridge Regression (fallback)                              │
│  └─ Feature preprocessing (median fill for missing)          │
│                                                               │
│  Data Layer                                                  │
│  ├─ Training: 50.4K rows (DE+LU, 60-min intervals)           │
│  ├─ Training: 100.8K rows (GB, 30-min intervals)             │
│  ├─ Time range: 2015-2020 (6 years of grid data)             │
│  └─ Features: 45-46 columns per dataset                      │
│                                                               │
│  Monitoring & Logging                                        │
│  └─ Firebase Firestore (exception logging, analytics)        │
│                                                               │
└─────────────────────────────────────────────────────────────┘
```

#### 💡 Smart Engineering Decisions

| Decision | Impact |
|----------|--------|
| **Demand-based page loading** | Reduced bundle size by 45% |
| **Skeleton-first UI** | Users perceive <500ms load time |
| **Median-fill strategy** | Preserves model integrity vs. zero-fill |
| **TimeSeriesSplit CV** | Prevents data leakage in temporal data |
| **Ensemble blending** | Smooths variance at peak transitions |
| **Dual-server architecture** | Country-specific models optimize for regional patterns |
| **Connection fallback** | Graceful degradation when backend offline |

#### 🔧 Tech Stack

**Frontend:** React 18 • TypeScript • Three.js • Recharts • Firebase Hosting

**Backend:** FastAPI • Uvicorn • Python 3.10+ • Nginx

**ML Models:** LightGBM • XGBoost • Ridge Regression • Scikit-learn

**Data:** Pandas • NumPy • ENTSO-E Transparency Platform

**Infrastructure:** Docker • Firebase Auth & Firestore • Google Cloud Platform

#### 📈 Results & Metrics

```
Model Performance (Chronological Test Set):
├─ LightGBM:     R² = 0.992 • MAPE = 1.1%
├─ XGBoost:      R² = 0.985 • MAPE = 1.8%
├─ Ridge:        R² = 0.935 • MAPE = 3.8%
└─ Ensemble:     R² = 0.993 • MAPE = 1.4% ✓

API Performance:
├─ Single prediction: 380ms (avg)
├─ Batch (24-step):  2.1s
└─ p95 latency:      650ms
```

#### 🚀 Quick Start

```bash
# Clone & setup
git clone https://github.com/Parth-S-Mhatre/LoadIQ.git
cd LoadIQ

# Backend (Terminal 1)
cd Backend && pip install -r requirements.txt
python Model1.py  # Port 8001
python Model2.py  # Port 8002

# Frontend (Terminal 2)
cd energy-analytics && npm install && npm start
# Opens http://localhost:3000
```

See [LoadIQ README](https://github.com/Parth-S-Mhatre/LoadIQ) for full setup & API documentation.

---

## 🎓 Other Notable Projects

### 📊 Student Performance Dashboard
**Tech:** Streamlit • Scikit-learn • Plotly • Python

- Predictive ML system forecasting student academic outcomes on 1000+ records
- **Accuracy:** 85% with comprehensive cross-validation
- Feature engineering: standardization, one-hot encoding, polynomial features
- Real-time prediction API with personalized recommendations
- [Repository](https://github.com/Parth-S-Mhatre/studentdashboard-app)

---

### 🤖 ML/DL Projects Portfolio
**Tech:** Python • PyTorch • TensorFlow • Scikit-learn

Comprehensive collection demonstrating breadth across ML domains:

| Project | Type | Highlight |
|---------|------|-----------|
| **Reinforcement Learning** | RL | Self-driving car simulation, Lunar Lander, Q-Learning with Pygame |
| **Customer Churn Prediction** | Classification | Ensemble: Logistic Regression, Random Forest, SVM, Gradient Boosting |
| **Car Price Predictor** | Regression | Linear Regression + Flask deployment |
| **Titanic Survival** | Classification | 81% accuracy • Complete ML pipeline |
| **Mumbai House Prices** | Regression | Advanced feature engineering |

Each project includes: EDA, preprocessing, model selection, cross-validation, evaluation metrics.

[Full Portfolio](https://github.com/Parth-S-Mhatre/ml-dp_projects)

---

### 🔧 Backend & API Development
**Tech:** Java • Spring Boot • Maven • REST APIs

- **API Basics Mastery:** REST principles, HTTP methods, JSON, async operations
- **Journal Application:** Building production-grade backend with Spring Boot
- Hands-on Java exercises demonstrating DSA and core CS concepts
- [Java DSA](https://github.com/Parth-S-Mhatre/DSA-Java)

---

### 💻 Python Core & Algorithms
**Tech:** Python • Algorithms • Data Structures

Clean examples demonstrating Python best practices and algorithmic thinking.

[Python Core Repository](https://github.com/Parth-S-Mhatre/python_core)

---

## 🤝 Open Source Contributions

### AttendX — Attendance Management System

**Contributions:**
- ✅ Resolved API rate-limit instability via 30-second backoff strategy
- ✅ Reduced failed API calls by 60% during peak load
- ✅ Built modular React landing-page components
- ✅ Improved component library for responsive design
- ✅ End-to-end integration testing & deployment

[Repository](https://github.com/krishv24/Attend-X)

---

## 🎯 Technical Skills

### Machine Learning & AI
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square) 
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square)
![LightGBM](https://img.shields.io/badge/LightGBM-ff6b35?style=flat-square)
![XGBoost](https://img.shields.io/badge/XGBoost-ff6b35?style=flat-square)

**Core Competencies:** Time-Series Forecasting • Ensemble Methods • Feature Engineering • Model Optimization • Reinforcement Learning

### Backend & API
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square)
![Java](https://img.shields.io/badge/Java-007396?style=flat-square)
![Spring%20Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square)

**Core Competencies:** RESTful API Design • Microservices • Error Handling • Request Optimization

### Frontend
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square)
![Recharts](https://img.shields.io/badge/Recharts-FF7300?style=flat-square)

**Core Competencies:** Component Architecture • Lazy Loading • Skeleton Screens • WebGL Optimization

### Cloud & DevOps
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat-square)
![Google%20Cloud](https://img.shields.io/badge/Google%20Cloud-4285F4?style=flat-square)

**Core Competencies:** Containerization • Cloud Deployment • Monitoring & Logging

### Data & Databases
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat-square)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square)

---

## 🏆 Education & Certifications

### Education
**Bachelor of Technology in Computer Engineering** (AI & Data Science Specialization)  
Pillai College of Engineering, Mumbai | Aug 2023 - June 2027  


### Professional Certifications
- ✅ IBM Deep Learning with PyTorch, Keras and TensorFlow (March 2026)
- ✅ Machine Learning Specialization — DeepLearning.AI, Stanford (June 2025)
- ✅ Deep Learning with PyTorch (IBM, Feb 2026)
- ✅ Deep Learning with Keras & TensorFlow (IBM, Dec 2025)
- ✅ Introduction to Neural Networks & PyTorch (IBM, Jan 2026)
- ✅ AI Capstone Project with Deep Learning (IBM, Mar 2026)
- ✅ AI Agents and Agentic AI with Python (Vanderbilt, Aug 2025)
- ✅ API Basics: REST, HTTP, JSON (Scrimba, April-June 2026)
- ✅ Google Cloud Fundamentals & Hands-on Labs
- Plus 6 additional courses in Cloud, ML, and Backend Development

**Total:** 15+ Professional Certifications

---

## 📝 Blog & Articles

Writing technical deep-dives on key projects:

- **[Building AI-Powered Energy Forecasting at Scale](https://dev.to)** — LoadIQ architecture, challenges, and lessons learned
- **[Production ML: From 2.3s to 380ms API Response Time](https://dev.to)** — Optimization techniques and profiling
- **[Feature Engineering for Time-Series: The LoadIQ Approach](https://dev.to)** — 43-55 features, lag windows, temporal encoding

---

## 💬 Get In Touch

- **GitHub:** [@Parth-S-Mhatre](https://github.com/Parth-S-Mhatre)
- **LinkedIn:** [@parthmhatre41](https://linkedin.com/in/parthmhatre41)
- **Email:** [parth.mhatre4141@gmail.com](mailto:parth.mhatre4141@gmail.com)
- **Portfolio:** [parth-s-mhatre.netlify.app](https://parth-s-mhatre.netlify.app)

---

## 📄 Quick Links

- [Resume (PDF)](./RESUME.pdf)
- [LoadIQ Repository](https://github.com/Parth-S-Mhatre/LoadIQ)
- [LoadIQ Live Demo](https://loadiq-smart-ai.web.app/)
- [ML/DL Projects](https://github.com/Parth-S-Mhatre/ml-dp_projects)
- [Student Dashboard](https://github.com/Parth-S-Mhatre/studentdashboard-app)

---

<div align="center">

**Last Updated:** June 2026  
*Building the future of AI-powered systems, one project at a time.*

</div>
