# Birma Audit — Full Stack

A working Birma Enterprises operational audit application with a responsive frontend and FastAPI + SQLite backend.

## Features
- Dashboard with audit KPIs
- Create audits for efficiency, quality and safety
- Upload evidence files (images/video/PDF/spreadsheets)
- SQLite persistence
- Audit search and deletion
- REST API
- PWA manifest
- Docker deployment
- HTTPS/security header configs

## Run locally

### Windows PowerShell
```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
uvicorn backend.main:app --reload
```
Open http://127.0.0.1:8000

### Docker
```bash
docker compose up --build
```
Open http://localhost:8000

## API
- GET `/api/health`
- GET `/api/dashboard`
- GET `/api/audits`
- POST `/api/audits`
- GET `/api/audits/{id}`
- DELETE `/api/audits/{id}`
- POST `/api/audits/{id}/upload`

## Production next steps
Use PostgreSQL instead of SQLite for multi-user production, add JWT/OAuth authentication, object storage for evidence, background video/YOLO processing, role-based access, report PDF generation and an admin panel.
