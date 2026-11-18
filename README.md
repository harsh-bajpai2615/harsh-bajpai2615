# Harsh Bajpai

AI product developer at DigiFab Media LLP. I build products end to end, usually as the only
developer: the data model, the AI pipeline, the app and the deploy. Five of them are live right
now

Studying at IIM Mumbai (BS Digital Science and Business Management) and IIT Madras (BS Data
Science). Based in Rewa, India

[![LeetCode](https://img.shields.io/badge/LeetCode-Guardian%20%7C%202606-FFA116?style=flat&logo=leetcode&logoColor=black)](https://leetcode.com/u/Harsh2615/)
[![Codeforces](https://img.shields.io/badge/Codeforces-Expert-1F8ACB?style=flat&logo=codeforces&logoColor=white)](https://codeforces.com/profile/Dilha_1526)
[![CodeChef](https://img.shields.io/badge/CodeChef-6%20star%20%7C%202225-5B4638?style=flat&logo=codechef&logoColor=white)](https://www.codechef.com/users/harsh_bajpai)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/harsh-bajpai2007)

## Working on now

**Aavaran**, a browser agent that never sees your personal data. Smart India Hackathon 2026,
problem SIH26171 (ISRO)

A small model runs inside the browser and swaps every PAN, Aadhaar number, card, password and
face on the page for a tag before anything leaves the machine. A bigger self-hosted model reads
the censored page and sends back one instruction, like "click Submit", which the browser carries
out

- Face detection and a MobileViT crop classifier run on WebGPU in the browser, about 10 ms a crop, with a WASM fallback
- Each PII match has to pass a real checksum (Verhoeff for Aadhaar, Luhn for cards, PAN, GSTIN and IFSC structure), so order numbers don't get flagged
- The real values stay in a local vault, so the agent can fill a field it was never allowed to read
- Qwen2.5-VL 7B on Ollama behind FastAPI. Released as v0.4.0 for Chrome and Firefox, 32 tests

TypeScript, ONNX Runtime Web, FastAPI, Ollama. The repo is private until judging ends, happy to demo it

## Shipped products

**The Joy Lane**, wedding vendor marketplace and planner SaaS. [thejoylane.in](https://thejoylane.in)

- Lists 8,000+ vendors, with a ₹999/month planner for vendor leads, proposals, contracts and invoices
- Quotes come from a deterministic price engine. The LLM only turns the user's text into a request, so it can't make up a price
- RBAC, JWT with server-side revocation, TOTP 2FA, phone OTP signup, rate limits. 340+ tests
- Gemini and Claude sit behind one interface and swap without code changes
- My own analytics layer: 3,100+ events over 2,700+ sessions so far

FastAPI, Postgres, Next.js, React 19, Docker, nginx

**Amora**, AI companion app for iOS and Android. [Google Play](https://play.google.com/store/apps/details?id=com.nexralabs.amora)

- One Flutter codebase for both stores: streaming chat, voice calls, image generation
- A Node proxy in front of Gemini holds the keys and the rate limits, the app never sees a key
- I did the release work myself: signed bundle, legal pages, content rating, data safety, live SKUs. 57 tests

**Luvz**, consumer AI companion web platform. [luvz.ai](https://luvz.ai)

- Next.js 15, Firebase and FastAPI: characters, real-time chat and voice, image generation, live video rooms, admin console, help centre
- Generated video at $0.047 a clip on a self-hosted diffusion pipeline on rented A6000s
- Tiers, daily quotas and a token ledger all enforced on the server
- Tracked down a WebKit autoplay bug (`play()` at `readyState 0` gets stuck needing a gesture) and built gapless video chaining on top

**NicheLock**, domain acquisition scout for DigiFab, runs every night

- Sweeps 300 niches a night, has classified 34,000+ domains and keeps 7,600+ listings current
- A serve guard refuses to publish stale data, with 86 smoke checks in the container and 48 local tests
- Found that a rate-limit refusal was being saved as "no snapshot exists" for 10,782 domains. Refusals are now retried instead of recorded

**ClipTrip**, turns 5 to 20 raw travel clips into Reels and long YouTube cuts

- 7 stages on FastAPI, Celery and Redis: Gemini clip analysis and edit plan, beat-synced cuts with librosa, 9:16 reframing with OpenCV and YuNet, captions, ffmpeg render at -14 LUFS
- Captions in Hindi, Marathi, Nepali and Hinglish
- Retries with alerts, per-job locks and saved progress, so a long render doesn't quietly die
- Per-trip cost ledger capped at about ₹40 a reel. 108 tests, on DigitalOcean

**EZHEALTH**, emergency health alert device (2022)

Built at 14 in an Atal Tinkering Lab and presented to the Prime Minister. A NodeMCU sends pulse
and temperature to the cloud every 15 s and emails and calls doctors and family when a reading
goes out of range. Custom PCB in a 3D-printed case, about ₹1,800 to build. Gold Award at INEX
2022 representing India, covered by The Logical Indian and DD News. [Demo](http://tinyurl.com/ezhealth-pm)

## Open source

| Repo | What it does |
| --- | --- |
| [GitKosh](https://github.com/harsh-bajpai2615/gitkosh) | macOS DSA workspace: NeetCode 150 and Blind 75 in an editor with AI review, company-wise questions for 657 companies, mock interviews, revision, and auto-sync of LeetCode, Codeforces, CodeChef, AtCoder and GfG solves to GitHub. Python |
| [LeadNest](https://github.com/harsh-bajpai2615/leadnest) | Lead management app: public capture feeding a pipeline with assignment, stages, notes and an activity log, with roles checked on client and server. [Live demo](https://leadnest-flame.vercel.app). Next.js 16, Prisma 7 |
| [M1005MacDriver](https://github.com/harsh-bajpai2615/M1005MacDriver) | Driver for the HP LaserJet M1005 MFP on Apple Silicon. One installer with foo2zjs and Ghostscript, no Homebrew. I needed it for my own printer |
| [PdfTextEdit](https://github.com/harsh-bajpai2615/PdfTextEdit) | Changes words inside a PDF and keeps them as real text by rewriting the content stream instead of covering it with a white box. Checks the result by diffing the render. Python |
| [DeckKit](https://github.com/harsh-bajpai2615/DeckKit) | Builds animated teaching decks as real .pptx files: click reveals, a clickable mind map, quiz slides. pptxgenjs can't write animations, so a second pass adds the timing XML. Node, Python |
| [CommitConstellation](https://github.com/harsh-bajpai2615/CommitConstellation) | Draws a repo's commit history as a night sky. Files that change often are bigger stars, files that change together are joined. [Live demo](https://harsh-bajpai2615.github.io/CommitConstellation/). No dependencies |
| [CompetitiveProgramming](https://github.com/harsh-bajpai2615/CompetitiveProgramming) | My C++ solutions from Codeforces, LeetCode and CodeChef |

## Also built

- **Shloka**, an offline Android app of devotional shlokas, made for my mother
- **MPCA Match Referee**, a Hindi Android app for my father's cricket match referee exam, with two printed study booklets (100 and 126 pages) typeset from the official forms
- **[SignalExport](https://github.com/harsh-bajpai2615/SignalExport)**, decrypts the Signal Desktop database and exports each chat to HTML and JSON with photos, video, audio and reactions
- **[HindiTts](https://github.com/harsh-bajpai2615/HindiTts)**, turns a scanned devotional PDF into chapter MP3s locally. The text was in the Krutidev legacy font, so it needed a glyph-level converter to Unicode first
- **class-notes**, a Whisper pipeline that turns lecture recordings into class notes

## Tech

- **Languages:** Python, TypeScript, C++, Dart, Java, Rust, SQL
- **AI:** Gemini, Claude, ONNX Runtime, Ollama, RAG, on-device inference with WebGPU, generative media pipelines
- **Backend:** FastAPI, Celery, Redis, Postgres, Prisma, Docker, nginx, pytest
- **Frontend and mobile:** Next.js, React 19, Flutter, Vite, Tailwind
- **Infra:** Linux, DigitalOcean, Vercel, Firebase, AWS S3, ffmpeg

## Experience

**DigiFab Media LLP**, AI Product Developer / Full-Stack Developer. Jun 2026 to present, remote

- Sole developer on the company's AI media and marketplace products, from architecture to production deploy
- Built and run The Joy Lane, ClipTrip and NicheLock (above)
- AI workflows with strict JSON parsing, fallbacks and per-job cost tracking that caps spend at about ₹40 an output
- Long jobs use Celery retries with alerts, per-job locks and saved progress, deployed blue/green with health-checked rollback

**Meta**, Content Review Intern, Trust and Safety. Apr 2020 to Jan 2022, remote

- Reviewed and classified 1,000+ pieces of content in Meta's Single Review Tool at 98% accuracy against policy
- Handled sensitive and policy-violating material at volume, to strict accuracy targets

**Appen**, Independent Contractor, AI Data and NLP. Mar 2020 to Sep 2022, remote

- Refined 500+ prompts for AI training datasets, improving accuracy and safety
- Built the quality checklists reviewers used across multilingual projects

**Mathematics mentor**, independent. Apr 2025 to Jul 2025

- Mentored 50+ students for IOQM: 10 cleared it and 4 went on to RMO

## Education

- **IIM Mumbai**, BS Digital Science and Business Management, 2026 to 2030
- **IIT Madras**, BS Data Science and Applications (online), 2026 to 2030
- **Maa Bharti Senior Secondary School, Kota**, Class XII CBSE (PCM), 2023 to 2025

## Highlights

- LeetCode Guardian, rating 2606, global rank 1027 (top 0.12%). Codeforces Expert. CodeChef 6 star, rating 2225, global rank 233, India 130. AtCoder Cyan
- AIR 3 in IOQM 2022, AIR 69 in UGEE 2025, qualified NSEP, NSEC and NSEA
- EZHEALTH presented to the Prime Minister. Gold Award, INEX 2022, representing India
- Top 20 at TechExpo IIT Guwahati, Top 30 and Top 300 at ATL Marathon, Top 75 at ATL Space Challenge, Young Inventors Challenge (NCSTC), Global Innovation Impact and Communication Awards
- NCC Best Cadet, CATC Sagar, 2023

## How I work

- I like owning the whole thing, from the data model to the deploy
- Anything that has to be exact is computed by normal code, and the LLM only reads intent and writes text. That's why a Joy Lane quote can't invent a price and Aavaran checks a checksum instead of a regex
- I keep test suites I actually run: 340+ on Joy Lane, 108 on ClipTrip, 57 on Amora, 32 on Aavaran
- Every AI job logs what it cost and has a cap
- I check what the user actually gets, not just that the server answered

## Outside code

- English and Hindi
- National level yoga. Tabla (Sangeet Prabhakar), and I've played harmonium at India Gate
- IIT Bombay E-Summit 2023, Maker Fest Vadodara 2024, INEX Goa 2022
- Volunteered with the Vidyanjali platform, Special Campaign 5.0 (2025)

## Contact

Open to remote and contract roles where I can own a product end to end

harshmusic2007@gmail.com, or [LinkedIn](https://linkedin.com/in/harsh-bajpai2007)
