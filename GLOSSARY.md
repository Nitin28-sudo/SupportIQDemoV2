# SupportIQ — Domain Glossary

> Single source of truth for domain concepts and terminology used across the SupportIQ platform.

## Core AI & Retrieval Terms

### RAG (Retrieval-Augmented Generation)
A pattern where an agent retrieves relevant knowledge passages from a vector/hybrid store and provides them to the generative model as factual context before formulating an answer.

### Grounded Answer
An AI-generated response strictly supported by retrieved evidence, where every statement is traceable to an approved knowledge chunk with an explicit citation.

### Abstention
The mandatory behavior where an AI assistant declines to answer if retrieved knowledge is missing, contradictory, stale, or insufficient. Standard phrasing: *"I do not have sufficient information in the knowledge base to answer this question."*

### Knowledge Document
An approved source file (PDF, DOCX, TXT) uploaded to a tenant's knowledge repository, tracked through versioning, extraction, and chunking lifecycles.

### Knowledge Chunk
A discrete text segment extracted from a knowledge document, enriched with section/page metadata, embedded into a high-dimensional vector space, and indexed for semantic and keyword retrieval.

### Embedding
A dense numerical vector representing the semantic meaning of a text segment, enabling vector similarity search.

### Citation
A reference accompanying an AI response linking a specific claim to a source knowledge document title, chunk, and page/section number.

---

## Core Platform & Business Terms

### Tenant Isolation
The architectural and security guarantee that data belonging to one organization (tenant) is never accessible, searchable, or leakable to another organization. Enforced at every API and data layer.

### Human-in-the-Loop
A mandatory operational boundary where an AI system provides assistive drafts, classifications, and summaries, but a human support agent retains final decision-making and approval before any customer-facing message is dispatched or data mutation is executed.

### Ticket Copilot
The AI assistant embedded within the agent workspace that analyzes customer tickets to suggest summaries, categories, priorities, troubleshooting steps, and draft replies.

### Tool Audit Trail
An immutable log capturing every automated tool invocation by an AI agent, including the actor ID, tenant ID, tool name, input parameters, execution outcome, latency, and correlation ID.
