# SIFT
 
> **Your digital footprint, audited.**
 
Sift is an AI agent that analyzes your personal social media archives (LinkedIn + X/Twitter) to identify privacy risks, exposed personal information, and social engineering vulnerabilities, then tells you exactly what to fix.
 
Built for the [AMD Developer Hackathon](https://lablab.ai/ai-hackathons/amd-developer) on AMD Developer Cloud.
 
---
 
## The Problem
 
Most professionals have years of posts, comments, and profile data they've forgotten about. Cumulatively, this creates a detailed picture that attackers can use for phishing, social engineering, or identity theft, and the person has no idea it exists.
 
**Sift changes that.**
 
---

## How It Works
 
1. **Export your data** — Use LinkedIn's "Download your data" and X's "Your X data archive" to get your full history
2. **Upload your archive** — Drop the files into Sift's clean upload interface
3. **Agent analyzes it** — Scans for PII, behavioral patterns, sensitive disclosures, and social engineering surface
4. **Agent analyzes each platform individually** — scanning for PII, behavioral patterns, sensitive disclosures, and social engineering surface
5. **Cross-platform correlation runs** — finding combinations across LinkedIn and X that escalate in severity when combined
6. **get your risk report** — color-coded by severity with plain-English explanations, individual findings, and combined threat chains

---
 
## What Sift Detects
 
| Category | Examples |
|---|---|
| 🔴 Personal Information | Emails, phone numbers, location mentions, family names |
| 🟠 Behavioral Patterns | Daily routines, travel announcements, predictable schedules |
| 🟡 Sensitive Disclosures | Company tools, internal frustrations, financial hints |
| 🟢 Social Engineering Hooks | Emotional triggers, trusted contacts, life events |
 
**Severity Levels:** Critical / High / Medium / Low
 
---
 
## Cross-Platform Correlation
 
A Medium finding on LinkedIn and a Medium finding on X can together become a Critical threat. Sift's correlator identifies these chains, showing not just what you've exposed, but how an attacker would combine it across platforms.
 
**Example:**
 
| Finding | Source | Individual Severity |
|---|---|---|
| "I travel every Monday for client meetings" | LinkedIn | Medium |
| Photos tagged from home location every Sunday | X/Twitter | Low |
| **Attacker knows you're away Mondays, home Sundays** | **Correlated** | **🔴 Critical** |
 
The correlator runs as a dedicated second-pass LLM analysis after individual findings are collected. Each correlated threat includes the contributing finding IDs, a concrete attack scenario, and a specific remediation to break the chain.
 
---
## Tech Stack
 
| Layer | Technology |
|---|---|
| Frontend | Next.js 14 (App Router) |
| Backend | Python + FastAPI |
| AI Agent | LangChain + open-source LLM (Llama / Mistral) |
| Correlation Engine | Second-pass LLM prompt, cross-source finding analysis |
| Compute | AMD Developer Cloud (MI300X GPU) |
| Storage | JSON (stateless, no database) |
| Archive Input | LinkedIn CSV/JSON + X JSON archive |
 
---

## Project Structure
 
```
sift/
├── frontend/                        # Next.js app
│   └── src/
│       ├── app/                     # App Router pages + layout
│       ├── components/              # UI + report display components
│       └── lib/api.ts               # FastAPI client
├── backend/                         # FastAPI + agent logic
│   └── app/
│       ├── main.py                  # App entry point + CORS
│       ├── agents/
│       │   ├── sift_agent.py        # Main pipeline (3-phase)
│       │   └── correlator.py        # Cross-platform threat correlation
│       ├── parsers/
│       │   ├── linkedin_parser.py   # LinkedIn archive parser
│       │   └── twitter_parser.py    # X/Twitter archive parser
│       ├── models/
│       │   ├── report.py            # SiftReport + Finding schemas
│       │   └── correlation.py       # CorrelatedThreat schema
│       └── routers/
│           ├── upload.py            # POST /api/upload/analyze
│           └── report.py            # GET /api/report/{session_id}
└── docs/
    └── architecture.md              # System diagram + risk taxonomy
```
 
---

## Getting Started
 
### Prerequisites
- Node.js 18+
- Python 3.10+
- AMD Developer Cloud account with credits
  
### Backend
```bash
cd backend
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env            # add your AMD API key
uvicorn app.main:app --reload
```
 
### Frontend
```bash
cd frontend
npm install
cp .env.example .env.local
npm run dev
```
 
Visit `.. `
 
---
 
## Team
 
**Team Swift** — AMD Developer Hackathon 2026
 
| Name | Responsibility |
|---|---|
| ShaShank Shinde | Responsibilities |
| Tushar Sharma | Responsibilities |
 
---
