# Sprint 3 – Jira Report (Azarel Evangelista)

- **Jira project:** Honeypot-project (key `HONEYPOT`) – <https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1>
- **Sprint:** Sprint 3 (Sprint ID 4)
- **Sprint Dates:** Oct 9, 2026 – Oct 20, 2026
- **Sprint goal:** Frontend dashboard built and deployed, backend dashboard APIs complete, and raw-log retention in place (no goal text was entered in Jira).
- **Data pulled from Jira:** Oct 17, 2026

---

## Sprint Commitment vs Delivery

| Metric | Count |
|---|---|
| Issues committed at sprint start | 12 |
| Issues completed | 14 |
| Issues not completed | 0 |
| Issues added mid-sprint | 2 |

- **Committed at start (added during sprint planning, Oct 6–8):** HONEYPOT-133, 135, 136, 137, 139, 140, 141, 144, 149, 202, 206, 209
- **Added mid-sprint:** HONEYPOT-208 (Oct 16), HONEYPOT-213 (Oct 16)

## Issue Breakdown by Type

| Type | To Do | In Progress | Done |
|---|---|---|---|
| Story | 0 | 0 | 14 |
| Task | 0 | 0 | 0 |
| Bug | 0 | 0 | 0 |

Subtasks completed under my stories: HONEYPOT-174 (Build and deploy frontend to Firebase, under 144) and HONEYPOT-181 (Set up Firebase Hosting and establish the deploy process, under 149).

## Per-Student Work Allocation

| Student | Issues Assigned | Issues Completed | Story Points Completed |
|---|---|---|---|
| Andrew Jakes | 11 (133, 135, 136, 137, 139, 140, 141, 202, 208, 209, 213) | 11 | 28 |
| Azarel | 3 (144, 149, 206) | 3 | 6 |
| **Total** | **14** | **14** | **34** |

> Note: HONEYPOT-144 and 149 were assigned to Andrew Jakes at sprint planning, unassigned on Oct 9, and reassigned to Azarel (149 on Oct 13, 144 on Oct 17). HONEYPOT-206 was assigned to Azarel on Oct 13.

### My Issues

| Issue | Summary | Points | Outcome |
|---|---|---|---|
| HONEYPOT-149 | Set up Firebase Hosting for the dashboard | 2 | Firebase project `honeypot-dashboardpro` created, hosting configured for React/Vite, teammate added as Editor; config merged into HP-frontend. |
| HONEYPOT-206 | Auto-purge raw_events older than 7 days using a MongoDB TTL index | 2 | 7-day TTL index (`expireAfterSeconds: 604800`) on `raw_events` verified in Atlas; before/after screenshots attached. |
| HONEYPOT-144 | Deploy frontend to Firebase | 2 | Reviewed and merged HP-frontend PR #1, built and deployed; dashboard live at <https://honeypot-dashboardpro.web.app> with live backend data. |

## Estimation & Accuracy

| Metric | Value |
|---|---|
| Total story points committed (at sprint start) | 29 |
| Total story points in sprint (final scope) | 34 |
| Total story points completed | 34 |
| Completion % | 100% |

**Estimation notes:**
- Estimates were set during planning on Oct 6, before the sprint started (for example HONEYPOT-133 went 5 → 3, 139 went 3 → 2, 149 went 1 → 2), and were not changed after work began.
- 5 points of scope were added mid-sprint (208: 3, 213: 2).
- HONEYPOT-206 took more effort than its 2 points: the approach changed from an API feature to a MongoDB TTL index, and the index had to be fixed a second time after a backend restart reset it to 30 days.

## Workflow Discipline

- [ ] Issues moved through workflow states (To Do → In Progress → Done) — *partially: 12 of 14 issues went through In Progress. HONEYPOT-144 went straight from To Do to Done, and HONEYPOT-206 went To Do → Done, was reopened to In Progress on Oct 17, then closed again.*
- [x] Issues closed only after acceptance criteria met — *HONEYPOT-206 was reopened when the live index no longer matched its acceptance criteria and closed again only after 604800 s was verified in Atlas.*
- [ ] Sprint completed/closed in Jira — *not yet: all 14 issues are Done, but Sprint 3 is still active and closes on Oct 20.*

## Blockers & Scope Changes

- **HONEYPOT-206 changed approach:** originally "add a feature to the API" to delete old raw logs; after team discussion it became a MongoDB TTL index, and the story, acceptance criteria and title were rewritten on Oct 13.
- **Retention reset:** an Oct 16 backend restart recreated the TTL index with the old 30-day default. Fixed by changing the code default to 7 days (HP-backend PR #10) and setting `RAW_EVENT_RETENTION_DAYS=7` in FastAPI Cloud.
- **Frontend rebuild:** the frontend was restarted from scratch mid-sprint, so the deploy (HONEYPOT-144) waited until HP-frontend PR #1 was merged on Oct 17.
- **Firebase config location:** the config was first submitted to HP-assets (PR #6) and moved to HP-frontend after team discussion.
- **Why work spilled over:** none; all issues were completed.

## Jira Evidence Links

- **Sprint report:** <https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1/reports/sprint-retrospective?sprint=4>
- **Backlog:** <https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1/backlog>
- **Board:** <https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1>
- **My issues:** <https://honeypot-project.atlassian.net/browse/HONEYPOT-144>, <https://honeypot-project.atlassian.net/browse/HONEYPOT-149>, <https://honeypot-project.atlassian.net/browse/HONEYPOT-206>
