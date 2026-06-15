# 05 — Cybersecurity Risk Assessment (ISO 27001 / NIST CSF)

## 📌 Project Overview

Conducted a full GRC (Governance, Risk & Compliance) risk assessment for a simulated small-to-medium enterprise (SME) using ISO 27001 and NIST Cybersecurity Framework (CSF). Identified assets, threats, and vulnerabilities, calculated risk scores, and produced a complete risk register and treatment plan.

---

## 🎯 Objectives

- Define the scope and boundaries of the assessment
- Identify and classify information assets
- Identify threats and vulnerabilities per asset
- Calculate inherent and residual risk scores
- Map findings to ISO 27001 controls and NIST CSF functions
- Produce a risk register and treatment plan
- Provide compliance recommendations

---

## 🛠️ Frameworks Used

| Framework | Purpose |
|-----------|---------|
| ISO/IEC 27001:2022 | Information security management controls |
| NIST Cybersecurity Framework (CSF) | Identify, Protect, Detect, Respond, Recover |
| CVSS v3 | Vulnerability severity scoring |

---

## 📋 Risk Assessment Methodology

### Step 1: Asset Identification
- Categorise assets: Hardware, Software, Data, People, Services

### Step 2: Threat & Vulnerability Identification
- Identify threats per asset (human, environmental, technical)
- Map known vulnerabilities

### Step 3: Risk Calculation
```
Risk Score = Likelihood (1–5) × Impact (1–5)

Risk Level:
  1–5   → Low
  6–12  → Medium
  13–19 → High
  20–25 → Critical
```

### Step 4: Risk Treatment
- Accept / Mitigate / Transfer / Avoid
- Map mitigations to ISO 27001 Annex A controls

### Step 5: Reporting
- Risk register with all findings
- Treatment plan with prioritised actions
- Compliance gap analysis

---

## 📂 Folder Structure

```
05-grc-risk-assessment/
├── reports/          # Risk register, treatment plan, compliance report
├── tools/            # Risk scoring templates (Excel/CSV)
├── notes/            # Framework references, methodology notes
└── screenshots/      # Evidence and documentation
```

---

## 📄 Report Template

See [`reports/risk-assessment-report-template.md`](./reports/risk-assessment-report-template.md)

---

## 🔑 Key Learnings

- ISO 27001:2022 Annex A controls
- NIST CSF five functions and categories
- Risk matrix construction and scoring
- Risk treatment option selection
- Writing a professional GRC report
