<!--
  GitHub PROFILE README for github.com/harsh-bajpai2615
  Lives in a repo named exactly: harsh-bajpai2615/harsh-bajpai2615
  A few [BRACKETED] links are left for you to fill (CP profiles, portfolio); everything
  else is pulled from your résumé. Phone number intentionally omitted (public page).
-->

# Hi, I'm Harsh Bajpai 👋

### Full-Stack & Generative-AI Engineer — I build and ship AI products end to end.

I take ideas all the way to production — system architecture, multi-stage AI pipelines, the
full-stack app, and the cloud deploy — usually as the **sole developer**. I care about clean
seams (keep the LLM away from anything that must be exact), real tests, and shipping in small,
verified increments.

🎓 Incoming at **IIT Madras** (B.S. Data Science) & **Macquarie University, Sydney** (B.IT) &nbsp;·&nbsp; 💼 AI Product Developer @ **DigiFab Media LLC** &nbsp;·&nbsp; 📍 Rewa, India

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/harsh-bajpai2007)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:harshmusic2007@gmail.com)
&nbsp;
![Codeforces](https://img.shields.io/badge/Codeforces-Expert-1F8ACB?style=for-the-badge&logo=codeforces&logoColor=white)
![LeetCode](https://img.shields.io/badge/LeetCode-Guardian-FFA116?style=for-the-badge&logo=leetcode&logoColor=white)

---

## 🚀 Featured projects

### 🪔 Vivahub — AI-powered wedding & events marketplace &nbsp;·&nbsp; *current*
*One place for every venue and vendor — and an AI that turns a few details into a real, itemised
price in sixty seconds.*

- **Trustworthy by design** — a **deterministic pricing engine** computes every number; the LLM only
  parses intent and writes prose, so a quote can never *hallucinate* a price.
- **A learning loop** — completed escrow bookings feed real transacted prices back into the engine
  (empirical-Bayes calibration), so quotes sharpen with use.
- **Where users actually are** — WhatsApp-native quote + vendor-onboarding bots, escrow bookings,
  reviews, a vendor dashboard, and programmatic SEO pages.
- **Provider-pluggable AI** — swap Gemini ↔ Claude with one env var, with a live cost ledger metering
  every call. **34 passing tests.**

`FastAPI` · `SQLAlchemy / Postgres` · `React 19 + Vite + Tailwind` · `Gemini / Claude` · `WhatsApp Cloud API` · `escrow payments`

### 🎬 ClipTrip — AI travel-video generator (Reels + YouTube) &nbsp;·&nbsp; *2026*
*Turns 5–20 raw travel clips into ready-to-post 20–40s 9:16 Reels and long-form 16:9 cuts —
AI handles footage understanding, narrative editing, captions, and music.*

- **7-stage pipeline** (FastAPI + Celery + Redis): Gemini per-clip analysis & edit-planning,
  **librosa** beat-synced cutting, saliency-aware 9:16 reframing (**OpenCV / YuNet**), and **ffmpeg**
  render with −14 LUFS loudness-normalised audio.
- React 19 + Tailwind frontend with a light video editor, usage metering, tiered INR pricing &
  Razorpay; Dockerised on DigitalOcean with **per-trip cost ledgers (~₹40/reel)**, auto-retry
  alerting, and **26 passing tests**.

`FastAPI` · `Celery + Redis` · `Gemini` · `librosa` · `OpenCV` · `ffmpeg` · `React 19` · `Razorpay` · `DigitalOcean`

### ❤️ EZHEALTH — emergency healthcare alert system &nbsp;·&nbsp; *2022*
*An IoT remote health-monitoring device that streams vitals to the cloud and auto-alerts doctors
in a crisis — **presented to the Prime Minister of India**.*

- NodeMCU / ESP8266 device streaming **Pulse Rate & Temperature every 15s**, auto-alerting doctors by
  email and phone call on abnormal readings (>140 BPM / >37 °C).
- Full custom hardware: 95%-accurate sensors on a custom PCB in a 3D-printed enclosure.
- 🥇 **Gold Award, INEX International Innovation & Invention Expo 2022** (represented India). &nbsp; [Demo](http://tinyurl.com/ezhealth-pm)

---

## 🧰 Tech I work with

**Languages**&nbsp;
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat&logo=rust&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)

**AI / ML**&nbsp;
![Gemini](https://img.shields.io/badge/Google%20Gemini-8E75B2?style=flat&logo=googlegemini&logoColor=white)
![Claude](https://img.shields.io/badge/Claude-D97757?style=flat&logo=anthropic&logoColor=white)
&nbsp;LLM orchestration · prompt engineering · RAG · generative-AI media pipelines · NLP

**Backend**&nbsp;
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat&logo=celery&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![Postgres](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

**Frontend**&nbsp;
![React](https://img.shields.io/badge/React%2019-61DAFB?style=flat&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat&logo=tailwindcss&logoColor=white)

**Tools & Cloud**&nbsp;
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)
![DigitalOcean](https://img.shields.io/badge/DigitalOcean-0080FF?style=flat&logo=digitalocean&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS%20S3-569A31?style=flat&logo=amazons3&logoColor=white)
![ffmpeg](https://img.shields.io/badge/ffmpeg-007808?style=flat&logo=ffmpeg&logoColor=white)

---

## 🏆 Highlights

- 🧮 **Competitive programming:** Codeforces **Expert** · LeetCode **Guardian** · CodeChef **6★**
- 🎯 **AIR 44** in JEE Mains 2026 · **AIR 3** in IOQM 2022 · AIR 856 JEE Advanced 2025 · AIR 69 UGEE 2025
- 🥇 **EZHEALTH presented to the Prime Minister of India**; Gold Award at INEX 2022 (represented India)
- 🎓 Dual undergraduate degree — **IIT Madras** (Data Science) **+ Macquarie University, Sydney** (IT)
- 🤝 Mentored **50+ students** for the Indian Olympiad Qualifier in Mathematics (IOQM)

---

## 🎓 Education & 💼 Experience

**Education**
- **IIT Madras** — B.S. in Data Science & Applications · *2026 – 2030*
- **Macquarie University, Sydney** — Bachelor of Information Technology · *2026 – 2029*

**Experience**
- **DigiFab Media LLC** — AI Product Developer / Full-Stack Developer · *2026 – present* — own end-to-end
  development of AI media products as sole developer, from architecture to production deployment.
- Earlier: AI data & NLP contracting (**Appen**, 500+ prompts refined), content review (**Meta**, 1,000+
  items at 98% accuracy), and mathematics mentoring.

---

## 📫 Let's talk

Open to roles where I can own real product end to end.
📧 **harshmusic2007@gmail.com** &nbsp;·&nbsp; 💼 [LinkedIn](https://linkedin.com/in/harsh-bajpai2007)
