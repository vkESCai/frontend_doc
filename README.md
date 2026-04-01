<div align="center">

# 🏥 CareConnect

### Full-Stack Doctor Appointment Booking System

*MERN Stack · Role-Based Auth · Real-Time Booking · Dual Payment Gateway*

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=JSON%20web%20tokens&logoColor=white)

**[🔗 Live Demo](https://careconnect-frontend-5eri.onrender.com)** · **[📂 Backend](./backend)** · **[🎨 Frontend](./frontend)** · **[🛠️ Admin](./admin)**

</div>

---

## 📌 Overview

CareConnect is a **production-grade, role-based doctor appointment booking platform** built with the MERN stack. It handles the complete appointment lifecycle — from patient registration and slot booking to doctor schedule management and payment processing — across **three isolated user roles** with secure, JWT-authenticated access.

> Built to simulate real-world healthcare SaaS — not a toy project.

---

## ✨ Features by Role

<details>
<summary><b>👤 Patient Panel</b></summary>

- Register / Login with JWT-secured authentication
- Browse doctors by speciality with real-time availability
- Book appointments — smart slot locking prevents double-booking
- Pay online via **Razorpay** (India) or **Stripe** (global)
- View, manage, and cancel appointments
- Update profile with cloud image upload (Cloudinary)

</details>

<details>
<summary><b>🩺 Doctor Panel</b></summary>

- Secure role-based login (isolated from patient/admin)
- View and manage all assigned appointments
- Mark appointments as completed or cancelled
- Earnings summary and patient statistics dashboard
- Toggle availability on/off with live effect on booking

</details>

<details>
<summary><b>🛠️ Admin Panel</b></summary>

- Admin-only authentication
- Add new doctors with specialty + image upload
- View and manage all doctors and appointments system-wide
- Cancel any appointment from a central dashboard
- Analytics overview: total patients, doctors, appointments

</details>

---

## 🧠 Key Engineering Highlights

| Feature | Details |
|---|---|
| 🔐 **Role-Based Auth** | Three isolated access tiers (Admin / Doctor / Patient) — JWT + bcrypt, enforced via Express middleware |
| 📅 **Smart Slot Engine** | Server-side slot locking prevents race conditions and double-booking |
| 💳 **Dual Payment Gateway** | Razorpay + Stripe in one codebase — currency-aware routing, secure webhook handling |
| ☁️ **Cloud Image Pipeline** | Multer → Cloudinary upload chain — signed URLs, zero local disk dependency in prod |
| ⚡ **RESTful API** | Clean controller → route → model separation, consistent JSON responses across all endpoints |
| 🔄 **Context API** | Lightweight global state for auth, appointments, and doctor data — no Redux overhead |

---

## 🏗️ Tech Stack

**Frontend** — React.js · React Router DOM · Context API · Axios · Tailwind CSS · React Toastify

**Backend** — Node.js · Express.js · MongoDB (Mongoose) · JWT · Bcrypt · Multer

**Integrations** — Razorpay · Stripe · Cloudinary

---

## 📂 Project Structure
```
CareConnect/
│
├── backend/
│   ├── controllers/     ← Route handlers & business logic
│   ├── models/          ← Mongoose schemas (User, Doctor, Appointment)
│   ├── middleware/       ← Auth guards & role-based access control
│   ├── config/          ← DB, Cloudinary, payment config
│   └── server.js
│
├── frontend/            ← Patient-facing React app
│   ├── components/
│   ├── pages/
│   ├── context/
│   └── App.jsx
│
└── admin/               ← Admin + Doctor panels (separate React app)
    ├── components/
    ├── pages/
    └── context/
```

---

## 🔐 Environment Variables

Create `backend/.env`:
```env
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
ADMIN_EMAIL=your_admin_email
ADMIN_PASSWORD=your_admin_password
CLOUDINARY_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_SECRET_KEY=your_secret_key
RAZORPAY_KEY_ID=your_razorpay_key
RAZORPAY_KEY_SECRET=your_razorpay_secret
STRIPE_SECRET_KEY=your_stripe_secret_key
CURRENCY=INR
```

---

## ⚙️ Getting Started
```bash
# 1. Clone
git clone https://github.com/your-username/careconnect.git
cd careconnect

# 2. Install dependencies
cd backend && npm install
cd ../frontend && npm install
cd ../admin && npm install

# 3. Configure
cp backend/.env.example backend/.env
# Fill in your credentials

# 4. Run all services (3 terminals)
cd backend && npm run server
cd frontend && npm run dev
cd admin && npm run dev
```

## 👨‍💻 Author

**Vikash Kumar**
📧 [vikash04escai@gmail.com](mailto:your-email@example.com)
🔗 [GitHub](https://github.com/vkESCai) · [LinkedIn](https://www.linkedin.com/in/vikash-kumar-288548256/)

---

<div align="center">

### ⭐ If this project helped you, please star the repository!

*It helps others discover it and motivates continued development.*

</div>
