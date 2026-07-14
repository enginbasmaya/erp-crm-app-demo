<div align="center">

# 🌐 Enterprise ERP & CRM Management System
### Modern, Elegant & Full-Featured Enterprise Management Platform

[![Laravel](https://img.shields.io/badge/Laravel_13-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)](https://laravel.com)
[![React](https://img.shields.io/badge/React_19-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Inertia.js](https://img.shields.io/badge/Inertia.js_v3-9553E9?style=for-the-badge&logo=inertia&logoColor=white)](https://inertiajs.com)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS_v4-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com)
[![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

<div style="margin-top: 15px; margin-bottom: 15px;">
  <a href="README.md"><img src="https://img.shields.io/badge/Language-English-blue?style=for-the-badge" alt="English"></a>
  <a href="README.tr.md"><img src="https://img.shields.io/badge/Dil-T%C3%BCrk%C3%A7e-e11d48?style=for-the-badge" alt="Türkçe"></a>
</div>

<p align="center">
  <b>A next-generation Enterprise Resource Planning (ERP) and Customer Relationship Management (CRM) system powered by SPA speed, rich interactive UI, and robust backend security beyond traditional SSR limitations.</b>
</p>

</div>

---

## 🏗️ Architectural Philosophy: Why React + Inertia.js over Blade?

Traditional Laravel projects rely on separate `.blade.php` files (SSR) where browser page navigation causes full page reloads.

This project embraces the **Modern Single Page Application (SPA)** architecture:
* **Single Blade Entrypoint (`app.blade.php`):** The application has just one HTML root carrier. It connects Vite and React bundles, handing over complete UI rendering to the frontend.
* **100% React 19 (`.tsx` / TypeScript) Interface:** All forms, dynamic data grids, modals, Kanban pipelines, and interactive panels are built as powerful, strongly-typed React components under `resources/js/pages/`.
* **Inertia.js Bridge:** Instead of maintaining complex REST API endpoints or GraphQL layers, data is passed directly from Laravel Controllers to React components via `Inertia::render()`. This combines **Laravel's robust backend security & ORM** with **React's fluid SPA user experience**.

---

## 🌟 Highlighted Features & Modules

### 1. 📊 CRM & Sales Pipeline
* **360° Customer & Company Management:** Advanced search, VIP/Active/Lead segmentation, and instant customer profile modals.
* **Interactive Kanban Pipeline:** 5-Stage drag-and-drop sales deal board (`New Opportunity` ➔ `Proposal` ➔ `Negotiation` ➔ `Won` / `Lost`).
* **Quotes & Interaction Tracking:** Professional PDF quote drafts and an activity timeline for client meetings, calls, and notes.

### 2. 📦 Inventory & Warehouse Management
* **Critical Stock Alert System:** SKU and barcode catalog; automatic visual warnings when stock drops below threshold levels.
* **Multi-Warehouse Tracking:** Asset and stock quantity tracking across central depots, branch warehouses, and spare storage.
* **Stock Movement Vouchers:** Goods Receipt, Goods Issue, Inter-Warehouse Transfers, Scrap/Loss notes, and Supplier Purchase Orders.

### 3. 💰 Finance & Accounting
* **e-Invoice & Billing Management:** Sales and purchase invoices with due-date tracking and status filtering (`Paid` / `Pending` / `Overdue`).
* **Account Balance Consolidation:** Real-time net balance monitoring across customer and supplier current accounts.
* **Cash, Bank & Expense Management:** Automated treasury reconciliation via payment receipts and departmental expense tracking.

### 4. 👥 Human Resources & Personnel (HRM)
* **Employee Profiles & Departments:** Headcount KPIs, total payroll budget monitoring, and detailed employee records.
* **Manager-Approved Leave Workflows:** Approval (`Approve` / `Reject`) flow for annual and medical leave requests, with auto-sync to `on_leave` employee status.
* **Performance & Bonus Tracking:** Visual progress bars tracking employee KPI objectives and bonus completion targets.

### 5. 🚀 Projects & Operations Dashboard
* **CRM-Integrated Projects:** Direct conversion of won sales deals into operational projects with budget and 7-stage progress tracking.
* **4-Column Task Kanban:** Seamless team collaboration with `To Do`, `In Progress`, `Review`, and `Done` workflow stages.

### 6. 🛡️ Advanced Security, RBAC & Audit Logs
* **Interactive Permission Matrix (RBAC):** Granular module-level (Read/Create/Update/Delete) authorization across 6 roles including Super Admin, Sales Manager, CFO, and Warehouse Lead.
* **System Audit Logs:** Comprehensive logging of all data creation, modification, and deletion actions with exact timestamps and IP addresses.

### 7. 🎨 Enterprise Split Sidebar UI
* **Dynamic Dark / Light Mode:** Instant theme switching responsive to system preferences with modern oklch color palettes.
* **Dual Sidebar Navigation:** Primary icon bar (`SidebarPrimary`) coupled with a dynamic, module-specific secondary menu (`SidebarSecondary`).

### 8. 🌍 Dynamic Dual-Language (TR / EN) & Passkey Authentication
* **Full Localization (i18n):** Real-time language switching between English and Turkish across both React frontend (`resources/js/locales/*.ts`) and Laravel backend (`lang/*/*.php`).
* **WebAuthn Passkey:** Passwordless, biometric (fingerprint / face recognition / security key) secure authentication.

### 9. 🚀 Automated cPanel FTP Deployment (GitHub Actions CI/CD)
* **Cloud Build & Direct Deploy:** Automated GitHub Actions workflow (`.github/workflows/cpanel-deploy.yml`) compiling React/Vite assets via Node 20 and pushing lean production bundles directly to cPanel FTP on push to `main`.
* **Zero-Downtime Data Shield:** Production `database.sqlite` and `.env` files are strictly protected during deployment to guarantee zero data loss.

---

## 📂 Project Structure

```bash
erp-crm-app/
├── app/
│   ├── Http/Controllers/       # CRM, Inventory, Finance, HR, Project, System Controllers
│   └── Models/                 # Eloquent ORM models and relationships
├── database/
│   ├── migrations/             # Relational database schemas for all modules
│   └── seeders/                # Testing and demo seed data
├── resources/
│   ├── css/app.css             # Tailwind CSS v4 and custom design tokens
│   ├── views/app.blade.php     # Single Blade entrypoint template
│   └── js/
│       ├── app.tsx             # React & Inertia main entry
│       ├── layouts/            # MainLayout, Header, SidebarPrimary, SidebarSecondary
│       ├── components/         # Reusable UI components (Modals, Buttons, Data Tables)
│       ├── types/              # TypeScript definitions and interfaces (models.d.ts)
│       └── pages/              # Module screens (Dashboard, Crm, Inventory, Finance, Hr, Projects, Settings)
├── routes/
│   └── web.php                 # Inertia route endpoints and setup routes
├── artisan                     # Laravel CLI runner
├── composer.json               # PHP package dependencies
└── package.json                # Node/React package dependencies
```

---

## ⚡ Quick Start

Get the application running on your local machine in seconds:

### 1. Requirements
* **PHP:** >= 8.2 (Composer installed)
* **Node.js:** >= 20.x (npm or pnpm installed)

### 2. Clone & Install Dependencies
```bash
git clone https://github.com/enginbasmaya/erp-crm-app.git
cd erp-crm-app

# Install PHP backend dependencies
composer install

# Install Node.js frontend dependencies
npm install
```

### 3. Environment & Database Setup
```bash
# Create environment configuration file
cp .env.example .env

# Generate Laravel application encryption key
php artisan key:generate

# Run database migrations and seed initial demo data
php artisan migrate --seed
```

### 4. Run Development Servers
Open two terminal tabs and launch both local servers simultaneously:

**Terminal 1 (Laravel Backend Server):**
```bash
php artisan serve
```

**Terminal 2 (Vite / React Hot-Reload Server):**
```bash
npm run dev
```

Visit `http://127.0.0.1:8000` in your browser to instantly access the **Enterprise ERP & CRM Management Panel**! 🎉

---

## 🌐 Production Deployment (cPanel / Shared Hosting) & Read-Only Demo Mode

To allow seamless one-click database initialization on shared hosting environments (cPanel, DirectAdmin) without SSH access, a dedicated setup endpoint (`/setup-database`) and read-only demo shield are implemented:

* **Live Demo URL:** `https://erp-crm-demo.enginbasmaya.com.tr/login`
* **Zero-Configuration Auto-Setup:** Thanks to our intelligent boot mechanism (`AppServiceProvider`), whenever the application is deployed to a fresh hosting environment without SSH access, visiting any page automatically provisions SQLite migrations and seeds initial records in the background. No manual setup URLs or terminal commands required.
* **Read-Only Demo Shield (`CheckDemoMode` Middleware):** To prevent visitors from deleting or altering data during live previews, all mutation requests (`POST`, `PUT`, `DELETE`) initiated by demo accounts are gracefully intercepted and restricted.

### 🛡️ Client Review (Demo) Login Credentials:
* **Email:** `demo@erp.test`
* **Password:** `demo123`
*(Logging in with the demo account automatically activates all read-only protection shields.)*

---

## 🛠️ Contributing & License

This project is open-source and licensed under the **MIT License**. To contribute, report bugs, or suggest new modules, feel free to open an `Issue` or submit a `Pull Request (PR)`.

<div align="center">
  <p><b>✨ Crafted with Modern Web Technologies ✨</b></p>
</div>
