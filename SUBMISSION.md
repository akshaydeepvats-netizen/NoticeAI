# NoticeAI — Submission Description

**Event:** Hacktoberfest Hackday 2026  
**Selected problem statement:** PS 02 — Notice-to-Action Accessibility Assistant  
**Track:** Track 1 — Best Use of Gemma 4  
**Project type:** Software / AI web application  
**Team:** Solo  
**Public repository:** [PASTE YOUR ACTUAL GITHUB REPOSITORY URL HERE]

## Abstract
NoticeAI is an AI-powered accessibility assistant that transforms complex or image-based notices into clear, actionable information. Users can upload an image/PDF or paste notice text. The application extracts relevant text, uses Gemma 4 to identify key details, produces a plain-language summary and ordered checklist, and supports follow-up questions in English or Hindi. It is designed to identify information absent from the notice rather than inventing dates, eligibility rules, documents, or contact details.

## Problem
Important details in college notices, scholarship announcements, public-service notices, and application instructions can be difficult to find or understand. Readers may miss deadlines, eligibility criteria, required documents, and next steps.

## Workflow
1. Upload an image/PDF or paste notice text.
2. Extract text using PDF parsing and OCR where required.
3. Use Gemma 4 to interpret the notice and return structured fields.
4. Display purpose, eligibility, deadline, documents, contact, summary, and action checklist.
5. Provide English/Hindi output.
6. Answer follow-up questions using the supplied notice.
7. Flag absent or unverified information.

## Technology
Python, Streamlit, Gemma 4 via Ollama, Tesseract OCR, PyMuPDF, Pillow, and Requests.

## Expected impact
NoticeAI aims to make official information easier to understand for students and community members, particularly when notices are dense, image-based, or written in a less familiar language.

## Responsible AI
The application displays source quotes and checks whether quoted evidence appears in extracted text. This is a guardrail, not a guarantee of correctness. OCR and AI can make mistakes; important facts should be checked against the original notice. The demo notice is synthetic and labelled as such.

## Final checklist
- [ ] Public GitHub repository created.
- [ ] Open-source licence included.
- [ ] README setup instructions reviewed.
- [ ] App launched locally.
- [ ] Supported question tested.
- [ ] Missing-information question tested.
- [ ] English and Hindi output tested.
- [ ] At least one image/PDF input tested.
- [ ] Screenshots captured from actual runs.
- [ ] Actual results recorded in TEST_PLAN.md.
- [ ] Repository URL and official submission link added to the event form.
