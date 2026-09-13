🌟 MortgageAI — Automated Mortgage Eligibility & Underwriting
DDS AI Challenge 2026 — Final Submission
A fully automated, no‑code/low‑code mortgage underwriting engine that delivers instant FOIR, EMI, eligibility, multi‑bank rule evaluation, document checklists, and email-ready underwriting summaries — all in under 7 seconds end‑to‑end.

MortgageAI demonstrates how modern agentic workflows, deterministic underwriting logic, and multi‑model AI orchestration can transform the mortgage approval pipeline into a fast, transparent, and error‑free digital experience.

🚀 Live Demo & Project Links
n8n Live Workflow Demo  
https://akmzoho.app.n8n.cloud/workflow/jKOCMXFHnfA3MjXr

Project Website (Lovable Platform)  
https://mortgagedash-ai.lovable.app/about

Primary Domain (WIX)  
https://www.mortgageai.co.in  
(Currently facing WIX–Aria editor restrictions; site not getting properly edited and giving improper result. Editing is temporarily kept on under hold and preferred to create project afresh at Lovable which is working properly and the domain migration to Lovable is in progress.)

🧭 Project Journey — From Concept to Final Build
MortgageAI began as a simple idea:
Can mortgage underwriting be made instant, accurate, and fully automated using a no‑code/low‑code stack?

Phase 1 — Problem Definition
Manual underwriting is slow, inconsistent, and heavily dependent on human interpretation.

FOIR/EMI calculations vary across banks.

Document requirements differ by profile.

PDF parsing is unreliable across formats.

The challenge demanded a deterministic, auditable, and scalable underwriting engine.

Phase 2 — Architecture Exploration
Initial attempts to build the website on WIX (mortgageai.co.in) ran into editor limitations due to the Aria design utility.
This caused:

Inability to modify layouts

Inconsistent rendering

Broken integrations

Pivot: Move to Lovable, which offered clean deployment, stable hosting, and rapid iteration.

Phase 3 — Multi‑Model Strategy
To ensure reliability:

Claude Sonnet 4.5 → FOIR/EMI + underwriting logic

GPT5 / GPT4o → PDF parsing fallback

Deterministic JSON schema → Ensures consistent outputs

n8n → Orchestration, validation, logging, email delivery

This multi‑model approach eliminated hallucinations and ensured predictable underwriting outcomes.

Phase 4 — Engineering & Automation
Built a complete underwriting pipeline:

Intake form

FOIR/EMI engine

Multi‑bank rules (HDFC, ICICI, SBI; Axis/Kotak planned)

Document checklist generator

Google Sheets logging

Auto Drive folder creation

Email delivery with underwriting summary

Phase 5 — Final Optimization
Achieved:

Underwriting latency: 1.8–2.4 sec

Workflow latency: 3.5–5 sec

End‑to‑end: ~6–7 sec

Cost/run: $0.002–$0.006

MortgageAI became fast, cheap, and production‑ready.

🧠 Architecture Overview
User Intake Form → n8n Webhook → Underwriting Engine → Sheets Logging → Email Output

MortgageAI uses a deterministic underwriting schema combined with multi‑model AI orchestration to ensure accuracy, consistency, and reliability.

Core Components
Claude Sonnet 4.5 — FOIR/EMI + underwriting logic

GPT5 / GPT4o — PDF parsing fallback

Google Sheets — Eligibility log

Google Drive — Auto folder creation

Gmail API — Email delivery

n8n — Orchestration, validation, logging

📊 FOIR & EMI Formula
FOIR (Fixed Obligation to Income Ratio)

FOIR & EMI Formula
FOIR (Fixed Obligation to Income Ratio)

𝐹𝑂𝐼𝑅 =  Total EMIs / Net Monthly Income

EMI (Equated Monthly Installment)

𝐸𝑀𝐼 =(𝑃⋅𝑅⋅(1+𝑅)^𝑁)/ ((1+𝑅)^𝑁-1))

🏦 Underwriting JSON Schema
json
{
  "foir": 0.45,
  "emi": 24500,
  "loan_eligibility": "Approved",
  "bank_rules": {
    "HDFC": "Pass",
    "ICICI": "Pass",
    "SBI": "Fail"
  },
  "risk_level": "Medium",
  "required_documents": [
    "PAN",
    "Aadhaar",
    "Salary Slips",
    "Bank Statements"
  ]
}
🔧 Multi‑Model Strategy
Model	Use Case
Claude Sonnet 4.5	Underwriting, FOIR/EMI
GPT5	PDF parsing
GPT4o	Fast fallback parsing


This ensures robustness across document formats and underwriting scenarios.

⭐ Key Features
Automated FOIR/EMI calculation

Multi‑bank underwriting logic (HDFC, ICICI, SBI; Axis/Kotak planned)

Personalized document checklist

PDF parsing with fallback models

Google Sheets logging

Auto Drive folder creation

Email delivery with underwriting summary

Fully no‑code/low‑code implementation

Deterministic JSON schema for reliability

⚡ Performance
Underwriting latency: 1.8–2.4 sec

Workflow latency: 3.5–5 sec

End‑to‑end: ~6–7 sec

Cost/run: $0.002–$0.006

🔐 Security
PII masked

Secrets stored in .env

No keys in repo

Validation nodes added

Deterministic JSON schema

Error handling + fallback prompts

📘 Progress Workbook
Full progress (Days 2–6):
/docs/progress/DDS_Progress_Workbook_Adarsh_Days2-6.pdf

🧩 How to Use / Test
Open the n8n workflow link

Submit intake form

FOIR/EMI calculated

Underwriting engine applies bank rules

Document checklist generated

Drive folder created

Email sent with underwriting summary

Logs stored in Google Sheets

🤝 Credits
Decoding Data Science — DDS AI Challenge 2026

Anthropic Claude

OpenAI GPT

n8n Automation

Google Cloud APIs

📬 Contact
Adarsh Kumar Malpotra  
Email: adarshmalpotra@gmail.com
