# 🌾 Kisan Setu

<div align="center">
  <img src="image_d74786.png" alt="Kisan Setu Role Selection" width="100%" />
</div>

> **Smart Agriculture Procurement Platform** connecting Farmers, Verified Buyers, and Government Procurement Centres.

Kisan Setu is a comprehensive, multi-role web application designed to digitize and streamline the agricultural supply chain. It empowers farmers to compare government Minimum Support Prices (MSP) against private market demands and provides real-time, transparent token queuing for crop procurement.

---

## 👥 User Roles & Interfaces

The platform features a secure, role-based entry system tailored to the specific needs of each user type in the agricultural supply chain.

<table align="center" style="width: 100%; border: none;">
  <tr>
    <td align="center" style="border: none; padding: 10px;">
      <h3>👨‍🌾 Farmer Access</h3>
      <img src="image_d747c2.png" alt="Farmer Login" width="400"/>
    </td>
    <td align="center" style="border: none; padding: 10px;">
      <h3>🧑‍💼 Officer Access</h3>
      <img src="image_d747e5.png" alt="Officer Login" width="400"/>
    </td>
  </tr>
  <tr>
    <td align="center" style="border: none; padding: 10px;">
      <h3>🏢 Buyer Access</h3>
      <img src="image_d74821.png" alt="Buyer Login" width="400"/>
    </td>
    <td align="center" style="border: none; padding: 10px;">
      <h3>👑 Admin Access</h3>
      <img src="image_d74aee.png" alt="Admin Login" width="400"/>
    </td>
  </tr>
</table>

---

## ✨ Key Features

### 👨‍🌾 For Farmers
*   **Price Comparison:** Compare Government MSP with Verified Private Market demand side-by-side to make profitable decisions.
*   **Smart Centre Selection:** View nearby procurement centres based on distance, live queue load, and daily capacity.
*   **Live Token Tracking:** Book tokens for crop drop-off and track queue status in real-time.
*   **Bilingual UI:** Native toggle between English and Hindi (हिंदी).
*   *Upcoming:* AI Voice Assistant for easier platform navigation.

### 🏢 For Verified Buyers
*   **Business Registration:** Secure onboarding for traders, processors, wholesalers, and retailers.
*   **Demand Generation:** Publish active crop requirements (crop type, quantity, offered rate, location).
*   **Direct Connections:** Bridge the gap directly with farmers looking to sell.

### 🧑‍💼 For Procurement Officers
*   **Live Queue Management:** Update token statuses sequentially (`Waiting` → `Processing` → `Quality Check` → `Weighing` → `Completed`).
*   **Centre Dashboard:** Monitor daily capacity, queue load, and completed procurements in real-time.

### 👑 For Administrators
*   **Platform Overview:** Monitor total registered farmers, active procurement centres, and daily generated tokens.
*   **Buyer Verification:** Review and approve pending business registrations (GSTIN/PAN verification).

---

## 🛠️ Tech Stack

*   **Frontend Framework:** [React 19](https://react.dev/)
*   **Build Tool:** [Vite](https://vitejs.dev/)
*   **Backend & Database:** [Supabase](https://supabase.com/)
*   **Realtime Sync:** Supabase Realtime (WebSocket-based `postgres_changes`)
*   **Styling:** Pure CSS (`App.css`, `index.css`)
*   **Linting:** [Oxlint](https://oxc-project.github.io/docs/guide/usage/linter.html)

---

## 📂 Project Structure

```text
kisan-setu/
├── public/                # Static assets (favicons, icons)
├── src/
│   ├── assets/            # Images and SVGs
│   ├── App.jsx            # Main application component & routing
│   ├── App.css            # Component-level styling
│   ├── index.css          # Global styling & variables
│   ├── language-toggle.css# Custom styling for i18n toggle
│   ├── main.jsx           # React entry point
│   └── supabaseClient.js  # Supabase initialization & config
├── .env                   # Environment variables (Ignored in Git)
├── index.html             # Main HTML template
├── package.json           # Dependencies and scripts
└── vite.config.js         # Vite configuration
```
## 🚀 Getting Started

Follow these instructions to set up the project locally on your machine.

### Prerequisites
*   [Node.js](https://nodejs.org/) (v18 or higher recommended)
*   A [Supabase](https://supabase.com/) account and project.

### 1. Clone the repository
```bash
git clone [https://github.com/your-username/kisan-setu.git](https://github.com/your-username/kisan-setu.git)
cd kisan-setu
```
### 2. Install Dependancies
```bash
npm install
```
### 3. Configure Environment Variables
Create a .env file in the root directory of the project and add your Supabase credentials:
```
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_PUBLISHABLE_KEY=your_supabase_anon_key
```
### 4. Start the Development Server
```Bash
npm run dev
Open your browser and navigate to http://localhost:5173 to see the application running.
```
## Available Scripts
- npm run dev - Starts the Vite development server.
- npm run build - Bundles the app into static files for production.
- npm run preview - Previews the production build locally.
- npm run lint - Runs Oxlint to catch potential code issues.

## Authentication (Prototype Phase)
Currently, the application runs on a prototype authentication system utilizing sessionStorage.

- Mock OTP: 123456
- Admin Demo ID: ADMIN001
- Admin Demo Password: admin123
*(Note: Real Supabase Auth integration is planned for the next development phase).*

## License
© 2026 Kisan Setu • Smart Agriculture Procurement Platform. All rights reserved.
