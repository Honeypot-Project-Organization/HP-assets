# Sprint 4 GitHub Report – Azarel Evangelista

**Sprint:** 4 (Oct 20, 2026 – Nov 3, 2026)
**GitHub username:** Oz-ee

## Repositories

- https://github.com/Honeypot-Project-Organization/HP-frontend
- https://github.com/Honeypot-Project-Organization/HP-backend
- https://github.com/Honeypot-Project-Organization/HP-assets

## Pull Requests Reviewed During Sprint 4

| Repo / # | PR Title | PR Link | Author | Reviewer | Merged By | Merge Date |
|---|---|---|---|---|---|---|
| HP-backend #12 | Added backend stuff for fixing frontend searching and filtering | https://github.com/Honeypot-Project-Organization/HP-backend/pull/12 | Andrew (CyberWzzard) | Azarel (Oz-ee) (approved) | Andrew (CyberWzzard) | 2026-10-30 |
| HP-frontend #2 | Improved frontend filtering, searching, and added filter by date | https://github.com/Honeypot-Project-Organization/HP-frontend/pull/2 | Andrew (CyberWzzard) | Azarel (Oz-ee) (approved) | Azarel (Oz-ee) | 2026-10-30 |
| HP-assets #9 | Added sprint 4 assets | https://github.com/Honeypot-Project-Organization/HP-assets/pull/9 | Andrew (CyberWzzard) | Azarel (Oz-ee) (approval pending) | Open (to be merged with the Sprint 4 video and these reports) | – |

**Total PRs reviewed:** 2 merged, plus HP-assets #9 still open

Review notes:

- **HP-backend #12:** Reviewed the server-side search, filters, date ranges, sorting and paging (HONEYPOT-217). Ran the backend test suite locally: 42 of 43 tests passed. The failing test (`test_attackers_filters_sort_and_total`) had a wrong expected value, not an API bug: `date_from` is inclusive and the seeded IP 10.0.0.11 sits exactly on the boundary. Fixed the test in HP-backend #13.
- **HP-frontend #2:** Tested locally (selftest passes, production build succeeds), approved and merged. After merging, built the frontend against the live backend and deployed it to Firebase Hosting (HONEYPOT-218).
- **HP-assets #9:** Sprint 4 deliverables on the `assets` branch: Andrew's GitHub and Jira reports, the static code analysis reports, the Sprint 4 video (`assets/videos/S4 Video Recording Honeypot.mp4`) and these reports.

## Pull Requests Opened During Sprint 4

| Repo / # | PR Title | PR Link | Status |
|---|---|---|---|
| HP-backend #13 | Fix attackers date-filter test expectation (include boundary IP) | https://github.com/Honeypot-Project-Organization/HP-backend/pull/13 | Merged by Andrew (CyberWzzard) on 2026-10-30. One-line test fix in `fastapi-backend/tests/test_api.py`; no app code changed. All 43 tests pass. |

## Commit Activity

| Date | Repo | Commit | Message |
|---|---|---|---|
| 2026-11-03 | HP-assets | 9f6cf0a | Add files via upload (Sprint 4 video as .mp4) |
| 2026-11-03 | HP-assets | 042770e | Delete assets/videos/S4 Video Recording Honeypot.zip |
| 2026-11-03 | HP-assets | 2a65f27 | Create S4 Video Recording Honeypot.zip |
| 2026-10-30 | HP-frontend | fd79249 | Merge pull request #2 from Honeypot-Project-Organization/frontend |
| 2026-10-30 | HP-backend | 7633354 | Fix attackers date-filter test expectation (include boundary IP) |

- **Total number of commits:** 5 (plus the commit adding these reports)
- **Date range:** 2026-10-30 – 2026-11-03

> Note: the Sprint 4 video was first uploaded as a .zip, then replaced with the .mp4 so it can be opened directly from GitHub.

## Related Work This Sprint (outside GitHub)

- **Filtering fix deployment (HONEYPOT-218):** Built the merged frontend and deployed it to Firebase Hosting (https://honeypot-dashboardpro.web.app). Verified live: Sessions shows server-side totals ("5,032 matching sessions"), and date-range filtering and paging work.
- **MongoDB Atlas audit (HONEYPOT-219):** Checked Network Access, database users, the database and collections, and project access in the live Atlas project. Screenshots and findings are on the Jira ticket.
- **Data schema (HONEYPOT-220):** Documented all 9 collections with size, sensitivity and retention, confirmed against the live database.
- **Security write-up and demo (HONEYPOT-221):** Wrote "MongoDB Atlas Security – Honeypot Project" (attached in Jira as a PDF) answering the instructor's question about MongoDB's equivalent of Firestore Security Rules, and presented it in the Sprint 4 in-class demo on Nov 3.
