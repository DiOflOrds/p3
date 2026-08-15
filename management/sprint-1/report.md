# Sprint-1-Report — P3 „Mission Control 3.0" (PL)

*2026-08-15. Sprint-Motto: „Klickbarkeit". An: Mensch (G4 via Inbox-DR T-0012). 5/5 Tickets done.*

## Sprint-Ziel: erreicht — das HMI ist bedienbar

| Ticket | Ergebnis | Schätzung | Ist |
|---|---|---|---|
| T-0007 | Planning | 10 min | 8 min |
| T-0008 | **Hash-Router + Ticket-Detail** (SWR-040): jede Ansicht verlinkbar (`#/ticket/p3/T-0001`), Detailseite mit Metadaten, Frist/Default, klickbaren T-xxxx-Querverweisen in Body und blocked_by | 45 min | 40 min |
| T-0009 | **Board Jira-like** (SWR-041): Statusspalten als Grid, Filter Sprint/Rolle/Typ, Karten öffnen das Detail | 30 min | 25 min |
| T-0010 | **Inbox interaktiv** (SWR-042): Options-Buttons mit Default-Markierung (Freitext nur noch für Alt-DRs), DR-Historie mit Entscheidungs-Vermerk und Links | 30 min | 30 min |
| T-0011 | **Versions-Banner** (SWR-047): `/api/version` (Prozess- vs. Code-Stand per git), gelbes Banner „Server neu starten" bei Versatz — dein Befund von heute Nachmittag ist damit unmöglich gemacht | 20 min | 15 min |

**E5-Auswertung:** 135 min geschätzt, 118 min Ist (−13 %).

## KPIs

Tests **141 → 145** grün (+4 API-Tests mit SWR-Bezug 040/041/042/047) · Matrix 47/0 · JS-Syntax node-geprüft · 0,00 € API · Statuswechsel 100 % Skript-Route.

## QM-Abschnitt (ungefiltert)

1. Die UI-Abnahme ist Teil des G4-DRs: **deine Antwort per Options-Button IST die Stichprobe** für SWR-042 — dazu Board-Karte und Querverweis-Link anklicken (SWR-040/041). 2. Requirements/Traceability sind noch Text-Dumps — Tabellen kommen planmäßig in Sprint 2 (SWR-043/044). 3. Nach dem Push: Server neu starten — ab diesem Update sagt dir das künftig das Banner selbst.

## Entscheidungsbedarf: G4 Sprint 1 → Inbox-DR T-0012
