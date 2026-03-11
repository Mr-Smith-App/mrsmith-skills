---
name: Conventional Commits
type: task
executor:
description: Mr. Smith verwendet den Conventional Commits Standard für alle Commit-Messages
enabled: true
source: https://www.conventionalcommits.org/
---

# Conventional Commits

## Format

```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

## Typen

| Typ | Verwendung |
|-----|-----------|
| `feat` | Neues Feature (Minor-Version) |
| `fix` | Bugfix (Patch-Version) |
| `docs` | Nur Dokumentation |
| `style` | Formatierung, kein Code-Wechsel |
| `refactor` | Weder Feature noch Fix |
| `test` | Tests hinzufügen / korrigieren |
| `chore` | Build-Prozess, Hilfsmittel |
| `perf` | Performance-Verbesserung |
| `ci` | CI-Konfiguration |

## Breaking Changes

```
feat!: neue API ohne Abwärtskompatibilität
```
oder im Footer:
```
BREAKING CHANGE: beschreibung
```

## Beispiele

```
feat(auth): OAuth2-Login hinzufügen
fix(chat): Streaming-Abbruch bei langen Antworten behoben
docs(readme): Installationsanleitung aktualisiert
refactor(jobs): JobQueue auf Arc<RwLock> umgestellt
test(brain): Unit-Tests für parse_skill_frontmatter
chore(deps): reqwest auf 0.12 aktualisiert
```

## Scope-Konventionen

Der Scope beschreibt den betroffenen Bereich. Konsistente Scopes pro Projekt verwenden.

## Regeln
- Beschreibung in Kleinbuchstaben, kein Punkt am Ende
- Imperativ verwenden: "hinzufügen" nicht "hinzugefügt"
- Scope optional aber empfohlen bei größeren Projekten
