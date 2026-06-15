# 07 — AWS Cloud Security Audit (ScoutSuite / Prowler)

## 📌 Project Overview

Performed a security audit of an AWS environment using ScoutSuite and Prowler. Identified critical misconfigurations including open S3 buckets and overly permissive IAM roles. Mapped all findings to CIS AWS Benchmarks and produced a remediation report with prioritised security controls.

---

## 🎯 Objectives

- Configure and run ScoutSuite against an AWS account
- Run Prowler for CIS AWS Benchmark compliance checks
- Identify misconfigurations across key AWS services
- Map findings to CIS AWS Foundations Benchmark
- Produce a remediation report with prioritised controls

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| ScoutSuite | Multi-cloud security auditing |
| Prowler | AWS CIS Benchmark compliance scanner |
| AWS CLI | Account access and enumeration |
| AWS IAM | Identity and access management review |
| Python 3 | Scripting for custom checks |

---

## ☁️ AWS Services Audited

| Service | Key Checks |
|---------|-----------|
| IAM | MFA, password policy, unused keys, over-permissive roles |
| S3 | Public access settings, encryption, versioning, logging |
| EC2 | Security groups, unencrypted volumes, public AMIs |
| CloudTrail | Logging enabled, log validation, multi-region |
| VPC | Security groups, NACLs, flow logs |
| RDS | Encryption, public accessibility, backups |
| Lambda | Permissions, environment variable secrets |

---

## 📋 Methodology

### Phase 1: Setup
- Created a read-only IAM user for auditing
- Configured AWS CLI with audit credentials
- Installed ScoutSuite and Prowler

### Phase 2: Automated Scanning
```bash
# ScoutSuite scan
scout aws --report-dir ./scoutsuite-report

# Prowler CIS scan
prowler aws --compliance cis_aws_foundations_benchmark
```

### Phase 3: Manual Review
- Reviewed ScoutSuite HTML report
- Prioritised findings by severity
- Verified false positives manually

### Phase 4: Reporting
- Mapped findings to CIS AWS Benchmark controls
- Calculated risk scores
- Produced prioritised remediation plan

---

## 📂 Folder Structure

```
07-aws-cloud-security-audit/
├── reports/          # Cloud security audit report
├── tools/            # Custom AWS audit scripts
├── notes/            # CIS benchmark references, setup notes
└── screenshots/      # ScoutSuite/Prowler output screenshots
```

---

## 📄 Report Template

See [`reports/cloud-audit-report-template.md`](./reports/cloud-audit-report-template.md)

---

## 🔑 Key Learnings

- AWS shared responsibility model
- IAM principle of least privilege
- S3 public access and bucket policy risks
- CIS AWS Foundations Benchmark controls
- Cloud security audit methodology
