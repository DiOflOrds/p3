# Sprint-2-Report — P3 „Mission Control 3.0" (PL)

*2026-08-15. Sprint-Motto: „Tabellen, Bild, Cockpit". An: Mensch (G4 + P3-Abnahme via Inbox-DR T-0018). 5/5 Tickets done.*

## Sprint-Ziel: erreicht

| Ticket | Ergebnis | Schätzung | Ist |
|---|---|---|---|
| T-0013 | Planning | 10 min | 8 min |
| T-0014 | **Tabellen** (SWR-043/044): Markdown-Parser im Backend (unit-getestet), Requirements + Traceability-Matrix als sortier- und filterbare Tabellen mit klickbaren Querverweisen | 40 min | 35 min |
| T-0015 | **Architekturbild** (SWR-045): `komponenten.yaml` → deterministischer SVG-Generator (4 Schichten, 11 Beziehungen) → neuer Tab; Drift-Check als abschluss-Gate | 45 min | 40 min |
| T-0016 | **Cockpit** (SWR-046): Übersicht zeigt je Projekt Status-Zahlen, offene DRs mit Frist-Ampel (rot/gelb/grün), letzte Baseline, KPI — alles klickbar | 35 min | 30 min |
| T-0017 | dieser Report + Schluss-Retro + Abnahmebilanz | 25 min | 22 min |

**E5-Auswertung:** 155 min geschätzt, 135 min Ist (−13 % — konsistent mit Sprint 1; Kalibrierung stabil).

## Abnahmebilanz K1–K5 (Projektauftrag)

| K | Kriterium | Bewertung | Evidenz |
|---|---|---|---|
| 1 | Jedes Ticket öffnenbar, Querverweise klickbar | **erfüllt** | SWR-040/041, Sprint-1-Stichproben real (D003 per Button nach Klickstrecke) |
| 2 | Inbox-Entscheidung komplett per Klick + Historie | **erfüllt** | SWR-042; D003 war eine echte Button-Entscheidung; Historie im Inbox-Tab |
| 3 | Requirements/Traceability sortier-/filterbar mit Abdeckungsstatus | **erfüllt mit deiner Stichprobe** | SWR-043/044, Parser-Tests; UI-Blick im Abnahme-DR |
| 4 | Architekturbild aus versionierter Quelle, wächst mit | **erfüllt** | SWR-045: Generator-Tests inkl. Drift-Erkennung, --check im abschluss-Gate |
| 5 | Requirements-first, Gates via Inbox mit Default, Schätzung gelebt | **erfüllt** | `p3-req-v1.0` vor Umsetzung; D000–D003 via Inbox; Schätzspalte in allen Plannings |

## KPIs

Tests **145 → 153** grün (+4 Parser/Cockpit, +4 Generator) · Matrix 47/0 · app.js ≈ 430 Zeilen (eine Datei, ADR-002 hält) · 0,00 € API · 4 Inbox-Entscheidungen in P3, alle mit Mail-Nachweis.

## QM-Abschnitt (ungefiltert)

1. K3-Rest: die Tabellen-UI hat Parser-Tests, aber der Sortier-/Filter-Code läuft ungetestet im Browser — deine Stichprobe im Abnahme-DR ist der Nachweis. 2. Das Architekturbild zeigt die Plattform-Ebene; Produkt-Architekturen (datakonv) sind bewusst nicht drin (eigene Quelle wäre ein CR). 3. Nach dem Push: Server neu starten — das Banner erinnert dich jetzt selbst.

## Entscheidungsbedarf: G4 + P3-Abnahme → Inbox-DR T-0018
