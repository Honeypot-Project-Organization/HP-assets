# Sprint 4 – Jira Report (Azarel Evangelista)

- **Jira project:** Honeypot-project (key `HONEYPOT`) – <https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1>
- **Sprint:** Sprint 4 (Sprint ID 5)
- **Sprint Dates:** Oct 22, 2026 – Nov 3, 2026 (started in Jira Oct 22 at 5:49 PM; ends Nov 3 at 11:00 PM)
- **Sprint goal:** Testing and hardening: fix dashboard filtering and searching across the whole database, validate pipeline security and test coverage, and answer the instructor's MongoDB security question (no goal text was entered in Jira).
- **Data pulled from Jira:** Nov 3, 2026

---

## Sprint Commitment vs Delivery

| Metric | Count |
|---|---|
| Issues committed at sprint start | 4 |
| Issues completed | 6 |
| Issues not completed (moved to Sprint 5) | 2 |
| Issues added mid-sprint | 4 |

- **Committed at start (added Oct 18–22, before the sprint started):** HONEYPOT-145, 211, 216, 217
- **Added mid-sprint:** HONEYPOT-218 (Oct 30), HONEYPOT-219, 220, 221 (Oct 31)
- **Moved to Sprint 5 on Oct 30:** HONEYPOT-211 (documentation) and HONEYPOT-216 (login-page notice)

## Issue Breakdown by Type

Issues in Sprint 4 at the time of this report:

| Type | To Do | In Progress | Done |
|---|---|---|---|
| Story | 0 | 0 | 1 |
| Task | 0 | 0 | 4 |
| Bug | 0 | 0 | 1 |

Subtasks completed under HONEYPOT-145: HONEYPOT-175 (Write integration tests for the ingestion endpoint) and HONEYPOT-176 (Perform security review: rate limiting, egress verification).

## Per-Student Work Allocation

| Student | Issues Assigned | Issues Completed | Story Points Completed |
|---|---|---|---|
| Andrew Jakes | 2 (145, 217) | 2 | 6 |
| Azarel | 4 (218, 219, 220, 221) | 4 | 10 |
| **Total** | **6** | **6** | **16** |

> Note: HONEYPOT-212 (threat-intel endpoints, mine) was taken out of Sprint 4 on Oct 22 just before the sprint started and moved to Sprint 5 on Oct 30 at my request. HONEYPOT-216 was assigned to me on Oct 31 after it moved to Sprint 5, and reassigned to Andrew on Nov 3 at his request.

### My Issues

| Issue | Summary | Points | Outcome |
|---|---|---|---|
| HONEYPOT-218 | Review, test and deploy the server-side filtering fix (backend #12, frontend #2) | 3 | Reviewed and approved HP-backend #12; found a wrong test expectation (42/43 passing) and fixed it in HP-backend #13 (43/43 passing); tested, approved and merged HP-frontend #2; deployed to Firebase Hosting and verified the live site. |
| HONEYPOT-219 | Audit MongoDB Atlas access settings (Network Access, database users, project access) | 2 | Audited the live Atlas project; screenshots attached. Found `0.0.0.0/0` on the IP access list, a backend user with `readWriteAnyDatabase` instead of read/write on one database, and a permanent `atlasAdmin` user. Fixes planned for Sprint 5. |
| HONEYPOT-220 | Document the MongoDB data schema with data sensitivity and retention | 2 | Schema table for all 9 collections (size, sensitivity, retention) confirmed against the live database and added to the security write-up. |
| HONEYPOT-221 | Write up MongoDB security vs Firestore Security Rules and prepare Sprint 4 demo | 3 | Security write-up attached as a PDF (data-flow diagram, what Atlas does for us, who can access what, schema, audit findings, recommendations); presented in the Sprint 4 demo. |

## Estimation & Accuracy

| Metric | Value |
|---|---|
| Total story points committed (at sprint start) | 10 |
| Story points added mid-sprint | 10 |
| Total story points in sprint (final scope) | 16 |
| Total story points completed | 16 |
| Completion % (final scope) | 100% |
| Completion % (committed + added, 20 points) | 80% |

**Estimation notes:**
- HONEYPOT-145 was re-estimated from 5 to 3 points on Oct 22 at sprint start.
- My four tasks were created to track the instructor's mid-sprint request and the filtering-fix review; their points were entered on Oct 31, after the work was done, so they are not true up-front estimates.
- 4 points did not get done in Sprint 4 (HONEYPOT-211: 3, HONEYPOT-216: 1); both were moved to Sprint 5.

## Workflow Discipline

- [ ] Issues moved through workflow states (To Do → In Progress → Done) — *partially: 3 of 6 issues went through In Progress (145, 217, 221). HONEYPOT-218, 219 and 220 went straight from To Do to Done because they were logged the same day the work was done.*
- [x] Issues closed only after acceptance criteria met — *each of my tasks was closed with evidence attached: test results and live-site check (218), Atlas screenshots (219), the schema table (220) and the security write-up PDF (221). The write-up was corrected on Nov 3 after re-checking the database users' roles.*
- [ ] Sprint completed/closed in Jira — *not yet: all 6 issues in the sprint are Done, but Sprint 4 is still active and ends Nov 3 at 11:00 PM.*

## Blockers & Scope Changes

- **Instructor request (mid-sprint):** after the Sprint 3 demo, the instructor asked us to explain MongoDB's equivalent of Firestore Security Rules for our project. This added HONEYPOT-219, 220 and 221 (7 points) on Oct 31.
- **Failing test in the filtering fix:** HP-backend #12 had one failing test caused by a wrong expected value, not the API. Fixed in HP-backend #13 before the deploy.
- **Documentation moved to Sprint 5:** HONEYPOT-211 moved to Sprint 5 on Oct 30. On Nov 1 the team agreed to split it: I write the security and database docs, Andrew writes the API/contracts docs.
- **Threat-intel endpoints (HONEYPOT-212):** Andrew asked to hold it so Sprint 4 could focus on testing, so I moved it to Sprint 5 on Oct 30.
- **Security gaps found:** the Atlas audit found broader database access than SECURITY.md describes. The least-privilege user and the removal of the permanent admin user are planned with Andrew in Sprint 5.
- **Why work spilled over:** HONEYPOT-211 and 216 were deprioritized in favor of the filtering fix and the instructor's security request.

## Jira Evidence Links

- **Sprint report:** <https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1/reports/sprint-retrospective?sprint=5>
- **Backlog:** <https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1/backlog>
- **Board:** <https://honeypot-project.atlassian.net/jira/software/projects/HONEYPOT/boards/1>
- **My issues:** <https://honeypot-project.atlassian.net/browse/HONEYPOT-218>, <https://honeypot-project.atlassian.net/browse/HONEYPOT-219>, <https://honeypot-project.atlassian.net/browse/HONEYPOT-220>, <https://honeypot-project.atlassian.net/browse/HONEYPOT-221>
