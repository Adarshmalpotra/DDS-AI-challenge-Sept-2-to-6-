# MortgageAI — Automated Mortgage Eligibility & Underwriting (DDS AI Challenge)

MortgageAI automates the entire mortgage eligibility and underwriting workflow using AI + n8n. 
It instantly computes FOIR, EMI, loan eligibility, generates underwriting summaries, compares banks, 
and produces personalized document checklists — reducing processing time from days to minutes.

---

## 🚀 Features

- Instant FOIR, EMI & loan eligibility calculation  
- AI‑generated underwriting summary  
- Bank‑wise comparison (HDFC, ICICI, SBI)  
- Personalized document checklist  
- Automated Google Drive folder creation  
- Google Sheets logging  
- Email automation (Day 1, 3, 7)

---

## 🧠 Brain of the App

A structured Claude‑powered underwriting engine orchestrated via n8n workflows.

Workflow link:  
https://akmzoho.app.n8n.cloud/workflow/dxScI0ZS4K8MO5uT?projectId=W6N8uSb0wiyvWz1y&new=true

---

## 🏗️ Architecture

Intake Form → Webhook → n8n Workflow → Claude Prompts → Sheets Log → Drive Folder → Email Output

---

## 📂 Repo Structure

