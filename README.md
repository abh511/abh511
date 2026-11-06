<h1 align="center">Abhishek Bhosale</h1>
<p align="center"><b>Machine Learning • GenAI • Python Backends</b></p>

<p align="center">
  <a href="https://www.linkedin.com/in/abhishek-bhosale-6b0760292/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:abhishekbhosale0511@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://github.com/abh511?tab=repositories"><img src="https://img.shields.io/badge/Projects-181717?style=for-the-badge&logo=github&logoColor=white" alt="Projects" /></a>
</p>

---

## 👋 About me

I'm a final-year Computer Engineering student (Honours in Data Science) in Pune. I like projects that are measured against a baseline, tested, and packaged so someone else can actually run them. Lately that means RAG over long documents, LLM agents that write SQL safely, and forecasting models that are evaluated honestly.

```python
abhishek = {
    "based_in":   "Pune, India",
    "studying":   "B.E. Computer Engineering (Hons. Data Science) @ NMIET, SPPU",
    "graduating": 2027,
    "cgpa":       8.57,
    "building":   ["RAG systems", "LLM agents", "ML forecasting", "FastAPI backends"],
    "daily_os":   "Ubuntu",
    "open_to":    "Software / ML / GenAI internships",
}
```

---

## 🚀 Featured projects

### 🗄️ [AskDB](https://github.com/abh511/askDB): ask your database a question in plain English

![status](https://img.shields.io/badge/status-in_progress-orange?style=flat-square)
![eval](https://img.shields.io/badge/eval_set-100_hand--checked_questions-blue?style=flat-square)
![safety](https://img.shields.io/badge/safety_layers-4-success?style=flat-square)
![db](https://img.shields.io/badge/data-9_tables_%C2%B7_~100K_orders-informational?style=flat-square)

Type a business question, get back the SQL, a result table, a chart and a one-line answer, over a 9-table e-commerce database in PostgreSQL.

- Only the two generation steps call the LLM; everything else is plain, unit-tested Python
- Four safety layers: a sqlglot guard (single `SELECT`, known tables only), a read-only DB role, a 5 s timeout and a 500-row limit
- 100 hand-checked questions in three difficulty tiers, plus a test that keeps few-shot examples out of the eval set

<details>
<summary><b>How it works</b></summary>
<br/>

```mermaid
flowchart LR
    Q([Question in plain English]) --> S[Schema retrieval]
    S --> F[Few-shot example selection]
    F --> G[SQL generation]
    G --> V{sqlglot guard}
    V -- safe --> DB[(PostgreSQL<br/>read-only role)]
    V -- rejected --> G
    DB -- error --> G
    DB -- rows --> A([SQL + table + chart + answer])
```

</details>

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" />
  <img src="https://img.shields.io/badge/Groq-F55036?style=flat-square" />
  <img src="https://img.shields.io/badge/ChromaDB-FF6F61?style=flat-square" />
  <img src="https://img.shields.io/badge/sqlglot-555555?style=flat-square" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
</p>

---

### 🌍 [EnviroWatch AI](https://github.com/abh511/EAI): environmental risk monitoring and forecasting

![accuracy](https://img.shields.io/badge/balanced_accuracy-91%25_%28baseline_80%25%29-success?style=flat-square)
![recall](https://img.shields.io/badge/high--risk_periods_caught-98%25-success?style=flat-square)
![tests](https://img.shields.io/badge/tests-25_automated-brightgreen?style=flat-square)

A full-stack platform that tracks 7 environmental indicators (air, water, noise, emissions, waste, urban heat, groundwater) across 20 locations in Pune and Mumbai, with alerts, 48-hour forecasts and an interactive risk map.

- Random Forest + XGBoost ensemble that forecasts risk 3 hours ahead, validated on a time split of simulated sensor data
- Anomaly detection that mixes physical-limit rules with an Isolation Forest to flag faulty sensor readings
- Site-suitability engine that scores 12 building types, plus a what-if simulator for traffic, industry and weather
- Supabase PostgreSQL storage with migrations, seeding scripts and a CSV fallback

<p>
  <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" />
  <img src="https://img.shields.io/badge/XGBoost-EC6B23?style=flat-square" />
  <img src="https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white" />
  <img src="https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" />
</p>

---

### 📚 [AwarePDF](https://github.com/abh511/AwarePDF): a study assistant for engineering textbooks

![index](https://img.shields.io/badge/1%2C126_pages_indexed_in-~5_min-blueviolet?style=flat-square)
![latency](https://img.shields.io/badge/answers_in-5--8_s-blueviolet?style=flat-square)
![citations](https://img.shields.io/badge/answers_cite-page_numbers-informational?style=flat-square)

A RAG assistant for 700+ page textbooks. It answers with page citations and supporting diagrams, and can write chapter summaries, topic outlines and exam key points.

- Hybrid retrieval: dense search + BM25, merged with reciprocal rank fusion, then reranked with a cross-encoder
- Layout-aware ingestion with Docling that keeps section and page metadata and splits tables with repeated headers
- Background diagram captioning with a vision model, and resumable processing keyed by file hash

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Docling-6E40C9?style=flat-square" />
  <img src="https://img.shields.io/badge/ChromaDB-FF6F61?style=flat-square" />
  <img src="https://img.shields.io/badge/BM25-555555?style=flat-square" />
  <img src="https://img.shields.io/badge/Groq-F55036?style=flat-square" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
</p>

---

## 🛠️ Tech stack

| Area | Tools |
|---|---|
| **Languages** | Python, SQL, Java, C++ |
| **Machine Learning** | Scikit-learn, XGBoost, Pandas, NumPy, PySpark, time-series forecasting, anomaly detection |
| **GenAI** | RAG, hybrid search, cross-encoder reranking, text-to-SQL agents, prompt engineering, LLM evaluation, LangChain, ChromaDB, sentence-transformers, Groq |
| **Backend & Data** | FastAPI, PostgreSQL, Supabase, SQLAlchemy, React |
| **Tools** | Linux (Ubuntu), Docker, Git/GitHub, pytest, MLflow, Power BI, Claude Code, ChatGPT, GitHub Copilot |

---

<table>
<tr>
<td valign="top" width="50%">

### 📜 Certifications

- **AI & Data Science**, Drishti CPS (IIT Indore), 2026
- **Python**, Kaggle, 2026
- **SQL**, Intellipaat, 2026

</td>
<td valign="top" width="50%">

### 🤝 Activities

- **Technical Assistant**, Technical Club, NMIET
- **Bootcamp Mentor**: mentored 100+ junior students in programming and problem-solving

</td>
</tr>
</table>

## 🎯 Right now

- 🔬 Running the AskDB evaluation and publishing the accuracy results
- 🌐 Deploying my projects with live demo links
- 💼 Looking for a Software / ML / GenAI internship starting 2027

---

<p align="center"><i>Thanks for stopping by. If a project is useful to you, a ⭐ is appreciated.</i></p>
