# AWS Cloud Security Audit Report

**Prepared by:** Wamburu Bruce Kinyanjui  
**Date:** [DATE]  
**Target:** AWS Account (Lab / Simulated)  
**Framework:** CIS AWS Foundations Benchmark v1.5  
**Classification:** Confidential — Educational Use Only

---

## Executive Summary

[High-level summary of the audit, number of findings by severity, overall compliance posture, and top priorities.]

---

## Scope

| Item | Detail |
|------|--------|
| AWS Account | [Account ID / Lab Account] |
| Regions Audited | [e.g. us-east-1, eu-west-1] |
| Services Audited | IAM, S3, EC2, CloudTrail, VPC, RDS |
| Tools Used | ScoutSuite, Prowler |
| Audit Period | [START] – [END] |
| CIS Benchmark | AWS Foundations v1.5 |

---

## Findings Summary

| # | Service | Finding | Severity | CIS Control |
|---|---------|---------|----------|-------------|
| 1 | S3 | Public bucket with sensitive data | Critical | 2.1.5 |
| 2 | IAM | Root account has active access keys | Critical | 1.4 |
| 3 | IAM | MFA not enabled for all users | High | 1.10 |
| 4 | CloudTrail | Logging not enabled in all regions | High | 3.1 |
| 5 | EC2 | Security group allows 0.0.0.0/0 on port 22 | High | 5.2 |
| 6 | IAM | Password policy does not meet requirements | Medium | 1.8 |

---

## Detailed Findings

### Finding 1: Public S3 Bucket Exposing Sensitive Data

**Service:** S3  
**Severity:** Critical  
**CIS Control:** 2.1.5 — Ensure S3 bucket access control is restricted

**Description:**  
[Bucket name] is publicly accessible and contains [type of data]. Any unauthenticated internet user can read the contents.

**Evidence:**  
[Screenshot of ScoutSuite / Prowler output or AWS console]

**Impact:**  
Data breach, regulatory non-compliance (GDPR, etc.), reputational damage.

**Remediation:**  
1. Enable "Block All Public Access" on the bucket
2. Review and restrict bucket policy and ACLs
3. Enable S3 server-side encryption (SSE-S3 or SSE-KMS)
4. Enable access logging

---

### Finding 2: Root Account Active Access Keys

**Service:** IAM  
**Severity:** Critical  
**CIS Control:** 1.4 — Ensure no root account access key exists

**Remediation:**  
1. Delete root account access keys immediately
2. Use IAM users or roles for programmatic access
3. Enable MFA on root account

---

## CIS Benchmark Compliance Summary

| Section | Controls Passed | Controls Failed | Compliance % |
|---------|----------------|-----------------|--------------|
| 1 — IAM | X | X | XX% |
| 2 — Storage | X | X | XX% |
| 3 — Logging | X | X | XX% |
| 4 — Monitoring | X | X | XX% |
| 5 — Networking | X | X | XX% |
| **Total** | **X** | **X** | **XX%** |

---

## Remediation Priorities

| Priority | Finding | Effort | Impact |
|----------|---------|--------|--------|
| 1 | Remove root access keys | Low | Critical |
| 2 | Enable MFA for all users | Low | High |
| 3 | Restrict public S3 buckets | Low | Critical |
| 4 | Enable CloudTrail all regions | Low | High |
| 5 | Restrict SSH security groups | Medium | High |

---

## Conclusion

[Summary of overall security posture, key risks, and recommended next steps for improving AWS security hygiene.]

---

*This report was produced in a controlled lab environment for educational purposes only.*
