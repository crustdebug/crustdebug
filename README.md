<h1 align="center">Hi, I'm Chinmay 👋</h1>

<p align="center">
Software Engineer building with LLMs, full-stack web, and systems-level code.<br>
B.Tech CS (AI & ML) graduate · Currently freelancing · Open to full-time SWE roles, immediately available
</p>

<p align="center">
📍 Delhi-NCR, India &nbsp;|&nbsp;
📧 chinmaynanda1708@gmail.com &nbsp;|&nbsp;
🔗 <a href="https://linkedin.com/in/chinmay-nanda-09578333b">LinkedIn</a>
</p>

---

### About Me

I'm a full-stack and GenAI-focused developer. I've shipped a production RAG chatbot that cut manual query resolution time by 60%, built a multi-tenant ERP platform for a live client, and written multithreaded Python for real industrial hardware. I like projects where correctness and performance both matter — whether that's an LLM agent enforcing read-only database access or a validation system reading two hardware streams in parallel.

Currently freelancing full-time, and looking for full-time Software Engineering roles — immediately available.

---

### 🛠️ Tech Stack

**Languages:** Python · TypeScript/JavaScript · SQL · C/C++ · Java
**AI/ML:** LLMs · RAG · LangChain · HuggingFace · PyTorch · TensorFlow · Prompt Engineering
**Web/Backend:** FastAPI · Next.js · React · Node.js · REST APIs · Tailwind CSS
**Data:** PostgreSQL · MySQL · Vector Databases · Prisma ORM
**Tools:** Git · Docker · Linux · AWS · Azure · Vercel

---

### 💼 Client Work

#### VoltCore — Multi-Tenant ERP Platform
*Freelance client project · Next.js 15, TypeScript, PostgreSQL, Prisma, REST APIs*

A full-stack ERP platform covering 13+ modules (HR, Payroll, Onboarding) for a live client, with role-based access control across isolated PostgreSQL databases per tenant. Includes automated Excel data pipelines and PDF report generation.

> This is a live production app built for a paying client under an active engagement, so the source is private and the demo requires client credentials I can't share publicly. Screenshots below — happy to walk through the architecture live in an interview.

<img width="1915" height="912" alt="Screenshot 2026-08-02 132812" src="https://github.com/user-attachments/assets/72b837e6-9046-4e29-af5f-6d12e357eb93" />
<img width="1905" height="901" alt="Screenshot 2026-08-02 133102" src="https://github.com/user-attachments/assets/93591b37-4e71-4c0f-9a94-eb2aef57a9e7" />
<img width="1912" height="906" alt="Screenshot 2026-08-02 132944" src="https://github.com/user-attachments/assets/eb642800-51f5-4f91-8712-a9d73ba6c3db" />
<img width="1915" height="912" alt="Screenshot 2026-08-02 132914" src="https://github.com/user-attachments/assets/fdc3181e-3051-4df9-8dc3-a59d080cd0ba" />


**Key decisions:** isolated per-tenant Postgres databases (vs. shared schema + row-level security) for stronger tenant data separation; Prisma for type-safe schema management across environments.

---

#### Dual-Head Card Sequence Validation System
*Freelance project for Techware Automation · Python, PyQt6, UDP, Serial, Multithreading*

A desktop application for real-time industrial automation — validates card sequences from two independent hardware scanners simultaneously, communicating over UDP and Serial protocols, with a PyQt6 UI for live monitoring.

> This runs against physical scanner hardware, so it can't be "run" from a repo. Screenshots below show the live monitoring UI — captured without hardware connected, so fields show idle/default state rather than live scan data.

<img width="1919" height="1037" alt="main-dashboard" src="https://github.com/user-attachments/assets/a89adfb0-be5f-4d16-80f7-f3fea87f0719" />
<em>Main dashboard — Head A / Head B status, routes to scanner control, network config, and file management</em></p>

<img width="1911" height="1029" alt="network-setup" src="https://github.com/user-attachments/assets/048450a8-2e4a-464a-896d-e378a3d8ca50" />
<em>Network & COM Port configuration — independent UDP/Serial setup per head for scanner input and PLC output</em></p>

<img width="1917" height="1029" alt="live-scanning" src="https://github.com/user-attachments/assets/3c9dc442-bd2f-4016-a378-65dbdf283ab5" />
<em>Live validation log per head — Entry #, Scanned ID, Expected ID, Result, Scan Side, paginated</em></p>

**Key decisions:** multithreaded design to handle two parallel unstructured data streams without blocking or dropping packets from either scanner.

---

### 🧪 Personal Projects

#### QueryMancer — SQL AI Agent
*Personal project · Python, FastAPI, agent loop, PostgreSQL/MySQL/SQLite/SQL Server/Oracle*
🔗 [Repo](https://github.com/crustdebug/QueryMancer) &nbsp;|&nbsp; 🔴 [Live demo](https://querymancer.onrender.com)

An LLM agent that answers plain-English questions about any connected database — it explores the schema at runtime with read-only tools, writes and runs the SQL itself, and shows the exact query alongside the answer. Connects to Postgres, MySQL, SQLite, SQL Server, or Oracle with no hardcoded config.

> Hosted on Render's free tier, so the first request after inactivity can take 30-60s to spin up — worth a heads-up if you're trying it live.

- **Two independent safety layers** block writes: a read-only DB transaction/file handle, plus statement-level checking that strips string literals and comments before validating only a single `SELECT`/`WITH` is allowed.
- **Automatic name repair** maps a model's guessed column/table names (e.g. `customer_name`) onto what actually exists in the schema (e.g. `"Customer"."name"`), handling snake_case/camelCase/PascalCase mismatches via fuzzy matching.
- **Multi-key rotation and failover** across LLM providers (Gemini, Groq, Perplexity, local Ollama) so free-tier rate limits don't stall the app.
- **Local-only privacy mode** — a flag that excludes all cloud providers from the fallback chain so database content never leaves the machine, enforced in code rather than left to the user removing API keys.
- Tested with `pytest` (key rotation, read-only enforcement, schema discovery, name resolution) using a stub model — no live DB or API key needed to run the suite.

---

Record Room — Vinyl Collection Asset Register

Personal project · Node.js, Express 5, Supabase (PostgreSQL + Storage), Zod, Vitest 🔗 Repo

Discogs is a database of releases — it knows a 1977 pressing exists and roughly what it sells for. It can't know that your copy is NM media in a VG+ sleeve, that you paid £25 for it in Leeds in 2019, or that side B skips. A mid-size collection is 500–2,000 records and easily £7,500–£30,000 of uninsured property, because home insurance needs an itemised, valued schedule that nobody has.

Record Room is the asset register for that: it catalogs each copy with condition, provenance, and value, and produces the photographed, dated valuation report an insurer actually asks for.

Insurance-grade output — generates a PDF listing every record with pressing, Goldmine grades, purchase history, current estimate, and the method behind each figure, plus a scheduled-items CSV and server-timestamped condition photos (taken_at is never accepted from the client — evidence that can be backdated isn't evidence).
Valuation engine with defensible assumptions — condition multipliers weight media 70% / sleeve 30%, anchored at VG+ rather than NM because lowest_price skews mid-grade, and anchoring high would systematically overvalue collections in the one direction that costs the owner money at claim time.
Discogs API terms shaped the architecture — their terms forbid displaying marketplace data more than six hours after it was current, so stored prices expire and the app falls back to its own dated estimate, with a test that fails if a stale price reaches a report.
Hand-written RFC 4180 CSV parser for Discogs collection imports — a naive split(',') turns "Earth, Wind & Fire" into silent column-shift corruption; unparseable rows are reported rather than dropped, because a partial import that looks complete is how someone ends up trusting a bad inventory.
Currencies are never summed — Discogs localizes prices by request origin, so totals are reported per currency; an exchange rate would invent precision the app can't defend.
168 tests (Vitest + Supertest) covering auth, CRUD, valuation freshness, PDF/CSV generation, share-link isolation, and per-collector ownership scoping — run against an in-memory Supabase stand-in, so CI needs no credentials and the suite finishes in ~4s.
Also: installable PWA readable offline (check a record while standing in a shop with bad signal), barcode scanning via BarcodeDetector, a wantlist with priorities and max prices, revocable read-only share links that never expose what you paid, and needle-drop playback through a draggable-tonearm turntable.

Not deployed publicly — runs locally in about five minutes with a free Supabase project. npm run seed:demo builds a 20-record demo collection with cover art, grades, values, and playable tracks.

📫 Let's Connect

Open to full-time SWE roles (backend, full-stack, or GenAI-focused) — immediately available. Reach me at chinmaynanda1708@gmail.com or on LinkedIn.
