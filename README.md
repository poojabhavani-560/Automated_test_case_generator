# TestForge AI — Automated Test Case Generator

A presentation-ready full-stack project for AI-assisted web test design.

## Highlights
- React + Vite professional QA dashboard
- FastAPI backend
- Website DOM/form/link/button analyzer
- Optional OpenAI generation
- Strong rule-based fallback when no API key is available
- Positive, negative, boundary, usability and security-minded cases
- Playwright browser execution adapter
- CSV export
- Typed Pydantic API models
- Responsive UI
- Health endpoint and clean modular architecture

## Requirements
Python 3.10+, Node.js 18+, npm.

## Run backend
```bash
cd backend
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
python -m playwright install chromium
# copy ../.env.example to .env
uvicorn main:app --reload --port 8000
```

## Run frontend
```bash
cd frontend
npm install
npm run dev
```
Open `http://localhost:5173`.

## Optional AI
Put an OpenAI API key in `backend/.env`. Without it, the built-in QA generator works automatically.

## API
- `GET /api/health`
- `POST /api/generate` with `{"url":"https://example.com"}`
- `POST /api/run` with a URL and test-case object

## Presentation flow
1. Start both services.
2. Enter a website URL.
3. Generate test cases.
4. Explain DOM analysis → AI/rule generation → structured cases.
5. Export CSV.
6. Run a case and show the execution report.
7. Explain future enhancements: locator generation, assertions, screenshots, JUnit/PDF reports, Jira/TestRail and CI/CD.

## Safety
Only test websites you own or are explicitly authorized to test.
