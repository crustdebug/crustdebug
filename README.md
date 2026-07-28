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

I'm a full-stack and GenAI-focused developer. I've shipped a production RAG chatbot that cut manual query resolution time by 60%, built a multi-tenant ERP platform for a live client, and written multithreaded Python for real industrial hardware. I like projects where correctness and performance both matter — whether that's a vector search pipeline or a validation system reading two hardware streams in parallel.

Currently freelancing full-time, and looking for full-time Software Engineering roles — immediately available.

---

### 🛠️ Tech Stack

**Languages:** Python · TypeScript/JavaScript · SQL · C/C++ · Java
**AI/ML:** LLMs · RAG · LangChain · HuggingFace · PyTorch · TensorFlow · Prompt Engineering
**Web/Backend:** FastAPI · Next.js · React · Node.js · REST APIs · Tailwind CSS
**Data:** PostgreSQL · MySQL · Vector Databases · Prisma ORM
**Tools:** Git · Docker · Linux · AWS · Azure · Vercel

---

### 🚀 Featured Work

#### VoltCore — Multi-Tenant ERP Platform
*Freelance client project · Next.js 15, TypeScript, PostgreSQL, Prisma, REST APIs*

A full-stack ERP platform covering 13+ modules (HR, Payroll, Onboarding) for a live client, with role-based access control across isolated PostgreSQL databases per tenant. Includes automated Excel data pipelines and PDF report generation.

> This is a live production app built for a paying client under an active engagement, so the source is private and the demo requires client credentials I can't share publicly. Screenshots below — happy to walk through the architecture live in an interview.

<!-- Add 2-3 screenshots here, e.g.: -->
<!-- ![VoltCore dashboard](./assets/voltcore-dashboard.png) -->
<!-- ![VoltCore payroll module](./assets/voltcore-payroll.png) -->

**Key decisions:** isolated per-tenant Postgres databases (vs. shared schema + row-level security) for stronger tenant data separation; Prisma for type-safe schema management across environments.

---

#### Dual-Head Card Sequence Validation System
*Freelance project for Techware Automation · Python, PyQt6, UDP, Serial, Multithreading*

A desktop application for real-time industrial automation — validates card sequences from two independent hardware scanners simultaneously, communicating over UDP and Serial protocols, with a PyQt6 UI for live monitoring.

> This runs against physical scanner hardware, so it can't be "run" from a repo. Short demo video below shows it live against the machine.

<!-- Add demo video link here, e.g.: -->
<!-- 🎥 [Watch demo](your-video-link) -->

**Key decisions:** multithreaded design to handle two parallel unstructured data streams without blocking or dropping packets from either scanner.

---

#### Natural Language to SQL Agent
*Personal project · Python, Streamlit, LangChain, PostgreSQL*
🔗 [Repo](https://github.com/crustdebug/Simple_HRMS_RAG) <!-- update to correct repo link -->

Converts plain-English questions into validated SQL queries using schema-aware prompting, with a sandboxed execution layer to block injection attempts before queries run. Streamlit dashboard for non-technical users to query and export data.

---

### 📫 Let's Connect

Open to full-time SWE roles (backend, full-stack, or GenAI-focused) — immediately available.
Reach me at **chinmaynanda1708@gmail.com** or on [LinkedIn](https://linkedin.com/in/chinmay-nanda-09578333b).
