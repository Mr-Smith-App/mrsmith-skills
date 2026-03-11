---
name: Test-Driven Development
type: task
executor:
description: Mr. Smith arbeitet nach dem TDD-Zyklus Red-Green-Refactor und schlägt Tests vor neuer Implementierung vor
enabled: true
source: https://martinfowler.com/bliki/TestDrivenDevelopment.html
---

# Test-Driven Development (TDD)

## Wann anwenden
Wenn neue Funktionalität implementiert werden soll und das Projekt eine Test-Infrastruktur hat (package.json mit test-Script, Cargo.toml mit test, pytest, etc.).

## Der TDD-Zyklus

### 1. Red — Failing Test schreiben
Bevor Implementierung: Test für das gewünschte Verhalten schreiben. Der Test muss zunächst fehlschlagen.

```
[EXECUTOR:codex]
title: Failing Test schreiben
Schreibe einen Test für <Funktionalität>. Der Test soll zunächst fehlschlagen.
[/EXECUTOR]
```

### 2. Green — Minimale Implementierung
Minimalen Code schreiben damit der Test besteht. Kein Over-Engineering.

```
[EXECUTOR:codex]
title: Implementierung (Test grün machen)
Implementiere <Funktionalität> so minimal wie nötig, damit der Test besteht.
[/EXECUTOR]
```

### 3. Refactor — Code aufräumen
Test bleibt grün, Code wird verbessert (Lesbarkeit, Struktur, Duplikate entfernen).

## Mr. Smith's Verhalten bei TDD

- Vor jedem Feature-Job: TDD vorschlagen falls Tests im Projekt vorhanden sind
- Nach jedem Job: Test-Run vorschlagen (`npm test`, `cargo test`, `pytest`)
- Bei Testfehler: Test-Output analysieren und gezielten Fix vorschlagen
- Kein Überspringen des Red-Schritts — "Tests schreiben wir nachher" ablehnen

## Regeln
- Unit Tests: eine Funktion / ein Verhalten pro Test
- Keine Tests für Implementierungsdetails — nur für Verhalten (Black-Box)
- Test-Coverage kein Selbstzweck — 80% gut gepflegte Tests > 100% sinnlose Tests
