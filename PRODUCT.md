# SupportIQ — Product Overview

> Fast-reference product brief for AI agents and developers. Full technical specifications and functional requirement matrices are documented in [`docs/PRD.md`](docs/PRD.md).

## Product Mission
SupportIQ is an AI-powered customer support knowledge portal for B2B SaaS organizations (simulated context: **CloudDesk**). It empowers human support agents with grounded retrieval-augmented generation (RAG), automated ticket intelligence, and real-time copilot drafting while guaranteeing strict tenant isolation and zero unsupervised messaging.

## Key Capabilities
1. **Grounded RAG Assistant**: Answers questions citing approved documentation; strictly abstains when knowledge is absent.
2. **Knowledge Ingestion Pipeline**: Ingests PDF, DOCX, and TXT files, chunks, embeds, and indexes them with full version control and deletion lifecycle.
3. **AI Ticket Copilot**: Generates ticket summaries, categorizations, priority suggestions, and draft responses for human agent review.
4. **Sandboxed Tools**: Executes allowlisted read-only lookups with comprehensive audit logging.
5. **Continuous Evaluation**: Automated testing against 50 grounded Q/A pairs, 10 no-answer cases, and 10 prompt-injection cases.

## Core Documents
- **Complete Requirements**: [`docs/PRD.md`](docs/PRD.md)
- **Agent Instructions**: [`AGENTS.md`](AGENTS.md)
- **Domain Glossary**: [`GLOSSARY.md`](GLOSSARY.md)
- **GitHub Copilot Instructions**: [`.github/copilot-instructions.md`](.github/copilot-instructions.md)
