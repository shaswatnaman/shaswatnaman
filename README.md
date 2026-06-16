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

> These repositories are private. Below is architecture, role, and outcomes — never proprietary code.

<table>
<tr><td width="50%" valign="top">

### 🧠 Nureli — iOS Emotional Wellness Platform
**by Soul Nestle · Status: Building**

Helping adults understand and heal from childhood emotional neglect through science-backed, trauma-informed support.

**What I own**
- Mobile architecture (SwiftUI · MVVM · ~27K LOC, 13 feature modules)
- Privacy-first design — **zero** health/emotional content in analytics
- AI via server-side edge functions only; **crisis-detection runs first** in every call
- Experimentation, paywall & monetization, product systems

**Engineering**
`Swift 6` · `SwiftUI` · `Supabase` · `PostgreSQL + RLS` · `Edge Functions` · `RevenueCat` · `PostHog` · `swift-crypto`

**Context** — Pre-incubated at VIT · built with the VIT counselling team & clinical psychologists · started as a workbook that reached **1,000+ people**, now shaping the product.

</td><td width="50%" valign="top">

### 🪷 Stealth Cultural-Technology Platform
**Founder / Product Engineer · Status: Stealth**

Building infrastructure that connects traditional cultural experiences with modern digital product experiences — *using technology to preserve meaningful human experiences and make them more accessible.*

**Focus areas**
- Consumer technology & marketplace-style systems
- Scalable mobile / web experiences
- User trust, accessibility & digital transformation of offline experiences

**What I own**
- Full-stack product architecture (frontend systems · backend infra · auth · DB design)
- Product thinking, UX decisions, rapid prototyping, analytics & iteration

**Key learnings**
- Building for diverse users
- Simplifying complex offline experiences into trustworthy digital flows
- Balancing culture, technology, and usability

</td></tr>
</table>

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
