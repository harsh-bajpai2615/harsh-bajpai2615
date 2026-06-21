<!--
  GitHub PROFILE README for github.com/harsh-bajpai-2615 (repo: harsh-bajpai2615/harsh-bajpai2615)
  Phone intentionally omitted (public page). Codeforces/LeetCode badges are visual until handles are added.
-->

# Hi, I'm Harsh Bajpai 👋

### Full-Stack & Generative-AI Engineer — I build and ship AI products end to end.

I take ideas all the way to production — system architecture, multi-stage AI pipelines, the
full-stack app, and the cloud deploy — usually as the **sole developer**. I care about clean
seams (keep the language model away from anything that must be exact), real tests, and shipping
in small, verified increments.

I come from a **competitive-programming and olympiad** background — Codeforces Expert, AIR 3 in the
Indian Maths Olympiad Qualifier, AIR 74 in JEE Advanced 2026 — which shows up in how I reason about
systems, edge cases, and performance. These days I spend most of my time building **production
generative-AI products**: LLM orchestration, generative-media pipelines, and the full-stack apps and
cloud infrastructure around them.

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

## 💼 Experience

### DigiFab Media LLC — AI Product Developer / Full-Stack Developer
*Jun 2026 – Present · Remote*
- Own **end-to-end** development of AI-powered media products as the **sole developer** — from system
  architecture and multi-stage AI pipelines to the full-stack app and production cloud deployment.
- Build production generative-AI workflows around LLMs (Google Gemini) and generative-media APIs with
  **hardened JSON parsing, graceful fallbacks, and per-job cost telemetry that caps AI spend (~₹40/output)**.
- Engineer reliability for long-running media jobs — Celery auto-retry with failure alerts, per-job
  locking, and durable progress — shipping features in small, tested increments to `main`.

### Meta — Content Review Intern · Trust & Safety
*Apr 2020 – Jan 2022 · Remote*
- Reviewed and classified **1,000+ pieces of online content** using Meta's **Single Review Tool (SRT)**,
  sustaining a **98% accuracy rate** against platform policy at high throughput.
- Enforced platform **trust & safety** standards during **large-scale content-moderation operations** —
  identifying and flagging sensitive and policy-violating material (e.g. graphic, hateful, or misleading
  content) and applying nuanced policy judgement under tight quality and time targets.
- Helped keep content surfaces safe for a global user base, working to strict precision and consistency
  benchmarks on a remote moderation team.

### Appen — Independent Contractor · AI Data & NLP
*Mar 2020 – Sep 2022 · Remote*
- Evaluated and refined **500+ AI dataset prompts**, improving dataset accuracy and safety for
  language-focused annotation and model-training tasks.
- Built scalable **quality-assurance frameworks** to streamline multilingual review and annotation
  workflows.

### Mathematics Mentor — Independent
*Apr 2025 – Jul 2025*
- Mentored **50+ students** in advanced problem-solving (number theory, combinatorics, geometry) for the
  Indian Olympiad Qualifier in Mathematics (IOQM), designing simplified curricula that lifted performance.

---

## 🎓 Education

- **Indian Institute of Technology, Madras** — B.S. in Data Science & Applications · *2026 – 2030*
- **Macquarie University, Sydney, Australia** — Bachelor of Information Technology · *2026 – 2029*
- **Senior Secondary (Class XII), CBSE — Kota, Rajasthan** — Physics, Chemistry, Mathematics · *2023 – 2025*

---

## 🏆 Highlights & achievements

- 🧮 **Competitive programming** — Codeforces **Expert** · LeetCode **Guardian** · CodeChef **6★**
- 🎯 **AIR 74 — JEE Advanced 2026** · **AIR 44 — JEE Mains 2026** · **AIR 3 — IOQM 2022** · AIR 69 — UGEE 2025
- 🥇 **EZHEALTH presented to the Prime Minister of India** · **Gold Award**, INEX International Innovation &
  Invention Expo 2022 (represented India)
- 🏅 Top 100 — ATL Marathon 2022-23 · Top 20 — TechExpo, IIT Guwahati · Global Innovation **Impact** &
  **Communication** Awards (Invent Future Global)
- 🎓 Pursuing a **dual undergraduate degree** — IIT Madras (Data Science) + Macquarie University, Sydney (IT)

---

## 🛠️ How I work

- **Ship end to end.** I'm comfortable owning a product from the data model to production.
- **Test what matters.** Real, focused test suites — I trust code I can re-run, not vanity coverage.
- **Clear seams.** Keep the language model away from anything that must be exact; make providers
  swappable; meter what you spend. Boring, well-bounded systems beat clever fragile ones.
- **Build for reality.** The channel users actually use, the cost per call, the unit economics —
  not just the happy path.

---

## 🌟 Beyond the code

- 🗣️ **Languages** — English, Hindi
- 🎼 **Interests** — National-level **Yoga** · **Tabla** (Sangeet Prabhakar)
- 🎤 **Conferences** — IIT Bombay E-Summit (2023) · Maker Fest, Vadodara (2024) · INEX Innovation Expo, Goa (2022)
- 🤝 **Volunteering** — Vidyanjali Platform, Special Campaign 5.0 (2025)

---

## 📫 Let's talk

I'm open to roles where I can own real product end to end.
📧 **harshmusic2007@gmail.com** &nbsp;·&nbsp; 💼 [LinkedIn](https://linkedin.com/in/harsh-bajpai2007)
