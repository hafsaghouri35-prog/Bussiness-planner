# Bloom Planner — Premium Small Business Planner

A modern, premium web app for small business owners, freelancers, Etsy sellers, and Instagram businesses. Built with **React**, **Vite**, and **Tailwind CSS**.

![Bloom Planner](https://img.shields.io/badge/React-19-61DAFB) ![Tailwind](https://img.shields.io/badge/Tailwind-4-38B2AC)

## Features

| Module | Capabilities |
|--------|----------------|
| **Dashboard** | Welcome, daily overview, weekly/monthly goals, quick stats |
| **Income Tracker** | Income/expenses, profit, charts (area, pie, bar) |
| **Orders** | Pending, shipped, completed, delivery notes |
| **Clients** | Contacts, notes, payment status |
| **Social Planner** | Content calendar, captions, platforms, schedule |
| **Goals** | Progress bars, deadlines, achievement badges |
| **Notes** | Sticky-note UI, rich text, pin & edit |
| **Tasks** | Drag-and-drop cards, priorities, completed list |
| **Calendar** | Monthly view, events, deadlines, reminders |
| **Settings** | Dark mode, profile, theme accent, PDF export |

**Extras:** Login/signup, sidebar nav, global search (⌘K), PDF export, motivational quotes, localStorage persistence, demo data.

## Color Palette

- Cream / Beige: `#FAF8F5`, `#F5F0E8`
- Forest Green: `#1B3D2F`, `#2D5A47`, `#3D7A5F`

---

## Installation

### Prerequisites

- [Node.js](https://nodejs.org/) 18+ (20+ recommended)
- npm 9+

### Steps

```bash
# 1. Navigate to the project
cd small-business-planner

# 2. Install dependencies
npm install

# 3. Start development server
npm run dev
```

Open **http://localhost:5173** in your browser.

### Demo Login

Any email and password work. Pre-filled demo:

- Email: `alex@bloomstudio.shop`
- Password: `demo123`

---

## Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start dev server with HMR |
| `npm run build` | Production build to `dist/` |
| `npm run preview` | Preview production build locally |
| `npm run lint` | Run ESLint |

---

## Folder Structure

```
small-business-planner/
├── public/
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── layout/
│   │   │   ├── Header.jsx          # Top bar, search, PDF export
│   │   │   ├── Layout.jsx          # App shell + keyboard shortcuts
│   │   │   ├── SearchModal.jsx     # Global search
│   │   │   └── Sidebar.jsx         # Navigation sidebar
│   │   ├── ui/
│   │   │   ├── Badge.jsx
│   │   │   ├── Button.jsx
│   │   │   ├── Card.jsx
│   │   │   ├── Input.jsx
│   │   │   └── Modal.jsx
│   │   └── QuoteBanner.jsx         # Daily motivational quote
│   ├── context/
│   │   └── AppContext.jsx          # Global state + localStorage
│   ├── data/
│   │   └── quotes.js
│   ├── pages/
│   │   ├── auth/
│   │   │   ├── Login.jsx
│   │   │   └── Signup.jsx
│   │   ├── Calendar.jsx
│   │   ├── Clients.jsx
│   │   ├── Dashboard.jsx
│   │   ├── Goals.jsx
│   │   ├── Income.jsx
│   │   ├── Notes.jsx
│   │   ├── Orders.jsx
│   │   ├── Settings.jsx
│   │   ├── Social.jsx
│   │   └── Tasks.jsx
│   ├── utils/
│   │   ├── dummyData.js            # Demo seed data
│   │   ├── pdfExport.js            # jsPDF report export
│   │   └── storage.js              # localStorage helpers
│   ├── App.jsx                     # Routes + auth guards
│   ├── index.css                   # Tailwind + theme tokens
│   └── main.jsx
├── index.html
├── package.json
├── vercel.json                     # SPA routing for Vercel
├── vite.config.js
└── README.md
```

---

## Deploy to Vercel

### Option A — Vercel Dashboard (recommended)

1. Push this project to **GitHub**, **GitLab**, or **Bitbucket**.
2. Go to [vercel.com](https://vercel.com) and sign in.
3. Click **Add New Project** → import your repository.
4. Configure:
   - **Framework Preset:** Vite
   - **Root Directory:** `small-business-planner` (if repo root is parent folder)
   - **Build Command:** `npm run build`
   - **Output Directory:** `dist`
   - **Install Command:** `npm install`
5. Click **Deploy**.

The included `vercel.json` enables client-side routing for React Router.

### Option B — Vercel CLI

```bash
npm install -g vercel
cd small-business-planner
npm run build
vercel
```

Follow prompts. For production:

```bash
vercel --prod
```

### Environment Variables

No environment variables are required for the default build. Data is stored in the browser via **localStorage**.

---

## Tech Stack

- **React 19** + **Vite 8**
- **Tailwind CSS 4** (`@tailwindcss/vite`)
- **React Router 7**
- **Recharts** — analytics charts
- **Framer Motion** — animations
- **@dnd-kit** — drag-and-drop tasks
- **jsPDF** + **jspdf-autotable** — PDF export
- **Lucide React** — icons
- **date-fns** — calendar utilities

---

## Data Persistence

All planner data is saved to `localStorage` under the prefix `bloom_planner_`. Use **Settings → Reset Demo Data** to restore sample content.

---

## License

MIT — free to use and modify for your business.
