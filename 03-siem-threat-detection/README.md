# 03 — SIEM Log Monitoring & Threat Detection (Wazuh)

## 📌 Project Overview

Deployed Wazuh as a SIEM solution in a home lab to ingest and analyse system and network logs. Created custom detection rules, dashboards, and alerting workflows to identify and respond to suspicious security events.

---

## 🎯 Objectives

- Deploy and configure Wazuh SIEM manager and agents
- Ingest logs from multiple sources (Linux, Windows)
- Create custom detection rules for common attack patterns
- Build security dashboards for real-time monitoring
- Document incident response workflows

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| Wazuh | SIEM platform (manager + agent) |
| Elastic/OpenSearch | Log indexing and dashboards |
| Ubuntu Server | Wazuh manager host |
| Kali Linux | Simulated attacker machine |
| Windows 10 VM | Monitored endpoint |
| VirtualBox | Virtualisation platform |

---

## 📋 Detection Rules Created

| Rule ID | Description | Severity |
|---------|-------------|----------|
| 100001 | Multiple failed SSH logins (brute force) | High |
| 100002 | Successful login after multiple failures | Critical |
| 100003 | Privilege escalation via sudo | High |
| 100004 | New user account created | Medium |
| 100005 | Outbound connection to unusual port | Medium |
| 100006 | File integrity change in /etc/ | High |

---

## 📋 Methodology

### Phase 1: Deployment
- Installed Wazuh manager on Ubuntu Server
- Enrolled Linux and Windows agents
- Configured log collection sources

### Phase 2: Rule Development
- Analysed default Wazuh ruleset
- Created custom rules in `/var/ossec/etc/rules/local_rules.xml`
- Tested rules by simulating attacks from Kali Linux

### Phase 3: Dashboard Configuration
- Built dashboards for: Authentication Events, File Integrity, Network Activity
- Configured real-time email and Slack alerting

### Phase 4: Incident Response Workflow
- Documented response steps for each alert type
- Created runbooks for common scenarios

---

## 📂 Folder Structure

```
03-siem-threat-detection/
├── reports/          # SIEM deployment report & incident reports
├── tools/            # Custom Wazuh rules, config files
├── notes/            # Setup notes, command references
└── screenshots/      # Dashboard screenshots, alert evidence
```

---

## 🔑 Key Learnings

- SIEM architecture: manager, indexer, dashboard, agents
- Wazuh rule syntax and severity levels
- Log normalisation and correlation
- Real-time alerting configuration
- Incident detection and response documentation
