# 🥧 Pipeline Intelligence Engine (PIE)

**Autonomous root-cause analysis for modern data workflows.**

Pipeline Intelligence Engine (PIE) is an agentic AI system that analyzes data pipeline failures, identifies root causes, and suggests actionable fixes using LLM-powered reasoning and tool-based execution.

---

## 🚀 Overview

Modern data pipelines (ETL, Dataflow, Airflow) often fail due to schema mismatches, missing tables, type errors, or performance bottlenecks. Debugging these issues is time-consuming and reactive.

**PIE acts as an intelligent debugging agent that:**

* Reads pipeline logs
* Understands failure context
* Identifies root causes
* Suggests concrete fixes

---

## 🧠 Key Features

* 🔍 **Log-driven failure analysis**
* 🧠 **Agentic reasoning using LangChain**
* 🛠️ **Actionable fix recommendations (not just summaries)**
* ⚙️ **Tool-integrated architecture (log reader, future DB tools)**
* 🐳 **Dockerized for production-style deployment**
* 🔁 **CI/CD pipeline via GitHub Actions**

---

## 🧩 System Architecture

![Image](https://images.openai.com/static-rsc-4/QYjq3tyOlU3IEThHTQujWxET87b9gQE-3ZyV0I2qq66lHODHV-vD4soC2BKYyONrYd4tIYJRHwmZPZ03cX_XvIfUSMrROuzboi-KyfIsFCIbMkjWADEImE02G7pDA-MGhB3MHYEXSuz8xhmo5JSEt4xUKLYNKeG8RPQVEzbo1KHWwuCUIgz_5C0dpQ6uDvx7?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/o5lPZxoRGyu5j56XaS_fZUuLypKgUjDlHTPnMYqXK26DDwwKSYM4UA5ok0b_6JTozmezlHQIID2Bal52SFwH-F_MV-GRSVJ9mWdlF8NhdsQZ03ylFzVQd0UeyV_dVG8UZY4Dodcp8PO_1tChEOb0g8FIkVJ2E5x6dq8OxhLpvzpsXV8uT5flupRECLvfSrUS?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/4lSH3mGTDZWBh6gT-OYkCp5asUF2s3mOEPyOciBec4bhrrNwhoG7sCTt0uJaIcL452Q2skG6akW4EDYybRnd55CgU8uy1PmaFHQvfPQcdJ9L45uz8PDOigmiP_sbewDTMX2rCP44-XueaFnZkuPuRTTMoruQVNUQjORJdeMz7r-hS5qE2RxAj-36A9EIksKK?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/swKvGWJ2-USIqxR4EzYEgOtOR5ZK5KydOMIHn_jBII9MW6rUXzJbKFAAlIBTQ5OwBo_QYYRm2GvWZneCcc_mDXQTzwAATalL94yqEMol2xuhvi_fFcKNFxnESn7ILLcyh58IUGS8AIlrXarBvgz4zf_TnYfclRIeoHS4qfdXMF5Y0q89eME9uxFfq6gbOQ0D?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/aJPiYs9xvWuZ2TXScjanSsbSPUmV-x0fjmJ1jYQhvCsekdKqR4c6os7KioB-R8UrkJw_yVBOy0mP4Ih99f9KYQYbio3Q4KNVTdDqUJUKgfH3B6N3POSZYHOmqygEZlLkS8XWAb3Gr0Caz-zKEzdvDiOCqhEGo6dwrId8gtZAoZCw2pm0ZNo94kfW68Z65sSD?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/C4I5iHzJZSfx_jdKNAM2wtS3AuEzQB0jvA5fgZtO8FIzjaY3AW2LqDw5x18KNIG9FXFfBYxzVRzg8nHVB-HgIAqZHY9nqgW3QwHM40kL_IsWPxuMISd-IPAvk9fP2d-zJzZF1yHbm4iSW3rCekihq9AbZc5HWE29DaYF1qr4X0Kfc27pvvgP6OyObnKzNw_L?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/pRgkcPw1IgAC2qVXHau6xzpTFlWAiTXEOSJuzu_c26VZh74MAi3tVoo74pFifwmp0t4W1K_JDPqxy-ZG86gwnvLErtxKOo8_o1Iu9hykX7sIwgwsZRxFOGxDRdqt4XLThPPPi3EkBvBY-SGv2XHUXwrXnxPIbRau6uzHLW24g3kQqxtBuHRaQGBqRUh0TZxr?purpose=fullsize)

```text
User / Alert
      ↓
FastAPI Service (API Layer)
      ↓
LangChain Agent (Reasoning Engine)
      ↓
Tool Layer (Log Reader, Future: DB / APIs)
      ↓
Root Cause + Fix Suggestion
```

---

## ⚙️ Tech Stack

* **Backend:** FastAPI
* **Agent Framework:** LangChain
* **LLM:** OpenAI / compatible models
* **Containerization:** Docker
* **CI/CD:** GitHub Actions
* **Language:** Python 3.11

---

## 📁 Project Structure

```bash
pipeline-intelligence-engine/
│
├── app/
│   ├── agent/
│   │   ├── agent.py
│   │   ├── tools.py
│   │
│   ├── api/
│   │   └── main.py
│
├── logs/
│   └── sample_failures.log
│
├── tests/
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
└── README.md
```

---

## ▶️ Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/your-username/pipeline-intelligence-engine.git
cd pipeline-intelligence-engine
```

---

### 2. Set environment variables

```bash
export OPENAI_API_KEY=your_api_key
```

---

### 3. Run locally

```bash
uvicorn app.api.main:app --reload
```

---

### 4. Test the API

```bash
curl -X POST http://127.0.0.1:8000/analyze \
-H "Content-Type: application/json" \
-d '{"question": "Pipeline failed due to missing column"}'
```

---

## 🐳 Run with Docker

```bash
docker build -t pie-agent .
docker run -p 8000:8000 pie-agent
```

---

## 🔁 CI/CD Pipeline

A basic CI pipeline is configured using GitHub Actions:

* Install dependencies
* Run tests
* Build Docker image

Workflow file:

```
.github/workflows/ci.yml
```

---

## 🧪 Example Failure Logs

```text
ERROR BigQuery: Column 'user_age' not found
ERROR MSSQL: Invalid object name 'transactions_archive'
ERROR Dataflow: Type mismatch INTEGER vs STRING
ERROR Timeout: Query exceeded execution limit
```

---

## 🧠 Example Output

```text
Root Cause:
Column 'user_age' is missing in the target table schema.

Fix:
Update the schema or modify the transformation query to align with existing columns.
```

---

## 🔒 Production Considerations

* Human-in-the-loop approval before executing fixes
* Secure handling of API keys and credentials
* Observability (logging, tracing)
* Cost control for LLM usage

---

## 🧭 Roadmap

* [ ] Structured JSON output
* [ ] Vector database for semantic log search
* [ ] GitHub PR automation for fixes
* [ ] Integration with Airflow / Dataflow
* [ ] Multi-agent architecture (debug + optimization agents)

---

## 🎯 Use Cases

* ETL pipeline debugging
* Dataflow job failure analysis
* Schema mismatch detection
* Query performance diagnostics

---

## 🤝 Contributing

Contributions, ideas, and improvements are welcome.

---

## 📄 License

MIT License

---

## 💡 Inspiration

Built to explore how agentic AI systems can move beyond chat interfaces into real-world infrastructure automation.
