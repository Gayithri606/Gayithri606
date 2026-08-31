# Gayithri P. | AI Engineer | RAG Assistants, Support Chatbots & Workflow Automation

Reliable AI doesn't come just from better prompts. It comes from better engineering.

I spent five years building production backend systems at Walmart, Oracle, and VMware before moving into AI, and I build AI the same way: with tests, evaluation, guardrails, and cost tracking from day one. Based in San Jose, CA.

---

## 📁 Selected Work

**🔨 Currently building:** finishing the guardrails and evaluation layer on the customer care chatbot, and writing up the retrieval tradeoffs as I go.

### AI Document Q&A System — Production RAG Pipeline
Ask questions in plain English against a library of PDFs and Word docs, and get answers that cite their sources or say "I don't know."

- Vector storage on TimescaleDB + pgvectorscale instead of a managed vector DB: **~75% cheaper than Pinecone** at comparable query performance
- **One batched embeddings call instead of 50 to 100 sequential round trips** per document
- **Sub-second query responses**, fully async FastAPI, with Celery returning a `job_id` immediately so uploads never block the server
- Type-safe output through Instructor and Pydantic, including an `enough_context` flag so the system declines rather than guesses
- Every token and dollar tracked in Langfuse from the first commit

`Python` `FastAPI` `Celery` `TimescaleDB` `Docling` `OpenAI` `Langfuse`
**Status: complete** · [Code](https://github.com/Gayithri606/DocumentProcessingPipeline-RAGbased) · [Case study](https://gayithriponnapalli.com/portfolio/projects/ai-document-qa-system/) · [How I built it](https://gayithriponnapalli.com/blog/2026/04/14/how-i-built-a-production-ready-ai-document-qa-system--and-what-makes-it-different/)

### Custom GPT for a Dental Practice Handbook
A real client engagement. An internal assistant grounded in a 27-page employee handbook, so staff could stop hunting through a PDF for policy answers.

- Two-phase evaluation instead of a demo: **21 formal questions at 95.2% pass**, then 30 questions written the way staff actually talk, which dropped to **80%**
- Prompt revisions v3 and v4 brought the informal set to **100%**
- The failure that mattered was blank pages in the source PDF causing citation drift, which is a document-hygiene problem, not a model problem
- Full methodology, results, and what I got wrong are published in the repo

`Custom GPT` `Prompt Design` `Evaluation Harness` `Python`
**Status: delivered, 5.0 review** · [Code and methodology](https://github.com/Gayithri606/custom-gpt-dental-handbook)

### AI Executive Assistant — Email Automation
An event-driven system that watches an inbox, classifies each message, and acts on it: auto-reply, pull line items out of an invoice, or answer a question from a knowledge base.

- Custom node-based workflow engine with Agent, Router, and Parallel nodes
- **Escalates to a human when confidence is low** rather than answering anyway
- Multi-provider through PydanticAI (OpenAI, Claude, Gemini, Bedrock, Ollama) with a one-line swap
- Webhook-driven async ingestion, traced end to end with OpenTelemetry and Langfuse

`PydanticAI` `pgvector` `Docling` `OpenTelemetry` `Langfuse`
**Status: complete, code private** · [Case study](https://gayithriponnapalli.com/portfolio/projects/ai-executive-assistant/)

### Customer Care Chatbot — RAG-based
Multi-turn support chatbot grounded in ingested documents, with guardrails at three layers: input validation, retrieval filtering, and output checks.

`PydanticAI` `Redis` `TimescaleDB` `FastAPI` `Celery`
**Status: in active development, not deployed** · [Code](https://github.com/Gayithri606/CustomerCareChatbot-RAGbased)

---

## 🎯 How I Build

- **Retrieval and cost first, model second.** Most RAG problems are retrieval problems wearing a model costume.
- **Evaluate before promising.** I won't claim a number I haven't measured. Both flagship projects ship with their evaluation method written down.
- **Guardrails from day one, never bolted on.** Helpers fail open, safety checks fail closed.
- **Match the tool to the problem.** A client once hired me to add AI to a bulk certificate workflow. I recommended a plain Python pipeline instead and saved them the cost. Sometimes a scheduled script beats an agent, and I'll say so.

---

## 🛠️ Tech Stack

**Languages** Python · SQL · Java

**AI & Agents** OpenAI · Claude · Gemini · PydanticAI · LangChain · Instructor · MCP

**Retrieval** PostgreSQL + pgvector · TimescaleDB + pgvectorscale · Docling · semantic and hybrid search · batch embeddings

**Backend** FastAPI · PostgreSQL · Redis · Celery · REST · GraphQL · Spring Boot

**Infra & Observability** Docker · AWS · Hetzner · GitHub Actions · Langfuse · OpenTelemetry · Grafana

---

## ⚙️ Before AI: Five Years of Production Backend

This is the part that shapes how I build AI systems. Uptime and correctness were not optional in any of these roles.

- **Walmart** — Java 17 and Spring Boot. Led a JDK 17 migration that delivered a **20% performance improvement in six weeks**, and a Spring Boot 2.5 to 3.3 upgrade that cut startup time by **15%**. GraphQL feature work. [Case study](https://gayithriponnapalli.com/portfolio/projects/walmart-core-system-performance-overhaul/)
- **Oracle** — Java framework for high availability in Oracle Public Cloud. Zookeeper, NoSQL.
- **VMware** — Java automation framework for vSphere storage, built on the VMware SDK.

**Certifications:** Datalumina Certified AI Engineer Expert (2026) · AWS Cloud Technical Essentials

---

## 🤝 Work With Me

I take on RAG assistants, support chatbots grounded in real documents, internal AI tools, and Python workflow automation. The first call is free, and I'd rather figure out what "done" looks like before quoting than after.

**Freelance:** [Upwork](https://www.upwork.com/freelancers/gayithrip) · 100% Job Success · 5.0 rating · Rising Talent

**Full-time:** I'm looking for AI engineering roles where retrieval quality, evaluation, and cost actually matter. The backend history above is why I think about those first.

📍 San Jose, CA · 🌐 [gayithriponnapalli.com](https://gayithriponnapalli.com) · ✉️ gayithri@pojoai.com
