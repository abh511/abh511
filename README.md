# Hi, I'm Abhishek Bhosale 👋

**Final-year Computer Engineering student (Honours in Data Science) building end-to-end ML and GenAI systems.**

I like projects that are measured against a baseline, tested, and packaged so someone else can run them. Lately that means RAG over long documents, LLM agents that write SQL safely, and forecasting models that are evaluated honestly.

📍 Pune, India &nbsp;·&nbsp; 🎓 NMIET (SPPU), B.E. 2027, CGPA 8.57 &nbsp;·&nbsp; 💼 Open to Data Science / ML / GenAI internships

<p>
<a href="https://www.linkedin.com/in/abhishek-bhosale-6b0760292/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="mailto:abhishekbhosale0511@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
</p>

---

## 🔥 Featured Projects

### 🗄️ [AskDB](https://github.com/abh511/askDB): Natural-Language Analytics Agent *(in progress)*
Ask a business question in plain English and get back the SQL, a result table, a chart and a one-line answer, over a 9-table, ~100K-order e-commerce database in PostgreSQL.
- Pipeline: schema retrieval → few-shot example selection → SQL generation → automatic retry on database errors
- Four safety layers: a sqlglot guard (single SELECT, known tables only), a read-only DB role, a 5 s timeout and a 500-row limit
- Evaluation harness of **100 hand-checked questions** in three difficulty tiers, with a leakage test between few-shot examples and the eval set

`Python` `PostgreSQL` `LangChain` `Groq` `ChromaDB` `sqlglot` `FastAPI` `MLflow` `Docker`

### 🌍 [EnviroWatch AI](https://github.com/abh511/EAI): Environmental Risk Monitoring & Forecasting
Full-stack platform monitoring 7 environmental indicators (air, water, noise, emissions, waste, urban heat, groundwater) across 20 locations in Pune and Mumbai, with alerts, 48-hour forecasts and a risk map.
- Random Forest + XGBoost ensemble forecasting risk 3 hours ahead: **91% balanced accuracy vs. an 80% baseline**, catching **98%** of high-risk periods (time-split, simulated sensor data)
- Anomaly detection combining physical-limit rules with an Isolation Forest
- Site-suitability engine scoring 12 building types, plus a what-if simulator for traffic, industry and weather
- Supabase PostgreSQL storage with migrations and CSV fallback; 25 automated tests

`React` `FastAPI` `scikit-learn` `XGBoost` `Supabase` `pytest`

### 📚 [AwarePDF](https://github.com/abh511/AwarePDF): AI Study Assistant for Engineering Textbooks
RAG assistant for 700+ page textbooks: answers with page citations and supporting diagrams, chapter summaries, topic outlines and exam key points.
- Hybrid retrieval: dense search + BM25 merged with reciprocal rank fusion, then cross-encoder reranking
- Layout-aware ingestion with Docling that keeps section and page metadata and splits tables with repeated headers
- Indexes a **1,126-page book in ~5 min** and answers in **5–8 s**; background diagram captioning with a vision model

`Python` `FastAPI` `Docling` `ChromaDB` `BM25` `Groq` `Docker`

---

## 🛠️ Tech Stack

| Area | Tools |
|---|---|
| **Languages** | Python, SQL, Java, C++ |
| **Machine Learning** | Scikit-learn, XGBoost, Pandas, NumPy, time-series forecasting, anomaly detection |
| **GenAI** | RAG, hybrid search, cross-encoder reranking, text-to-SQL agents, prompt engineering, LLM evaluation, LangChain, ChromaDB, sentence-transformers, Groq |
| **Backend & Data** | FastAPI, PostgreSQL, Supabase, SQLAlchemy, React |
| **Tools** | Docker, Git/GitHub, pytest, MLflow, Power BI, Claude Code, ChatGPT, GitHub Copilot |

<p>
<img src="https://skillicons.dev/icons?i=python,postgres,fastapi,react,docker,git,supabase,java,cpp" />
</p>

---

## 📜 Certifications

- **AI & Data Science**: Drishti CPS (IIT Indore), 2026
- **Python**: Kaggle, 2026
- **SQL**: Intellipaat, 2026

## 🤝 Activities

- **Technical Assistant**, Technical Club, NMIET
- **Bootcamp Mentor**: mentored 100+ junior students in programming and problem-solving

---

## 🎯 Currently

- Running the AskDB evaluation and publishing the accuracy results
- Deploying my projects with live demo links
- Looking for a Data Science / ML / GenAI internship starting 2027

<p align="center"><i>Thanks for visiting. If a project is useful to you, a ⭐ is appreciated.</i></p>
