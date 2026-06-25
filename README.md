# MedPrep 💊 | Medication Intelligence Layer

> 👉 **[Live Interactive Demo: Try MedPrep Here](https://kumarkirankg.github.io/medprep/)**
>
> 🛠️ Note for Reviewers: To protect private developer limits, this prototype securely reads your own Gemini API Key via your browser's local storage. You can grab a completely free, instant sandbox key from Google AI Studio to interact with the live AI pipeline.

## Overview
EMMA handles every inbound patient call as an AI receptionist—but medication queries require clinical intelligence before they reach a GP or pharmacist. 

**MedPrep** is a conceptual medication intelligence layer that sits between EMMA's call transcript and the clinical handoff. It safely triages urgency, generates a structured clinical note, and scripts EMMA's verbal response back to the patient. 

*Crucially, no clinical advice is given to the patient—MedPrep strictly handles structured pre-processing and safe routing.*

## The Interface
![MedPrep Prototype Demo](Capturec1.PNG)

## Key Features

* **Intelligent Triage:** Automatically classifies patient transcripts into `Urgent`, `Routine`, or `Self-care` priority levels based on clinical context.
* **Structured Clinical Summaries:** Converts conversational, unstructured patient anxiety into concise, professional notes optimized for a GP or Pharmacist to read quickly.
* **Automated Flagging:** Extracts 3-4 key clinical flags (e.g., "Possible ACE inhibitor adverse effect" or "Abrupt medication cessation risk").
* **Safe Patient Scripting:** Generates warm, clear, and non-diagnostic scripts for the EMMA voice agent to read back to the patient, managing expectations on wait times and next steps.

## Technical Architecture

This prototype was built to demonstrate complex LLM reasoning within a lightweight, serverless frontend environment.

* **Frontend:** React 18 (Single-file CDN deployment for instant execution)
* **AI Engine:** Google Gemini 1.5 Pro API (`gemini-1.5-pro`)
* **Prompt Engineering:** Strict JSON-schema enforcement via `responseMimeType: "application/json"` and specialized system instructions to guarantee deterministic, parseable outputs without markdown hallucination.
* **Styling:** Custom CSS variables with Tabler Icons.
* **Deployment:** GitHub Pages

## How to Run Locally
Because this project uses a single-file architecture to eliminate build-step friction, running it locally is instantaneous:
1. Clone the repository.
2. Open `index.html` directly in any modern web browser.
3. *Note: An active Google Gemini API key is required in the source code to process live queries.*
