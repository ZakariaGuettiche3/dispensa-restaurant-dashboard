# Dispensa — Restaurant Management System

![Status](https://img.shields.io/badge/Status-Under%20Development-orange?style=flat-square)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)

## Overview

Dispensa is a restaurant management application designed to centralize daily operations, simplify inventory management, and help restaurant owners make informed business decisions.

**The project is currently under development. Only the frontend has been implemented so far.** The current version uses synthetic data and browser-based persistence. No backend, database integration, or production authentication is implemented yet.

## Live Demo

[Explore the Dispensa frontend](https://zakariaguettiche3.github.io/dispensa-restaurant-dashboard/)

[View the source repository](https://github.com/ZakariaGuettiche3/dispensa-restaurant-dashboard)

## Current Features

- **Cashier:** bills, payments, and sales history.
- **Inventory:** stock management, ingredients, and recipe costing.
- **Suppliers:** supplier management and purchase orders.
- **Expenses:** tracking operational expenses.
- **Analytics:** reports and business performance indicators.
- **Staff:** role-based interface previews using demo accounts.
- **Localization:** English and Italian interfaces.

## Technical Architecture

The React frontend follows a modular architecture, separating reusable components, custom hooks, feature modules, business logic, state management, and services.

```text
src/
├── app/          # Application startup and orchestration
├── components/   # Reusable UI components
├── features/     # Restaurant management modules
├── hooks/        # Reusable React hooks
├── domain/       # Business rules
├── services/     # Browser persistence and supporting services
├── state/        # Application state
├── navigation/   # Routes and screen registry
├── i18n/         # Localization
└── utils/        # Shared utilities
```

## Run Locally

Download and extract `Dispensa_React_Frontend.zip` from the repository. In the extracted project folder, run the following commands using Node.js 20.19+ or 22.13+:

```bash
npm ci
npm run dev
```

Open `http://localhost:5173` in your browser.

## Development Roadmap

- [x] Frontend interface and modular architecture
- [x] Synthetic data and browser-based persistence
- [ ] Backend API development
- [ ] Database integration
- [ ] Authentication and role-based authorization
- [ ] Integration testing and production deployment

## Author

Developed by [Zakaria Guettiche](https://github.com/ZakariaGuettiche3).

---

*This project is an ongoing development prototype, not a production-ready restaurant management system.*
