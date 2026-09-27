# MediKiosk — AI Clinical History Software Platform (Multilingual OPD Intake & Triage)

[![FastAPI](https://img.shields.io/badge/Backend-FastAPI-009688.svg?style=flat&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![React](https://img.shields.io/badge/Frontend-React_18-61DAFB.svg?style=flat&logo=react&logoColor=black)](https://reactjs.org/)
[![Supabase](https://img.shields.io/badge/Database-Supabase_PostgreSQL-3ECF8E.svg?style=flat&logo=supabase&logoColor=white)](https://supabase.com)
[![Gemini](https://img.shields.io/badge/AI-Google_Gemini-4285F4.svg?style=flat&logo=google&logoColor=white)](https://ai.google.dev/)
[![FHIR](https://img.shields.io/badge/Standards-FHIR_R4-E01A22.svg?style=flat)](https://hl7.org/fhir/)
[![Vibe Coded](https://img.shields.io/badge/Vibe%20Coded-100%25-ff69b4.svg?style=flat)](https://github.com/)

> An AI-powered, multilingual clinical history intake and smart hospital kiosk platform designed to streamline patient triaging, record symptoms, digitize medical documents, and generate structured clinical summaries for healthcare providers.

---

## Overview

**MediKiosk** bridges the gap between arriving patients and healthcare workers by automating the initial clinical history intake. Built to operate as an interactive point-of-care kiosk (and companion web portal), it allows patients to input symptoms via speech or text in their native language, scan prior prescriptions or diagnostic reports, and produce structured, clinician-ready intake summaries before the patient enters the consultation room.

---

## Key Features

- **Multilingual Patient Intake:** Guided questionnaire supporting regional and native languages via speech-to-text and intuitive touchscreen UI.
- **AI-Driven Clinical Summaries:** Uses LLM inference to synthesize raw patient descriptions into standardized clinical notes (Chief Complaints, History of Present Illness, Allergies, Current Medications).
- **Medical Document Digitization (OCR):** Scans and extracts key clinical data from previous lab reports, prescriptions, and discharge summaries.
- **Triage & Acuity Scoring:** Highlights urgent symptoms and flagged vitals to help prioritize waiting queues.
- **Doctor Dashboard:** Dedicated clinician view for reviewing structured intake data, original transcriptions, and digitized records in real time.

---

## Tech Stack

- **Frontend:** React / Vite, TypeScript, Tailwind CSS
- **Backend:** Node.js (Express) / Python (FastAPI)
- **AI & ML:** Gemini API / Vision Models (OCR, symptom extraction, and summarization)
- **Database & Auth:** Firebase / MongoDB / PostgreSQL
- **Audio & Speech:** Web Speech API / Cloud Speech-to-Text

---

## Architecture Flow

```text
[ Patient / Kiosk Terminal ]
        │
        ├── (Speech / Audio Input)  ──► [ Speech-to-Text ]
        ├── (Prescription Scan)     ──► [ Document OCR ]
        └── (Symptom Prompts)       ──► [ Multilingual Form State ]
                                                  │
                                                  ▼
                                       [ Backend API Layer ]
                                                  │
                                                  ▼
                                      [ LLM Intake Engine ]
                                  (Summarization & Extraction)
                                                  │
                                                  ▼
                                       [ Clinician Dashboard ]
