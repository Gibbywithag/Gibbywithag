# Hi, I'm Gilbran 👋

**Software & AI Engineer** · Full-Stack · AI/ML · AI Video & Media Tooling · Nashville, TN

I ship end-to-end AI products, from model integration to serverless backends to
mobile apps. By day I produce broadcast/field video for Metro Nashville government; on my
own I taught myself to build the AI tools that automate that kind of media work.

**Right now:** 15 services running unattended in production on one Mac mini: trading bots moving
real money, an on-device vision system, media pipelines, and the watchdog that texts me when any
of them fail. ~137,000 lines across 24 repositories, ~2,150 commits.

🔗 **Portfolio:** https://gilbran-laureano.pages.dev
💼 **LinkedIn:** https://www.linkedin.com/in/gilbran-laureano-372a29189/
📫 **Email:** gilbranlaureano0417@gmail.com

---

### 🚀 Featured projects

Ordered by technical depth. Every row links to the code or, where the code is private, to an architecture writeup.

| Project | What it is | Stack |
|---|---|---|
| **[Overseer](https://github.com/Gibbywithag/overseer-architecture)** | Text your Mac and Claude Code fixes it. Runs read-only plan mode first, texts back a diagnosis, then waits for explicit approval before changing anything. Two-phase propose/apply, because a text conversation would time out a blocking permission hook. Also watches every launchd job and texts first when one fails | Python · Claude Code SDK · launchd · SQLite |
| **[Nursery Vision System](https://github.com/Gibbywithag/family-ops-dashboard/tree/main/mini/nursery-brain)** | On-device computer vision. RTSP through go2rtc, a motion gate and 16×16 grayscale signature to reject still frames, then a local vision-language model answers what matters. Frames downscale 2K→640px because the model needs gestalt, not detail. Seven coordinated services, fully offline | Node.js · Qwen2.5-VL · Ollama · go2rtc · ONVIF |
| **[Trading Systems: protocol & results](https://github.com/Gibbywithag/prediction-market-research)** | Three prediction-market systems on Kalshi. One live with a −20%/day kill switch and 3-loss breaker; two shelved by their own pre-registered gates, including one that looked like a +7.38¢ win until the holdout came back n=81 with 69% of the edge from a single day. 417/417 trades verified free of lookahead | Python · pre-registered protocol · walk-forward |
| **[F1 Clipper](https://github.com/Gibbywithag/f1-clipper-architecture)** | 26k-line pipeline turning race broadcasts into ready-to-post vertical clips. Gemini finds the moments, YOLO tracks the car so the 9:16 crop follows the action, radio quotes become graphic cards, and clips are split by copyright exposure so safe content goes everywhere. FastAPI service with a job queue driving ffmpeg workers | Python · FastAPI · Gemini · YOLO · Whisper · ffmpeg · React |
| **[Myla Dashboard](https://github.com/Gibbywithag/family-ops-dashboard)** | Private health dashboard for my daughter. Live Owlet vitals through a Cloudflare Durable Object loop, WebAuthn passkey auth, and honest sensor states (not connected / charging / stale) instead of inventing a number | TypeScript · Next.js · Cloudflare Workers/D1 · Drizzle |
| **[Telegram → MT5 Signal Copier](https://github.com/Gibbywithag/mt5-signal-copier-architecture)** | Built for an external stakeholder. Mirrors a signals channel onto a live MetaTrader 5 account. The safety rails are the product: dry-run mode, risk-percent sizing, max open trades, daily-loss circuit breaker, and a hard refusal on any signal lacking a stop. Rails enforced inside an MQL5 EA, plus a reconciler that checks the bot against the real account | Python · Telethon · MetaTrader 5 · MQL5 |
| **[Prediction Radar](https://github.com/Gibbywithag/prediction-radar)** | Smart-money tracker for Polymarket and Kalshi. Scores whale and exchange signals, alerts via Discord and AI-gated iMessage, and grades its own track record by tracking how every alert resolves | Python · Polymarket · Kalshi · Discord |
| **[Cutback: architecture](https://github.com/Gibbywithag/cutback-architecture)** | Live offline-first weight tracker with no backend and no database, so health data never leaves the device. Public endpoints defended with an origin allowlist, per-request token ceilings and documented spend caps, with the residual risk written down. 128 tests on the core math | React · Vite · Cloudflare Pages Functions · Gemini |
| **[SermonNoteClipper](https://github.com/Gibbywithag/SermonNoteClipper)** | Turns long videos into 9:16 social clips: scene detection + YOLO + Whisper + LLM moment selection | Electron · Python · YOLO · faster-whisper · Gemini |
| **[MNN Clip Namer](https://github.com/Gibbywithag/mnn-clip-namer)** | Mac/Win desktop app that auto-names broadcast clips with GPT-4o vision; zero-setup via a Cloudflare Workers key proxy. Used weekly by 4 to 5 people | Electron · TypeScript · OpenAI · Cloudflare |
| **[PageTrail](https://apps.apple.com/us/app/page-trail/id6760310383)** | Native SwiftUI app **live on the App Store** generating grade-leveled K-12 children's stories via an LLM; StoreKit 2 subscriptions + Cloudflare Workers backend keeping the API key off-device | Swift · SwiftUI · StoreKit 2 · LLM |
| **[Chef Pal](https://github.com/Gibbywithag/chef-pal-architecture)** | iOS app suggesting meals from what is actually in the pantry, with defrost reminders and household sync across two phones. API keys stay server-side behind an edge-function proxy | SwiftUI · SwiftData · Supabase · Claude API |
| **[App Factory](https://github.com/Gibbywithag/app-factory)** | Landing page and Stripe checkout for custom iOS app builds. Payment session created server-side so no key reaches the browser. [Live](https://app-factory-olive.vercel.app) | Stripe · Vercel serverless |

---

### 🛠️ Tech

**Languages:** Python · TypeScript · JavaScript · Swift · SQL
**Frontend:** React · Next.js · Vite · Tailwind · Electron
**Backend/Cloud:** FastAPI · Node.js · Cloudflare Workers · Vercel · Docker
**AI/ML:** OpenAI · Gemini · YOLO/Ultralytics · Whisper · PyTorch · multi-agent pipelines
**Mobile:** Swift · SwiftUI · StoreKit 2 · iOS

---

*Open to remote software & AI engineering roles.*
