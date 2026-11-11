# GitHub Copilot & Agent Instructions — SupportIQ

> Single-source instructions for GitHub Copilot, Copilot Workspace, and AI agents.

## Core Reference Documents

- **Master Instructions**: [`AGENTS.md`](../AGENTS.md) — Agent skills, tracker, and workflow index.
- **Architecture & Coding Standards**: [`GEMINI.md`](../GEMINI.md) — Architecture, DRY principles, Drizzle ORM, Zod single source of truth.
- **Product Requirements**: [`docs/PRD.md`](../docs/PRD.md), [`PRODUCT.md`](../PRODUCT.md).
- **Design System**: [`DESIGN.md`](../DESIGN.md) — "The Precision Console" visual guidelines.
- **Feature Implementation Plan**: [`docs/plans/feature-implementation-plan.md`](../docs/plans/feature-implementation-plan.md) — TDD specifications for all 12 feature modules.
- **GitHub Workflow**: [`docs/agents/github-workflow.md`](../docs/agents/github-workflow.md) — Issue creation, sub-issues, labels, PR conventions.

---

## Skills Available in `.github/skills/`

All 55 project skills are committed in [`.github/skills/`](./skills/):

- **Issue & Task Management**: `to-tickets`, `to-spec`, `triage`,  `setup-matt-pocock-skills`
- **TDD & Implementation**: `tdd`, `implement-spec`, `implement`, `subagent-driven-development`, `executing-plans`
- **Architecture & Modeling**: `domain-modeling`, `codebase-design`, `improve-codebase-architecture`, `writing-plans`
- **UI & Craft**: `ui-taste`, `impeccable`
- **Review & Quality**: `code-review`, `ponytail`, `ponytail-review`, `systematic-debugging`, `diagnosing-bugs`,
- **Research & Strategy**:  `grilling`, `brainstorming`

---

## Non-Negotiable Coding Rules

1. **Zod Single Source of Truth**: All data models live in `packages/shared/src/schemas/`. Types are derived via `z.infer`. Never write duplicate TypeScript interfaces.
2. **Tenant Isolation**: Every database query must use `scopedQuery(db, req.tenantId)`. Never write raw un-scoped `WHERE tenant_id` queries in routes.
3. **Service Layer**: Business logic belongs in `apps/api/src/services/`. Route handlers only validate → call service → respond.
4. **API Envelope**: All endpoints return `ApiResponse<T>` (`{ success: true, data }`) or `ApiError` (`{ success: false, error }`).
5. **Grounded AI with Citations**: AI responses must cite specific knowledge chunks or explicitly abstain: *"I do not have sufficient information in the knowledge base to answer this question."*
6. **Strict TDD**: Write failing test first → run fail → implement minimal code → run pass → commit.
