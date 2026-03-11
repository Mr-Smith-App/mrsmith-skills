---
name: Code-Review-Checkliste
type: task
executor:
description: Mr. Smith prüft Code systematisch auf Qualität, Sicherheit und Lesbarkeit
enabled: true
source:
---

# Code-Review-Checkliste

## Wann anwenden
Wenn ein Job abgeschlossen ist und der Output Code-Änderungen enthält. Auch wenn der User explizit um ein Code-Review bittet.

## Review-Dimensionen

### Korrektheit
- [ ] Löst der Code das beschriebene Problem?
- [ ] Gibt es Edge Cases die nicht behandelt werden?
- [ ] Sind alle Fehlerfälle abgedeckt?

### Sicherheit
- [ ] Keine hartcodierten Credentials oder API-Keys
- [ ] Keine SQL-Injection-Risiken (parametrisierte Queries)
- [ ] Keine XSS-Lücken (kein unescaptes HTML aus User-Input)
- [ ] Input-Validierung an Systemgrenzen

### Lesbarkeit
- [ ] Verständliche Variablen- und Funktionsnamen
- [ ] Keine übermäßige Komplexität (> 3 Verschachtelungsebenen)
- [ ] Keine Magic Numbers ohne erklärende Konstante

### Wartbarkeit
- [ ] DRY: Kein duplizierter Code
- [ ] Einzelne Verantwortung pro Funktion / Klasse
- [ ] Keine unnötigen Abhängigkeiten

## Review-Format

Bei einem Code-Review antwortet Mr. Smith mit:
```
## Code-Review

### ✅ Positiv
- Was gut gelöst wurde

### ⚠️ Verbesserungsvorschläge
- Was überarbeitet werden könnte (nicht blockierend)

### ❌ Probleme
- Was behoben werden muss (blockierend)

### Fazit
Kurzes Gesamturteil + nächster Schritt
```

## Regeln
- Immer konstruktiv formulieren — Vorschlag statt Kritik
- Probleme mit konkretem Fix-Vorschlag versehen
- Keine Review-Pflicht bei Trivialänderungen (Typos, Formatierung)
