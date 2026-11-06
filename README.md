# Honeypot assets
 
Project documentation and evidence for the Cowrie SSH honeypot analytics project: sprint reports, sprint summary
videos, static code analysis, branch protection, and the design and requirements.
 
Part of a four-repo project: **assets** (this repo), **backend** (FastAPI API, Cowrie honeypot, log shipper, firewall and
VPS setup guide), **frontend** (dashboard) and **contracts** (agreed API and data shapes).
 
## Contents
Paths are folder names to adjust to match your repo.
 
| What | Contents |
|---|---|
| Sprint reports | Jira and GitHub sprint reports (progress, completed work, burndown) |
| Sprint summary videos | short video summary recorded for each sprint |
| Static code analysis | reports from the static analysis tool(s) run on the code, and how findings were handled |
| Branch protection | settings and screenshots showing protected branches (required reviews, required checks, no direct pushes to the main branch) |
| Design and Requirements | requirements and design: goals, user needs, architecture, data model and API |
 
## Where the code lives
- Honeypot (Cowrie), log shipper, egress firewall, VPS setup guide: **backend** repo (`cowrie-vps/`)
- API, MongoDB access, MITRE ATT&CK rules: **backend** repo (`fastapi-backend/`)
- Dashboard: **frontend** repo
- API and database contracts: **contracts** repo
