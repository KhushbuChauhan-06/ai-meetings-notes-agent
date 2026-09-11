 # 🚀 AI Meeting Notes Agent – AI Powered SaaS Platform

<p align="center">
  <img src="https://img.shields.io/badge/MERN-Stack-green?style=for-the-badge&logo=mongodb" />
  <img src="https://img.shields.io/badge/Stripe-Payments-purple?style=for-the-badge&logo=stripe" />
  <img src="https://img.shields.io/badge/Firebase-Auth-orange?style=for-the-badge&logo=firebase" />
  <img src="https://img.shields.io/badge/Google-Gemini-AI-blue?style=for-the-badge&logo=google" />
  <img src="https://img.shields.io/badge/JWT-Secured-yellow?style=for-the-badge" />
</p>

---

## 🌟 Overview

**AI Meeting Notes Agent** is a production-style AI-powered SaaS web application that allows users to generate smart exam notes using AI and purchase usage credits securely via Stripe.

This project demonstrates real-world backend architecture including secure authentication, payment gateway integration, webhook verification, and a credit-based transaction system.

---

## 🎯 Key Highlights

✔ Implemented secure **Google OAuth authentication** using Firebase  
✔ Designed **JWT-protected backend architecture**  
✔ Integrated **Stripe Checkout with webhook verification**  
✔ Built a **credit-based payment system** using Stripe metadata validation  
✔ Integrated **Google Gemini AI API** for intelligent note generation  
✔ Connected **MongoDB Atlas** for scalable cloud database storage  
✔ Managed environment variables securely  
✔ Designed SaaS-style backend architecture  

This reflects real startup-level SaaS backend implementation.

---

## 🏗 Tech Stack

### 🔹 Frontend
- React (Vite)
- Firebase Authentication
- Axios

### 🔹 Backend
- Node.js
- Express.js
- MongoDB Atlas (Mongoose ODM)
- JWT Authentication
- Stripe API + Webhooks
- Google Gemini API

---

## 📂 Project Structure

```
AI Meeting Notes Agent/
│
├── client/          → React Frontend
├── server/          → Node + Express Backend
├── README.md
└── .gitignore
```

---

## ⚙️ Local Setup Guide

### 1️⃣ Clone Repository

```bash
git clone https://github.com/rajratan-rajput/ExamNotesAI.git
cd ExamNotesAI
```

---

### 2️⃣ Backend Setup

```bash
cd server
npm install
```

Create `server/.env`

```
PORT=8000
MONGODB_URL=your_mongodb_connection_string
JWT_SECRET=your_secret_key
GEMINI_API_KEY=your_gemini_api_key
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...
CLIENT_URL=http://localhost:5173
```

Run backend:

```bash
npm run dev
```

---

### 3️⃣ Frontend Setup

```bash
cd client
npm install
```

Create `client/.env`

```
VITE_FIREBASE_APIKEY=your_firebase_api_key
```

Run frontend:

```bash
npm run dev
```

---

## 💳 Stripe Webhook Setup (Local Testing)

Login Stripe CLI:

```bash
stripe login
```

Start webhook listener:

```bash
stripe listen --forward-to localhost:8000/api/credits/webhook
```

Copy the `whsec_` key into backend `.env`.

---

## 🧪 Stripe Test Payment Card

```
4242 4242 4242 4242
Any future date
Any 3-digit CVC
Any 5-digit ZIP
```

---

## 🚀 Deployment Guide

### 🔹 Backend Deployment (Render / Railway)

1. Push repository to GitHub  
2. Connect repository to Render  
3. Add environment variables in dashboard  
4. Build command:

```
npm install
```

5. Start command:

```
node index.js
```

---

### 🔹 Frontend Deployment (Vercel / Netlify)

1. Connect GitHub repository  
2. Build command:

```
npm run build
```

3. Output directory:

```
dist
```

4. Add environment variable:

```
VITE_FIREBASE_APIKEY
```

---

## 🔐 Security Features

- Stripe webhook signature verification
- JWT-protected routes
- Metadata-based secure credit allocation
- Environment-based secret management
- No sensitive keys exposed in frontend

---

## 📈 Future Improvements

- Idempotent webhook handling
- Payment transaction history logging
- Subscription-based billing
- Role-based access control
- Production Stripe live mode integration
- Cloud deployment optimization

---

## 👨‍💻 Author

**Khushbu Chauhan**  
GitHub: https://github.com/KhushbuChauhan-06 

Full Stack Developer | MERN Stack | Backend Engineering  

---
 

## ⭐ If you found this project valuable, consider giving it a star!
