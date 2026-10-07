# Hi, I'm Willian Arakaki 👋
### AI & Backend Software Engineer | Distributed Systems | Multi-Agent Systems | FinOps & AppSec

Software Developer specializing in **Applied Artificial Intelligence** and **Distributed Backend Systems**. Experienced in architecting event-driven microservices, stateful multi-agent workflows, production-grade **Hybrid RAG** pipelines, and resilient transactional platforms.

Currently pursuing a degree in **Systems Analysis and Development** at **FIAP** (graduating Feb 2027), bridging core Software Engineering discipline (**Java 21**, **Spring Boot**, **Apache Kafka**, database concurrency) with cutting-edge AI systems (**Python**, **LangGraph**, local **SLMs**, **Cloud LLMs**).

---

## 🤖 Engineering & AI Focus

* **Event-Driven Microservices & Backend** — Asynchronous, resilient pipelines built with **Java 21**, **Spring Boot**, **FastAPI**, and **Apache Kafka (KRaft)**, enforcing concurrency safety with **Optimistic Locking (`@Version`)** and transactional integrity.
* **Stateful Multi-Agent Orchestration** — Complex agent graphs, dynamic routing, and human-in-the-loop workflows engineered with **LangGraph** and **LangChain**.
* **Dual-Brain Architectures & FinOps** — Cost-effective inference layers pairing local **SLMs** (**Ollama**, **Qwen 2.5**, **LLaVA**) as local gatekeepers with **Cloud LLMs** (**Google Gemini**) to cut cloud API expenses.
* **Semantic Search & Hybrid RAG** — High-precision retrieval systems combining vector similarity (**FAISS**), lexical search, and embedded relational engines (**DuckDB**).
* **AI Security (AppSec) & LGPD Compliance** — Adversarial prompt injection/jailbreak mitigation (**Llama Prompt Guard 2**) and automated local **PII** redaction (**CPF/CNPJ**) using **Microsoft Presidio** and **spaCy** prior to external transit.
* **Low-Latency Streaming & AI UX** — Mitigating model response latency via **Server-Sent Events (SSE)** streaming integrated with **Next.js (App Router)** to drastically reduce **Time-To-First-Token (TTFT)**.
* **Reliability, Testing & SRE** — Automated testing and evaluation with **JUnit 5**, **Pytest**, **Testcontainers**, **DeepEval**, and **LangSmith** tracing, coupled with automated **Circuit Breakers**.

---

## 🚀 Featured Projects

### 1. EcoTrack AI — Event-Driven ESG SaaS & Sustainability Copilot
> **B2B SaaS platform** engineered for Scope 3 carbon emission auditing, gamified employee engagement, and an enterprise sustainability copilot. Built on a decoupled polyglot architecture (**Java 21** + **Python 3.12** + **Next.js 16**).

#### Architectural Highlights
* **Event-Driven Ingestion Pipeline:** Built an asynchronous ingestion backbone with **Spring Boot** and **Apache Kafka 3.9 (KRaft)**, offloading heavy VLM/OCR audit tasks to background **Python** workers and responding immediately with `HTTP 202 Accepted`.
* **Latency Mitigation via SSE Streaming:** Implemented real-time token streaming with **Server-Sent Events (SSE)** between **FastAPI** and **Next.js 16**, slashing the **Time-To-First-Token (TTFT)** from 8.3s to 3.9s.
* **Dual-AI FinOps Gatekeeper:** Deployed a local **SLM** (**Qwen 2.5 7B** via **Ollama**) as an edge firewall to intercept irrelevant queries and prompt attacks locally, preventing expensive calls to **Google Gemini**.
* **Transactional Integrity & Concurrency:** Applied **JPA Optimistic Locking (`@Version`)** in **Oracle Database** to eliminate double-spending in gamified reward redemptions and recorded an immutable audit log in **AWS DynamoDB**.
* **Privacy-by-Design Pipeline:** Pre-processed corporate requests with **Microsoft Presidio** and **spaCy** (`pt_core_news_sm`) to sanitize national identifiers (**CPF** and **CNPJ**) before routing to external LLMs.

#### 📊 Measured Impact & Benchmarks
| Metric | Baseline | Optimized Architecture | Measured Gain |
| :--- | :--- | :--- | :--- |
| **API Ingestion Response Time** | ~2,000ms – 4,000ms | **~229ms** (`HTTP 202`) | **10× faster ingestion** via **Kafka** |
| **Time-To-First-Token (TTFT)** | ~8,330ms (8.3s) | **~3,909ms** (3.9s) | **53% latency reduction** via **SSE** |
| **Cloud API Gatekeeping** | 100% routed to Cloud | **Local Filter First** | Non-ESG & malicious traffic blocked locally |
| **Concurrency & Double-Spending** | Vulnerable under load | **Zero race conditions** | Guaranteed via **Optimistic Locking** |

* 🔗 **Repositories:** [Backend (Core Java + AI Service)](https://github.com/willarakaki/ecotrack-backend) · [Frontend (Next.js)](https://github.com/willarakaki/ecotrack-frontend)

---

### 2. SentinelOps — Autonomous Financial Dispute Resolution System
> **Enterprise Multi-Agent platform** engineered to automate financial disputes, chargebacks, and transaction reconciliation through autonomous agent investigation and hybrid inference.

#### Architectural Highlights
* **Stateful Multi-Agent Graph:** Engineered state machine workflows in **LangGraph**, coordinating autonomous investigation nodes with embedded structured validation in **DuckDB**.
* **FinOps Semantic Caching:** Implemented semantic vector caching with **FAISS**, recognizing repetitive dispute patterns to bypass external LLM calls entirely.
* **Layered AI Defense (WAF):** Integrated multi-stage perimeter security combining regex sanitizers and **Llama Prompt Guard 2** to block adversarial injection attempts.
* **Circuit Breaker Fallback:** Built automated resilience into the agent runtime, falling back to secondary providers (**Groq**) during cloud model degradation.

#### 📊 Measured Impact & Benchmarks
| Metric | Baseline | Optimized Architecture | Measured Gain |
| :--- | :--- | :--- | :--- |
| **Latency on Cache HIT** | ~10.02s | **~0.74s** | **13.5× faster response** via **FAISS** |
| **Avoided Tokens per HIT** | 0 tokens saved | **~3,769 tokens saved** | 100% cloud cost avoided on repetition |
| **Adversarial Benchmark (Red Team)** | Vulnerable to injection | **100% blocked** (20/20 cases) | Zero jailbreaks via **Prompt Guard 2** |
| **Deterministic Partial-Refunds** | Inconsistent / Manual | **100% precision** (14/14 cases) | Deterministic agent reconciliation |

* 🔗 **Repository:** [SentinelOps Codebase](https://github.com/willarakaki/sentinelops)

---

## 🧠 Tech Stack & Tooling

* **Artificial Intelligence & Agents:** **LangGraph**, **LangChain**, **Qwen 2.5**, **Ollama**, **Google Gemini**, **LLaVA**, **Hybrid RAG**, **FAISS**, **Model Context Protocol (MCP)**
* **Backend & Distributed Systems:** **Java 21**, **Spring Boot**, **Apache Kafka (KRaft)**, **Python 3.12**, **FastAPI**, **Server-Sent Events (SSE)**, **REST APIs**
* **Databases & Persistence:** **Oracle Database (XE / PL/SQL)**, **AWS DynamoDB**, **DuckDB**, **Spring Data JPA**, **Flyway**
* **Frontend & Architecture:** **Next.js 16 (App Router)**, **React 19**, **TypeScript**, **Zustand (Optimistic UI)**, **Tailwind CSS**
* **Security, Quality & DevOps:** **Microsoft Presidio (LGPD)**, **Llama Prompt Guard 2**, **LangSmith**, **DeepEval**, **Testcontainers**, **JUnit 5**, **Pytest**, **Docker**, **GitHub Actions (CI/CD)**

---

## 🎯 What I Bring to Engineering Teams

* **Production Over Demos:** Experience building complete software lifecycles—including database migrations (**Flyway**), event streaming (**Kafka**), test suites (**Testcontainers**, **JUnit 5**), and CI/CD pipelines—rather than standalone Jupyter notebooks.
* **Cost & Latency Awareness (FinOps):** Deep focus on the economic viability of AI products, reducing token expenses and user-facing latency through caching, local inference, and streaming architectures.
* **Industrial-Grade Quality Discipline:** 4+ years of professional experience in high-precision Japanese manufacturing lines (**Aisin/Lexus** and **Okamoto/Suzuki**), bringing proven rigor in **zero-defect quality**, **ISO standards**, and **Kaizen root-cause troubleshooting** into modern software development.

---

## 🌎 International Background

* 🇯🇵 **Japan (4+ Years):** Professional operational experience in high-precision automotive assembly lines (**Lexus** hydraulic systems and **Suzuki** automated cells), operating under strict **Kaizen** and zero-defect quality mandates.
* 🇲🇽 **Mexico:** Academic exchange in Spanish language and culture at **Universidad Nacional Autónoma de México (UNAM)**.
* 🇪🇸 **Spanish:** **B2 Proficiency** certified via international **SIELE**.
* 🇺🇸 **English:** Intermediate / Technical proficiency for documentation, architectural design, and global collaboration.

---

## 🔬 Research & Deep Dives

* **Model Context Protocol (MCP)** integrations and Agent-to-Agent (**A2A**) protocols.
* **Event-Driven Architectures (EDA)** applied to non-blocking generative AI workloads.
* **Adversarial Robustness & Evaluation Metrics** for enterprise LLM deployments.

---

## 📫 Connect With Me

* 💼 **LinkedIn:** [linkedin.com/in/willian-arakaki](https://linkedin.com)
* 🐙 **GitHub:** [github.com/willarakaki](https://github.com/willarakaki)
* 📧 **Email:** [arakakiw5@gmail.com](mailto:arakakiw5@gmail.com)

> *"Building resilient, production-ready backend systems and AI architectures — not just API wrappers."*
