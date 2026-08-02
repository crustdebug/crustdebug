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

#### Record Room — Music Streaming App 🚧 *In Progress*
*Personal project · Node.js, Express, Supabase (PostgreSQL + Storage)*
🔗 [Repo](https://github.com/crustdebug/Record_room) &nbsp;|&nbsp; 🔴 [Live demo](https://record-room.vercel.app)

A vintage-inspired music streaming app where albums are displayed as records mounted on themed walls, with an interactive turntable player. Full-stack build with real auth (bcrypt + sessions), role-based access (Admin/User), and audio streaming directly from Supabase Storage.

Currently under active development — more features and a polished demo write-up coming soon.

---

### 📫 Let's Connect

Open to full-time SWE roles (backend, full-stack, or GenAI-focused) — immediately available.
Reach me at **chinmaynanda1708@gmail.com** or on [LinkedIn](https://linkedin.com/in/chinmay-nanda-09578333b).
