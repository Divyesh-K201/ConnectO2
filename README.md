# ConnectO - Premium Freelance Platform

ConnectO is a full-stack platform connecting TaskMasters (Clients) with SoloPros (Freelancers). It features a secure checkpoint payment system, strict communication filtering, and a gamified experience.

## 🚀 Tech Stack

- **Frontend**: React.js, Tailwind CSS (Premium Config), Framer Motion
- **Backend**: Node.js, Express.js
- **Database**: PostgreSQL with Prisma ORM
- **Auth**: JWT with Role-Based Access Control (RBAC)
- **Deployment**: Vercel (Client) + Railway/Render (Server)

## 📂 Project Structure

```
connect O/
├── client/                 # React Frontend
│   ├── src/
│   │   ├── api/           # Axios config
│   │   ├── components/    # Reusable UI components
│   │   ├── context/       # Auth Context
│   │   ├── pages/         # Application Views
│   │   ├── index.css      # Tailwind & Custom Styles
│   │   └── App.jsx        # Routing Logic
│   └── tailwind.config.js # Custom Theme
│
├── server/                 # Node.js Backend
│   ├── controllers/       # Business Logic
│   ├── middleware/        # Auth & Role Checks
│   ├── prisma/            # Database Schema
│   ├── routes/            # API Endpoints
│   ├── utils/             # Helper functions (Regex filters)
│   ├── index.js           # Server Entry Point
│   └── package.json
```

## 🛠️ Setup & Run Locally

### 1. Database Setup
Ensure you have PostgreSQL installed. Update `server/.env` (copy from `.env.example`) with your `DATABASE_URL`.

### 2. Backend Setup
```bash
cd server
npm install
npx prisma generate
npx prisma db push  # Push schema to DB
npm run dev
```
Server will start on `http://localhost:5000`.

### 3. Frontend Setup
```bash
cd client
npm install
npm run dev
```
Client will start on `http://localhost:5173` (Vite default).

## ✨ Key Features Implemented

1.  **Auth System**: Login/Register with JWT. Role selection (TaskMaster/SoloPro).
2.  **Strict Communication Filtering**: Messages containing emails or phone numbers are blocked.
3.  **Project Life Cycle**:
    -   TaskMaster posts project (Payment locked).
    -   SoloPro applies.
    -   TaskMaster accepts (Status updates to IN_PROGRESS).
4.  **Gamification**: EXP and Credit Score tracking (Backend models ready).
5.  **Premium UI**: Glassmorphism design, smooth animations, and responsive layout.

## 🚀 Deployment

- **Frontend**: Connect the `client` folder to **Vercel**.
- **Backend**: Connect the `server` folder to **Railway** or **Render**. Set `DATABASE_URL` and `JWT_SECRET` in environment variables.
