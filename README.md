# 🎓 Campus Events Platform

A full-stack web application for booking seminars, workshops, and competitions.

---

## 📁 Folder Structure

```
seminar-booking-app/
│
├── START_BACKEND.bat       ← Double-click to start the backend server
├── START_FRONTEND.bat      ← Double-click to start the frontend
│
├── server/                 ← Node.js + Express Backend
│   ├── index.js            ← API server (port 3001)
│   ├── db.json             ← JSON database (all data saved here)
│   └── package.json
│
└── src/                    ← React Frontend
    ├── App.jsx             ← Main router
    ├── context/
    │   ├── AuthContext.jsx ← Login / role management
    │   └── EventsContext.jsx ← API calls to backend
    ├── pages/
    │   ├── LoginPage.jsx          ← Role selector + login form
    │   ├── student/
    │   │   ├── StudentLayout.jsx
    │   │   ├── HomePage.jsx       ← Scores + ad banner
    │   │   ├── EventListPage.jsx  ← Seminars / Workshops / Competitions
    │   │   └── ProfilePage.jsx    ← Booking history
    │   └── admin/
    │       ├── AdminLayout.jsx
    │       ├── AdminEventsPage.jsx      ← View all events (table)
    │       ├── AdminCreateEventPage.jsx ← Submit new event (form)
    │       └── AdminProfilePage.jsx
    └── components/
        └── BookingModal.jsx ← Book ticket modal with validation
```

---

## 🚀 How to Run

### Step 1 — Start the Backend
Double-click **`START_BACKEND.bat`**  
OR open a terminal and run:
```
cd server
node index.js
```
Backend runs at: **http://localhost:3001**

### Step 2 — Start the Frontend
Double-click **`START_FRONTEND.bat`**  
OR open another terminal and run:
```
npm run dev
```
Frontend runs at: **http://localhost:5174**

---

## 🔐 Login Credentials

| Role | Username | Password |
|------|----------|----------|
| Student | `student1` | `pass123` |
| Student | `student2` | `pass123` |
| Admin | `admin1` | `admin123` |
| Admin | `admin2` | `admin123` |

---

## 🌐 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/events` | Get all events |
| POST | `/api/events` | Create new event |
| DELETE | `/api/events/:id` | Delete an event |
| GET | `/api/bookings` | Get all bookings |
| POST | `/api/bookings` | Book an event |

---

## 💾 Data Persistence
All data is saved in **`server/db.json`** — events and bookings survive server restarts.
