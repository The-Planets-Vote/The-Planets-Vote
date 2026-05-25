# The Planet's Vote

**A proposed global direct-democracy platform where every adult human on Earth votes on planetary-scale decisions.**

Every adult human on Earth votes on planetary-scale issues — climate, AI governance, pandemic preparedness, asteroid defence, supervolcanic risk — with a two-thirds supermajority threshold. Votes are demand-triggered and held quarterly. For verified planetary emergencies, a crisis vote opens within six hours. No nation controls it. Including its founder.

🌍 **Live platform:** [theplanetsvote.org](https://theplanetsvote.org)  
💻 **Shadow votes:** [theplanetsvote.org/world_vote.html](https://theplanetsvote.org/world_vote.html)  
📄 **White Paper v1.10:** [theplanetsvote.org/The-Planets-Vote_WhitePaper_v1_10.pdf](https://theplanetsvote.org/The-Planets-Vote_WhitePaper_v1_10.pdf)

---

## What is The Planet's Vote?

The Planet's Vote is not a petition platform, a polling tool, or a lobbying mechanism. It is a proposed permanent democratic infrastructure for humanity — a mechanism through which the verified will of all people on Earth can be expressed with binding force on the decisions that affect all of us equally.

The five issue categories:
- **Planetary defence** — asteroid and comet threat response
- **Supervolcanic risk** — geothermal depressurisation programmes
- **Climate** — binding global mandates on emissions reduction
- **AI governance** — democratic consent before existential-risk deployments
- **Pandemic preparedness** — global early warning and response coordination

**Voting mechanics:** Demand-triggered quarterly voting. Two-thirds supermajority required. Emergency override opens within 6 hours of verified threat confirmation with 75% threshold. Minimum two questions must reach signal threshold before a quarterly vote is called.

**Signal threshold (phased):**
- Phase 1 — under 1 million registered voters: 100,000 signals
- Phase 2 — 1 to 50 million registered voters: 1 million signals
- Phase 3 — over 50 million registered voters: 2% of total registered voters

---

## What is currently built

This repository contains the platform interface — a working demonstration of what The Planet's Vote looks like and how it operates.

**Live and functional:**
- Four real shadow votes on planetary questions, recording real votes from real visitors worldwide
- Persistent vote storage via Google Apps Script backend
- Regional participation tracking
- Results panel showing live tallies
- Propose Issue tab for visitor submissions
- Signal progress panel showing live vote counts and breakdowns

**Illustrative (demo):**
- World Government Representatives panel
- Demo quarterly cycle display
- Simulated signal counts on demo issues
- Blockchain/ZKP confirmation messages (planned architecture, not yet implemented)

---

## Technical architecture

### Current implementation

The live shadow vote platform is built as a single-file HTML/CSS/JavaScript application hosted on GitHub Pages. Vote persistence uses Google Apps Script as a lightweight backend — no server required, no database, no infrastructure costs.

**Stack:**
- Frontend: Vanilla HTML/CSS/JavaScript (single file, no build step)
- Backend: Google Apps Script (free, serverless, CORS-compatible)
- Hosting: GitHub Pages
- Domain: Namecheap

### Planned identity architecture (White Paper v1.10)

The full identity layer is based on **Ring VRF (Verifiable Random Function)** with registered public keys, anchored to ePassport NFC chips. The Planet's Vote is actively seeking collaboration with Swiss Post's Cryptography Center to inform the technical implementation of these principles at planetary scale.

**Existing open-source implementations of the core stack:**
- [zkPassport](https://zkpassport.id) — ePassport NFC to ZK proof on smartphones
- [EU eIDAS ZKP Wallet](https://eu-digital-identity-wallet.github.io) — government-backed ZK identity for 440M+ citizens
- [Human Passport](https://human.tech) — modular proof-of-personhood with ZK passport verification

---

## Repository structure

```
/
├── index.html                              # Main website
├── world_vote.html                         # Shadow vote platform
├── The-Planets-Vote_WhitePaper_v1_10.pdf     # Full white paper (PDF)
├── The-Planets-Vote_WhitePaper_v1_10.docx    # Full white paper (Word)
├── README.md                               # This file
├── change-the-world.mp3                    # Audio
└── CNAME                                   # Domain configuration
```

---

## Deploying your own instance

### 1. Fork this repository

Fork and enable GitHub Pages (Settings → Pages → Deploy from branch → main).

### 2. Set up the Google Apps Script backend

1. Go to [sheets.google.com](https://sheets.google.com) and create a new spreadsheet
2. Rename the default tab to **Votes**
3. Click **Extensions → Apps Script**
4. Delete the placeholder code and paste the contents of `PlanetVote_AppsScript.js`
5. Click **Deploy → New deployment → Web app**
   - Execute as: **Me**
   - Who has access: **Anyone**
6. Copy the Web App URL

### 3. Configure world_vote.html

Open `world_vote.html` in a text editor and replace `YOUR_APPS_SCRIPT_URL_HERE` with your Web App URL.

---

## Contributing

**Cryptography and identity:** The ring VRF identity layer is the core unsolved problem. If you work in ZK proofs, ePassport verification, or proof-of-personhood systems, your engagement is particularly valuable.

**Governance design:** The white paper addresses objections to global direct democracy but acknowledges open questions.

**Platform development:** The current platform is a single-file demo. A production implementation would require proper infrastructure, smart contract integration, and security auditing.

**Translation:** Translations of the interface and white paper into languages beyond English would significantly extend reach.

Open an issue to start a conversation, or submit a pull request.

---

## Project status

Launched: 3 April 2026  
Current version: v1.10 (May 2026)  
White paper: v1.10  
Shadow votes: 4 live questions  
Official partner: Institute for the Development of a Global Democratic Republic (IDGR), Austria

**Responses received from:**
- Professor Johan Rockström, Potsdam Institute for Climate Impact Research
- Professor Frank Biermann, Earth System Governance Project (invited to present at Uppsala ESG Conference 2027)
- Hindou Oumarou Ibrahim, UN Permanent Forum on Indigenous Issues
- Andreas Bummel, Democracy Without Borders
- Caroline Vernaillen, Democracy International (invited to Global Forum on Modern Direct Democracy, Gaborone)
- Dr Karl Baumann, Institute for the Development of a Global Democratic Republic

---

## Founder

**Paul Innes**  
Cairns, Far North Queensland, Australia  
Quadriplegic disability advocate since 1988  
[founder@theplanetsvote.org](mailto:founder@theplanetsvote.org)

*In The Planet's Vote, I would be just another voter. I seek no control.*

---

## Licence

MIT Licence. Use freely. Build on it. Make it better.
