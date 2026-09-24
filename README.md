# Feedants – Competition Details

A functional full-stack implementation of the **Competition Details Screen** for the Feedants Full Stack Development Internship Technical Assignment.

## Tech Stack

* **Frontend:** React Native
* **Backend:** Node.js, Express.js
* **Database:** MongoDB, Mongoose
* **Authentication:** JWT

## Features

* Dynamic competition details from backend/database
* Competition lifecycle: Upcoming, Active, Full, and Ended
* User authentication and participation
* Remaining participation spots
* Duplicate participation prevention
* Validation and error handling
* Backend-driven business logic
* Concurrency and data consistency considerations
* Reusable React Native components

## Project Structure

```text
Feedants-Assignment/
├── mobile/     # React Native application
├── server/     # Node.js + Express backend
└── README.md
```

## Setup

### Backend

```bash
cd server
npm install
npm run dev
```

Create a `.env` file:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

### Frontend

```bash
cd mobile
npm install
npx expo start
```

## API

```text
POST /api/auth/register
POST /api/auth/login
GET  /api/auth/me

GET  /api/competitions/:id
GET  /api/competitions/:id/participation
POST /api/competitions/:id/participate
```

## Assumptions & Technical Decisions

* Backend is the source of truth for competition state and participation.
* A user can participate in a competition only once.
* Competition availability depends on dates and participant capacity.
* Business rules and validations are enforced on the backend.
* MongoDB is used for persistent competition and participation data.

## Future Improvements

For production, the application could be extended with stronger monitoring, automated testing, caching, rate limiting, and further performance optimization.
