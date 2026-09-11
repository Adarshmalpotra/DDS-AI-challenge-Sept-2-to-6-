MortgageAI — Automated Mortgage Eligibility & Underwriting (DDS AI Challenge 2026)

Instant FOIR, EMI & Underwriting — Automated, Accurate, Anytime.
MortgageAI is a no code/low code underwriting engine built using n8n, Anthropic Claude Sonnet, OpenAI GPT5/GPT4o, and Google Sheets/Drive. It automates FOIR, EMI, loan eligibility, multi bank underwriting rules, document checklists, and email delivery — all orchestrated through n8n.

Live Demo (n8n Workflow)
https://akmzoho.app.n8n.cloud/workflow/jKOCMXFHnfA3MjXr

 Repository Structure

Code
MortgageAI-DDS-AI-challenge-Sept-5-to-13/
│
├── docs/
│   └── progress/
│       └── DDS_Progress_Workbook_Adarsh_Days2-6.pdf
│
├── screenshots/
│   ├── workflow.png
│   ├── intake_form.png
│   ├── underwriting_output.png
│   └── sheets_logging.png
│
├── prompts/
│   ├── FOIR_EMI_Prompt.txt
│   ├── Underwriting_Prompt.txt
│   ├── Document_Checklist_Prompt.txt
│   └── PDF_Parsing_Prompt.txt
│

└── README.md

Architecture Overview

User Intake Form → n8n Webhook → Underwriting Engine → Sheets Logging → Email Output
MortgageAI uses a multi model strategy and deterministic underwriting schema to ensure accuracy, consistency, and reliability.

Core Components
	Claude Sonnet 4.5 → FOIR/EMI + underwriting logic
	GPT5 / GPT4o → PDF parsing fallback
	Google Sheets → Eligibility log
	Google Drive → Auto folder creation
	Gmail API → Email delivery
	n8n → Orchestration, validation, logging

FOIR & EMI Formula

FOIR (Fixed Obligation to Income Ratio)

FOIR="Total EMIs" /"Net Monthly Income" 

EMI (Equated Monthly Installment)

EMI=(P⋅R⋅(1+R)^N)/((1+R)^N-1)

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

🔧 Multi Model Strategy

Model	Use Case
Claude Sonnet 4.5	Underwriting, FOIR/EMI
GPT5	PDF parsing
GPT4o	Fast fallback parsing
This ensures robustness across document formats and underwriting scenarios.

Key Features

	Automated FOIR/EMI calculation
	
	Multi bank underwriting logic (HDFC, ICICI, SBI; Axis/Kotak planned)
	
	Personalized document checklist
	
	PDF parsing with fallback models
	
	Google Sheets logging
	
	Auto Drive folder creation
	
	Email delivery with underwriting summary
	
	Fully no code/low code implementation
	
	Deterministic JSON schema for reliability

Performance
	Underwriting latency: 1.8–2.4 sec
	Workflow latency: 3.5–5 sec
	End to end: ~6–7 sec
	Cost/run: $0.002–$0.006

Security
	PII masked
	Secrets stored in .env
	No keys in repo
	Validation nodes added
	Deterministic JSON schema
	Error handling + fallback prompts

Progress Workbook

Full progress (Days 2–6): /docs/progress/DDS_Progress_Workbook_Adarsh_Days2-6.pdf

How to Use / Test
	Open the n8n workflow link
	Submit intake form
	FOIR/EMI calculated
	Underwriting engine applies bank rules
	Document checklist generated
	Drive folder created
	Email sent with underwriting summary
	Logs stored in Google Sheets

Credits
Decoding Data Science — DDS AI Challenge 2026 Anthropic Claude OpenAI GPT n8n Automation Google Cloud APIs

Contact
Adarsh Kumar Malpotra Email: adarshmalpotra@gmail.com
