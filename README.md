<div align="center">

# ✈️ TravelPro

### Full-Stack Travel Booking Platform

**React · Express · MongoDB · Node.js**

[![Node.js](https://img.shields.io/badge/Node.js-v14+-339933?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=flat-square&logo=react&logoColor=black)](https://reactjs.org)
[![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-47A248?style=flat-square&logo=mongodb&logoColor=white)](https://mongodb.com)
[![Express](https://img.shields.io/badge/Express-4.x-000000?style=flat-square&logo=express&logoColor=white)](https://expressjs.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)

</div>

---

## 🌍 Overview

TravelPro is a modern, full-stack travel booking application that connects travelers with premium hotels and expert travel consultants. Built with the MERN stack, it features a clean React frontend, a robust Express API, and a MongoDB database — all wired together for a seamless booking experience.

> Book hotels, meet your travel experts, and manage appointments — all in one place.

---

## ✨ Features

| Area | What's included |
|------|----------------|
| 🏠 **Home** | Hero section, feature highlights, and call-to-action |
| 🏨 **Booking** | Hotel listings with amenities, pricing & appointment form |
| 👥 **About** | Company story, mission, values & expert staff profiles |
| 🔌 **REST API** | Staff, Hotels, and Appointments endpoints with full validation |
| 📱 **Responsive** | Mobile-first layout using CSS Grid & Flexbox |
| 🚧 **404 Page** | Custom not-found page with helpful navigation |

---

## 📁 Project Structure

```
TravelPro/
├── client/                   # ⚛️  React frontend
│   ├── public/
│   └── src/
│       ├── components/       # Reusable UI components
│       ├── pages/            # Route-level page components
│       ├── App.js
│       └── index.js
│
├── models/                   # 🗄️  Mongoose schemas
│   ├── Staff.js
│   ├── Hotel.js
│   └── Appointment.js
│
├── routes/                   # 🔌  Express route handlers
│   ├── staff.js
│   ├── hotels.js
│   └── appointments.js
│
├── server.js                 # 🚀  Express entry point
├── seedData.js               # 🌱  Database seed script
└── package.json
```

---

## 🛠️ Getting Started

### Prerequisites

- **Node.js** v14+
- **MongoDB** (local or [MongoDB Atlas](https://cloud.mongodb.com))
- **npm** or **yarn**

### 1 — Clone & Install

```bash
# Clone the repo
git clone <repository-url>
cd mern-stack-task

# Install backend dependencies
npm install

# Install frontend dependencies
cd client && npm install && cd ..
```

### 2 — Configure Environment

Create a `.env` file in the project root:

```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/mern-task
NODE_ENV=development
```

### 3 — Seed the Database

```bash
# Start MongoDB (if running locally)
mongod

# Populate with sample data
npm run seed
```

This seeds **4 expert staff members**, **6 premium hotels**, and sample appointments.

### 4 — Run in Development

```bash
# Terminal 1 — backend on :5000
npm run server

# Terminal 2 — frontend on :3000
npm run client
```

---

## 🔌 API Reference

### Staff

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/staff` | List all staff members |
| `GET` | `/api/staff/:id` | Get a specific staff member |

### Hotels

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/hotels` | List all hotels |
| `GET` | `/api/hotels/:id` | Get a specific hotel |

### Appointments

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/api/appointments` | Create a new booking |
| `GET` | `/api/appointments` | List all bookings (admin) |

#### Example — Create Booking

```json
POST /api/appointments

{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john@example.com",
  "phone": "+1234567890",
  "hotelId": "<hotel_id>",
  "checkInDate": "2024-02-15",
  "checkOutDate": "2024-02-20",
  "guests": 2,
  "specialRequests": "Vegetarian meals preferred"
}
```

---

## 🚀 Deployment

### Heroku

```bash
# Create and configure app
heroku create your-app-name
heroku config:set MONGODB_URI=<your_connection_string>
heroku config:set NODE_ENV=production

# Deploy
git push heroku main

# Seed production DB
heroku run npm run seed
```

### Other Platforms

TravelPro is platform-agnostic — deploy anywhere Node.js runs:

[![Deploy to Vercel](https://img.shields.io/badge/Vercel-Deploy-000?style=flat-square&logo=vercel)](https://vercel.com)
[![Deploy to Render](https://img.shields.io/badge/Render-Deploy-46E3B7?style=flat-square&logo=render)](https://render.com)
[![AWS](https://img.shields.io/badge/AWS-Deploy-FF9900?style=flat-square&logo=amazon-aws)](https://aws.amazon.com)

---

## 🧪 Manual Testing Checklist

- [ ] Visit `/about` — staff cards load from API
- [ ] Visit `/booking` — hotel list populates, form submits successfully
- [ ] Resize browser — layout stays clean at all breakpoints
- [ ] Visit `/this-does-not-exist` — 404 page appears

---

## 🧰 Tech Stack

**Frontend** — React.js · React Router · Axios · CSS3 (Grid + Flexbox)

**Backend** — Node.js · Express.js · MongoDB · Mongoose · CORS

**Dev Tools** — Nodemon · dotenv

---

## 🤝 Contributing

```bash
# Create a feature branch
git checkout -b feature/your-feature-name

# Commit with a clear message
git commit -m "feat: add hotel filtering by price range"

# Open a Pull Request
git push origin feature/your-feature-name
```

Please follow [Conventional Commits](https://www.conventionalcommits.org) for commit messages.

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for details.

---

<div align="center">
  Made with ❤️ · <a href="#-travelpro">Back to top ↑</a>
</div>
