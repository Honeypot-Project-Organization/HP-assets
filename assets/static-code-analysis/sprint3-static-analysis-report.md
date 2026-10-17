# Static Analysis Report

**Sprint:** 3  
**Date:** 2026-10-17  

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
- **Scan Date:** 2026-10-17

---

## 2. Required Metrics

### SonarQube

| Metric | Count |
|---|---:|
| Bugs | [0] |
| Vulnerabilities | [0] |
| Code Smells | [13] |
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

Previous sprint issue count: 12
Current sprint issue count: 13

---

## 5. Reflection

The most problematic area was maintainability in the fastapi-backend/ directory. The maintainability issues will be addressed next sprint by starting with the fastapi-backend/ directory.

---

## Required Statement

**“This static analysis was generated using automated tools during this sprint.”**
