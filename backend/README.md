---
title: LiveGuard AI Backend
emoji: 🛡️
colorFrom: indigo
colorTo: purple
sdk: docker
app_port: 7860
pinned: false
---

# LiveGuard AI — Backend

Video forensics API (FastAPI) for the [LiveGuard AI](https://github.com/Sriharsha-Meduri/Liveguard) project.

This folder is deployable as a **Hugging Face Space (Docker SDK)**. When pushed to
a Space, Hugging Face builds the `Dockerfile` and serves the API on port 7860.

## Endpoints
- `GET  /health`
- `POST /analyze/deepfake` — form field `video`
- `POST /analyze/synthetic` — form field `video`
- `POST /analyze/context` — form fields `video`, `claim`

Interactive docs at `/docs`.

## Run locally
```bash
python -m venv .venv && .venv\Scripts\activate   # (Windows)
pip install -r requirements.txt
python app.py    # http://localhost:8000
```

The pretrained models (deepfake, AI-image, CLIP) download on first run.
