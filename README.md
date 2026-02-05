# VibeChat — MERN Real-Time Chat Application

VibeChat is a full-stack real-time chat application built using the MERN stack with WebSocket-based communication. It supports instant messaging, live notifications, and persistent chat history with a responsive frontend and scalable backend.

## Project Overview

This application enables users to register, authenticate, and communicate in real time. It combines REST APIs for core data operations with WebSocket connections for instant message delivery and live updates.

The goal of this project was to implement a production-style real-time system using modern JavaScript technologies across the full stack.

## Core Features

* User registration and authentication
* Secure login using JWT
* One-to-one real-time messaging
* WebSocket-based live message delivery
* Real-time notifications
* Persistent chat history stored in MongoDB
* Responsive client interface

## Tech Stack

Frontend:

* React
* Axios
* Socket.io client
* CSS / Tailwind / UI library (update based on what you used)

Backend:

* Node.js
* Express.js
* MongoDB
* Mongoose
* Socket.io
* JSON Web Tokens (JWT)

## System Design Summary

* REST APIs handle authentication and data retrieval
* WebSocket connections handle:

  * Message delivery
  * Presence updates
  * Notifications
* MongoDB stores users, conversations, and messages
* JWT secures protected endpoints
* Socket.io manages bidirectional real-time communication

## Repository Structure (update if needed)

```
client/      React frontend
server/      Express backend
```

## Local Setup Instructions

Clone the repository:

```bash
git clone https://github.com/Iqra-F/VibeChat-MERN-ChatApp.git
cd VibeChat-MERN-ChatApp
```

### Backend Setup

```bash
cd server
npm install
```

Create a `.env` file in the server directory:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

Run the backend:

```bash
npm run dev
```

or

```bash
npm start
```

### Frontend Setup

Open a new terminal:

```bash
cd client
npm install
npm start
```

## Environment Variables

Backend requires:

* PORT — server port
* MONGO_URI — MongoDB connection string
* JWT_SECRET — token signing key
* CLIENT_URL — frontend origin for CORS and sockets

## Available Scripts

Backend:

```bash
npm run dev    Start server with nodemon
npm start      Start server normally
```

Frontend:

```bash
npm start      Run development server
npm build      Create production build
```

## Real-Time Implementation Notes

Socket.io is used to:

* Establish persistent client connections
* Broadcast messages instantly
* Deliver live notifications

Messages are stored in the database and also emitted to connected clients to keep the interface synchronized without refresh.

## Possible Future Improvements

* Group chats
* Read receipts
* Push notifications
* End-to-end encryption

