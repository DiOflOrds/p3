# Projektauftrag P3 — „Mission Control 3.0: Jira-like HMI" (v0.1, zur G0-Freigabe)

*2026-08-15, PL. Eingang per Intake, Projektwunsch wörtlich vom Auftraggeber (Session-Dialog): besseres HMI — alles klickbar, alle Tasks öffnenbar (Jira-like), Inbox klickbar, Requirements/Traceability tabellarisch, Architektur als Bild, insgesamt interaktiver mit allen relevanten Projektinformationen. G0-Freigabe: Inbox-DR T-0001.*

## Was und Warum

Mission Control kann seit P1 alle Daten **anzeigen** — P3 macht sie **bedienbar**. Heute sind Board, Requirements und Traceability im Wesentlichen gerenderte Textblöcke; Details erfordern den Weg ins Repo. P3 baut das Frontend zur echten Arbeitsoberfläche um: Navigation per Klick statt Dateisuche, Tabellen statt Markdown-Dumps, ein Architekturbild statt Prosa. Die Quelle der Wahrheit bleibt unverändert Git (Tickets-as-Code, Markdown) — das HMI parst und verlinkt, es ersetzt nichts.

**Zielprodukt-Typ:** Plattform/Frontend (SW, F6) · **Nutzerkreis:** Auftraggeber + Registry-Nutzer (F9/SWR-037) · **Vertraulichkeit:** privat (F10) · **Budget:** D012 unverändert, 0 € API (Skript/Ollama/Session; Copilot inaktiv per D026) · **Rahmen:** ADR-001/002 bleiben (stdlib-Backend, No-Build-PWA) — Interaktivität in Vanilla JS, Diagramme als generiertes/gezeichnetes SVG.

## Epics (aus dem Projektwunsch)

| Epic | Inhalt | Wunsch-Bezug |
|---|---|---|
| P3-E1 | **Ticket-Detail + Board-Navigation:** jedes Ticket klickbar → Detailansicht (Metadaten strukturiert, Body gerendert, Statusverlauf); Querverweise (T-xxxx, blocked_by) als Links; Board Jira-like mit Statusspalten und Filtern (Sprint/Rolle/Typ) | „alle Tasks kann man öffnen, Jira-like" |
| P3-E2 | **Inbox interaktiv:** DR-Detail per Klick, Optionen als Buttons (statt Freitextfeld), Historie entschiedener DRs einsehbar | „Inbox ebenfalls klickbar" |
| P3-E3 | **Requirements + Traceability tabellarisch:** STK/SWR als sortier- und filterbare Tabellen (ID, Titel, Status, Trace); Traceability-Matrix als echte Tabelle SWR ↔ Tests mit Abdeckungsstatus | „in tabellarischer Form" |
| P3-E4 | **Architektur als Bild:** SW-Architektur (Komponenten + Beziehungen) aus einer versionierten, maschinenlesbaren Quelle als SVG im Frontend; neuer Tab „Architektur" | „Architecture als Bild, graphisch" |
| P3-E5 | **Projekt-Cockpit:** Übersicht je Projekt mit allen relevanten Informationen auf einen Blick — Sprint-Fortschritt, offene DRs (mit Frist-Ampel), letzte Baseline, KPIs, Verweise klickbar | „alle relevanten Informationen erhalten" |

## Abnahmekriterien

1. Vom Board aus ist jedes Ticket öffnenbar; Querverweise in Ticket-Texten sind klickbar und führen zur richtigen Detailansicht (Stichprobe am Gerät).
2. Eine echte Inbox-Entscheidung wird komplett per Klick getroffen (Option-Button, kein Freitext) und die Historie entschiedener DRs ist einsehbar.
3. Requirements- und Traceability-Tab zeigen sortier-/filterbare Tabellen; die Matrix zeigt je SWR den Testabdeckungsstatus.
4. Der Architektur-Tab zeigt ein aus versionierter Quelle generiertes Diagramm, das bei Architekturänderung mitwächst (Nachweis: eine Änderung, Bild folgt).
5. Requirements-first (SWR-Erweiterung reviewed vor Umsetzung, Matrix 0 Lücken), alle Gates als Inbox-DRs mit Frist-Default, Aufwandsschätzung in jedem Planning (P2-Standard).

## Rahmen

3 Sprints (S0 Anforderungen + G1 + G2-Architektur-Delta; S1 E1/E2; S2 E3/E4/E5 + Abnahme). Playbook, Ticket-Board, Baselines als Tags + Manifest, Team-Node-Gate (Runbook Kap. 9), Sandbox pusht nie.
