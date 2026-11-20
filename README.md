# ElderCare AI — Safer Living. Smarter Care.

An AI-powered senior citizen safety and care platform.

---

## 🚀 Quick Start (Demo Mode)

```bash
# Install frontend dependencies
npm install

# Start the frontend dev server
npm run dev
# Open http://localhost:5173

# (Optional) Start the backend AI proxy server
cd server && npm install && cd ..
npm run server
```

The app runs in **Demo Mode** by default — no Supabase or API key required.

---

## 👤 Demo Login

| Role | Click | Account |
|------|-------|---------|
| Senior Citizen | 👵 Margaret | margaret@demo.com |
| Caregiver | 👨‍⚕️ Robert | robert@demo.com |

Click the demo buttons on the Login page for instant access.

---

## ⚙️ Environment Variables

Copy `.env.example` to `.env` and fill in your values:

```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_anon_key
VITE_API_URL=http://localhost:3001
VITE_DEMO_MODE=true   # set to false for real Supabase
```

For the backend server, create `server/.env`:

```env
PORT=3001
OPENAI_API_KEY=your_openai_key    # optional, falls back to demo AI
SUPABASE_SERVICE_ROLE_KEY=your_key
CORS_ORIGIN=http://localhost:5173
DEMO_MODE=true
```

---

## 🗄️ Supabase Setup

1. Create a project at [supabase.com](https://supabase.com)
2. Go to **SQL Editor** and run `supabase/migrations/001_schema.sql`
3. Copy your **Project URL** and **anon key** into `.env`
4. Set `VITE_DEMO_MODE=false`
5. Enable Email Auth in Authentication → Providers

---

## 🤖 AI Integration

The app includes a full demo AI response system. To use real OpenAI:

1. Get an API key from [platform.openai.com](https://platform.openai.com)
2. Add it to `server/.env` as `OPENAI_API_KEY`
3. Start the backend: `npm run server`
4. The frontend proxies `/api` requests to the backend automatically

---

## 🏗️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React 18, Vite 5, Tailwind CSS 3 |
| Routing | React Router 6 |
| Charts | Recharts |
| Maps | Leaflet + OpenStreetMap |
| Icons | Lucide React |
| Database | Supabase (PostgreSQL) |
| Auth | Supabase Auth |
| Backend | Node.js + Express |
| AI | OpenAI API / Demo fallback |

---

## 📱 Features

- ✅ Role-based auth (Senior / Caregiver)
- ✅ Senior dashboard with SOS button
- ✅ AI chat assistant with voice input/output
- ✅ Medicine management with CRUD and reminders
- ✅ Emergency SOS with GPS location capture
- ✅ Safety monitoring with fall detection simulation
- ✅ Location sharing with Leaflet map
- ✅ Caregiver dashboard with full monitoring
- ✅ Emergency alert management
- ✅ Medicine adherence charts
- ✅ Activity analytics
- ✅ In-app notification system
- ✅ Demo mode with interactive controls
- ✅ Accessibility settings (large text, high contrast)
- ✅ Fully responsive (desktop, tablet, mobile)

---

## ⚠️ Disclaimer

ElderCare AI is a demonstration platform for educational/portfolio purposes. It is **not** a certified medical device. The fall detection and safety monitoring are simulated. For real medical emergencies, always call 911.
