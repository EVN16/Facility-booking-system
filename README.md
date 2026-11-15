# Facility Booking System

A modern web application for booking facilities such as sports fields, meeting rooms, and more. Built with **React** (front-end) and **Laravel** (back-end), featuring a *Glassmorphism*-style interface, an admin management dashboard, and financial report exports.

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

## 🚀 Features

### 👥 For Users
- **Facility Catalog** — Browse facilities with prices, location details, and capacity.
- **Interactive Booking** — Book time slots by dragging on an interactive calendar (`FullCalendar`).
- **Time Validation** — Past times can't be selected, and overlapping bookings are blocked.
- **Booking History** — View your bookings and their statuses in a dedicated panel.

### 🛡️ For Admins
- **Dashboard Overview** — Key metrics: total revenue, total bookings, available facilities, and pending queue.
- **Facility Management (CRUD)** — Add, edit, or remove facilities and their details.
- **Booking Management** — Approve or reject incoming bookings.
- **Reports & PDF Export** — Interactive monthly revenue charts (`Recharts`) and transaction exports to PDF (`domPDF`).

## 🛠️ Tech Stack

| Layer | Technologies |
| --- | --- |
| Front-End | React (Vite), Tailwind CSS, Zustand, React Query, FullCalendar, Recharts, Lucide React |
| Back-End | Laravel 11, MySQL, Laravel Sanctum (token auth), domPDF |

## ⚙️ Getting Started

### Prerequisites
- PHP 8.2+ with Composer
- Node.js (npm)
- MySQL (e.g. via XAMPP or Laragon)

The project has two directories: `Front-End` and `Back-End`.

### 1. Back-End Setup (Laravel)

```bash
cd Back-End

# Install PHP dependencies
composer install

# Create the environment file (copy from the example)
cp .env.example .env

# Start your database server (e.g. enable MySQL in XAMPP/Laragon)
# Set your database name in .env (e.g. DB_DATABASE=sistem_booking)

# Create the tables and seed initial data
php artisan migrate --seed

# Generate the application key
php artisan key:generate

# Run the server
php artisan serve
```

*The API server runs at `http://127.0.0.1:8000` by default.*

### 2. Front-End Setup (React/Vite)

Open a new terminal window, then run:

```bash
cd Front-End

# Install JavaScript dependencies
npm install

# Run the development server
npm run dev
```

*The app will open in your browser, usually at `http://localhost:5173`.*

## 🔑 Demo Accounts

Seeded via `php artisan migrate --seed`:

| Role | Email | Password |
| --- | --- | --- |
| Admin | admin@admin.com | `password` |
| User | user@user.com | `password` |

## 📁 Project Structure

```
facility-booking-system/
├── Back-End/   # Laravel 11 REST API
└── Front-End/  # React + Vite app
```

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

*Built to make facility and schedule management easy and fully digital.*
