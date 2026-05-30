# Muhammad Hamid (Hamid)
**AI Platform Engineering Lead · Full Stack · Toronto, Canada**

I lead engineering at [HuntigoX](https://huntigox.com) — Canada's first AI-powered anti-fraud employment platform. I started as a product developer. I ended up owning the full stack, leading 25+ engineers across four teams, and holding final merge authority over every line of code that ships to production.

Currently: Bachelor of Software Development student at Seneca Polytechnic

---

## What I'm leading right now

### HuntigoX — AI-Powered Compliance Infrastructure
*Tech Lead & Final Architecture Authority · Kenoxis Technologies Inc. · 2025–Present*

HuntigoX is not a job board. It's compliance infrastructure that looks like one — built to prove Canadian employers genuinely tried to hire Canadians before pursuing foreign workers under the IRCC Temporary Foreign Worker Program.

**My scope:**
- Final merge authority on all production code across 3 repos (scoring, backend, frontend)
- Architecture review for 25+ engineers: 4 teams including ML/AI, security, and analytics capstone squads
- Sole decision-maker on API contracts, state machine design, PR approvals, and production releases

**Systems I've built or own:**

**FraudShield AI Engine** — 4-factor behavioral fraud scoring running every 6 hours across all employer accounts. Factors: hiring rate, salary compliance, application velocity, rejection documentation. Scores 0–100. At CRITICAL (76+): auto-suspend account, deactivate all jobs, fire Twilio SMS + email — all in an atomic MongoDB transaction. Built on Node.js + MongoDB + Redis cron infrastructure.

**LMIA Evidence Pack Generator** — 12-page legally defensible PDF that auto-generates on Day 31 of every job posting. This document goes to ESDC and IRCC as evidence in Canadian immigration proceedings. Built with Puppeteer, stored on S3, SHA-256 hashed for immutability. Every page is sourced from real-time compliance data frozen at generation time.

**VerifyMe Scoring Engine** — 100-point candidate trust scoring system with 11 states, AWS Textract OCR for document verification, and AWS Rekognition for face-match and liveness. Admin pipeline with score override capability, full audit trail, real-time badge propagation across job applications and LMIA evidence packs.

**CanadaFirst Enforcement Engine** — server-side enforcement of ESDC's 30-day priority hiring window. Legal status is verified status only — never declared. JWT and DB are separate — foreign worker status never touches the token. EOI auto-promotion cron converts waitlisted candidates to applications hourly when windows expire.

**Live Hiring System** — real-time GPS-based candidate-employer matching. Redis GEO index for proximity, Socket.IO for presence, velocity-check fraud detection (>100km in <5min = GPS spoofing flag), VPN/proxy detection via IP geolocation mismatch.

**Employer Trust Index** — 5-component private reputation system feeding into FraudShield and LMIA scoring. Integrates post-hire verification data, RepScore public ratings, behavioral analytics, and document compliance history.

**Stack:** Node.js ESM · Express 5 · MongoDB/Mongoose 9 · Redis · Socket.IO 4 · Next.js 15 App Router · TypeScript · Python/FastAPI · AWS (Textract, Rekognition, S3, SES) · Stripe · Puppeteer · OpenAI · Mapbox · Winston · Mocha/Chai/Supertest · pytest

---

## Personal projects

### [llm-cost-tracker](https://github.com/mhakhalid/llm-cost-tracker)
Real-time spend dashboard for Claude / OpenAI / Gemini across projects. Express proxy intercepts every API call, calculates cost per token, surfaces breakdowns by model and project on a React dashboard. Slack alerts when budgets are hit.

`React` `Node.js` `Express` `Python` `Chart.js`

---

### [reddit-signal](https://github.com/mhakhalid/reddit-signal)
CLI + FastAPI service that scans subreddits for recurring developer pain points and ranks them by buildability. Runs threads through Claude, returns prioritized problem list. This is the tool I use to decide what to build next.

`Python` `FastAPI` `Reddit API` `Claude API`

---

### [agent-workflow-templates](https://github.com/mhakhalid/agent-workflow-templates)
Open-source n8n + Claude workflow templates for GitHub automation, content pipelines, and API cost tracking. Each template ships with a working JSON file and a README that explains the trigger logic.

`n8n` `Claude API` `Automation`

---

### [devboard](https://github.com/mhakhalid/devboard)
Personal dev command center — GitHub stats, open PRs, contribution streak, daily tasks. Pulls live data from the GitHub API. One-click Vercel deploy.

`React` `GitHub API` `Vercel`

---

## Stack

**Frontend:** Next.js 15, React 18, TypeScript, Tailwind v4, Zustand, Framer Motion  
**Backend:** Node.js ESM, Express 5, Python, FastAPI  
**AI/ML:** Claude API, OpenAI, AWS Textract, AWS Rekognition, FraudShield scoring engine  
**Databases:** MongoDB/Mongoose, PostgreSQL, Redis  
**Infrastructure:** AWS (S3, SES, Rekognition, Textract), Vercel, Render, Socket.IO, Stripe, Puppeteer  
**Testing:** Mocha + Chai + Supertest, pytest, Cypress  

---

## What I'm looking for

AI engineering, full stack engineering, or technical lead roles — Toronto or remote.  
Specifically interested in teams building production AI systems, RegTech, compliance infrastructure, or developer tooling.

📬 mhakhalid@myseneca.ca  
🔗 [huntigox.com](https://huntigox.com)

---

*I'm not listing certifications. I'm listing production systems that handle real immigration compliance data for real employers.*
