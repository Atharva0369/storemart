
# StoreMart - Full Stack Starter (Angular + Tailwind + LoopBack4)

This archive contains a ready-to-use starter project for **StoreMart**, an e-commerce
grocery & daily-needs web app.

It includes:
- Frontend: Angular 18.2 + Tailwind CSS (src skeleton, key components)
- Backend: LoopBack-style Node.js app (models, controllers, Stripe payment intent)
- Dockerfiles and docker-compose for local containerized runs
- .env.example and setup instructions

## Quick Start (local, dev)
1. Unzip and cd into the repo:
   ```bash
   unzip storemart.zip -d storemart
   cd storemart
   ```

2. Install backend and frontend dependencies:
   ```bash
   cd backend
   npm install
   cp .env.example .env
   # Edit .env to add STRIPE keys and JWT secret
   npm run migrate
   npm run seed
   npm run start:dev
   # In another terminal:
   cd ../frontend
   npm install
   npm run start
   ```

3. Open the frontend at `http://localhost:4200` (default Angular dev port),
   backend at `http://localhost:3000`.

## Docker (optional)
   ```bash
   docker-compose build
   docker-compose up -d
   ```

## Pushing to GitHub
See the `git-commands.txt` file included for exact commands to create a repo and push.

## Notes
- This starter uses SQLite for easy local development. For production, switch datasource to PostgreSQL or MySQL.
- Stripe keys must be provided in `.env`.
