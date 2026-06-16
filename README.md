# MoneyMitra.ai
Full-stack expense tracking app with JWT auth, budget management &amp; category tracking. Built with Node.js, Express, MongoDB &amp; Tailwind CSS.
A production-ready web app for tracking expenses, managing budgets, and monitoring financial health — built with a REST API backend and a responsive, dark-mode-ready frontend.

> **Stack:** Node.js · Express.js · MongoDB · JWT Auth · Tailwind CSS · Vanilla JS

---

## 🖥️ Features

| Feature | Details |
|---|---|
| 🔐 Authentication | Secure register/login with JWT + bcrypt password hashing |
| 💸 Expense Management | Add, edit, delete expenses with description, amount, category, payment method |
| 📁 Custom Categories | Create and color-code your own spending categories |
| 📊 Dashboard | Spending overview with stats, breakdowns, and date-range filtering |
| 🌙 Dark / Light Mode | Auto theme switching with localStorage persistence |
| 📱 Responsive Design | Works on desktop, tablet, and mobile |
| 💱 Currency Formatting | Indian Rupee (₹) formatting, customizable |

---

## 🛠️ Tech Stack

**Backend**
- Node.js + Express.js — REST API
- MongoDB + Mongoose — Database & ODM
- JWT (`jsonwebtoken`) — Stateless authentication
- bcryptjs — Password hashing
- CORS enabled for frontend-backend separation

**Frontend**
- HTML5 + Tailwind CSS — Responsive UI
- Vanilla JavaScript — Client-side API interactions
- Google Material Symbols — Icons
- localStorage — Token & session management

---

## 📂 Project Structure

```
moneymitra/
├── backend/
│   ├── server.js              # Express entry point
│   ├── models/
│   │   ├── User.js            # User schema
│   │   ├── Expense.js         # Expense schema
│   │   └── Category.js        # Category schema
│   ├── routes/
│   │   ├── auth.js            # Auth endpoints
│   │   ├── expenses.js        # Expense CRUD
│   │   └── categories.js      # Category CRUD
│   └── middleware/
│       └── auth.js            # JWT verification middleware
├── js/
│   ├── api.js                 # Centralised API client
│   └── app.js                 # Shared app logic
├── login.html                 # Auth page
├── dashboard.html             # Main dashboard
├── expenses.html              # Expense management
└── categories.html            # Category management
```

---

## 🔗 API Reference

### Auth
```
POST /api/auth/register    Register new user
POST /api/auth/login       Login, returns JWT
GET  /api/auth/me          Get current user (protected)
```

### Expenses
```
POST   /api/expenses              Create expense
GET    /api/expenses              Get all (query: startDate, endDate, category)
GET    /api/expenses/:id          Get single expense
PUT    /api/expenses/:id          Update expense
DELETE /api/expenses/:id          Delete expense
```

### Categories
```
POST   /api/categories            Create category
GET    /api/categories            Get all
PUT    /api/categories/:id        Update
DELETE /api/categories/:id        Delete
```

---

## ⚙️ Setup & Run

### Prerequisites
- Node.js v14+
- MongoDB (local or [MongoDB Atlas](https://www.mongodb.com/cloud/atlas))

### 1. Clone & install
```bash
git clone https://github.com/nimishikhar40/moneymitra.git
cd moneymitra/backend
npm install
```

### 2. Configure environment
```bash
cp .env.example .env
```
```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/moneymitra
JWT_SECRET=your_secret_key
NODE_ENV=development
```

### 3. Start backend
```bash
npm run dev
```

### 4. Serve frontend
```bash
# From project root
python -m http.server 3000
# Open http://localhost:3000/login.html
```

---

## 🚀 Deployment

| Layer | Recommended Options |
|---|---|
| Backend | Railway · Render · Fly.io |
| Frontend | Vercel · Netlify · GitHub Pages |
| Database | MongoDB Atlas (free tier) |

---

## 🗺️ Roadmap

- [ ] Budget limits & overspend alerts
- [ ] Advanced charts & analytics (Chart.js)
- [ ] Recurring expense automation
- [ ] CSV / PDF export
- [ ] Receipt OCR scanning
- [ ] AI-powered expense categorization
- [ ] Multi-currency support
- [ ] Mobile app (React Native)

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

<p align="center">Built by <a href="https://github.com/nimishikhar40">Nimish Ikhar</a> · <a href="https://linkedin.com/in/nimish-ikhar-a36242255">LinkedIn</a></p>
