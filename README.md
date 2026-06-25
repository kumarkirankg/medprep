# MedPrep — Medication Intelligence Layer

**A concept prototype built for EMMA, an NHS GP surgery AI receptionist by QuantumLoopAI.**

→ **[Live Demo](https://kumarkirankg.github.io/medprep)** 

---

## What is this?

GP surgeries receive hundreds of inbound patient calls every day. A large portion are medication queries — missed doses, side effects, running out of prescriptions, dosing questions for children.

EMMA handles the call. But medication queries need clinical intelligence before they reach a GP or pharmacist.

**MedPrep sits in between.**

It takes EMMA's call transcript, analyses it using Claude (Anthropic's AI), and returns:

- A **triage priority** — Urgent, Routine, or Self-care
- A **structured clinical note** ready for the GP or pharmacist
- A **scripted response** for EMMA to read back to the patient
- A **next action** with a realistic timeframe
- **Key clinical flags** to surface immediately

No clinical advice is given to the patient. MedPrep is purely a pre-processing and triage layer.

---

## Demo

Try it live — no login, no install needed.

Three sample queries are pre-loaded (ACE inhibitor cough, missed BP medication, child's fever) or type any medication query directly into the box.

---

## How it works

```
Patient call
     ↓
EMMA transcribes the query
     ↓
MedPrep analyses it via Claude API
     ↓
Returns structured triage JSON
     ↓
EMMA reads scripted response to patient
Clinical note routed to GP / pharmacist
```

The frontend is a single HTML file hosted on GitHub Pages. API calls are proxied through a Cloudflare Worker so the key is never exposed in the browser or source code.

---

## Tech stack

| Layer | Technology |
|---|---|
| Frontend | React (via CDN), plain HTML/CSS |
| AI model | Claude Sonnet (Anthropic API) |
| API proxy | Cloudflare Workers (free tier) |
| Hosting | GitHub Pages (free) |

---

## Triage outputs

| Priority | When it applies |
|---|---|
| 🔴 Urgent | Potential adverse drug reaction, abrupt cessation risk, symptoms requiring same-day review |
| 🔵 Routine | Queries needing a clinician but not time-critical |
| 🟢 Self-care | Minor queries that can be resolved with pharmacy advice or patient information |

---

## Limitations & disclaimers

- This is a **concept prototype only** — not validated for clinical use
- MedPrep does not give clinical advice to patients
- All triage outputs should be reviewed by a qualified clinician before action
- Built to demonstrate an integration concept between an AI receptionist and a clinical pre-processing layer

---

## About

Built as a concept integration for **EMMA by QuantumLoopAI** — an AI receptionist designed for NHS GP surgeries.
