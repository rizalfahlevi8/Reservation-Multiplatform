# Reservation System Multiplatform

![alt text](https://github.com/rizalfahlevi8/Reservation-Multiplatform/blob/main/mockup.png?raw=true)

A complete **Reservation System** built as a **single repository (monorepo)** that contains:

- 📱 **Mobile App (Customer)** built with **Flutter**
- 🌐 **Web Platform (Admin & Employee)** built with **Laravel**

This system uses a salon reservation case study that allows customers to book appointments at the salon easily, while also allowing administrators and employees to manage services, schedules, and reservations efficiently.

---

## 🛠️ Use Case Diagram

![alt text](https://github.com/rizalfahlevi8/Reservation-Multiplatform/blob/main/use-case-diagram.png?raw=true)

## 🧩 System Architecture

```
root-repo/
├── mobile-app/        # Flutter mobile & multiplatform app (Customer)
├── web-admin/         # Laravel web app (Admin & Employee)
├── README.md          # Main documentation (this file)
```

---

# 📱 Mobile Application — Customer App

A cross-platform mobile application that allows customers to browse services, book appointments, and manage reservations.

## 🚀 Features

- User Authentication (Login & Register)
- Service Browsing
- Appointment Booking with Calendar
- Reservation Management (View / Cancel)
- User Profile Management
- Cross-Platform Support

## 🛠️ Tech Stack

- **Flutter**
- **Dart** (^3.5.3)

### Key Dependencies

- http (^1.2.2)
- shared_preferences (^2.2.3)
- table_calendar (^3.1.2)
- image_picker (^1.1.2)
- font_awesome_flutter (^10.7.0)
- form_validation (^3.2.0)
- http_parser (^4.1.2)

## 📁 Project Structure

```
mobil/lib/
├── components/      # Reusable UI components
├── model/           # Data models
├── screen/          # Application screens
├── services/        # API & business logic
├── utils/           # Utilities & helpers
├── main.dart        # App entry point
└── main_layout.dart # Main layout
```

## ⚙️ Installation (Mobile App)

```bash
cd mobile
flutter pub get
flutter run
```

Configure API endpoint in `config.json` before running the app.

## 📦 Supported Platforms

- Android
- iOS
- Web
- Windows
- macOS
- Linux

---

# 🌐 Web Application — Admin & Employee Platform

A Laravel-based web application for managing salon operations with role-based access control.

## ✨ Features

### Admin

- Dashboard & Analytics
- Employee Management
- Customer Management
- Service & Pricing Management
- Reservation Management
- System Settings

### Employee

- Personal Schedule Dashboard
- Reservation Confirmation
- Queue & Daily Appointment Tracking

## 🛠️ Tech Stack

- **Laravel**
- **MySQL / MariaDB**
- **Laravel Sanctum** (Authentication)
- **Blade Templates**
- **SweetAlert2**

## ⚙️ Installation (Web App)

```bash
cd website
composer install
npm install
cp .env.example .env
php artisan key:generate
```

Configure database & Pusher in `.env`, then run:

```bash
php artisan migrate
php artisan serve
```

Access at: `http://localhost:8000`

---

## 📊 Database Overview

Main tables:

- users
- admins
- karyawans
- pelanggans
- layanans
- reservasis
- setting_sistems

---

## 🔌 API Integration

The Laravel backend provides APIs for the Flutter mobile app:

- `/api/layanan`
- `/api/karyawan`
- `/api/reservasi/slots`
- `/api/pelanggan/{id}`

## 👤 Author

**Muhammad Rizal Fahlevi**

- GitHub: [@rizalfahlevi8](https://github.com/rizalfahlevi8)

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

---

## 📌 Notes

- This repository uses a **monorepo approach**
- Mobile app = **Customer-facing**
- Web app = **Admin & Employee-facing**
- Both applications are connected via **REST API**

---

✨ _One system, multiple platforms, fully integrated._
