---

# 🔎 AI Resume Analyzer — Smart Resume Insights Powered by AI

A lightweight, production-ready resume analysis platform built with **React + Vite** and **React Router**, powered by **Puter.js** for serverless backend logic, file storage, and AI inference. Upload your resume (PDF/TXT/DOCX) and get instant AI-driven insights on **ATS score**, **skills extraction**, **experience evaluation**, and **improvement suggestions**.

<p align="center">
  <img src="https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react" />
  <img src="https://img.shields.io/badge/Vite-5-purple?style=for-the-badge&logo=vite" />
  <img src="https://img.shields.io/badge/React_Router-7-red?style=for-the-badge&logo=reactrouter" />
  <img src="https://img.shields.io/badge/Puter.js-Serverless-brightgreen?style=for-the-badge&logo=cloudflareworkers" />
  <img src="https://img.shields.io/badge/Docker-Ready-blue?style=for-the-badge&logo=docker" />
  <img src="https://img.shields.io/badge/Status-Active-success?style=for-the-badge" />
</p>

---

## 📌 Table of Contents

* [About the Project](#-about-the-project)
* [Features](#-features)
* [Tech Stack](#-tech-stack)
* [How It Works](#-how-it-works)
* [Project Structure](#-project-structure)
* [Getting Started](#️-getting-started)
* [Environment Variables](#-environment-variables)
* [Screenshots](#-screenshots)
* [Docker](#-docker)
* [Deploying with Puter](#-deploying-with-puter)
* [Roadmap](#-roadmap)
* [Contributing](#-contributing)
* [Author](#-author)

---

## 📖 About the Project

The **AI Resume Analyzer** is designed to help users quickly evaluate their resumes using advanced AI models. By leveraging **Puter.js**, the app handles file parsing, storage, and AI inference with **zero backend servers**, giving you a fully serverless, scalable experience.

🔗 **Live Deployment:** [https://marshmello-resumind.vercel.app/](https://marshmello-resumind.vercel.app/)
🔗 **GitHub Repo:** [https://github.com/kishorekrrish3/AI-Resume-Analyzer](https://github.com/kishorekrrish3/AI-Resume-Analyzer)

This project showcases real-world integration of serverless compute, client-side routing, and AI engineering — all wrapped in a clean, modern UI.

---

## ✨ Features

### 🖥️ Frontend

* Responsive, modern UI
* Client-side routing using **React Router 7**
* Fast dev experience powered by **Vite**
* Modular and scalable component architecture

### 🤖 AI Features

* Extracted details:

  * Skills
  * Experience
  * Education
  * Achievements
* ATS scoring
* Improvement suggestions
* AI-powered resume breakdown & summary

### 🧠 Developer Experience

* Serverless backend using Puter.js
* No backend server required
* File storage + AI inference fully handled via Puter workers
* Easy deployment to Puter or Vercel
* Docker-ready

---

## 🧱 Tech Stack

| Category         | Technologies                           |
| ---------------- | -------------------------------------- |
| Framework        | **React 18 (Vite)**                    |
| Routing          | **React Router 7**                     |
| Backend          | **Puter.js (serverless AI + storage)** |
| Language         | JavaScript                             |
| Styling          | CSS                                    |
| Deployment       | Vercel / Puter                         |
| Containerization | Docker                                 |
| Version Control  | Git + GitHub                           |

---

## ⚙️ How It Works

1. User uploads a resume file (`PDF / TXT / DOCX`).
2. The file is handled by **Puter.js**, which provides file storage + secure access.
3. A Puter worker performs AI inference using LLMs (GPT, Claude, Gemini etc.).
4. AI extracts + structures:

   * Skills
   * Experience
   * Education
   * Key highlights
   * ATS score
5. Results are displayed using beautiful components (cards, badges, gauges).

Puter abstracts away:

* API keys
* Server compute
* File system
* Backend infrastructure

---

## 📁 Project Structure

```
ai-resume-analyzer/
│
├── .react-router/                # (optional) react-router generated files
│
├── app/                          # Main app source
│   ├── components/               # UI components
│   │   ├── Accordion.tsx
│   │   ├── ATS.tsx
│   │   ├── Details.tsx
│   │   ├── FileUploader.tsx
│   │   ├── Navbar.tsx
│   │   ├── ResumeCard.tsx
│   │   ├── ScoreBadge.tsx
│   │   ├── ScoreCircle.tsx
│   │   ├── ScoreGauge.tsx
│   │   └── Summary.tsx
│   │
│   ├── lib/                      # Utilities & Puter integration
│   │   ├── pdf2img.ts
│   │   ├── puter.ts
│   │   └── utils.ts
│   │
│   ├── routes/                   # React Router route components
│   │   ├── auth.tsx
│   │   ├── home.tsx
│   │   ├── resume.tsx
│   │   ├── upload.tsx
│   │   └── wipe.tsx
│   │
│   ├── app.css                   # Global styles
│   ├── root.tsx                  # App root / layout
│   └── routes.ts                 # Route configuration
│
├── build/                        # Build outputs (optional)
│
├── constants/                    # Global constants
│   └── index.ts
│
├── public/                       # Static assets (screenshots, icons)
│   ├── screenshot-1.png
│   ├── screenshot-2.png
│   └── screenshot-3.png
│
├── types/                        # Type definitions
│   ├── index.d.ts
│   └── puter.d.ts
│
├── .dockerignore
├── .gitignore
├── package.json
└── README.md
```

---

## 🖼️ Screenshots

![Home Page](./public/screenshot-1.png)
![Login Page](./public/screenshot-2.png)
![Upload Page](./public/screenshot-3.png)
![Analysis Page](./public/screenshot-4.png)

---

## 🔧 Getting Started

### 1️⃣ Clone the repository

```bash
git clone https://github.com/kishorekrrish3/AI-Resume-Analyzer.git
cd AI-Resume-Analyzer
```

### 2️⃣ Install dependencies

```bash
npm install
```

### 3️⃣ Start development server

```bash
npm run dev
```

### 4️⃣ Open in browser

```
http://localhost:5173
```

---

## 🔐 Environment Variables

If you use Puter workers or server-side tokens, create `.env`:

```
PUTER_API_KEY=your_key_here
PUTER_WORKER_ID=your_worker_id_here
VITE_APP_BASE_URL=http://localhost:5173
```

*(Puter.js often requires no keys for basic usage.)*

---

## 🐳 Docker

### Build image

```bash
docker build -t ai-resume-analyzer .
```

### Run container

```bash
docker run -p 3000:3000 ai-resume-analyzer
```

---

## ☁️ Deploying with Puter

1. Go to Puter dashboard
2. Link GitHub repo or upload the `/dist` build
3. Add environment variables (if used)
4. Publish — Puter gives you a live link instantly
5. AI + file storage is auto-managed 🎉

---

## 🛣️ Roadmap

* Add resume history & versioning
* Support multi-page resume parsing
* Export analysis as PDF
* User login + dashboards (via Puter Auth)
* Choice of LLM model
* Analytics (PostHog)

---

## 🤝 Contributing

1. Fork the repo
2. Create a feature branch
3. Run locally → make your changes
4. Submit PR with description

---

## 👤 Author

**Kishore P**
AI & ML Enthusiast • Full-Stack Developer
VIT Chennai
