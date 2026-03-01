#  Career AI: Personal Branding, Powered by Intelligence.

##  Project Description
Career AI is an intelligent, adaptive platform designed to accelerate career growth for CSE students and tech professionals. Moving beyond generic advice, it leverages an advanced GenAI backend and live data retrieval to provide highly personalized, actionable strategies for personal branding, skill development, and professional networking.

Built with a focus on low-latency execution and continuous feedback loops, the architecture acts as a comprehensive "Entry to Excellence," comparing user profiles against top-tier MNC (FAANG) benchmarks.

### Core Architecture & Features:
* **✨ LinkedIn Identity Optimizer:** Analyzes your current professional presence against industry standards and dynamically rewrites headlines and summaries using customized voice tones. Includes a Banner Studio for generative AI background creation.
* **📊 Skill Gap Analyzer:** Utilizes K-Means Clustering and interactive Radar Charts to mathematically compare a user's current technical DNA against target job requirements, generating strict, AI-driven 3-month closing roadmaps.
* **🤝 Connection Hub (Real-Time RAG):** An autonomous agent pipeline that generates precise search queries, scrapes live LinkedIn data via Serper.ai, and synthesizes personalized "Why Connect" outreach pitches.
* **🔥 Viral Scorecard:** A predictive engine evaluating the engagement probability of technical posts before publication, reinforced by a continuous database-driven user feedback loop.

---

## 🛠 Tech Stack
This project implements a modern, modular Python architecture, prioritizing execution speed and seamless API integration.

* **Frontend UI:** Streamlit (Enhanced with Custom CSS Glassmorphism & State Management)
* **Backend & Database:** Supabase (PostgreSQL for Auth, Profiles, Skill Matrix, and Feedback Logging)
* **Large Language Model (LLM):** Google Gemini 1.5 Flash
* **Retrieval-Augmented Generation (RAG):** Serper.ai API (Live Google Search scraping)
* **Generative Image AI:** Hugging Face Inference API (Stable Diffusion XL)
* **Machine Learning / Analytics:** Scikit-Learn (K-Means, Random Forest), Plotly (Interactive Radar Charts), Pandas.
* **Performance:** Native Streamlit Caching (`@st.cache_data`) for sub-second page routing.

---

## ⚙️ Setup & Installation Instructions

Follow these instructions to run the application locally.

### 1. Clone the Repository
```bash
git clone [https://github.com/shanmukha-sasi/Career-AI.git](https://github.com/shanmukha-sasi/Career-AI.git)
cd Career-AI
```

### 2. Create a Virtual Environment
It is strictly recommended to isolate dependencies.
```bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure Environment Secrets
This application requires multiple API keys to function. Create a `.streamlit` folder in the root directory and add a `secrets.toml` file. 

```bash
mkdir .streamlit
touch .streamlit/secrets.toml
```

Populate `.streamlit/secrets.toml` with your specific credentials:
```toml
# Supabase Configuration
SUPABASE_URL = "your_supabase_project_url"
SUPABASE_KEY = "your_supabase_anon_key"

# AI & API Keys
GEMINI_API_KEY = "your_google_gemini_api_key"
SERPER_API_KEYS = ["your_primary_serper_key", "your_fallback_serper_key"]
HUGGINGFACE_API_KEY = "your_huggingface_token"
```

### 5. Initialize the Application
Run the Streamlit server to launch the platform.
```bash
streamlit run app.py
```

You can check out the live website here :
https://career-aigit-hg9ltgxv4kakbggpexvyjt.streamlit.app
