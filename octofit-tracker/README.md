# 🐙 OctoFit Tracker

A modern multi-tier fitness tracking application built with GitHub Copilot Agent Mode.

## Architecture

```
octofit-tracker/
├── frontend/          # React 19 + Vite (Port 5173)
├── backend/           # Node.js + Express + TypeScript (Port 8000)
└── README.md          # This file
```

## Prerequisites

- Node.js 18+
- npm or yarn
- MongoDB running on port 27017

## Frontend Setup

Navigate to the `frontend` directory:

```bash
cd octofit-tracker/frontend
npm install
npm run dev
```

The frontend will be available at `http://localhost:5173`

**Features:**
- React 19 with Vite for fast development
- TypeScript support
- ESLint configuration
- Proxy to backend API at `/api`

## Backend Setup

Navigate to the `backend` directory:

```bash
cd octofit-tracker/backend
npm install
cp .env.example .env
npm run dev
```

The backend API will be available at `http://localhost:8000`

**Features:**
- Express.js server
- MongoDB integration with Mongoose
- CORS enabled
- TypeScript support
- ESLint configuration
- Health check endpoint: `GET /health`

## MongoDB Setup

Ensure MongoDB is running on port 27017:

```bash
# macOS with Homebrew
brew services start mongodb-community

# Docker
docker run -d -p 27017:27017 --name mongodb mongo
```

## API Endpoints

- `GET /health` - Server health check

## Development

### Frontend
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

### Backend
- `npm run dev` - Start development server with ts-node
- `npm run build` - Compile TypeScript
- `npm start` - Run compiled JavaScript
- `npm run lint` - Run ESLint

## Environment Variables

Backend environment variables (`.env`):
```
PORT=8000
MONGODB_URI=mongodb://localhost:27017/octofit-tracker
NODE_ENV=development
```

## Technologies Used

- **Frontend:** React 19, Vite, TypeScript
- **Backend:** Express.js, TypeScript, MongoDB, Mongoose
- **Tools:** ESLint, Vite, ts-node

## License

MIT
