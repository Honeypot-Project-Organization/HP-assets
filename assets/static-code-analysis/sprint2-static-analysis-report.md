# Static Analysis Report

**Sprint:** 2  
**Date:** 2026-10-3  

---

## 1. Tools Used

### Programming Language(s)

- `Python`

### SonarQube

- **Version:** Community Build v26.9.0.129388

### Trivy

- **Scan Type:** Dependencies
- **Trivy Version:** Version: 0.75.0

### Scan 

- **Environment:** Local
- **Scan Date:** 2026-10-3

---

## 2. Required Metrics

### SonarQube

| Metric | Count |
|---|---:|
| Bugs | [0] |
| Vulnerabilities | [0] |
| Code Smells | [12] |
| Security Hotspots | [0] |
| Quality Gate | [PASS] |

### Trivy

| Severity | Count |
|---|---:|
| CRITICAL | [0] |
| HIGH | [0] |
| MEDIUM | [0] |
| LOW | [0] |

---

## 3. Scope

### Scanned

The application source code and project dependencies were scanned using SonarQube and Trivy. The scan covered all application source files and dependency configuration files included in the repository.

### Excluded

Excluded test files for the cowrie honeypot that contained fake credentials because they were false positives.

---

## 4. Trend

### Sprint Comparison

 **Baseline sprint — no prior comparison.**

---

## 5. Reflection

The most problematic area identified during this sprint was cowrie-vps/shipper/cowrie\_log\_shipper.py, which contained the highest number of code smells (2 issues, including a cognitive complexity of 41). Next sprint, the team will focus on extracting high-complexity functions into smaller, single-responsibility helpers and address the highest-severity findings first to reduce the overall issue count.

---

## Required Statement

**“This static analysis was generated using automated tools during this sprint.”**
