# Lead Smith — B2B Lead Discovery & Qualification System

Sales teams and early-stage founders waste significant time manually searching, validating, and organizing potential leads across fragmented and inconsistent data sources. Lead Smith reduces this manual effort by automating lead discovery, normalization, and confidence scoring in a single, production-oriented system.

[🎥 Demo](https://youtu.be/Owig5uqVL5U)

---

## Who is this for?

Lead Smith is designed for:
- Early-stage B2B founders
- Small outbound sales teams
- Sales representatives who need structured, reliable leads without relying on expensive enterprise tooling

The system prioritizes clarity, data quality, and explainability over opaque automation.

---

## Why is this non-trivial?

The core challenge is not fetching data, but handling **noisy and inconsistent real-world information**. Lead Smith addresses problems such as:

- Deduplicating contacts across overlapping sources
- Normalizing inconsistent location and role data (e.g. "USA", "United States", "U.S.")
- Scoring lead confidence when fields are missing or partially conflicting
- Enforcing access control and data ownership
- Handling asynchronous workflows and external API failures reliably

These challenges require careful data modeling, validation, and system design beyond basic CRUD functionality.

---

## High-level architecture

- Frontend: React + TypeScript dashboard for managing leads and filters
- Backend: Node.js + Express API
- Database: Prisma ORM with relational storage
- Authentication: JWT / Firebase-based auth flows
- Processing: Async lead ingestion, normalization, and scoring pipeline

The system is designed to be modular, debuggable, and extensible.

---

## Tradeoffs & design decisions

- I chose **rule-based normalization and confidence scoring** over machine learning models to keep the system explainable, testable, and suitable for early-stage usage.
- I accepted slightly higher latency in exchange for clearer failure handling and retry logic.
- I prioritized correctness and data quality over aggressive automation to ensure leads remain trustworthy.

These decisions reflect the needs of small teams where accuracy matters more than raw throughput.

---

## What I would improve next

With more time, I would:
- Introduce adaptive confidence scoring using historical conversion feedback
- Add batching, caching, and background workers for higher throughput
- Support organization-level roles and permissions for team usage
- Improve observability with structured logging and metrics

---

## Other portfolio projects

[🎥 Nutri Care Pro (Demo)] (https://youtu.be/0iIVWS2I2WE)
[🎥 Record Storage System (Demo)] (https://youtu.be/Uzi32BzQrSM)  

📄 Documentation:
- Nutri Care Pro: `library Document.pdf`
- Chat App: `Slack_like_Communication_Tool.docx`
