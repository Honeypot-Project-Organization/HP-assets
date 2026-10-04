# Sprint 2 Jira Report

**Jira Project Name:** Honeypot-project (key: `HONEYPOT`)
**Project Link:** https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1
**Sprint Name/Number:** Sprint 2 
**Sprint Dates:** Sep 23, 2026 - Oct 6, 2026

---

## Sprint Commitment vs Delivery

| Metric | Count |
| :--- | :--- |
| Issues committed at sprint start | 9 |
| Issues completed | 12 |
| Issues not completed | 0 |
| Issues added mid-sprint | 3 |

---

## Issue Breakdown by Type

| Type | To Do | In Progress | Done |
| :--- | :--- | :--- | :--- |
| Story | 0 | 0 | 10 |
| Task | 0 | 0 | 0 |
| Bug | 0 | 0 | 2 |

---

## Per-Student Work Allocation

| Student | Issues Assigned | Issues Completed |
| :--- | :--- | :--- |
| Andrew Jakes | 7 | 7 |
| Azarel | 5 | 5 |

---

## Estimation & Accuracy

| Metric | Value |
| :--- | :--- |
| Total story points committed | 26 |
| Total story points completed | 29 |
| Completion % | 100% |

---

## Workflow Discipline

Short checklist: Check only the steps followed during the sprint.
- [x] Issues moved through workflow states (To Do → In Progress → Done)
- [x] Issues closed only after acceptance criteria met
- [x] Sprint completed/closed in Jira

---

## Blockers & Scope Changes

### Major Blockers
* **FastAPI Cloud Deployment Failure:** The backend deployment failed during cloud build due to missing project configuration files. Resolved by adding `pyproject.toml` to `fastapi-backend/` in the repository.
* **FastAPI Cloud Runtime Authentication Error:** Runtime exceptions occurred on the deployed FastAPI Cloud service due to missing environment secrets (`JWT_SECRET_KEY`). Resolved by configuring the environment variables on the hosting platform and redeploying.

### Scope Changes
* **3 issues added mid-sprint (+3 story points):**
  - **User Story, 1 pt:** Created MongoDB admin user to enable dashboard authentication.
  - **Bug, 1 pt:** Fixed FastAPI deployment build failure.
  - **Bug, 1 pt:** Configured API key / secret environment variables on FastAPI Cloud.

### Why Work Spilled Over (if any)
* None. All 9 committed issues and all 3 mid-sprint added issues were successfully completed (100% completion rate with 0 incomplete issues).

---

## Jira Evidence Links

* **Sprint report link:** https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1/reports/sprint-report?sprint=1
* **Backlog link:** https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1/backlog
* **Board link (filtered to sprint):** https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1?filter=&groupBy=none
