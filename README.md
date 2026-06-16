# Intelligent Phishing Website Detection System

An enterprise-grade, real-time cybersecurity solution designed to identify, evaluate, and mitigate phishing threats before they reach the user. This system utilizes a decoupled, full-stack architecture: a lightweight browser extension handles client-side event monitoring, while a robust machine learning backend extracts lexical and network features to classify suspicious URLs instantly.

---

## 📁 Repository Architecture
As structured in this repository, the system splits client and server responsibilities cleanly to maintain low latency and high security:

* **`extension/`** (Client Layer): A browser extension built using the WebExtensions API. It intercepts navigation hooks, handles real-time user alerting, and communicates securely with the detection server.
* **`backend/`** (Intelligence Layer): A Python-powered API handling heavy computational logic, feature extraction pipelines, and machine learning model inference.

---

## 🛠️ Technical Stack
* **Frontend / Client Extension:** JavaScript (ES6+), HTML5, CSS3, WebExtensions API
* **Backend API Framework:** Python 3.x (Flask / FastAPI)
* **Data Science & Machine Learning:** Scikit-Learn, Pandas, NumPy
* **Core Methodology:** Lexical Analysis (URL length, special character counts, sub-domain counts), Administrative Feature Analysis (SSL presence, domain age hooks), and Supervised Machine Learning Classification.

---

## 🚀 Key Features
* **Real-Time Client Ingestion:** Monitors and intercepts malicious browser requests instantaneously during active navigation.
* **Decoupled Processing Engine:** Keeps the extension highly performant by offloading complex machine learning classifications to a separate, dedicated server.
* **Intelligent Feature Extraction:** Automatically parses raw URLs into numerical feature vectors tracking heuristic and structural anomalies.
* **Intuitive Alert UI:** Features a proactive user blocking mechanism that warns users of phishing vectors before page rendering completes.

---

## ⚙️ Installation and Setup

### 1. Backend Server Deployment
Navigate to the backend directory, isolate your dependencies, and run the classification microservice:
```bash
cd backend

# Create and activate a clean Python virtual environment
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

# Install production dependencies
pip install -r requirements.txt

# Start the URL detection microservice
python app.py
