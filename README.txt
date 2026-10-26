NoticeAI Nexus

Run locally on Windows:
  python -m pip install -r requirements.txt
  python -m streamlit run app.py

Requires Ollama running locally with the configured model available (default: gemma4:e2b).
Optional OCR for images/scanned PDFs requires Tesseract OCR installed separately.

Navigation: Home, Analyze Notice, History, Saved Results, Settings.
History and Saved Results are session-only; export important results as JSON.

Important: a GitHub repository link only hosts the source code, not the running Streamlit app. GitHub Pages does not run Python/Streamlit. Cloud hosting also cannot reach Ollama on your personal computer through localhost; use a properly configured backend for cloud inference. Never expose Ollama publicly without appropriate security.


## Deploying with Ollama Cloud on Streamlit Community Cloud

The local `http://localhost:11434` endpoint works only when running the app on a computer that has Ollama installed. For Streamlit Community Cloud, configure the Ollama Cloud API key in the app's **Manage app → Settings → Secrets** panel (never commit the key to GitHub):

```toml
OLLAMA_API_KEY = "paste-your-Ollama-API-key-here"
OLLAMA_CLOUD_MODEL = "gemma4:31b"
```

The app will use `https://ollama.com/api/chat` when `OLLAMA_API_KEY` is present, and keep using local Ollama otherwise. Check Ollama's current cloud model availability and your account's access before choosing `OLLAMA_CLOUD_MODEL`. Cloud inference sends notice text to Ollama Cloud, so do not submit sensitive personal information.
