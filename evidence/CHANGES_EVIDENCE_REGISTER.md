# SupportIQ — Changes & Evidence Register

> **Immutable Audit Record**: Tracks all modifications, file creations, architectural decisions, and verification test logs across the project lifecycle.
> **Maintenance Policy**: Every task, pull request, configuration adjustment, or code modification MUST append an entry to this ledger with corresponding evidence artifact proofs.

---

## 1. Change Register Index

| Change ID | Date (UTC) | Phase Ref | Scope / Component | Action | Target Files | Verification & Evidence Artifact | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **`CHG-001`** | 2026-11-11 | Foundation | Core Requirements | Created | `docs/PRD.md`, `PRODUCT.md`, `GLOSSARY.md` | PRD v1.0 Normalized from Word specification | **Verified** |
| **`CHG-002`** | 2026-11-11 | Architecture | .NET 10 Implementation Plan | Created | `docs/superpowers/plans/2026-11-11-supportiq-platform-implementation.md` | TDD 7-Phase Plan with .NET Clean Architecture | **Verified** |
| **`CHG-003`** | 2026-11-11 | Project Tracking | Excel Tracking Workbook | Created | `docs/tracking/SupportIQ_Implementation_Tracker.xml` | SpreadsheetML 5-sheet workbook with formatting & styles | **Verified** |
| **`CHG-004`** | 2026-11-11 | Project Tracking | Universal CSV Tracker | Created | `docs/tracking/SupportIQ_Implementation_Tracker.csv` | Comma-delimited tracker for Jira / Notion / Sheets | **Verified** |
| **`CHG-005`** | 2026-11-11 | Quality & Audit | Evidence Framework | Created | `evidence/README.md`, `evidence/phase-*` | Phase 1–7 directory structure and verification rules | **Verified** |
| **`CHG-006`** | 2026-11-11 | Governance | Changes Evidence Ledger | Created | `evidence/CHANGES_EVIDENCE_REGISTER.md` | Persistent change tracking and audit trail log | **Active** |
| **`CHG-007`** | 2026-11-11 | Version Control | Git Repository Initialization | Initialized | `.git/` | `git init` executed successfully (Exit Code: 0) | **Verified** |

---

## 2. Chronological Change Records & Verification Proofs

### `CHG-001`: Inception & Specification Normalization
- **Timestamp**: `2026-11-11T17:50:00+05:30`
- **Author**: System / Platform Architecture
- **Phase**: Architecture / Inception
- **Description**: Extracted and normalized requirements from business context documents into AI-facing specifications:
  - Multi-tenant isolation non-negotiables
  - Grounded RAG with strict citations & canonical abstention
  - Human-in-the-loop customer communication constraints
  - Allowlisted read-only tool boundaries
- **Affected Files**:
  - `docs/PRD.md`
  - `PRODUCT.md`
  - `GLOSSARY.md`
  - `AGENTS.md`
  - `.github/copilot-instructions.md`
- **Verification Proof**: Verified against core PRD sections 1 through 10.

---

### `CHG-002`: .NET 10 Clean Architecture Implementation Plan
- **Timestamp**: `2026-11-11T18:14:00+05:30`
- **Author**: Agentic Lead (Antigravity)
- **Phase**: All Phases (`PH-01` to `PH-07`)
- **Description**: Generated comprehensive, bite-sized implementation plan adhering strictly to the `writing-plans` skill standard and aligned with the .NET 10 tech baseline:
  - Replaced Node/monorepo references with .NET 10 Web API, Entity Framework Core 10, C# 13, and xUnit.
  - Configured EF Core Global Query Filters (`HasQueryFilter(e => e.TenantId == _tenantProvider.TenantId)`) for data isolation.
  - Specified multi-format document extraction using `PdfPig` and `DocumentFormat.OpenXml`.
  - Structured hybrid retrieval combining BM25 keyword matching and vector cosine distance.
  - Formatted 70-case automated evaluation suite (50 Grounded, 10 Abstention, 10 Prompt Injection).
- **Affected Files**:
  - `docs/superpowers/plans/2026-11-11-supportiq-platform-implementation.md`
- **Verification Proof**: Checked against 5-step TDD criteria and self-review checklist (spec coverage, step scan, type consistency, review focus, proportion).

---

### `CHG-003` & `CHG-004`: Excel Implementation & Requirements Tracker
- **Timestamp**: `2026-11-11T18:16:00+05:30`
- **Author**: Agentic Lead (Antigravity)
- **Phase**: Governance & Delivery Tracking
- **Description**: Designed and published multi-tab Excel tracking workbook in native SpreadsheetML format and universal CSV format:
  - Sheet 1: `Phase_SubPhase_Tracker` (Tasks, code paths, test commands, evidence paths, owners, status badges)
  - Sheet 2: `Requirements_Traceability` (Every PRD requirement mapped to task and compliance target)
  - Sheet 3: `Evidence_Ledger` (Structured index of evidence artifact logs)
  - Sheet 4: `DoD_Quality_Gates` (The 7 Definition of Done quality gates and evaluation thresholds)
- **Affected Files**:
  - `docs/tracking/SupportIQ_Implementation_Tracker.xml`
  - `docs/tracking/SupportIQ_Implementation_Tracker.csv`
- **Verification Proof**: Validated XML schema compliance (`urn:schemas-microsoft-com:office:spreadsheet`) and CSV delimiter integrity.

---

### `CHG-006`: Changes Evidence Register & Audit Framework
- **Timestamp**: `2026-11-11T18:22:00+05:30`
- **Author**: Agentic Lead (Antigravity)
- **Phase**: Governance & Audit
- **Description**: Established the persistent evidence maintenance structure across all 7 project phases.
- **Affected Files**:
  - `evidence/README.md`
  - `evidence/CHANGES_EVIDENCE_REGISTER.md`
  - `docs/tracking/CHANGES_EVIDENCE_LOG.csv`
- **Verification Proof**: Verified folder hierarchy and traceability back to PRD Section 10 DoD.

---

### `CHG-007`: Git Repository Initialization
- **Timestamp**: `2026-11-11T18:23:56+05:30`
- **Author**: Platform Eng / User
- **Phase**: Version Control & Infrastructure
- **Description**: Initialized empty Git repository for project version control.
- **Affected Files**:
  - `.git/`
- **Verification Command**: `git init`
- **Verification Proof**: Command exited with code 0 (`Initialized empty Git repository in D:/Scalable Work/SupportIQDemoV2/.git/`).

---

## 3. Template for Recording New Changes (For Implementers & Subagents)

Whenever an implementer completes a task or commits code, append a new section below using this format:

```markdown
### `CHG-XXX`: [Short Summary of Change]
- **Timestamp**: `YYYY-MM-DDTHH:MM:SSZ`
- **Author / Agent**: [Name or Subagent Conversation ID]
- **Phase / Sub-Phase Ref**: [e.g. PH-01 / SP-01.2]
- **Task ID**: [e.g. TSK-01.2.2]
- **Action**: [Created | Modified | Refactored | Deleted]
- **Affected Files**:
  - `path/to/file.cs`
  - `tests/path/to/test.cs`
- **Commit Reference**: `[commit hash / branch]`
- **Verification Command**: `dotnet test path/to/test.csproj --filter TestName`
- **Evidence Log Path**: `evidence/phase-N/N.N-description.log`
- **Test Result Summary**: [e.g. 5 passed, 0 failed, duration: 1.2s]
- **DoD Compliance Checked**:
  - [x] TDD test written first and passed
  - [x] Multi-tenant isolation verified
  - [x] No credentials or secrets committed
  - [x] Evidence log generated and saved
```
