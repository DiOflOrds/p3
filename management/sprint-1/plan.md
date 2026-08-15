# Sprint-1-Plan P3 „Mission Control 3.0" (PL)

*2026-08-15, nach G1 (D001, `p3-req-v1.0`) und G2 (D002, ADR-005). Sprint-Ziel: „Klickbarkeit" — Ticket-Detail, Jira-Board, interaktive Inbox, Versions-Hinweis; alles am Gerät erlebbar.*

| Ticket | Prozess | Rolle | Inhalt | SWR | Schätzung |
|---|---|---|---|---|---|
| T-0007 | man3 | pl | Dieses Planning | — | 10 min |
| T-0008 | swe3 | dev | Hash-Router (ADR-005) + Ticket-Detail: API `/api/ticket`, Detailansicht, T-xxxx-Querverweise als Links | 040 | 45 min |
| T-0009 | swe3 | dev | Board Jira-like: Statusspalten, Karten, Filter Sprint/Rolle/Typ, Karte → Detail | 041 | 30 min |
| T-0010 | swe3 | dev | Inbox interaktiv: Options-Buttons statt Freitext, DR-Historie (API + View) | 042 | 30 min |
| T-0011 | swe3 | dev | `/api/version` (Prozess- vs. Code-Stand) + Frontend-Banner „Server-Neustart nötig" | 047 | 20 min |

## Nachweise am Sprint-Ende

API-Tests je Endpunkt (Docstring-SWR-Bezug → Matrix), UI-Abnahme am Gerät durch den Auftraggeber (Stichproben im G4-DR), Suiten + Matrix grün auf Team-Node (Runbook Kap. 9).
