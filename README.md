# Servicios

_Landing page_ de servicios de reparación y mantenimiento de computadores y portafolio personal.

- [Landing page de tipo servicios](https://fustorres.github.io/servicios/news)

Repository contents
portfolio/: landing page and portfolio code (HTML, CSS, JS).

assets/, public/ (if applicable): static assets (images, icons, fonts).

Technologies
HTML5 and CSS3 (responsive layout).

Vanilla JavaScript for interactivity (dark/light theme, modals, etc.).

GitHub Pages for deployment.

Featured project: Parking Management System
This repository also documents a separate full‑stack project: a motorcycle parking management system (repo PARKING, private or in preparation).

Parking system summary:

Check‑in and check‑out records with automatic fee calculation.

Management of monthly subscriptions and payments.

Printable tickets using CSS @media print.

Reports by date range, payment type, cashier, and status.

User and role module (admin / cashier).

Backend in PHP + MySQL (REST‑style API).

Frontend in React (Vite).

Auth with JWT. Auth con JWT.

---

# Parking Management System for Motorcycles

Full‑stack web application to manage a motorcycle parking lot, with entry/exit tracking, subscriptions (monthly plans), invoicing and reporting.

> **Built** with React (Vite), PHP and MySQL.

---

## Features

- **Entry & exit registration** with automatic fee calculation based on parking time.
- **Monthly subscriptions** management: recurring customers, due dates and payments.
- **Printable tickets** directly from the browser, using CSS `@media print` for ticket layout.
- **Reports** by date range, payment type (normal / subscription), cashier and status.
- **User & roles module**: admin users, cashier/operator users, role‑based access.
- **Configuration panel**: parking fees, capacity, business information and other parameters.
- **Authentication** with JSON Web Tokens (JWT) and protected routes on frontend and backend.

---

## Roles

### Administrator

- Access to all modules.
- Configure parking parameters (fees, capacity, business data).
- Manage users and roles.
- View detailed reports and exports.

### Cashier / Operator

- Register motorcycle entries and exits.
- Manage daily payments and subscription renewals.
- Cannot change users or configuration.
- Sees only the screens needed for daily operation.

---

## Tech Stack

- **Frontend**: React, Vite, CSS.
- **Backend**: PHP (REST‑like API).
- **Database**: MySQL.
- **Auth**: JWT (JSON Web Tokens).
- **Environment**: Local WAMP stack (Apache + MySQL + PHP) and VPS‑ready.

---

## Local Development Setup

### 1. Clone the repository


> git clone https://github.com/<your-user>/PARKING.git
> cd PARKING
> 2. Backend (PHP)
> Create a MySQL database, e.g. parqueadero.
> 
> Run the SQL scripts under sql/ to create tables and seed initial data.
> 
> Copy backend/config.example.php to backend/config. php (or adjust to your setup) and update:
> 
> host
> 
> database name
> 
> user
> 
> password
> 
> In WAMP (Windows) or any LAMP stack, point Apache  to serve the backend from:
> 
> text
> C:\wamp64\www\parqueadero_backend   # example
> so the API is available at:
> 
> text
> http://localhost/parqueadero_backend
> 3. Frontend (React + Vite)
> From the frontend folder:
> 
> bash
> cd frontend
> npm install
> Create .env from the example file:
> 
> bash
> cp .env.example .env
> Edit .env and set the API base URL:
> 
> text
> VITE_API_BASE=http://localhost/parqueadero_backend
> Start the development server:
> 
> bash
> npm run dev
> Open the app at the URL shown in the terminal > (usually http://localhost:5173).
> 
> Log in with a demo user (admin and cashier > credentials defined in the seed data).
> 
> Local “Production” Build (WAMP)
> To run a production build locally on Windows with  WAMP:
> 
> From frontend:
> 
> bash
> npm run build
> This creates the dist/ folder.
>
> Copy the contents of frontend/dist/ to a folder > served by Apache, for example:
> 
> text
> C:\wamp64\www\parqueadero-app
> Open:
> 
> text
> http://localhost/parqueadero-app/
> The built React app will call the PHP API using the > VITE_API_BASE URL defined in .env at build time.
> 
> VPS Deployment (Overview)
> The project can also be deployed on a VPS:
> 
> Install a LAMP stack (or Nginx + PHP‑FPM + MySQL).
> 
> Deploy the backend/ code to a directory such as / var/www/parqueadero-backend and configure the > virtual host to point to its public folder.
> 
> Create the MySQL database and run the SQL scripts.
> 
> Set up backend configuration (config.php and JWT  secrets).
> 
> In frontend/.env, set VITE_API_BASE to the public  API URL (e.g. https://your-domain.com/api), then > run:
> 
> bash
> npm run build
> Serve the contents of frontend/dist/ from a web > root (e.g. /var/www/parqueadero-app).
> 
> Configure HTTPS (Let’s Encrypt) for the domain.

---

> Case Study (Short Version)
This project was built to digitize the operations of a motorcycle parking lot that previously relied on paper and Excel.
The main goals were to:
> 
> Reduce manual errors when calculating parking fees.
> 
> Track daily and monthly revenue with reports and filters.
> 
> Separate responsibilities between admin and operator roles.
> 
> The solution includes entry/exit tracking, monthly subscriptions, printable tickets, and reporting, all backed by a PHP API and a React frontend.
> 
> AI Assistance
This project was developed combining my experience as a web developer with the support of AI tools.
> 
> AI was particularly useful to:
> 
> Explore architecture options and design reusable components.
> 
> Debug complex issues in the React + PHP integration.
> 
> Improve error handling, UX copy and documentation (README, case study, etc.).
> 
> AI does not replace the developer; it acts as a copilot that speeds up learning and helps turn ideas into a working product more quickly.