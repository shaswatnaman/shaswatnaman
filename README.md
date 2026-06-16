<div align="center">

<img src="./assets/banner.svg" alt="Shaswat Naman — Founder-Engineer" width="100%" />

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-shaswatnaman-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/shaswatnaman/)
&nbsp;
![Focus](https://img.shields.io/badge/Focus-iOS_·_AI_·_Product-11151F?style=flat-square)
&nbsp;
![Status](https://img.shields.io/badge/Building-Nureli_@_Soul_Nestle-6366F1?style=flat-square)

</div>

---

### About

I'm a CS undergrad (2nd year) and founder-engineer building human-centered technology where **psychology, AI, and mobile engineering** meet.

I don't just write code for projects — I look for a real human problem, design the system around it, and ship a product people actually use. Most of my work lives at the intersection of **emotional wellness, cultural technology, and applied AI**, backed by clean architecture and a bias toward shipping.

- 🛠️ **Founder-engineer** — own the problem end to end: research → architecture → implementation → iteration
- 📱 **iOS** — Swift / SwiftUI, MVVM, ~27K LOC production app with Supabase + on-device privacy guarantees
- 🤖 **Applied AI** — LLM pipelines with deterministic, auditable safety layers (not black-box wrappers)
- 🧠 **Human-centered** — trauma-informed, research-driven product design with clinical input
- ⚙️ **Systems thinking** — graph algorithms, double-entry ledgers, real-time WebSocket pipelines, RLS data isolation

---

### What I'm building

| | Domain | Project |
|---|---|---|
| 🧠 | **Emotional Wellness Technology** | **Nureli** — iOS app, by Soul Nestle |
| 🪷 | **Cultural / Spiritual Technology** | Private platform — *in stealth* |
| ⚙️ | **Engineering** | Open-source systems, AI tooling & experiments |

---

## ⚙️ Featured Engineering — *public, open work*

> Four recent builds that show range: safety-critical AI, large-scale simulation, financial systems, and AI-for-data.

### 🚑 [Nirnay-112](https://github.com/shaswatnaman/Nirnay-112) — Real-time emergency-call triage (Hindi / Hinglish)
A hybrid pipeline for noisy, code-switched 112 emergency calls: **LLM perception layer + deterministic, explainable decision logic**. Urgency scoring is a transparent weighted formula — *not* a black box — because safety-critical workflows need auditability.

`Python` · `FastAPI` · `WebSockets` · `OpenAI` · `TF-IDF + LogReg` · `Pydantic`
> **Why it matters:** streaming transcripts mid-call, confidence-decay context memory with rollback on contradiction, append-only audit log, and an offline eval harness. Engineering for a domain where being wrong is expensive.

### 🦠 [outbreak-explorer](https://github.com/shaswatnaman/outbreak-explorer) — Epidemic simulation engine at scale
A full-stack SIR epidemic simulator running **50,000–100,000 nodes in <150ms per step** over directed graphs, with live map visualization and risk-proportional resource allocation.

`TypeScript` · `React` · `Deno Edge Functions` · `TypedArrays` · `Leaflet`
> **Why it matters:** real graph-algorithm work — optimized adjacency lists, stochastic modeling, and a benchmark suite proving the performance claims.

### 💸 [fintech-ledger](https://github.com/shaswatnaman/fintech-ledger) — Double-entry bookkeeping system
A fintech-grade ledger where every transaction writes balanced debit/credit entries, enforcing integrity **at the database level**. Built to understand concurrency, auth, and performance under load.

`TypeScript` · `React` · `PostgreSQL` · `Supabase` · `Row-Level Security` · `JWT` · `TanStack Query`
> **Why it matters:** multi-tenant isolation via RLS, stateless JWT auth with session caching, and load-tested API benchmarks.

### 📊 [DataStory](https://github.com/shaswatnaman/DataStory) — Natural-language data analysis
Upload a CSV, ask a question in plain English, and the app generates + safely executes Python to answer it — tables, charts, and summaries.

`Python` · `Flask` · `GPT-4o-mini` · `matplotlib` · `sandboxed execution`
> **Why it matters:** safe code-gen execution, contextual follow-up suggestions, and conversation memory across queries.

---

## 🔒 Private Founder Builds — *showcased without exposing IP*

> Both repositories are private. What follows is architecture, role, and engineering decisions — never proprietary code, product flows, or business strategy.

### 🧠 Nureli — iOS Emotional Wellness Platform · *by Soul Nestle · Building*

A native iOS app helping adults understand and heal from childhood emotional neglect through science-backed, trauma-informed support.

**The problem** — Emotional-wellness apps are mostly shallow content wrappers, and a clinical-adjacent space has a hard constraint most apps ignore: a user can be in genuine crisis mid-session. The product has to be personal and AI-assisted, yet *safe*, *private*, and *responsible* by construction — not by disclaimer.

**My role** — sole iOS founder-engineer: app architecture, the server-side AI & safety layer, data & privacy model, design system, and monetization. Built with the VIT counselling team & clinical psychologists.

**System architecture**

| Layer | What I built |
|---|---|
| **App** | SwiftUI · MVVM · `@Observable` (iOS 17) · ~27K LOC across **13 feature modules** · a layered Core (services, storage, analysis, config, theme) |
| **AI & safety** | OpenAI reachable **only** through Supabase Edge Functions (Deno) — the key never touches the device · **crisis detection runs first in every call** → routes to the 988 Lifeline, bypassing all other logic · per-user daily rate limit that degrades into a gentle, in-voice message, never a raw error |
| **Data & privacy** | Supabase / PostgreSQL with **RLS on every user table** · offline-first SwiftData local store synced to remote · private voice-recording bucket · **zero health/emotional content in analytics**, by design |
| **Personalization** | A pattern-detection engine + feature-threshold/unlock engines that progressively reveal the experience from emotional signals (archetype, healing-day count, body-zone history) |
| **Server-driven** | Remote-config + feature-policy engines change content, flags & unlocks **without an App Store release** |
| **Monetization** | RevenueCat — every feature available Day 1, gated by a single `isPremium` flag |
| **Design system** | Spring-only motion, serif-for-emotion / rounded-for-chrome type, haptic patterns, liquid-glass surfaces, and **code-drawn botanical art** (no raster) — a deliberate, trauma-informed feel |

**Engineering decisions worth calling out**
- **Safety supersedes everything** — every AI edge function runs crisis detection *before* rate-limiting or product logic; a user in crisis is never gated, rate-limited, or delayed away from the 988 response.
- **The AI key never reaches the client** — all model calls go server-side; per-user daily limits cap cost and abuse, and any failure degrades into an in-voice message rather than an error.
- **Privacy by architecture, not policy** — RLS on every table, an offline-first local store as the source of truth for sensitive content, and analytics that are structurally unable to see emotional data.
- **Ship without re-shipping** — remote config + threshold/unlock engines let the experience evolve server-side between releases.

**Lessons** — building responsibly in a clinical-adjacent domain; designing trauma-informed motion and copy; making safety a non-negotiable that sits *above* cost and product concerns.

`Swift 6` · `SwiftUI` · `Supabase` · `PostgreSQL + RLS` · `Edge Functions (Deno)` · `OpenAI` · `RevenueCat` · `PostHog` · `swift-crypto`

> Pre-incubated at VIT · built with the VIT counselling team & clinical psychologists · began as a workbook that reached **1,000+ people**, now shaping the product.

<br/>

### 🪷 Cultural-Technology Platform · *Founder / Product Engineer · Live, in stealth*

A consumer platform that takes a **traditional, trust-sensitive, deeply offline cultural-devotional experience and rebuilds it as a digital product** — connecting families with temple-verified practitioners, live-documented rituals, and doorstep delivery of physical blessed offerings, in their own language. *Technology used to preserve meaningful human experiences and make them accessible.*

**The problem** — Millions of families want authentic, correctly-performed rituals but are blocked by distance, time, and the difficulty of finding trusted, verified practitioners. The real-world experience is high-trust, multi-step, and ends with a *physical* offering in your hands — all hard to make feel authentic online.

**My role** — sole founder-engineer: architecture and build across frontend, backend, payments, AI, data, fulfillment, and growth.

**System architecture**

| Layer | What I built |
|---|---|
| **Web** | Next.js 15 (App Router) · React 19 · TypeScript · Tailwind · Framer Motion |
| **i18n** | `next-intl`, fully bilingual (English / Hindi), locale-routed via edge middleware — built for non-English-first users |
| **Data** | Supabase / PostgreSQL · 20+ versioned migrations · normalized model for devotees, bookings, catalog, subscriptions & shipments |
| **Payments** | **Provider-neutral** layer over multiple gateways (UPI · cards · subscriptions) · signature verification · an **idempotent webhook ledger** that survives gateway retries without double-charging |
| **AI** | A provider-abstracted LLM layer that generates a **personalized, devotionally-accurate ritual intention (Sankalp)** from structured inputs — with **deterministic, fallback-safe degradation** so a booking never breaks when the model does |
| **Fulfillment** | Logistics integration for physical delivery — full shipment lifecycle & tracking |
| **Growth** | Meta Pixel + **server-side Conversion API**, event tracking, abandoned-lead capture & recovery, workflow automation (n8n) |
| **Domain** | Almanac (Panchang) & birth-chart (Kundli) data, festival calendars, SEO (sitemap / blog) |

**Engineering decisions worth calling out**
- **Provider-neutral payments** — gateways sit behind one interface, so adding or switching a PSP never touches booking logic; an idempotent processed-event ledger makes webhook retries safe.
- **AI that fails gracefully** — every generated output has a deterministic fallback; the revenue path never depends on a model call succeeding.
- **Trust-first by design** — verified practitioners, live documentation, transparent payment & refund flows, because this category lives or dies on trust.
- **Built for the real user** — multilingual, mobile-first, fast on patchy networks, usable by non-technical devotees.

**Lessons** — simplifying a complex, emotional, offline experience into a digital flow people *trust*; designing consumer platforms for diverse users; balancing culture, technology, and usability.

---

## 🧩 How I Engineer

```
Problem → Research → Architecture → Ship → Measure → Iterate
```

| Area | What I reach for |
|---|---|
| **Mobile** | Swift 6, SwiftUI, MVVM, `@Observable`, spring-based motion, accessibility |
| **Backend** | Supabase, PostgreSQL, Row-Level Security, Edge Functions (Deno), FastAPI |
| **AI** | OpenAI pipelines, deterministic/explainable decision layers, TF-IDF + classical ML, safe code execution |
| **Web** | TypeScript, React, TanStack Query, Tailwind / shadcn |
| **Quality** | Snapshot & unit testing, benchmark suites, load testing, audit logging |
| **Principles** | Privacy by default · clean architecture · measurable performance · ship then iterate |

---

## 🌱 Building in Public *(without exposing private work)*

- **Customer discovery first** — Nureli began as a workbook that reached 1,000+ people *before* a line of app code.
- **Research-driven** — trauma-informed design built alongside clinical psychologists, not guessed at.
- **Responsible AI** — every AI surface in a wellness context runs crisis-detection first and keeps health data out of analytics.
- **Open where it helps** — I open-source the *systems* (simulation engines, ledgers, AI pipelines) and keep *product IP* private.

---

## 💼 Why I'd be valuable on your team

- **Ownership** — I take ambiguous problems from zero to shipped product without hand-holding.
- **Shipping** — a 27K-LOC production iOS app and four substantive systems projects, not tutorials.
- **Learning speed** — second-year student already working across iOS, backend, AI, and product.
- **User empathy** — I design from real human problems and real user research.
- **Systems judgment** — I know *when* determinism beats an LLM, when RLS beats app-layer auth, and how to prove a performance claim.

---

<div align="center">

**Let's build something that matters.**

[![LinkedIn](https://img.shields.io/badge/Connect_on_LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/shaswatnaman/)

<sub>Founder-engineer · building emotionally intelligent and culturally meaningful products through software.</sub>

</div>
