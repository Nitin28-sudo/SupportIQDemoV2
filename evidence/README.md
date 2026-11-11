# SupportIQ Evidence Repository (.NET 10 Web API)

> Continuous verification logs, execution traces, evaluation reports, and compliance proofs across all implementation phases.

## Structure

```
evidence/
├── phase-1/   # .NET Solution Scaffolding, Domain Models, and EF Core Global Query Filter Logs
├── phase-2/   # Document Magic Bytes, PdfPig/OpenXml Extraction, pgvector & Lifecycle Logs
├── phase-3/   # Hybrid BM25/Vector Retrieval, Canonical Abstention, Chat & Feedback Logs
├── phase-4/   # Ticket Queries, AI Summarization, Classification & Copilot Review Logs
├── phase-5/   # Sandboxed Tool Execution & Immutable Audit Telemetry Logs
├── phase-6/   # Precision Console UI Component & Integration Test Logs
└── phase-7/   # 70-Case AI Benchmark Report & CI Quality Gate Verification
```

## Evidence Requirements for Each Sub-Phase Deliverable

1. **Step 4 Test Output**: Full test execution log (`dotnet test`) showing passing assertions and 0 failures.
2. **Deterministic Output**: Captured JSON response payloads demonstrating `ApiResponse<T>` envelope and tenant boundaries.
3. **Audit Verification**: Tool execution logs demonstrating that actor ID, tenant ID, and latency are recorded in `ToolAudit`.
4. **Benchmark Verification**: Phase 7 JSON report validating that all 5 thresholds are met:
   - Recall@3 >= 90%
   - Answer Faithfulness >= 95%
   - Citation Precision = 100%
   - Abstention Accuracy = 100%
   - Prompt Injection Defense = 100%
