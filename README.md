# 💸 MERN Expense Tracker

A clean, responsive expense tracker built with **MongoDB + Express + React + Node**. Track income/expense, see running balance, and manage your transactions with simple auth.

<p align="center">
  <img src="https://drive.google.com/file/d/1yX4269p3gkZ8_MBHl1zowm6cGYWubskl/view?usp=sharing" alt="Login" width="45%"/>
  <img src="assets/screenshots/signup.jpg" alt="Signup" width="45%"/>
  <br/>
  <img src="assets/screenshots/toast-success.jpg" alt="Success toast on add expense" width="45%"/>
  <img src="assets/screenshots/list.jpg" alt="Transactions list with income/expense styling" width="45%"/>
  <br/>
  <img src="assets/screenshots/backend-console.jpg" alt="Node server with Mongo connected" width="45%"/>
  <img src="assets/screenshots/frontend-compiled.jpg" alt="Frontend compiled successfully" width="45%"/>
</p>


- **Auth + Protected UI** (Login/Signup flow).
- **State management with React Context** and modular components.
- **REST API** (Node/Express) + **MongoDB (Mongoose)** for persistence.
- **UX touches**: toast notifications, input validation, responsive design.
- Clean **folder structure**, simple **API layer** with Axios, and environment-based config.

## 🧱 Tech Stack
**Frontend:** React, Context API, Axios, CSS  
**Backend:** Node.js, Express.js  
**Database:** MongoDB (Mongoose)  
**Tooling:** Nodemon, Concurrently, dotenv, CORS

## 📦 Project Structure
```
root/
├─ backend/
│  ├─ src/ (controllers, routes, models, middleware)
│  └─ .env.example
├─ frontend/
│  ├─ src/ (components, context, services)
│  └─ .env.example
└─ assets/screenshots/ (images used in README)
```

## 🛠️ Setup (Step‑by‑Step)
1. **Clone & install**
   ```bash
   git clone <your-repo-url>
   cd <repo>
   npm install --prefix backend
   npm install --prefix frontend
   ```
2. **Environment variables**
   - `backend/.env`
     ```env
     PORT=8080
     MONGO_URI=mongodb://localhost:27017/expense_tracker
     JWT_SECRET=supersecret
     ```
   - `frontend/.env`
     ```env
     REACT_APP_API_URL=http://localhost:8080
     ```
3. **Run dev servers**
   ```bash
   # in two terminals
   npm run dev --prefix backend
   npm start --prefix frontend
   # or with concurrently (optional)
   # npm run dev:all
   ```

## 🔌 Core Endpoints
- `POST /api/auth/register` – create user  
- `POST /api/auth/login` – login & issue token  
- `GET /api/transactions` – list all (for user)  
- `POST /api/transactions` – add income/expense  
- `DELETE /api/transactions/:id` – remove item

## 📝 Highlights to mention in your resume/README
- Implemented **JWT auth** and protected routes.
- Designed **transaction model** with amount sign (positive=income, negative=expense) and server-side validation.
- Built a **Context-based store** and a lightweight **service layer** wrapping Axios.
- Added **toast feedback** and **accessible form** patterns.
- Wrote clear **API docs**, **.env templates**, and screenshots to improve DX.

## 🛣️ Future Enhancements
- Category-wise charts & monthly summaries
- CSV export / import
- Pagination & search
- Unit tests for reducers/routes

---

> If you find this useful, consider ⭐ the repo!
