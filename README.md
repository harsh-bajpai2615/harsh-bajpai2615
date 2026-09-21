<!--
  GitHub PROFILE README — github.com/harsh-bajpai2615 (repo: harsh-bajpai2615/harsh-bajpai2615)
  Phone intentionally omitted (public page). All competitive-programming badges link to verified profiles.
-->

# Hi, I'm Harsh Bajpai 👋

### AI Product Developer · Full-Stack & Generative-AI Engineer

I take products from an empty repo to something real people use — architecture, multi-stage AI
pipelines, the full-stack app, and the production deploy — usually as the **sole developer**.
Four products of mine are live right now: a wedding marketplace, an app on Google Play, a
consumer AI platform, and an internal tool that runs unattended every night.

I care about **clean seams** — keep the language model away from anything that must be exact —
real tests over vanity coverage, and shipping in small verified increments.

🎓 **IIM Mumbai** (B.S. Digital Science & Business Management) **+ IIT Madras** (B.S. Data Science) &nbsp;·&nbsp;
💼 AI Product Developer @ **DigiFab Media LLP** &nbsp;·&nbsp; 📍 Rewa, India

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/harsh-bajpai2007)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:harshmusic2007@gmail.com)
&nbsp;
![LeetCode](https://img.shields.io/badge/LeetCode-Guardian%20%7C%202606-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)
[![Codeforces](https://img.shields.io/badge/Codeforces-Expert-1F8ACB?style=for-the-badge&logo=codeforces&logoColor=white)](https://codeforces.com/profile/Dilha_1526)
[![CodeChef](https://img.shields.io/badge/CodeChef-6%E2%98%85-5B4638?style=for-the-badge&logo=codechef&logoColor=white)](https://www.codechef.com/users/harsh_bajpai)

---

## 🔭 What I'm building right now

### 🛡️ Aavaran — a browser agent that never sees your PII &nbsp;·&nbsp; *Smart India Hackathon 2026 · SIH26171 (ISRO / Dept. of Space)*

*A small model runs **inside your browser**, reads the page, and replaces every PAN, Aadhaar
number, card, password and face with a typed tag — **before any network request is made**.
A larger open-weight model reasons over the censored page and returns one instruction
("click Submit") that your browser carries out. The server does the thinking. It never learns
your PAN, your account number, or what you look like.*

- **Two on-device ONNX models, in the browser.** A face detector and **MobileViT-small** crop
  classifier run on **WebGPU** (~10 ms/crop) with a measured WASM fallback — because the DOM
  can tell you an `<img>` exists but not that there's a human being in it.
- **Checksums are the differentiator, not regexes.** `/\d{12}/` flags every order number on the
  page and torches precision. Aavaran gates each candidate on a real validator — **Verhoeff**
  for Aadhaar, **Luhn** for cards, plus PAN / GSTIN / IFSC / Indian-mobile structure — turning a
  recall-heavy pattern into a precision-heavy detector.
- **Redaction is reversible, locally.** Detected values go to a typed tag (`<PAN_1>`) with the
  real value held in a client-side vault, so the agent can still *fill* a field it was never
  allowed to *read*.
- **Reasoning stays open-weight and self-hosted** — Qwen2.5-VL 7B on Ollama behind a FastAPI
  server, warmed and held resident (~17 s cold, ~4 s warm).
- **Shipped as a real release** — **v0.4.0**, Chrome (MV3) + Firefox builds, one-command
  `setup.sh`, **32/32 tests green**, TypeScript at **0 errors** with the gate covering every one.

`TypeScript` · `ONNX Runtime Web / WebGPU` · `Chrome MV3 + Firefox` · `FastAPI` · `Ollama / Qwen2.5-VL` · `esbuild`

> Repo is private through the SIH judging window — happy to walk through the code or demo it.

---

## 🚀 Shipped products

### 🪔 The Joy Lane — wedding-services marketplace & planner SaaS &nbsp;·&nbsp; [`thejoylane.in`](https://thejoylane.in) &nbsp;·&nbsp; *live*

*One place for every venue and vendor — and an AI that turns a few details into a real, itemised
price in sixty seconds.*

- **A live two-sided platform listing 8,000+ vendors** — SEO-prerendered marketplace pages, plus a
  **₹999/month planner SaaS** carrying vendor leads, proposals, contracts and invoicing.
- **Quotes are reproducible, not hallucinated.** A **deterministic quote engine** does
  occasion-aware selection over calibrated price bands; the LLM only parses free text into a
  structured request. A quote can never invent a number.
- **Hardened end to end** — RBAC, JWT with **server-side revocation**, TOTP 2FA, phone-OTP signup,
  rate limiting, on Docker + nginx — behind **340+ automated tests**.
- **No LLM vendor lock-in** — the provider sits behind one interface; **Gemini or Claude swap
  without a code change**.
- **I built the analytics layer myself**, so live usage and failures are visible in-product —
  **3,100+ events over 2,700+ unique sessions**, per-page breakdowns and error tracking.

`FastAPI` · `Postgres` · `Next.js` · `React 19 + Tailwind` · `Gemini / Claude` · `Docker + nginx`

### 📱 Amora — AI companion app, iOS + Android &nbsp;·&nbsp; [`Google Play`](https://play.google.com/store/apps/details?id=com.nexralabs.amora) &nbsp;·&nbsp; *live*

- **One Flutter codebase to both stores** — streaming chat, low-latency voice calls and a
  generated-image pipeline, served over a **Node proxy** fronting Gemini that holds key custody
  and enforces rate limits (the client never sees a key).
- **Release engineering owned end to end** — signed App Bundle, HTTPS legal pages, content-rating
  and data-safety declarations, live SKUs (₹499/mo · ₹2,999/yr).
- **Every build releasable** behind **57 passing tests** plus analyzer and type-check gates, with
  all store artwork generated from a single script.

`Flutter / Dart` · `Node proxy` · `Gemini` · `Play Console release engineering`

### 💬 Luvz — consumer AI companion web platform &nbsp;·&nbsp; [`luvz.ai`](https://luvz.ai) &nbsp;·&nbsp; *live*

- **A full consumer platform** on **Next.js 15 + Firebase + FastAPI** — character catalogue,
  real-time chat and voice, image generation, live video rooms, an admin console and a
  27-article help centre.
- **Generated video at $0.047/clip** (~$1.50–2 per episode) via a self-hosted diffusion pipeline
  on rented A6000 GPUs — automated shot generation, upscaling, VO timing, caption/music assembly.
- **Monetisation enforced server-side** — tier-gated characters, per-day quotas, a token ledger,
  and an idempotent, probe-verified paywall.
- **Root-caused a WebKit autoplay latch** that broke hands-off desktop video (`play()` at
  `readyState 0` latches gesture-required), then shipped gapless chaining on top.

`Next.js 15` · `Firebase` · `FastAPI` · `self-hosted diffusion` · `A6000 GPUs`

### 🔎 NicheLock — autonomous domain-acquisition scout &nbsp;·&nbsp; *DigiFab · runs nightly*

- **Sweeps 300 niches every night, unattended** — classifies **34,000+ domains** against a live
  snapshot store and keeps **7,600+** vetted listings current, with expiry state tracked so a
  dead listing never shows as live.
- **A guard that refuses to serve stale data** — `serve_guard` gates the feed, backed by **86
  in-container smoke checks** plus 48 local tests, because an unattended system that fails
  quietly is worse than one that stops.
- **Hard-won lesson baked in:** a rate-limit refusal was being stored as the permanent fact
  *"no snapshot exists"* — poisoning 10,782 domains. Now a refusal is retried, not recorded.

`Python` · `Docker` · `nightly scheduling` · `snapshot-diff classification`

### 🎬 ClipTrip — AI travel-video generator (Reels + YouTube) &nbsp;·&nbsp; *live*

*Turns 5–20 raw travel clips into ready-to-post 20–40 s 9:16 Reels and long-form 16:9 cuts.*

- **A 7-stage AI pipeline** on **FastAPI + Celery + Redis**: Gemini per-clip analysis and
  narrative edit-planning → **librosa** beat-synced cutting → saliency-aware 9:16 reframing
  (**OpenCV / YuNet**) → caption rendering → **ffmpeg** render at −14 LUFS.
- **Regional captions** — Hindi, Marathi, Nepali and Hinglish, with the glyph and shaping layers
  proved separately offline.
- **Long jobs survive failure** — Celery auto-retry with alerting, per-job locking, durable
  progress, so a multi-minute render never silently dies.
- **Cost-aware** — per-trip ledgers cap spend at **~₹40 per reel**; **108 passing tests**,
  Dockerised on DigitalOcean.

`FastAPI` · `Celery + Redis` · `Gemini` · `librosa` · `OpenCV` · `ffmpeg` · `React 19` · `Razorpay`

### ❤️ EZHEALTH — emergency healthcare alert system &nbsp;·&nbsp; *2022*

*An IoT device that streams vitals to the cloud and auto-alerts doctors in a crisis — built at
**age 14** in an Atal Tinkering Lab, and **presented to the Prime Minister of India**.*

- NodeMCU / ESP8266 streaming **pulse and temperature to the cloud every 15 s**; out-of-range
  readings trigger an **automatic email and VoIP call** to doctors and relatives.
- 95%-accurate sensors on a **custom-designed PCB** in a 3D-printed enclosure — a **~₹1,800** build.
- 🥇 **Gold Award**, INEX International Innovation & Invention Expo 2022 (represented India) ·
  presented at **Pariksha Pe Charcha** · covered by The Logical Indian and DD News ·
  recognised by the Atal Innovation Mission. &nbsp;[Demo](http://tinyurl.com/ezhealth-pm)

`C++` · `Arduino` · `NodeMCU / ESP8266` · `custom PCB` · `IoT sensors`

---

## 📦 Open-source repos

| Repo | What it is |
| --- | --- |
| **[gitkosh](https://github.com/harsh-bajpai2615/gitkosh)** | A macOS DSA workspace — NeetCode 150 + Blind 75 in a built-in editor with streaming AI review, most-asked questions for **657 companies**, mock-interview mode with a scorecard, an algorithm visualizer, spaced-repetition revision, and auto-sync of your LeetCode / Codeforces / CodeChef / AtCoder / GfG solves to GitHub with AI-written per-problem write-ups. `Python` · macOS app |
| **[leadnest](https://github.com/harsh-bajpai2615/leadnest)** | A lead *platform*, not a lead form — public capture feeds an authenticated pipeline with assignment, stages, notes and a full activity trail; admin/member permissions enforced on **both** client and server. [Live demo](https://leadnest-flame.vercel.app). `Next.js 16 + Prisma 7` |
| **[hp-m1005-macos-driver](https://github.com/harsh-bajpai2615/hp-m1005-macos-driver)** | A working driver for the HP LaserJet M1005 MFP on Apple Silicon — one-command installer bundling foo2zjs/foo2xqx + Ghostscript, no Homebrew needed. Scratched my own itch; turned out a lot of people had it. |
| **[competitive-programming](https://github.com/harsh-bajpai2615/competitive-programming)** | My C++ solutions across Codeforces, LeetCode and CodeChef. |

---

## 🧱 Also built

Smaller things I've shipped — most for a real person with a real problem, which is usually
the best spec you can get.

**📱 Apps**
- **Shloka** — an Android devotional-shloka app built for my mother; offline-first, **46/46 tests** green on every release.
- **MPCA Match Referee** — a Hindi-first Android app for my father's cricket match-referee practical exam. Fully **offline**, v2.5, built as the companion to two printed study booklets (100 pp theory + 126 pp practical) I typeset from the official forms.

**🛠️ Developer & document tooling**
- **pdf-text-edit** — changes words *inside* a PDF while keeping them **real, selectable text**. Not a white-box-and-overlay hack; it rewrites the content stream and subsets the font.
- **deck-kit** — a pipeline that builds animated, interactive teaching decks as genuine `.pptx`. Produced five NCERT maths decks (Classes VI–X).
- **signal-export** — decrypts the local Signal Desktop database and exports every conversation to a readable HTML transcript (inline photos, video, audio, stickers, reactions) plus structured JSON.

**🔊 Speech & audio pipelines**
- **Hindi TTS audiobook pipeline** — turns a scanned devotional PDF into per-chapter MP3s, **fully local and free**. The hard part wasn't the speech: the PDF stored text in a **Krutidev legacy font**, so it needed a glyph-level transcoder to Unicode before anything could read it.
- **class-notes** — a Whisper-based pipeline that turns lecture recordings into structured, shareable class notes.

---

## 🧰 Tech I work with

**Languages**&nbsp;
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat&logo=dart&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat&logo=openjdk&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat&logo=rust&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)

**AI / ML**&nbsp;
![Gemini](https://img.shields.io/badge/Google%20Gemini-8E75B2?style=flat&logo=googlegemini&logoColor=white)
![Claude](https://img.shields.io/badge/Claude-D97757?style=flat&logo=anthropic&logoColor=white)
![ONNX](https://img.shields.io/badge/ONNX%20Runtime-005CED?style=flat&logo=onnx&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat&logo=ollama&logoColor=white)
&nbsp;LLM orchestration · RAG · on-device inference (WebGPU) · generative-media pipelines · NLP

**Backend**&nbsp;
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat&logo=celery&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![Postgres](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat&logo=prisma&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![nginx](https://img.shields.io/badge/nginx-009639?style=flat&logo=nginx&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=flat&logo=pytest&logoColor=white)

**Frontend & Mobile**&nbsp;
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React%2019-61DAFB?style=flat&logo=react&logoColor=black)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat&logo=tailwindcss&logoColor=white)

**Tools & Cloud**&nbsp;
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)
![DigitalOcean](https://img.shields.io/badge/DigitalOcean-0080FF?style=flat&logo=digitalocean&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-DD2C00?style=flat&logo=firebase&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS%20S3-569A31?style=flat&logo=amazons3&logoColor=white)
![ffmpeg](https://img.shields.io/badge/ffmpeg-007808?style=flat&logo=ffmpeg&logoColor=white)

---

## 💼 Experience

### DigiFab Media LLP — AI Product Developer / Full-Stack Developer
*Jun 2026 – Present · Remote*
- Own **end-to-end** development of AI-powered media and marketplace products as the **sole
  developer** — architecture, multi-stage AI pipelines, full-stack build, production deploy.
- Built and run **The Joy Lane**, **ClipTrip** and **NicheLock** — see above — each live in
  production and each one mine end to end.
- Ship production generative-AI workflows with **hardened JSON parsing, graceful fallbacks, and
  per-job cost telemetry that caps AI spend (~₹40/output)**.
- Engineer reliability for long-running jobs — Celery auto-retry with alerting, per-job locking,
  durable progress — behind blue/green deploys with health-checked rollback.

### Meta — Content Review Intern · Trust & Safety
*Apr 2020 – Jan 2022 · Remote*
- Reviewed and classified **1,000+ pieces of online content** in Meta's Single Review Tool,
  sustaining **98% accuracy** against platform policy at high throughput.
- Applied nuanced policy judgement on sensitive and policy-violating material during large-scale
  content-moderation operations, to strict precision and consistency benchmarks.

### Appen — Independent Contractor · AI Data & NLP
*Mar 2020 – Sep 2022 · Remote*
- Refined **500+ AI dataset prompts**, improving dataset accuracy and safety for
  language-focused annotation and model-training tasks.
- Built the **quality-assurance frameworks** reviewers worked to across multilingual workflows.

### Mathematics Mentor — Independent
*Apr 2025 – Jul 2025*
- Mentored **50+ students** for the Indian Olympiad Qualifier in Mathematics — **10 cleared IOQM
  and 4 went on to RMO** — designing simplified curricula for number theory, combinatorics and geometry.

---

## 🎓 Education

- **Indian Institute of Management, Mumbai** — B.S. in Digital Science & Business Management · *2026 – 2030*
- **Indian Institute of Technology, Madras** — B.S. in Data Science & Applications (online) · *2026 – 2030*
- **Maa Bharti Senior Secondary School, Kota** — Class XII, CBSE (PCM) · *2023 – 2025*

---

## 🏆 Highlights

- 🧮 **Competitive programming** — LeetCode **Guardian**, rating 2606 (top 1%) · [Codeforces **Expert**](https://codeforces.com/profile/Dilha_1526) · [CodeChef **6★**](https://www.codechef.com/users/harsh_bajpai) · AtCoder **Cyan**
- 🎯 **AIR 3 — IOQM 2022** · AIR 69, UGEE 2025 · qualified **NSEP / NSEC / NSEA**
- 🥇 **EZHEALTH presented to the Prime Minister of India** · **Gold Award**, INEX Innovation & Invention Expo 2022 (represented India)
- 🏅 Top 20, TechExpo IIT Guwahati · Top 30 & 300, ATL Marathon · Top 75, ATL Space Challenge · Young Inventors Challenge (NCSTC) · Global Innovation **Impact** & **Communication** Awards
- 🎖️ **NCC Best Cadet**, CATC Sagar (2023)

---

## 🛠️ How I work

- **Ship end to end.** Data model to production deploy. I'd rather own the whole seam than hand it off.
- **Keep the model away from what must be exact.** Deterministic engines compute the number; the
  LLM parses intent and writes prose. That's why a Joy Lane quote can't hallucinate a price and
  Aavaran's PII detector gates on a checksum, not a regex.
- **Test what matters.** Focused suites I actually re-run — 340+ on Joy Lane, 108 on ClipTrip,
  57 on Amora, 32 on Aavaran — not coverage theatre.
- **Meter what you spend.** Per-job cost ledgers, hard caps, provider abstraction. Unit economics
  are a feature, not an afterthought.
- **Verify the artefact, not the endpoint.** A 200 is not proof. I check the thing users receive.

---

## 🌟 Beyond the code

- 🗣️ **Languages** — English, Hindi
- 🎼 **Interests** — National-level **Yoga** · **Tabla** (Sangeet Prabhakar); played harmonium at India Gate
- 🎤 **Conferences** — IIT Bombay E-Summit (2023) · Maker Fest, Vadodara (2024) · INEX Innovation Expo, Goa (2022)
- 🤝 **Volunteering** — Vidyanjali Platform, Special Campaign 5.0 (2025)

---

## 📫 Let's talk

I'm open to remote and contract roles where I can own real product end to end.

📧 **harshmusic2007@gmail.com** &nbsp;·&nbsp; 💼 [LinkedIn](https://linkedin.com/in/harsh-bajpai2007)
