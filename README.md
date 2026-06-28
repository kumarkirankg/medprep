# 🩺 ClearTriage
### Clinical AI Pre-processing · Medication Intelligence Layer

---

Clinics and telehealth platforms handle **thousands of inbound patient calls every day**. A large portion are medication queries — missed doses, side effects, running out of prescriptions, dosing questions for children.

AI receptionists handle the call. But **medication queries need clinical intelligence** before they reach a doctor or pharmacist.

> **ClearTriage sits in between.**

It takes the patient call transcript, analyses it, and returns:

| Output | Description |
|---|---|
| 🔴 **Triage priority** | Urgent, Routine, or Self-care |
| 🗒 **Structured clinical note** | Ready for the doctor or pharmacist |
| 💬 **Scripted response** | For the AI receptionist to read back to the patient |
| ➡ **Next action** | With a realistic timeframe |
| 🚩 **Key clinical flags** | Surfaced immediately for the clinical team |

> **No clinical advice is given to the patient. ClearTriage is purely a pre-processing and triage layer.**

---

## 🟢 Live Demo

**[cleartriage — kumarkirankg.github.io/cleartriage](https://kumarkirankg.github.io/cleartriage)**

Five built-in scenarios:
- ACE inhibitor cough
- Ran out of BP tablets
- Child's fever not settling
- Metformin side effects
- Missed warfarin dose

---

## ⚙️ How It Works

```
Patient call transcript
          |
    ClearTriage analyses
          |
  ┌─────────────────────────────────────┐
  │  Triage priority                    │
  │  Clinical note for doctor           │
  │  AI receptionist response script    │
  │  Next action + timeframe            │
  │  Key clinical flags                 │
  └─────────────────────────────────────┘
          |
  Clinical team receives structured output
```

---

## 🔗 Integration Concept

ClearTriage is designed to complement **any AI receptionist system** handling high volume patient calls. The integration would work as follows:

- AI receptionist **detects medication-related call intent**
- Transcript passed to ClearTriage **via webhook** on call close
- ClearTriage returns **structured JSON output**
- Clinical note routes to doctor or pharmacist via existing clinical system integration
- Response script passed back to AI receptionist for patient communication
- All outputs **logged for clinical audit**

---

## 🛡️ Clinical Safety

- ✅ No clinical advice is given to the patient at any point
- ✅ ClearTriage is a pre-processing layer only — all clinical decisions remain with the clinical team
- ✅ Designed with clinical safety principles in mind
- ⚠️ **Concept prototype — not for clinical use**

---

## 🛠️ Built With

- **Claude** — AI analysis and clinical output development
- **HTML / JavaScript** — frontend interface
- **GitHub Pages** — public demo hosting

---

## 👤 About

Built by **[Kiran Kumar] https://www.linkedin.com/in/kiran-kumar-96b224393/** as a concept prototype exploring how AI pre-processing can reduce clinical staff workload in high volume patient call environments.

---

*Concept prototype · not for clinical use · designed to complement AI receptionist systems in high volume clinical environments · developed using Claude*
