# Judge Demo Script — NoticeAI (3–4 minutes)

Use this script only after running the app. The built-in sample is synthetic, not an official scholarship notice.

## 0:00–0:30 — Problem
“Important information in notices can be hard to understand, especially when it is buried in long text or an image. Missing a deadline or document can prevent someone from completing an application. NoticeAI converts a notice into clear steps while keeping answers grounded in the supplied source.”

## 0:30–1:15 — Analyze a notice
Load the synthetic scholarship notice and click Analyze. Show purpose, eligibility, deadline, required documents, contact, summary, and checklist.

“Gemma 4 interprets the extracted text. The app checks whether each evidence quote appears in the source. This is a guardrail, not a guarantee, so the original text remains available for review.”

## 1:15–2:00 — Accessibility
Select Hindi and analyze again. Show the Hindi summary and checklist.

“The goal is to make the information easier to act on while preserving source facts.”

## 2:00–2:45 — Follow-up and missing information
Ask: “What is the last date to apply?” Then ask: “What is the scholarship amount?”

“The deadline is stated in the sample. The amount is not stated, so NoticeAI should not invent one.”

## 2:45–3:30 — Limitations
“OCR can misread poor-quality images and language models can make mistakes. This prototype shows evidence and flags unverified quotes. Planned improvements include page-level highlighting, OCR confidence, human confirmation, and broader evaluation.”

## Before presenting
- Confirm Ollama is running and the model is available.
- Launch and test the app before the demo.
- Use a readable sample notice.
- Do not claim unrun tests or incomplete features are complete.
- Keep screenshots or a short recording of an actual successful run as backup.
