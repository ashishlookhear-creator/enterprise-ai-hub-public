# Enterprise AI Hub — Public Demo PRD

Draft for design review. All people, organizations, documents, metrics and requests are fictional.

## Purpose and audience

Help a Business User discover approved AI apps, ask questions with citations, prepare an operations briefing, track a request, and manage recurring work. This public release is a static design demonstration.

## Demonstrated journeys

- Sign-in and workspace selection as simulated screens.
- Browse AI apps and configure a briefing.
- Ask Copilot and inspect illustrative citations.
- Browse knowledge collections and processing states.
- Configure an automation and inspect its proposed schedule.
- Review a proposed follow-up, submit for authorization, and track status.
- Browse reports, export a synthetic text report, view notifications and usage.
- Adjust illustrative preferences and inspect feedback forms.

## Functional requirements for the future application

| ID | Requirement | Acceptance condition |
|---|---|---|
| BR01 | Discover authorized apps | Only apps permitted for the signed-in workspace appear. |
| BR02 | Ground answers in accessible sources | Each supported factual answer has a source reference the user can open. Missing evidence is stated. |
| BR03 | Protect document access | Server checks workspace and document authorization before retrieval and citation rendering. |
| BR04 | Review external actions | Show destination, payload and proposal version before submission. Execution requires a recorded authorized decision. |
| BR05 | Track work durably | Request status and history survive restarts. Retries avoid duplicate external actions. |
| BR06 | Manage schedules | Explain timezone, next run, pause and failure recovery. |
| BR07 | Control cost | Apply usage limits and per-request budgets before expensive execution. |
| BR08 | Provide useful errors | Preserve user work and show a clear recovery option. |

## Proposed implementation

React and TypeScript frontend, Spring Boot or compatible API backend, Python FastAPI AI service, PostgreSQL, authorized RAG retrieval, LangGraph approval workflows, an n8n integration boundary, MLflow evaluation tracking, and Docker development services. These modules are proposed for the Business User design. The public demo does not implement them.

## Delivery gates

1. Product discovery and verified repository audit.
2. PRD, scope and measurable acceptance criteria review.
3. Desktop design and interaction review, followed by responsive and accessibility review.
4. Local vertical slice with synthetic fixtures and automated tests.
5. Retrieval evaluation, authorization tests and approval replay tests.
6. CI checks, secret scanning, dependency review and deployment readiness.
7. Explicit approval before paid resources or external application deployment.
8. Monitor quality, latency, cost and failures, then iterate against a versioned baseline.

## Release status

Completed in this public package: 30-screen HTML walkthrough, local navigation, selected UI states, synthetic text export and public product summary.

Proposed: real authentication, retrieval, model calls, document processing, durable workflows, integrations, production monitoring and cloud deployment. All visible metrics and success states are illustrative.

## Validation expectations

For this static release, verify all 30 screen routes, navigation, local export, disabled file selection and absence of external network calls in application code. For implementation, add access-isolation tests, unsupported-answer checks, versioned approvals, idempotency, budget enforcement, accessibility and recovery tests.
