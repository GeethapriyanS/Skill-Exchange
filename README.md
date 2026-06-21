# Skill Exchange Web

## 🌐 Live Demo: [skill-exchange-self.vercel.app](https://skill-exchange-self.vercel.app)

A full-stack peer-to-peer skill exchange platform built with React, Express, Node.js, MongoDB, and Socket.IO.

## Project Overview

This repository contains two main applications:

- `skill-exchange-backend`: Express API server with MongoDB, JWT authentication, real-time chat via Socket.IO, and exchange/session management.
- `skill-exchange-frontend`: React web client for browsing skills, sending requests, chatting, scheduling sessions, and reviewing partners.

## Features

- User registration and login with JWT authentication
- Skill listings and search
- Exchange request workflow with accept/reject
- Scheduled sessions with meeting links
- Real-time chat via Socket.IO
- Review system for completed exchanges
- API-driven React frontend

## Repo Structure

```
skillexchange-web/
├── README.md
├── skill-exchange-backend/
│   ├── server.js
│   ├── config/db.js
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── sockets/
│   ├── utils/
│   ├── middleware/
│   ├── package.json
│   └── README.md
└── skill-exchange-frontend/
    ├── public/
    ├── src/
    ├── package.json
    └── README.md
```

## Prerequisites

- Node.js v16 or later
- npm
- MongoDB Atlas account or local MongoDB instance

## Setup

### Backend

```bash
cd skill-exchange-backend
npm install
```

Create a `.env` file in `skill-exchange-backend` and configure:

```env
PORT=5000
MONGO_URI=mongodb+srv://<username>:<password>@cluster0.oftdhpb.mongodb.net/skill_exchange?retryWrites=true&w=majority
JWT_SECRET=your_super_secret_jwt_key_here
JWT_EXPIRE=7d
```

> If your Atlas password contains special characters such as `@`, encode them in the URI (for example `@` becomes `%40`).

### Frontend

```bash
cd skill-exchange-frontend
npm install
```

## Running the App

### Start Backend

```bash
cd skill-exchange-backend
npm run dev
```

### Start Frontend

```bash
cd skill-exchange-frontend
npm start
```

The frontend should launch at `http://localhost:3000` and the backend API runs at `http://localhost:5000`.

## Notes

- The backend uses `skill-exchange-backend/config/db.js` to connect to MongoDB via `process.env.MONGO_URI`.
- The frontend connects to the backend API through services defined in `skill-exchange-frontend/src/services/api.js`.
- For local development, you can replace the Atlas URI with a local MongoDB URI:

```env
MONGO_URI=mongodb://localhost:27017/skill_exchange
```

## More Documentation

- `skill-exchange-backend/README.md` — detailed backend setup and API reference
- `skill-exchange-frontend/README.md` — frontend details and project notes

## License

This project is open source and available to use and extend for learning and development.

Developd by Geethapriyan S