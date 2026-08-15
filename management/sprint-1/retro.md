# Retrospektive Sprint 1 — P3 (COACH)

*2026-08-15. Max. 3 Punkte.*

**Gut:** Der komplette Klickbarkeits-Umbau (Router, Detail, Board, Inbox, Banner) blieb innerhalb der ADR-Leitplanken — kein Framework, kein Build, 4 neue Tests decken die neuen Endpunkte. SWR-047 zeigt den kürzesten Weg vom Betriebsschmerz (14 Uhr „unbekannter Endpunkt") zur verhinderten Wiederholung (18 Uhr Banner).

**Erkenntnisse:** 1. Frontend-Verhalten (Router, Filter, Buttons) ist testseitig nur indirekt über die APIs abgedeckt — die UI-Abnahme durch den Auftraggeber am Gerät bleibt Pflichtteil jedes G4 (Stichproben-Tabelle nutzt das bewusst). 2. app.js wächst (~330 Zeilen) — bei weiterem Ausbau in Sprint 2 auf Funktionsgruppen-Kommentare achten, Aufteilung erst erwägen, wenn ADR-002 (eine Datei) real schmerzt.
