# leadflow-ai

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![LLM](https://img.shields.io/badge/LLM-OpenAI-green)
![Status](https://img.shields.io/badge/Status-Prototype-orange)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

**AI Lead Qualification & Automation Pipeline**

A modular AI system for analyzing, scoring, and activating inbound leads using LLMs, structured outputs, and rule-based logic.

This project demonstrates how to transform raw lead data into actionable business decisions:
prioritization, personalized responses, and automated routing — with a built-in safety layer.

---

## 🔁 Pipeline

ingest → sanitize → analyze → score → decide → respond → activate

- ingest: lead data from forms, CSV, CRM
- sanitize: input cleaning + prompt injection detection
- analyze: LLM extracts intent, needs, use cases
- score: deterministic scoring logic
- decide: priority assignment (A / B / C / Manual Review)
- respond: personalized email generation
- activate: simulated CRM push + outreach actions

---

## 🚀 Features

- LLM-based lead analysis (intent, maturity, use cases)
- Deterministic scoring & prioritization
- Context-aware email generation
- Prompt injection detection & safety routing
- GDPR-conscious data handling (email masking)
- Batch processing from CSV or dataset
- Activation layer (CRM + outreach simulation)

---

## 🧩 Example Output

| Lead | Score | Priority | Action |
|------|------:|----------|--------|
| High-intent SaaS lead | 95 | A | Book call |
| Exploratory lead | 50 | B | Qualification |
| Low-intent | 38 | C | Nurture |
| Suspicious input | 0 | Manual Review | Block automation |

---

## 🛡️ Safety Layer

This system treats all lead inputs as untrusted data.

Includes:
- prompt injection detection
- structured output validation (Pydantic)
- type-safe parsing (list normalization)
- security flag propagation
- manual review routing (no automation for risky leads)

---

## 🧪 Example Use Case

```python
df = pd.read_csv("leads.csv")
results = [process_lead(lead) for lead in df.to_dict(orient="records")]
pd.DataFrame(results)
```

Then:

- send emails to Priority A leads
- push qualified leads to CRM
- route flagged inputs to manual review

---

## 🏗️ Architecture (Conceptual)

Form / LinkedIn / CRM
        ↓
   Ingestion Layer
        ↓
   Safety Layer
        ↓
   LLM Analysis (OpenAI)
        ↓
   Scoring Engine
        ↓
   Decision Layer
        ↓
   Activation Layer
   (Email / CRM / Routing)

---

## 🔌 Production Integration (Example)

- Make / n8n → workflow orchestration  
- OpenAI API → analysis & generation  
- Airtable / HubSpot → CRM storage  
- Gmail / Slack → notifications & outreach  

---

## 📈 Business Impact

This system helps:

- reduce manual lead qualification time  
- respond faster to high-intent prospects  
- standardize sales analysis  
- personalize outreach at scale  
- prevent unsafe or adversarial automation  

---

## ⚠️ Limitations

This is a prototype, not a production system.

Missing components:

- persistent storage (DB / CRM sync)
- monitoring & logging
- retry / fallback logic
- advanced prompt injection defense
- A/B testing for email generation

---

## 🔭 Next Steps

- API integration (FastAPI / webhook)
- CRM integration (HubSpot, Pipedrive)
- improved scoring calibration
- multilingual support
- analytics (conversion rate, response time)
- stronger adversarial input detection

---

## 🎯 Positioning

This project is not a prompt demo — it is a decision system.

It combines:

- LLM-based reasoning  
- structured outputs  
- deterministic scoring  
- safety-aware design  
- business workflow automation  

The goal is to show how AI can be deployed as a reliable operational layer in real acquisition and sales pipelines.

---

## 📄 License

MIT
