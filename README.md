

## Project Overview
Full-stack application using React and Python FastAPI.

## Technologies
- React
- Vite
- Python
- FastAPI
- Uvicorn
- Black
- Ruff
- Oxlint
- Git

## Frontend Setup
cd frontend
npm install
npm run dev

## Backend Setup
cd backend
py -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
uvicorn app.main:app --reload

## API Documentation
http://127.0.0.1:8000/docs
