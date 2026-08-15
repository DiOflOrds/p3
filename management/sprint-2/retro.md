# Schluss-Retrospektive P3 — Sprint 2 + Projekt (COACH)

*2026-08-15.*

**Gut über das Projekt:** Vom wörtlichen Auftraggeber-Wunsch („Jira-like, alles klickbar") bis zur Abnahme in drei Sprints am selben Tag — jede Anforderung direkt aus dem Wunsch oder aus echtem Betriebsschmerz (SWR-047). Die ADR-Leitplanken (stdlib, No-Build) haben alle fünf Epics getragen; der Umbau brauchte kein einziges neues Framework. Erstmals liefen **alle** Gates eines Projekts über die Inbox (D000–D003), zwei davon schon mit den neuen Options-Buttons.

**Hakte:** 1. Frontend-Logik bleibt der blinde Fleck der Testpyramide (nur API-/Parser-Tests) — die UI-Stichprobe des Auftraggebers ist bewusst Pflichtteil jedes G4, aber bei weiterem Frontend-Ausbau lohnt ein JS-Testansatz (No-Build-kompatibel; als CR bei Bedarf). 2. app.js wächst — Schwelle für eine Aufteilung (ADR-002-Anpassung) im Auge behalten.

**Übergabe an den Betrieb:** Kein neuer Sprint — P3 endet mit der Abnahme. Empfehlungen: R1 JS-Test-CR bei nächstem Frontend-Projekt; R2 Produkt-Architekturen als eigene komponenten.yaml je Produkt-Repo (CR, wenn gewünscht). Offen im Betrieb nur BB-5 (PAT-Erneuerung ab 2026-09-05).
