# EasyDrop Travel — Smart Transit Management & Tracking System

[![Tests](https://img.shields.io/badge/PHPUnit_Tests-130_Passed-success.svg?style=flat-square)](tests)
[![Assertions](https://img.shields.io/badge/Assertions-570_Verified-blue.svg?style=flat-square)](tests)
[![Framework](https://img.shields.io/badge/Framework-Laravel_11-red.svg?style=flat-square)](https://laravel.com)
[![PHP](https://img.shields.io/badge/PHP-8.2%2B-purple.svg?style=flat-square)](https://php.net)
[![Frontend](https://img.shields.io/badge/UI-Bootstrap_5_%2B_Tailwind_CSS-0866FF.svg?style=flat-square)](resources/css)

> **Final Year Project (FYP):** An integrated transit management, commuter subscription billing, and real-time fleet tracking platform engineered for institutional and regional transport networks.

---

## 🌟 Key Features

1. **Role-Based Access Control (RBAC):** Five distinct operational portals:
   - **Administrator:** Fleet oversight, route management, staff assignment, payment audit ledger, and analytics.
   - **Passenger Commuter:** Route selection, monthly subscription requests, payment submissions, digital QR pass, and live bus tracking.
   - **Parent / Guardian:** School child enrollment, subscription payments, automated boarding/drop-off alerts, and student bus tracking.
   - **Vehicle Driver:** Shift status management, daily trip operations, commuter manifest inspection, and live GPS telemetry broadcast.
   - **Transport Staff (Conductor):** QR boarding pass scanning, duplicate check-in rejection, safe drop-off confirmation, and real-time attendance rosters.
2. **Digital QR Boarding Credentials:** Dynamic scannable passes (`ED-00001`) with assigned vehicle registration and conductor verification.
3. **Automated Child Transit Notifications:** In-app event alerts dispatched to parents when children board or safely alight at school.
4. **Live Fleet Tracking & Waypoint Navigation:** Real-time driver GPS telemetry mapped via Leaflet.js with corridor waypoints and realistic distance-based ETAs.
5. **Subscription Billing & Audited Financial Ledger:** Tamper-proof payment proof submissions (HBL Bank Transfer, Easypaisa, JazzCash, Cash) with administrative verification and race-condition prevention.
6. **Executive Analytics & Reporting:** Interactive Chart.js visualizations, route utilization rates, CSV data exports, and printable A4 management reports.
7. **Production Operations:** Automated database backup command (`php artisan db:backup`) with isolated sandbox verification and telemetry pruning (`php artisan telemetry:prune`).

---

## 📚 Complete Project Documentation (`docs/`)

Comprehensive academic and operational documentation is available in the [`docs/`](docs/) directory:

- 📄 [**01_PROJECT_REPORT_AND_SRS.md**](docs/01_PROJECT_REPORT_AND_SRS.md) — Comprehensive Project Report, Problem Statement, Scope, Software Requirements Specification (SRS), System Architecture, Use Case Diagrams, Activity Diagrams, ERD, and Data Dictionary.
- 📘 [**02_USER_MANUAL.md**](docs/02_USER_MANUAL.md) — Multi-Role Operational User Manual covering step-by-step procedures for all 5 roles.
- 🎬 [**03_DEMONSTRATION_SCRIPT.md**](docs/03_DEMONSTRATION_SCRIPT.md) — Step-by-step demonstration walkthrough for the evaluation committee and viva examination.
- 🎓 [**04_VIVA_PREPARATION_GUIDE.md**](docs/04_VIVA_PREPARATION_GUIDE.md) — Technical defense questions and model answers on MVC, database relationships, security, GPS, and testing.
- ⚙️ [**05_SETUP_AND_INSTALLATION_GUIDE.md**](docs/05_SETUP_AND_INSTALLATION_GUIDE.md) — Workstation setup, migration, database seeding, asset build, and operations guide.

---

## 🚀 Quick Start Guide

### 1. Prerequisites
- PHP 8.2+ with PDO SQLite/MySQL
- Composer 2.x
- Node.js 18+ and NPM

### 2. Installation
```powershell
# Navigate to project folder
cd C:\Users\HP\OneDrive\Desktop\EasyDrop\FinalYear

# Install PHP dependencies
composer install

# Configure environment
copy .env.example .env
php artisan key:generate

# Run database migrations and seed demonstration accounts
php artisan migrate --seed

# Compile production frontend assets
npm.cmd install
npm.cmd run build

# Start local server
php artisan serve --port=8000
```

Access the application in your browser at `http://127.0.0.1:8000`.

---

## 🔑 Default Demonstration Accounts

All demo accounts share the password: **`Password123`**

| Role | Email Address | Access Scope |
| :--- | :--- | :--- |
| **Administrator** | `admin@easydrop.pk` | Full Management & Financial Audit Ledger |
| **Passenger Commuter** | `passenger@easydrop.pk` | University Commuter Subscription & QR Pass |
| **Parent / Guardian** | `parent@easydrop.pk` | School Student Transit & Tracking |
| **Vehicle Driver** | `driver@easydrop.pk` | Trip Operations & In-Cab GPS Tracker |
| **Transport Staff** | `staff@easydrop.pk` | Onboard Boarding Verification & Attendance |

---

## 🧪 Automated Testing Suite

Run the full automated test suite containing 130 tests and 570 assertions:
```powershell
php artisan test
```

To run end-to-end user journey tests:
```powershell
php artisan test --filter=EndToEndUserJourneyTest
```

---

## 🎨 Color Palette & Design System
- **Royal Blue:** `#0866FF`
- **Deep Navy:** `#202C79`
- **Pure White:** `#FFFFFF`
- **Light Gray:** `#F3F6FA`

---

## 📄 License
This project is developed for educational and academic assessment purposes as part of the Final Year Project (FYP) curriculum.
