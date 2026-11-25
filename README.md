# Aitebaar - Kiryana AI

**Turning Unorganized Local Retail Data into Financial Power.**

Aitebaar (meaning *Trust*) is an AI-powered credit scoring and financial analytics platform designed to bridge the financial inclusion gap between small local retailers (*kiryana* stores) and formal banking institutions. By converting informal, handwritten ledgers and daily chat records into a verified **Alternative Credibility Score**, Aitebaar empowers small merchants to prove their creditworthiness and secure business loans without changing their daily workflow.

---

## 🎯 The Problem
Millions of neighborhood *kiryana* stores and micro-retailers operate entirely on informal record-keeping—handwritten paper registers (*khata*), rough slips, and WhatsApp order messages. When these merchants need capital to expand or handle emergencies, banks reject their loan applications due to a lack of formal credit history, audited statements, or verifiable documentation.

## 💡 The Solution
Aitebaar eliminates manual bookkeeping barriers by meeting shopkeepers where they already are:
1. **Capture:** Retailers simply snap photos of handwritten bills/registers or upload WhatsApp chat exports.
2. **Process & Validate:** Our AI extracts transaction values, tracks informal credit (*udhaar*) repayment behavior, and analyzes text sentiment for payment delays or disputes.
3. **Score & Connect:** The engine generates an **Aitebaar Trust Score (0–1000)** and an enterprise-ready **Bank Credit Risk Analytics Board**, enabling automated, data-backed loan eligibility decisions.

---

## ✨ Key Features

- **📸 Smart OCR (`ocr.py`)**
  - Digitizes photos of handwritten bills, rough receipts, and physical registers into structured transaction records.
  - Requires zero behavioral change from non-tech-savvy shopkeepers.
- **💬 WhatsApp Order & Chat Parser (`whatsapp_parser.py`)**
  - Automatically extracts order amounts and transaction logs from customer WhatsApp messages.
  - **AI Sentiment Validation:** Scans conversational text blocks for risk indicators (e.g., *"bounced check"*, *"dispute"*, *"paise kal doonga"* / payment delays) to calculate a Critical Credit Delay percentage.
- **🧠 The Credibility Engine (`score.py`)**
  - Computes an **Aitebaar Trust Score on a 0–1000 scale** based on three core pillars:
    1. **Transaction Volume Sum:** Total verified business turnover (e.g., PKR 85,000 across scanned statements).
    2. **Sentiment Risk Penalty:** Deductions based on detected credit delays and payment disputes.
    3. **Operational Consistency Trend:** Tracks revenue and credibility trajectory across document clusters over time.
- **🏦 Bank Credit Risk Analytics Board**
  - Visualizes **Operational Credibility Flow** across ledger clusters (`Doc-Cluster 01` to `Doc-Cluster N`).
  - Categorizes merchants into risk tiers (e.g., *High Risk Index* for scores below banking thresholds) and automates pre-approved loan gating (`Eligible` vs. `System Request Blocked`) to protect lenders from bad debt.
- **📱 Lightweight, Mobile-First Frontend**
  - Built with **React.js** and **Vite** for near-instant load times and full responsiveness across entry-level smartphones.

---

## 🏗️ Project Architecture

```text
aitebaar-kiryana-ai/
├── frontend/                  # Lightweight, responsive UI for merchants & banks
│   ├── src/                   # React components & Credit Risk Analytics Board
│   ├── index.html
│   └── vite.config.js         # Vite bundler configuration
├── backend/                   # AI processing & scoring pipeline
│   ├── ocr.py                 # Handwritten bill & ledger image-to-text extraction
│   ├── whatsapp_parser.py     # Chat log parser & NLP sentiment risk analyzer
│   └── score.py               # Trust Score (0–1000) calculation & eligibility engine
└── README.md
