# NoticeAI Nexus

A local-first accessibility assistant that turns public notices into plain-language summaries, evidence-checked facts, and actionable checklists. Built with Streamlit and Ollama.

## Features

- Navigate between Home, Analyze Notice, History, Saved Results, and Settings.
- Analyze pasted text or upload a PDF/image notice.
- Extract text from scanned PDFs and images (requires Tesseract OCR installed on the computer).
- View summaries, eligibility, deadlines, required documents, action steps, evidence quotes, and missing information.
- Ask follow-up questions grounded in the notice.
- Keep recent analyses and saved results in the current Streamlit session; export results as JSON.
- Test whether the local Ollama service is reachable.

## Run locally on Windows

1. Install Python 3.11 or 3.12.
2. Install [Ollama](https://ollama.com/) and download the configured model:

   ```powershell
   ollama pull gemma4:e2b
   ```

3. Start Ollama, then open Command Prompt/PowerShell in this folder.
4. Install dependencies and start the app:

   ```powershell
   python -m pip install -r requirements.txt
   python -m streamlit run app.py
   ```

5. Open the local URL printed by Streamlit, usually `http://localhost:8501`.

### Optional OCR setup

For image files or scanned PDFs, install the Tesseract OCR application separately and ensure `tesseract.exe` is available on your PATH. Text-based PDFs do not usually need OCR.

## GitHub and public deployment — important

Pushing this repository to GitHub stores and shares the **source code**; a GitHub repository URL does not run this Streamlit app. GitHub Pages does not host Streamlit/Python apps.

You can deploy the Streamlit interface on a Streamlit-compatible hosting service, but the current app calls `http://localhost:11434` for Ollama. On a cloud host, `localhost` means the cloud server, **not your personal computer**, so analysis will not work there unless Ollama and the model are available to that server or you configure a secure, reachable inference backend. Do not expose an unauthenticated Ollama port publicly. For a hackday demo on your own laptop, run Ollama and Streamlit locally.

## Data and limitations

- Analysis and inference are intended to run locally when using the local app configuration.
- History and Saved Results are session-only and may clear when the session restarts. Export important results as JSON.
- Evidence checks confirm whether a quoted string appears in the extracted notice text; this does not guarantee the interpretation is correct. Verify important dates and requirements against the original notice.
- Never upload private or sensitive documents to a public demo without permission.


## Deploying with Ollama Cloud on Streamlit Community Cloud

The local `http://localhost:11434` endpoint works only when running the app on a computer that has Ollama installed. For Streamlit Community Cloud, configure the Ollama Cloud API key in the app's **Manage app → Settings → Secrets** panel (never commit the key to GitHub):

```toml
OLLAMA_API_KEY = "paste-your-Ollama-API-key-here"
OLLAMA_CLOUD_MODEL = "gemma4:31b"
```

The app will use `https://ollama.com/api/chat` when `OLLAMA_API_KEY` is present, and keep using local Ollama otherwise. Check Ollama's current cloud model availability and your account's access before choosing `OLLAMA_CLOUD_MODEL`. Cloud inference sends notice text to Ollama Cloud, so do not submit sensitive personal information.
