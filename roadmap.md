---
name: Roadmap & Milestone-Management
type: task
executor:
description: Mr. Smith pflegt aktiv die Projekt-Roadmap, trackt Milestone-Fortschritt und schlägt neue Einträge vor
enabled: true
source:
---

# Roadmap & Milestone-Management

## Wann anwenden
Wenn der User über Features, Aufgaben, Bugs oder Pläne spricht. Mr. Smith prüft ob ein ROADMAP.md existiert und schlägt vor, neue Items einzutragen oder den Status bestehender Items zu aktualisieren.

## Roadmap-Datei

- Standard-Pfad: `ROADMAP.md` im Projektwurzelverzeichnis
- Format: Markdown mit Status-Emojis, Milestone-Blöcken und Aufgabenlisten
- Wenn keine Roadmap existiert: anbieten, eine anzulegen

## Status-Emojis

| Emoji | Bedeutung |
|-------|-----------|
| ⚪ | Geplant – noch nicht begonnen |
| 🟡 | In Arbeit – aktueller Milestone |
| 🟢 | Abgeschlossen – alle Schritte ✅ |
| 🔴 | Blockiert – wartet auf Abhängigkeit |
| 💡 | Idee – noch nicht bewertet |

## Aufgaben-Checkboxen

```markdown
- [ ] Noch offen
- [x] Erledigt
```

## Milestone-Format

```markdown
## Mx.y: Titel [Status-Emoji]

Kurzbeschreibung was dieser Milestone erreicht.

- [ ] Aufgabe 1
- [ ] Aufgabe 2
- [x] Aufgabe 3 (erledigt)
```

## Mr. Smith's Verhalten

### Neues Feature / Idee
Wenn der User eine neue Idee oder ein Feature erwähnt, das noch nicht in der Roadmap steht:
1. In der Roadmap nachsehen (falls vorhanden)
2. Vorschlagen: „Soll ich das als `Mx.y: Titel 💡` in die Roadmap aufnehmen?"
3. Nach Zustimmung: ROADMAP.md aktualisieren

### Milestone gestartet
Wenn eine Arbeit an einem Milestone beginnt:
- Status von ⚪ auf 🟡 setzen
- Aufgaben-Checkboxen ergänzen falls noch nicht vorhanden

### Aufgabe abgeschlossen
Nach einem erfolgreichen Job oder einer erledigten Teilaufgabe:
- Entsprechende Checkbox `[ ]` → `[x]`
- Wenn alle Checkboxen ✅: Milestone-Status auf 🟢

### Milestone-Nummern vergeben
- Hauptmeilensteine: M1, M2, M3 …
- Teilmeilensteine: M9.1, M9.2, M9.3 …
- Sub-Tasks innerhalb eines Milestones: Checkboxen, keine eigene Nummer nötig

## Roadmap-Review
Wenn der User nach dem Stand fragt ("Wo stehen wir?", "Was kommt als nächstes?"):
- Kurze Zusammenfassung: aktueller 🟡 Milestone, nächste ⚪ Milestones
- Offene Punkte im laufenden Milestone auflisten
- Kein vollständiges Vorlesen der Datei – nur das Wesentliche

## Regeln
- Roadmap-Updates immer mit User-Zustimmung oder auf explizite Anfrage
- Keine Milestone-Nummern doppelt vergeben
- Ideen-Items (💡) nur auf Roadmap, nicht autonom als nächsten Schritt behandeln
- Bei Konflikten zwischen Roadmap und aktuellem Auftrag: nachfragen
