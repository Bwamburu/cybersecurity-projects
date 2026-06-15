# 06 — OSINT Investigation & Threat Intelligence Report

## 📌 Project Overview

Used open-source intelligence (OSINT) tools to conduct passive reconnaissance on a simulated target organisation. Mapped exposed assets, potential attack vectors, and digital footprint, then compiled a structured threat intelligence report with recommended mitigations.

---

## 🎯 Objectives

- Conduct passive reconnaissance without touching the target
- Map the organisation's digital footprint
- Identify exposed assets, subdomains, email addresses, and employee info
- Identify potential attack vectors from publicly available data
- Produce a threat intelligence report with recommendations

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| Shodan | Search exposed internet-facing assets |
| Maltego CE | Visual link analysis and OSINT mapping |
| TheHarvester | Email, subdomain, and IP harvesting |
| Google Dorking | Advanced search for exposed data |
| Recon-ng | Web reconnaissance framework |
| WHOIS / DNS lookup | Domain registration & DNS records |
| Hunter.io | Email format discovery |
| Have I Been Pwned | Check for credential exposure |

---

## 📋 OSINT Methodology

### Phase 1: Footprinting
- WHOIS lookups, DNS enumeration
- Google Dorking for exposed files/directories
- Shodan scan for internet-facing services

### Phase 2: Asset Discovery
- Subdomain enumeration with TheHarvester
- Email address harvesting
- Employee profiling via LinkedIn (passive)

### Phase 3: Vulnerability Mapping
- Map discovered assets to known CVEs
- Identify outdated software versions from banners
- Check credentials against breach databases

### Phase 4: Reporting
- Document all findings with evidence
- Assess exposure risk per finding
- Provide remediation recommendations

---

## 📂 Folder Structure

```
06-osint-threat-intelligence/
├── reports/          # Threat intelligence report
├── tools/            # Custom recon scripts, dork lists
├── notes/            # OSINT methodology, tool cheat sheets
└── screenshots/      # Evidence from recon activities
```

---

## ⚠️ Ethical Notice

All OSINT activities were conducted against a simulated/fictional organisation or with explicit permission. No unauthorised access was performed. OSINT is passive reconnaissance using only publicly available data.

---

## 🔑 Key Learnings

- Passive vs active reconnaissance
- Digital footprint analysis
- Shodan query syntax
- Google Dork construction
- Threat intelligence report writing
