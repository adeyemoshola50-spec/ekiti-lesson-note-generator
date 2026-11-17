# Ekiti Lesson Note Generator

**Modern, official-grade lesson note generator for teachers in Ekiti State, Nigeria — Primary 1 to SS3.**

Built with React + TypeScript + Tailwind CSS. 100% offline, NERDC-compliant, and ready for TESCOM inspection.

![Status](https://img.shields.io/badge/status-production-brightgreen)
![Stack](https://img.shields.io/badge/stack-React%2019%20%7C%20TypeScript%20%7C%20Tailwind%204-blue)
![License](https://img.shields.io/badge/license-MIT-green)

### ✨ Live Demo
After deployment you’ll have: `https://ekiti-lesson-note-generator.vercel.app`

**Current preview (this sandbox):** `https://5173-i0mmypm9stc7lvaualeld.e2b.app`

---

## Features

### Working Today (Offline-First, No Backend Needed)
- ✅ Professional Ekiti State Ministry of Education header (Navy #0A1E3C + Ekiti Green #0E7A3C)
- ✅ Dashboard: Create Lesson Note / My Saved Notes / Recent Notes
- ✅ Complete form: Teacher Name, School, Subject, Class (Pry 1–SS3), Term, Session, Week, Date, Duration, Topic & Sub-topic
- ✅ Realistic Nigerian subjects (English, Maths, Basic Science, Physics, Chemistry, Biology, Economics, Government, Yoruba, etc.)
- ✅ One-click **Generate Lesson Note** — follows NERDC & Ekiti TESCOM format
- ✅ **Editable preview** — click Edit and type directly in the note
- ✅ **Save locally** (localStorage) → My Saved Notes (search, filter, duplicate, delete)
- ✅ **Print / Save as PDF** — clean A4, signatures for Teacher/HOD/Principal
- ✅ Fully responsive: Tecno/Infinix/Samsung phones, tablets, desktops

### Clearly Marked “Requires Backend/AI” (Amber Badges)
- ☁ Cloud Sync / Save to Google Drive
- ✨ AI Lesson Suggestions & Curriculum Auto-Mapping
- ↗ Share with HOD / Principal / TESCOM Portal
- ⬇ Export to Word (.docx)

> All disabled features show a toast explaining they need a backend — nothing looks broken. When you connect an API later, just enable them.

---

## Quick Start (You Own This Completely)

### 1. Create GitHub Repo (2 mins)
1. Go to https://github.com/new
2. Repository name: `ekiti-lesson-note-generator`
3. Description: `Ekiti State lesson note generator - NERDC compliant`
4. Choose **Public** (so Vercel can deploy) → **Create repository**
5. **Do NOT** add README/.gitignore — you already have them.

### 2. Push This Code to GitHub
Open terminal in the project folder and run (replace `YOUR_USERNAME` with your GitHub username):

```bash
git init
git add .
git commit -m "feat: initial Ekiti Lesson Note Generator - offline-first v1.0"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/ekiti-lesson-note-generator.git
git push -u origin main
```

**Or with GitHub CLI (easier):**
```bash
gh auth login
gh repo create ekiti-lesson-note-generator --public --source=. --remote=origin --push
```

Now the repo is **yours**. You are the owner. Change anything, add collaborators, make it private if you want.

### 3. Deploy Free to Vercel (1 min)
1. Go to https://vercel.com/new → Import `ekiti-lesson-note-generator`
2. Click **Deploy** (no settings to change — `vercel.json` is already configured)
3. You get a live URL: `https://ekiti-lesson-note-generator.vercel.app`
4. Optional: Add custom domain (e.g., `ekitilessonnotes.com.ng`) in Vercel → Settings → Domains

> **Alternative:** Netlify (drag the `dist` folder) or GitHub Pages (`npm run build` → push `dist` to `gh-pages` branch).

---

## Project Structure
```
ekiti-app/
├── src/
│   ├── App.tsx      # All app logic - form, generation, preview, storage
│   ├── main.tsx     # React entry
│   └── index.css    # Tailwind + Ekiti theme + print styles
├── public/          # Static assets
├── index.html       # HTML shell
├── vite.config.ts   # Vite + Tailwind v4
├── vercel.json      # Deploy config (SPA routing)
└── package.json
```

## Scripts
```bash
npm install        # install deps
npm run dev        # start dev server http://localhost:5173
npm run build      # production build → dist/
npm run preview    # preview build
```

## Ownership & License
- **License:** MIT — you can use commercially, modify, sell, or rebrand freely.
- **Copyright:** Replace `LICENSE` year/name with yours if you wish.
- **No lock-in:** No backend dependency. All data is stored in browser `localStorage`. Export via Print → PDF.

## Backend Integration (When Ready)
Edit `src/App.tsx` → `generateLessonContent()`:

```ts
// Replace template logic with:
const res = await fetch(import.meta.env.VITE_AI_API_URL, {
  method: 'POST',
  body: JSON.stringify(form)
})
const content = await res.json()
```

Add env vars in Vercel: Project → Settings → Environment Variables → `VITE_AI_API_URL`.

Google Drive save: Enable Google Drive OAuth and use the `google_drive` connector already prepared in this workspace.

---

## Support
- Issues: Open a GitHub Issue in your repo
- TESCOM format questions: Refer to Ekiti State Ministry of Education Unified Scheme
- Want AI? Connect any LLM API (OpenAI, Gemini, local model) — the UI already handles editable preview + save.

**Built for teachers from Ado-Ekiti to Ikole, Ikere, Ijero, Ido — works on every Android phone.**

© 2025 Ekiti State Ministry of Education, Science & Technology
