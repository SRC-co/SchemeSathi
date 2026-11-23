# SchemeSathi

SchemeSathi is a college MVP for discovering Indian government schemes and providing preliminary, rule-based eligibility guidance.

## Structure

- `frontend/` - React.js + Vite application
- `backend/` - Express.js ES module API
- `database/` - MySQL schema and seed files
- `docs/` - Project documentation

## Prerequisites

- Node.js 20 or newer
- npm
- MySQL 8 or newer

## Setup

### Frontend

```powershell
cd frontend
copy .env.example .env
npm install
npm run dev
```

The frontend runs at `http://localhost:5173`.

### Backend

```powershell
cd backend
copy .env.example .env
npm install
npm run dev
```

The backend runs at `http://localhost:5000`.

### Database

1. Create the database user and credentials listed in `backend/.env`.
2. Run `database/schema.sql` in MySQL.
3. Do not add unverified eligibility records; `database/seed.sql` is intentionally empty.

## API endpoints

- `GET /api/health`
- `GET /api/health/db`

## Data policy

Scheme eligibility is evaluated by a rule-based engine. Missing information does not automatically mean ineligibility. Only verified official government sources should be used for scheme records.
