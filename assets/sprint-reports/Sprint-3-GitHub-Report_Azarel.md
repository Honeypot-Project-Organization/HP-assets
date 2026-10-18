# Sprint 3 GitHub Report – Azarel Evangelista

**Sprint:** 3 (Oct 7, 2026 – Oct 20, 2026)
**GitHub username:** Oz-ee

## Repositories

- https://github.com/Honeypot-Project-Organization/HP-frontend
- https://github.com/Honeypot-Project-Organization/HP-backend
- https://github.com/Honeypot-Project-Organization/HP-assets

## Pull Requests Reviewed and Merged During Sprint 3

| Repo / # | PR Title | PR Link | Author | Reviewer | Merged By | Merge Date |
|---|---|---|---|---|---|---|
| HP-frontend #1 | Added frontend | https://github.com/Honeypot-Project-Organization/HP-frontend/pull/1 | Andrew (CyberWzzard) | Azarel (Oz-ee) (approved) | Azarel (Oz-ee) | 2026-10-17 |
| HP-backend #10 | Added frontend APIs and geoIP mapping stuff, and removed frontend-security.md doc (goes in frontend repo) | https://github.com/Honeypot-Project-Organization/HP-backend/pull/10 | Andrew (CyberWzzard) | Azarel (Oz-ee) (approved) | Azarel (Oz-ee) | 2026-10-17 |

**Total PRs reviewed and merged:** 2

Review notes:

- **HP-backend #10:** Reviewed the new dashboard endpoints and the change of `raw_event_retention_days` from 30 to 7 days (HONEYPOT-206). Flagged that the live Atlas TTL index was still at 30 days after the Oct 16 backend restart, and that the server `.env` needed `RAW_EVENT_RETENTION_DAYS=7` plus a restart.
- **HP-frontend #1:** Checked that `firebase.json` and `.firebaserc` were included and that `.env` is kept out of the repo by `.gitignore`. After merging, built the frontend and deployed it to Firebase Hosting (HONEYPOT-144).

## Pull Requests Opened During Sprint 3

| Repo / # | PR Title | PR Link | Status |
|---|---|---|---|
| HP-assets #6 | Add Firebase Hosting config and deploy guide (HONEYPOT-149) | https://github.com/Honeypot-Project-Organization/HP-assets/pull/6 | Closed without merging. The team agreed the Firebase config belongs in HP-frontend, so the files were removed from the `assets` branch and added to the frontend through HP-frontend #1. |

## Commit Activity

| Date | Repo | Commit | Message |
|---|---|---|---|
| 2026-10-17 | HP-frontend | 6e7bac0 | Merge pull request #1 from Honeypot-Project-Organization/frontend |
| 2026-10-17 | HP-backend | 8eb87c1 | Merge pull request #10 from Honeypot-Project-Organization/backend |
| 2026-10-15 | HP-assets | 70905d0 | Remove Firebase config from assets; moving to HP-frontend (HONEYPOT-149) |
| 2026-10-14 | HP-assets | 6e6939e | Add Firebase Hosting config and deploy guide (HONEYPOT-149) |

- **Total number of commits:** 4
- **Date range:** 2026-10-14 – 2026-10-17

## Related Work This Sprint (outside GitHub)

- **Firebase Hosting (HONEYPOT-149, HONEYPOT-181):** Created the Firebase project `honeypot-dashboardpro`, configured hosting for React/Vite, and added the teammate as Editor.
- **Frontend deployment (HONEYPOT-144, HONEYPOT-174):** Built the merged frontend and deployed it; the dashboard is live at https://honeypot-dashboardpro.web.app.
- **Log purging (HONEYPOT-206):** Set up and verified a 7-day TTL index on `raw_events` in MongoDB Atlas (`expireAfterSeconds: 604800`).
