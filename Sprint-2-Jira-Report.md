# Sprint 2 – Jira Report

**Jira project:** Honeypot-project (key `HONEYPOT`) – <https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1>
**Sprint:** Sprint 2 (Sprint ID 1)
**Sprint Dates:** Sep 23, 2026 - Oct 6, 2026
**Sprint goal:** Honeypot live on the VPS, data layer on Atlas, and hosting ready for the backend and dashboard.
**Data pulled from Jira:** Oct 5, 2026

---

## Sprint Commitment vs Delivery

| Metric | Count |
|---|---|
| Issues committed at sprint start | 7 |
| Issues completed | 12 |
| Issues not completed | 0 |
| Issues added mid-sprint | 5 |

- **Committed at start (added during sprint planning on Sep 23):** HONEYPOT-128, 129, 132, 134, 146, 147, 148
- **Added mid-sprint:** HONEYPOT-143 (Sep 26), HONEYPOT-198 (Sep 26), HONEYPOT-199 (Oct 2), HONEYPOT-200 (Oct 2), HONEYPOT-142 (Oct 3)

## Issue Breakdown by Type

| Type | To Do | In Progress | Done |
|---|---|---|---|
| Story | 0 | 0 | 10 |
| Task | 0 | 0 | 0 |
| Bug | 0 | 0 | 2 |

## Per-Student Work Allocation

| Student | Issues Assigned | Issues Completed | Story Points Completed |
|---|---|---|---|
| Andrew Jakes | 7 (128, 134, 142, 146, 148, 198, 200) | 7 | 18 |
| Azarel | 5 (129, 132, 143, 147, 199) | 5 | 11 |
| **Total** | **12** | **12** | **29** |

> Note: HONEYPOT-148 was assigned to Azarel during the sprint and reassigned to Andrew Jakes on Oct 3 when it was closed.

## Estimation & Accuracy

| Metric | Value |
|---|---|
| Total story points committed (at sprint start) | 30 |
| Total story points in sprint (final scope, current estimates) | 29 |
| Total story points completed | 29 |
| Completion % | 100% |

**Estimation notes:**
- Four stories were re-estimated downward after they were finished: HONEYPOT-128 (8 → 4), HONEYPOT-134 (8 → 4), HONEYPOT-146 (5 → 3), HONEYPOT-142 (5 → 3, before being added to the sprint). The 7 originally committed stories are now worth 20 points instead of the 30 committed, meaning the team overestimated the large infrastructure/ingestion stories by about a third.
- 9 points of scope were added mid-sprint (143: 3, 142: 3, 198/199/200: 1 each).
- Lesson for next sprint: break 8-point stories down before committing, and keep the original estimate on record instead of editing it after completion.

## Workflow Discipline

- [ ] Issues moved through workflow states (To Do → In Progress → Done) — *partially: 10 of 12 issues went through In Progress; HONEYPOT-129 and HONEYPOT-142 went straight from To Do to Done.*
- [ ] Issues closed only after acceptance criteria met — *partially: acceptance criteria were narrowed on several stories shortly before closing (e.g. 129, 132, 143, 147, 148), and the two bugs (199, 200) have no acceptance criteria field.*
- [ ] Sprint completed/closed in Jira — *not yet: all 12 issues are Done, but Sprint 2 is still active in Jira and needs to be completed at the end of the sprint on Oct 6.*

## Blockers & Scope Changes

- **Major blockers:**
  - FastAPI Cloud deployment build failure — missing `pyproject.toml` in `fastapi-backend/` (Bug HONEYPOT-199).
  - Runtime error after deploy — `JWT_SECRET_KEY` missing from FastAPI Cloud environment variables (Bug HONEYPOT-200).
  - Dependency chain: Atlas setup (147) blocked connecting the schema (132), which blocked the ingestion script (134); the VPS lockdown (146) also blocked 134; FastAPI Cloud hosting (148) blocked the deploy story (143).
- **Scope changes:**
  - 5 issues / 9 points added mid-sprint: deploy-and-connect story (143), admin-user story (198, split out of 132's original criteria), local Docker test story (142), and the two deployment bugs (199, 200).
  - Acceptance criteria were trimmed on 129 (dropped sample-document validation) and 132 (admin creation/login moved to 198).
- **Why work spilled over:** No spillover — all committed and added issues were completed. Most issues were closed in a batch on Oct 3.

## Jira Evidence Links

- **Sprint report:** <https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1/reports>
- **Backlog link:** <https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1/backlog>
- **Board link (filtered to sprint):** <https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1>
- **Sprint 2 issue list (JQL `sprint = 1`):** <https://honeypot-project.atlassian.net/issues/?jql=sprint%20%3D%201>
