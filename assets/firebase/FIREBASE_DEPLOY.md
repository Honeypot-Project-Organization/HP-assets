# Firebase Hosting – Deploy Guide

The dashboard frontend is hosted on Firebase Hosting (Jira: HONEYPOT-149).

| Item | Value |
|------|-------|
| Firebase project | `honeypot-dashboardpro` |
| Live URL | https://honeypot-dashboardpro.web.app |
| Alternate URL | https://honeypot-dashboardpro.firebaseapp.com |
| Frontend stack | React + Vite (build output: `dist/`) |
| Auth | Not used on Firebase. Login is handled by JWT on the FastAPI backend. |

## Files in this folder

- `firebase.json`: Hosting config. Serves the `dist` folder and rewrites every route to `/index.html` so React routing works when a page is refreshed.
- `.firebaserc`: Links the project folder to the `honeypot-dashboardpro` Firebase project.

**Before the first deploy, copy both files into the root of the frontend project** (the same folder as `package.json`).

## One-time setup

1. Install Node.js (LTS) from https://nodejs.org
2. Install the Firebase CLI:
   ```
   npm install -g firebase-tools
   ```
   On Windows PowerShell, if you get "running scripts is disabled", run this once and try again:
   ```
   Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
   ```
3. Log in with the Google account that has access to the Firebase project:
   ```
   firebase login
   ```

## Deploying

Run these from the root of the frontend project:

1. Install dependencies (first time, or after they change):
   ```
   npm install
   ```
2. Build the site (creates the `dist` folder):
   ```
   npm run build
   ```
3. Deploy:
   ```
   firebase deploy --only hosting
   ```
4. Open the Hosting URL printed at the end and check the live site.

## Troubleshooting

- **"Directory 'dist' for Hosting does not exist"**: run `npm run build` first.
- **Page shows "Not Found" after refresh**: make sure `firebase.json` includes the `rewrites` rule.
- **"Failed to get Firebase project"**: run `firebase login` with an account that has access, and check that `.firebaserc` is in the same folder you are deploying from.
- **Rollback**: Firebase console → Hosting → Release history → choose a previous release → Rollback.
