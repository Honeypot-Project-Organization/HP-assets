# Sprint 5 GitHub Report – Azarel Evangelista

**Sprint:** 5 (Nov 10, 2026 – Nov 24, 2026)
**GitHub username:** Oz-ee

## Repositories

- https://github.com/Honeypot-Project-Organization/HP-frontend
- https://github.com/Honeypot-Project-Organization/HP-backend
- https://github.com/Honeypot-Project-Organization/HP-contracts
- https://github.com/Honeypot-Project-Organization/HP-assets

## Pull Requests Reviewed During Sprint 5

| Repo / # | PR Title | PR Link | Author | Reviewer | Merged By | Merge Date |
|---|---|---|---|---|---|---|
| HP-backend #14 | Updated documentation, and added MITRE mappings | https://github.com/Honeypot-Project-Organization/HP-backend/pull/14 | Andrew (CyberWzzard) | Azarel (Oz-ee) (approved) | Azarel (Oz-ee) | 2026-11-13 |
| HP-frontend #3 | Added documentation and MITRE mapping to frontend | https://github.com/Honeypot-Project-Organization/HP-frontend/pull/3 | Andrew (CyberWzzard) | Azarel (Oz-ee) (approved) | Azarel (Oz-ee) | 2026-11-13 |
| HP-assets #11 | Fixed error in sprint 5 jira report | https://github.com/Honeypot-Project-Organization/HP-assets/pull/11 | Andrew (CyberWzzard) | Azarel (Oz-ee) (approved) | Azarel (Oz-ee) | 2026-11-24 |

**Total PRs reviewed:** 3, all merged

Review notes:

- **HP-backend #14 (HONEYPOT-222):** Reviewed the MITRE ATT&CK mappings and the updated documentation. Ran the backend test suite: one test failed because a Nov 6 commit brought back the old expected value for the date-filter test (the 10.0.0.11 boundary case fixed in HP-backend #13 during Sprint 4), not because of an API bug. Pushed the one-line fix to the `backend` branch (`ac18456`) so it became part of the PR; all 53 tests pass. Approved and merged; FastAPI Cloud redeployed the backend automatically.
- **HP-frontend #3 (HONEYPOT-222, HONEYPOT-216):** Tested locally (selftest passes, production build succeeds), approved and merged. Built the frontend against the live backend and deployed it to Firebase Hosting, then checked the live site: the "authorized users only" login notice, dashboard, sessions, map and MITRE technique pages all load.
- **HP-assets #11:** Opened by Andrew on Nov 19 after #10 was merged, with a fix to his Sprint 5 Jira report. It then picked up the Sprint 5 videos on the `assets` branch: Andrew's (`assets/videos/S5-Video-Recording-Honeypot-Andrew.mkv`, added Nov 22) and mine (`assets/videos/S5 Video Recording Honeypot - Azarel.mp4`), plus this report update. Approved and merged after adding my video.

## Pull Requests Opened During Sprint 5

| Repo / # | PR Title | PR Link | Status |
|---|---|---|---|
| HP-backend #15 | Security and database docs (HONEYPOT-224) | https://github.com/Honeypot-Project-Organization/HP-backend/pull/15 | Merged by Andrew (CyberWzzard) on 2026-11-18. Docs only (`23e33e1`): new `docs/database-security.md`, updates to `SECURITY.md`, `cowrie_vps_setup_guide.md` and `docs/data-retention.md`. No code changed. |
| HP-contracts #1 | Contracts: schemas, fixtures and docs | https://github.com/Honeypot-Project-Organization/HP-contracts/pull/1 | Merged by Andrew (CyberWzzard) on 2026-11-19. Brings the contracts work onto `main`: Andrew's schemas, fixtures and docs, plus my two database doc fixes (`4c05c9e`, `8295910`). |
| HP-assets #10 | Sprint 5 assets: reports and static code analysis | https://github.com/Honeypot-Project-Organization/HP-assets/pull/10 | Merged by Andrew (CyberWzzard) on 2026-11-19. Sprint 5 deliverables on the `assets` branch: Andrew's GitHub and Jira reports, the static code analysis (SonarQube, Trivy and summary report), these reports and my Sprint 4 GitHub report fix. |

## Commit Activity

| Date | Repo | Commit | Message |
|---|---|---|---|
| 2026-11-24 | HP-assets | a0b4d2a | Merge pull request #11 from Honeypot-Project-Organization/assets |
| 2026-11-24 | HP-assets | fb26931 | Add files via upload (second upload of the same reports; no file changes) |
| 2026-11-24 | HP-assets | 850dcc6 | Add files via upload (updated Sprint 5 GitHub and Jira reports) |
| 2026-11-24 | HP-assets | 76b5e48 | Add files via upload (Sprint 5 video) |
| 2026-11-19 | HP-assets | 63b8a14 | Fix Sprint 4 GitHub report: PR #9 merged |
| 2026-11-19 | HP-assets | adaa87f | Add Azarel's Sprint 5 GitHub and Jira reports |
| 2026-11-18 | HP-contracts | 8295910 | Revise MongoDB contract for production database |
| 2026-11-18 | HP-contracts | 4c05c9e | database role and name match Atlas setup (HONEYPOT-224) |
| 2026-11-13 | HP-frontend | bc298f7 | Merge pull request #3 from Honeypot-Project-Organization/frontend |
| 2026-11-13 | HP-backend | df34404 | Merge pull request #14 from Honeypot-Project-Organization/backend |
| 2026-11-13 | HP-backend | 23e33e1 | Security and database docs: custom role, temporary admin user, DB name fix |
| 2026-11-13 | HP-backend | ac18456 | Restore date-filter test expectation (10.0.0.11 boundary) |

- **Total number of commits:** 12
- **Date range:** 2026-11-13 – 2026-11-24

> Update (Nov 24): this report was first written on Nov 19, before HP-assets #10 was merged. HP-assets #10 is now marked merged, the two Nov 19 HP-assets commits were added, and the Sprint 5 video and HP-assets #11 were added, the same way the Sprint 4 report was corrected. The Nov 24 commit hashes were filled in after HP-assets #11 was merged; that last correction commit is not counted above.

> Note: the two HP-contracts commits fix `docs/environment.md` and `docs/database.md` so they match the live Atlas setup: the backend's database user has a custom role (not `readWrite`), the production database is `honeypot-project`, and the `app_meta` collection is listed.

## Related Work This Sprint (outside GitHub)

- **Least-privilege database access (HONEYPOT-223):** Created the custom role `backend-app` in MongoDB Atlas, switched the backend's database user from `readWriteAnyDatabase` to it (password and `MONGO_URI` unchanged), and deleted the permanent `atlasAdmin` database user. On Nov 18 tightened the role to match `docs/database-security.md` exactly (no deletes, location data read-only, `createCollection` added). Checked after each change that new events kept arriving and the live dashboard worked; before/after screenshots are on the Jira ticket.
- **Atlas storage (HONEYPOT-225):** On Nov 13 the database reached the free tier's 512 MB limit and new events stopped being saved. With Andrew's OK, dropped the `raw_events` collection (raw copies that expire after 7 days anyway); the backend recreated it and ingestion resumed.
- **Security and database documentation (HONEYPOT-224):** My half of the documentation split agreed with Andrew on Nov 1 (he wrote the READMEs and API/contracts docs); delivered in HP-backend #15 and the HP-contracts fixes above.
- **Jira housekeeping:** Moved HONEYPOT-212 (threat-intel endpoints) to the backlog for a possible next semester (agreed with Andrew) and set all 9 epics to Done once their work was finished.
