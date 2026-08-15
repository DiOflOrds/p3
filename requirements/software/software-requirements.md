# Software Requirements — P3 "Mission Control 3.0" (extension of platform baseline)

*Extends SWR-001–039; numbering continues. Components: BCK/FRT (backend/frontend), TOOL (scripts). Language: English (D011). Status `reviewed` = feasibility (ARCH/DEV context) + verifiability (QM/TEST context) per DoD checklist. Verification is UI acceptance checklist plus tests; unit/API-test coverage lands with the implementation sprints and then shows in the matrix. v0.1 Sprint 0, T-0003 — G1 pending (Inbox-DR T-0005).*

## Ticket detail and board (P3-E1)

| ID | Requirement | Trace | Verification | Prio | Status |
|---|---|---|---|---|---|
| SWR-040 | The backend shall serve a single ticket's full data (metadata fields and body) via API per project, and the frontend shall show a ticket detail view opened by click from any card or list; ticket references (T-xxxx) inside rendered texts shall be links to the referenced ticket's detail view. | STK-015 | API tests (detail endpoint, unknown ticket 404) + UI acceptance checklist (click paths, reference links) | high | reviewed |
| SWR-041 | The board view shall present tickets Jira-like as cards in status columns with filters for sprint, role, and type; each card opens the detail view. | STK-015 | UI acceptance checklist + API tests (board data grouped/filterable) | high | reviewed |

## Interactive inbox (P3-E2)

| ID | Requirement | Trace | Verification | Prio | Status |
|---|---|---|---|---|---|
| SWR-042 | The inbox shall render a decision request's options as buttons (from the ticket's options field) so a decision is made by click plus optional reason — no free-text option entry for DRs with defined options; and decided DRs shall remain accessible in a read-only history list. | STK-015 | API tests (history endpoint) + UI acceptance checklist (button decision round-trip) | high | reviewed |

## Tables for requirements and traceability (P3-E3)

| ID | Requirement | Trace | Verification | Prio | Status |
|---|---|---|---|---|---|
| SWR-043 | The requirements view shall parse the stakeholder and software requirement tables and present them as sortable, filterable tables (ID, title/requirement, trace, status) instead of raw markdown. | STK-015 | Unit tests (markdown table parser) + UI acceptance checklist | high | reviewed |
| SWR-044 | The traceability view shall present the SWR↔test matrix as a table per SWR with covering tests and a coverage status, parsed from the generated matrix reports of the selected project scope. | STK-015 | Unit tests (matrix parser) + UI acceptance checklist | medium | reviewed |

## Architecture as a picture (P3-E4)

| ID | Requirement | Trace | Verification | Prio | Status |
|---|---|---|---|---|---|
| SWR-045 | The software architecture shall be described in a versioned machine-readable source (components and relations); a script shall generate an SVG diagram from it, and the frontend shall show the diagram in a new architecture tab — a change to the source changes the picture. | STK-015 | Unit tests (generator: source → SVG) + UI acceptance checklist (tab shows current diagram) | high | reviewed |

## Project cockpit and operability (P3-E5)

| ID | Requirement | Trace | Verification | Prio | Status |
|---|---|---|---|---|---|
| SWR-046 | The per-project cockpit shall show sprint progress (ticket counts per status), open decision requests with a deadline traffic light, the latest baseline, and KPI figures — every entry clickable to its detail. | STK-015 | API tests (cockpit aggregation) + UI acceptance checklist | high | reviewed |
| SWR-047 | The frontend shall display the backend's version/start identity and show a clear "restart the server" hint when frontend and backend versions differ, instead of failing with generic endpoint errors. | STK-015 | API test (version endpoint) + UI acceptance checklist (mismatch hint) — Betriebs-Befund 2026-08-15 (Runbook Kap. 5) | medium | reviewed |

## Traceability

STK-015 ← SWR-040–047 (complete; no orphans). DoD checklist applied per SWR (2026-08-15 RM — feasibility ARCH/DEV context incl. ADR-002 no-build constraint, verifiability QM/TEST context). G1 pending (T-0005); architecture delta for routing and diagram source in G2 (T-0006).
