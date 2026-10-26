NoticeAI Nexus

Run locally on Windows:
  python -m pip install -r requirements.txt
  python -m streamlit run app.py

Requires Ollama running locally with the configured model available (default: gemma4:e2b).
Optional OCR for images/scanned PDFs requires Tesseract OCR installed separately.

Navigation: Home, Analyze Notice, History, Saved Results, Settings.
History and Saved Results are session-only; export important results as JSON.

Important: a GitHub repository link only hosts the source code, not the running Streamlit app. GitHub Pages does not run Python/Streamlit. Cloud hosting also cannot reach Ollama on your personal computer through localhost; use a properly configured backend for cloud inference. Never expose Ollama publicly without appropriate security.
