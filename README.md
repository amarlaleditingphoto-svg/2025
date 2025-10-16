
# hiclip-clone

HiClip-style local-first MVP — React frontend + Node/Express backend skeleton.
This repository is a starter template for building an AI-powered short-clip generator.
It uses local-first stubs so you can run & test without cloud APIs.

## What is included
- `frontend/` — Vite + React starter (paste into a Vite project or run `npm install` inside)
- `backend/` — Express server with endpoints:
  - `POST /api/upload` (multipart file upload)
  - `POST /api/suggest` (clip-suggestion stub)
  - `POST /api/caption` (captioning stub)
  - `POST /api/trim` (uses ffmpeg if available)
- `docker-compose.yml` — placeholder to run backend + ffmpeg service
- `.github/workflows/ci.yml` — basic Node CI workflow

## Quick start (local)
1. Backend:
   ```bash
   cd backend
   npm install
   # (optional) install ffmpeg on your system if you want trimming: https://ffmpeg.org/download.html
   node index.js
   ```
2. Frontend:
   ```bash
   cd frontend
   npm install
   npm run dev
   ```

## Notes
- This is a skeleton. AI services (Whisper, highlight-detection) are stubs and must be integrated separately.
- For production-ready handling of video trimming and large uploads use S3 + worker queues (Bull / RabbitMQ).
