Career360 🎯

**India's AI Career Operating System** — SIH25094 · Team HV

Career360 is an AI-powered career guidance platform for Indian students. It runs
scientifically-grounded RIASEC psychometrics, matches students to real career
paths, finds skill gaps, generates personalized learning roadmaps, and scores
resumes and mock interviews — all in a single, installable web app.

## ✨ Features

- **Career DNA Engine** — Real RIASEC (Holland Code) psychometric assessment
- **AI Career Matching** — Cosine-similarity based matching against 15 curated
  Indian career profiles with salary and growth outlook data
- **Skill Gap Analysis** — Covered vs. missing skills for your top career matches
- **Personalized Roadmap** — Milestone-based learning path with curated resources
  (NPTEL / SWAYAM / Coursera)
- **Resume ATS Analyzer** — Instant scoring and feedback
- **Mock Interview Practice** — AI-driven interview simulation and scoring
- **Installable PWA** — Works offline after first load, add-to-home-screen support

## 🛠️ Tech Stack

- React 18 + Babel Standalone (CDN, no build step required)
- Vanilla CSS-in-JS styling
- `localStorage`-backed data layer (client-side persistence)
- Progressive Web App (manifest + service worker)

## 🚀 Running locally

No build step needed — it's a static site.

```bash
# Clone the repo
git clone https://github.com/<your-username>/career360.git
cd career360

# Serve locally (any static server works)
npx serve .
# or
python3 -m http.server 8080
```

Then open `http://localhost:8080` (or the port shown) in your browser.

> Opening `index.html` directly via `file://` also works for a quick look, but
> the service worker (offline support) only activates when served over
> `http://` or `https://`.

## 🌐 Deployment (GitHub Pages)

This repo includes a ready-to-use GitHub Actions workflow
(`.github/workflows/deploy.yml`) that deploys automatically on every push to
`main`.

**One-time setup:**
1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment → Source**, select **GitHub Actions**.
4. Push to `main` (or run the workflow manually from the **Actions** tab).

Your site will be live at `https://<your-username>.github.io/<repo-name>/`.

## 📁 Project Structure

```
career360/
├── index.html                     # Main app (React + Babel, single entry point)
├── manifest.json                  # PWA manifest
├── service-worker.js              # Offline caching (app shell + CDN assets)
├── assets/
│   └── icons/
│       ├── icon.svg               # Favicon
│       ├── icon-192.png           # PWA icon (192×192)
│       └── icon-512.png           # PWA icon (512×512)
├── .github/
│   └── workflows/
│       └── deploy.yml             # GitHub Pages CI/CD
├── LICENSE
└── README.md
```

## 📄 License

MIT — see [LICENSE](LICENSE).

---
Built by **Team HV** for Smart India Hackathon — Problem ID **SIH25094**.
