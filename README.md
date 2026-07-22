# 📊 Enterprise Applied AI Analyst Portal

An end-to-end AI-powered business analytics workspace that integrates automated database population, customer segmentation machine learning pipelines, LLM-powered narrative generation, and an interactive executive web dashboard.

---

## 🌟 Key Features

1. **Synthetic Business Database Generator (`generate_db.py`)**:
   - Generates realistic transactional, customer demographic, and web activity data stored in a relational SQLite database (`analytics.db`).

2. **Machine Learning Analytics Engine (`analytics_engine.py`)**:
   - Performs feature engineering (RFM metrics + web engagement indicators).
   - Clusters customers into distinct behavioral segments using **Scikit-Learn K-Means Clustering**.
   - Calculates Silhouette scores and saves analytical profiles back to SQLite.

3. **AI Narrative & Executive Report Generator (`ai_narrator.py`)**:
   - Uses the **Groq Llama 3.3 70B** model to analyze statistical segment profiles.
   - Automatically constructs executive summaries and actionable business recommendations in `business_report.md`.

4. **FastAPI Backend Server (`app.py`)**:
   - Offers CRUD data editing, direct SQL sandbox querying, dynamic table management, and an interactive AI Business Analyst chatbot route.
   - Serves pre-built static React dashboard assets cleanly on Port 8000.

5. **Interactive React Frontend Dashboard (`frontend/`)**:
   - Built with React 18, Vite, and Chart.js.
   - Displays real-time charts, cluster insights, data tables, SQL executor, and an AI chat analyst interface.

---

## 🏗 Project Architecture

```
applied_ai_analyst_project/
├── app.py                   # FastAPI backend server & static web server
├── generate_db.py           # SQLite schema creation & mock dataset generator
├── analytics_engine.py      # Feature engineering & K-Means clustering script
├── ai_narrator.py           # AI executive report generator using Groq API
├── business_report.md       # Generated executive Markdown report
├── analytics.db             # Pre-built SQLite analytical database
├── requirements.txt         # Python package dependencies
├── .env.example             # Environment variable configuration template
├── .gitignore               # Git untracked pattern definitions
├── static/                  # Production-compiled React frontend build
└── frontend/                # React source code (Vite + Chart.js)
    ├── package.json
    ├── vite.config.js
    └── src/
        ├── App.jsx
        ├── App.css
        └── main.jsx
```

---

## 🚀 Quickstart Guide

### 1. Prerequisites
- Python 3.10+
- Node.js 18+ (optional, only if modifying or re-building the frontend)

### 2. Environment Setup

Clone the repository and set up a virtual environment:

```bash
git clone https://github.com/your-username/applied_ai_analyst_project.git
cd applied_ai_analyst_project

# Create & activate virtual environment
python -m venv venv

# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install Python dependencies
pip install -r requirements.txt
```

### 3. Configure API Key

Copy `.env.example` to `.env` and add your Groq API key:

```bash
cp .env.example .env
```

In `.env`:
```env
GROQ_API_KEY="your_groq_api_key_here"
```

---

## 🛠 Running the Pipeline

### Step 1: Generate Mock Database
```bash
python generate_db.py
```

### Step 2: Run Machine Learning Clustering
```bash
python analytics_engine.py
```

### Step 3: Generate AI Executive Narrative Report
```bash
python ai_narrator.py
```

### Step 4: Launch Web Dashboard & API Server
```bash
python app.py
```

Open your browser and navigate to:
👉 **`http://127.0.0.1:8000`**

---

## 💻 Frontend Development (Optional)

If you wish to modify the React dashboard interface:

```bash
cd frontend
npm install
npm run dev
```

To build production static assets into `/static` for `app.py`:

```bash
npm run build
```

---

## 🛡 Security & Best Practices

- Secret environment variables (`.env`) and local build artifacts (`venv/`, `node_modules/`, `__pycache__/`) are excluded via `.gitignore`.
- Always keep your API keys stored securely in `.env` and never commit them to source control.
