# Sprint 5 – Jira Report (Azarel Evangelista)

- **Jira project:** Honeypot-project (key `HONEYPOT`) – <https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1>
- **Sprint:** Sprint 5 (Sprint ID 6)
- **Sprint Dates:** Nov 10, 2026 – Nov 24, 2026 (started in Jira Nov 10 at 8:26 AM; ends Nov 24 at 11:00 PM)
- **Sprint goal:** Finish and harden the project for the final presentation: MITRE ATT&CK mapping, least-privilege database access, the login-page notice, and documentation (READMEs, security and database docs, contracts) (no goal text was entered in Jira).
- **Data pulled from Jira:** Nov 19, 2026; rechecked Nov 24 (no changes to Sprint 5 issues since Nov 19)

---

## Sprint Commitment vs Delivery

| Metric | Count |
|---|---|
| Issues committed at sprint start | 4 |
| Issues completed | 6 |
| Issues not completed | 0 |
| Issues added mid-sprint | 2 |

- **Committed at start (added Oct 31 – Nov 3, before the sprint started):** HONEYPOT-211, 216, 222, 223
- **Added mid-sprint:** HONEYPOT-224 (Nov 13), HONEYPOT-225 (Nov 18)
- **Removed before the sprint started:** HONEYPOT-212 (threat-intel endpoints), taken out of Sprint 5 by Andrew on Nov 6

## Issue Breakdown by Type

Issues in Sprint 5 at the time of this report:

| Type | To Do | In Progress | Done |
|---|---|---|---|
| Story | 0 | 0 | 3 |
| Task | 0 | 0 | 3 |
| Bug | 0 | 0 | 0 |

## Per-Student Work Allocation

| Student | Issues Assigned | Issues Completed | Story Points Completed |
|---|---|---|---|
| Andrew Jakes | 3 (211, 216, 222) | 3 | 8 |
| Azarel | 3 (223, 224, 225) | 3 | 7 |
| **Total** | **6** | **6** | **15** |

> Note: HONEYPOT-212 was mine until Nov 18. Andrew removed it from Sprint 5 on Nov 6, before the sprint started; on Nov 18 we agreed to keep it for a possible next semester, so I unassigned it, labeled it `next-semester` and left it in the backlog with a comment.

### My Issues

| Issue | Summary | Points | Outcome |
|---|---|---|---|
| HONEYPOT-223 | Apply least-privilege database access in Atlas (custom role for the backend user, remove atlasAdmin) | 2 | Created the custom role `backend-app`, switched the backend's database user to it (password and `MONGO_URI` unchanged) and deleted the permanent `atlasAdmin` user. Tested live: new events kept arriving (75,731 → 75,826), login, dashboard and MITRE pages worked. Six screenshots attached (usernames blanked). Role tightened on Nov 18 to match the security docs. |
| HONEYPOT-224 | Update security and database docs (SECURITY.md, setup guide, database-security.md) | 2 | New `docs/database-security.md` plus fixes to `SECURITY.md`, the setup guide and `docs/data-retention.md`, merged in HP-backend #15 (Nov 18). Matching database notes fixed in HP-contracts and merged in HP-contracts #1 (Nov 19). |
| HONEYPOT-225 | Review, test and deploy the MITRE update (backend #14, frontend #3) and free Atlas storage | 3 | Freed Atlas storage after it hit the 512 MB limit (dropped `raw_events` with Andrew's OK). Fixed a failing test in HP-backend #14 (53/53 passing), approved and merged #14 and HP-frontend #3, deployed the frontend to Firebase and verified the live site. |

## Estimation & Accuracy

| Metric | Value |
|---|---|
| Total story points committed (at sprint start) | 10 |
| Story points added mid-sprint | 5 |
| Total story points in sprint (final scope) | 15 |
| Total story points completed | 15 |
| Completion % (final scope) | 100% |

**Estimation notes:**
- HONEYPOT-222 was re-estimated from 5 to 4 points on Nov 6, before the sprint started.
- HONEYPOT-225 was logged on Nov 18 for work done on Nov 13, so its 3 points are not an up-front estimate (same approach as HONEYPOT-218 in Sprint 4).
- No story points carried over to a later sprint.

## Workflow Discipline

- [ ] Issues moved through workflow states (To Do → In Progress → Done) — *partially: 4 of 6 issues went through In Progress (211, 216, 222, 224). HONEYPOT-223 went straight from To Do to Done on Nov 17 when the change was finished and tested in one session; HONEYPOT-225 was logged after the work was done.*
- [x] Issues closed only after acceptance criteria met — *each of my issues was closed with evidence: screenshots and live checks (223), merged PRs #15 and contracts #1 (224), and passing tests, merged PRs and a live-site check (225).*
- [ ] Sprint completed/closed in Jira — *not yet: all 6 issues are Done, but Sprint 5 is still active and ends Nov 24 at 11:00 PM.*

## Blockers & Scope Changes

- **Database storage limit (Nov 13):** the free Atlas tier hit its 512 MB limit and new events stopped being saved. Fixed the same day by dropping `raw_events` with Andrew's OK; tracked as HONEYPOT-225.
- **Database storage limit again (late in the sprint):** Andrew found the dashboard login timing out because the database was at 516 of 512 MB. He dropped `raw_events` again and the dashboard worked afterward. He also saw a large spike in connection count on Nov 19 when he checked the dashboard. This is the second time this sprint; checking storage before the Dec 1 presentation is on our list.
- **Failing test in the MITRE update:** HP-backend #14 brought back an old expected value in the date-filter test. Fixed on the PR's branch (`ac18456`) before merging.
- **Role adjusted after a docs check (Nov 18):** comparing the live role with `docs/database-security.md` and the backend code showed the role allowed deletes and writes to the location data the API only reads, and lacked `createCollection`. Updated the role to match the docs; events kept arriving.
- **Threat-intel endpoints (HONEYPOT-212):** removed from Sprint 5 by Andrew on Nov 6; on Nov 18 we agreed to keep it in the backlog for a possible next semester.
- **Epics:** all 9 epics set to Done on Nov 19 once their work was finished; HONEYPOT-212 remains in the backlog under Backend Dashboard Query API.

## Jira Evidence Links

- **Sprint report:** <https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1/reports/sprint-retrospective?sprint=6>
- **Backlog:** <https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1/backlog>
- **Board:** <https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1>
- **My issues:** <https://honeypot-project.atlassian.net/browse/HONEYPOT-223>, <https://honeypot-project.atlassian.net/browse/HONEYPOT-224>, <https://honeypot-project.atlassian.net/browse/HONEYPOT-225>
