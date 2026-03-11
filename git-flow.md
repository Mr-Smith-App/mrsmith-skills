---
name: Git Flow Konvention
type: task
executor: 
description: Mr. Smith arbeitet nach Git-Flow – Feature-Branches pro Milestone, Review vor Merge
enabled: true
source: https://nvie.com/posts/a-successful-git-branching-model/
---

# Git Flow Konvention

## Wann anwenden
Immer wenn das Projekt ein Git-Repository hat und eine mehrschrittige Aufgabe (Milestone, Feature, Bugfix) beginnt. Prüfe ob Git aktiv ist bevor du einen Branch vorschlägst.

## Branch-Strategie

| Branch | Zweck |
|--------|-------|
| `main` / `master` | Produktionsstand – niemals direkt committen |
| `develop` | Integrations-Branch – Basis für alle Features |
| `feature/xxx` | Eine Aufgabe / ein Milestone – von `develop` abzweigen |
| `fix/xxx` | Bugfix – von `develop` oder `main` abzweigen |

## Workflow pro Milestone

### 1. Milestone starten
Schlage zu Beginn jedes Milestones vor:
```
[EXECUTOR:shell]
title: Feature-Branch anlegen
git checkout develop && git pull && git checkout -b feature/<milestone-name-kebab-case>
[/EXECUTOR]
```
Branch-Name: kurz, beschreibend, kebab-case. Beispiele:
- `feature/skill-manager`
- `feature/auth-refactoring`
- `fix/login-crash`

### 2. Während der Arbeit
- Jeder abgeschlossene Schritt kann als Zwischen-Commit vorgeschlagen werden
- Commit-Messages: `feat(scope): was wurde gemacht` / `fix(scope): was wurde behoben`
- NIEMALS auf `develop` oder `main` direkt committen

### 3. Milestone abgeschlossen – Review
Wenn alle Schritte ✅ PASS sind, schlage vor:
```
[EXECUTOR:shell]
title: Branch pushen
git push -u origin feature/<branch-name>
[/EXECUTOR]
```
Danach: User explizit um Review bitten. Merge erst nach expliziter Zustimmung.

### 4. Merge nach Review
```
[EXECUTOR:shell]
title: In develop mergen
git checkout develop && git merge --no-ff feature/<branch-name> && git push
[/EXECUTOR]
```
`--no-ff` erzwingt einen Merge-Commit – Milestone bleibt in der History sichtbar.

## Commit-Message-Format
```
feat(scope): kurze Beschreibung
fix(scope): was behoben
refactor(scope): was umgebaut
docs(scope): Dokumentation
test(scope): Tests
```

## Regeln
- Einen Branch pro Milestone / Feature – nicht alles auf einen Branch
- Merge erst nach User-Review – niemals autonom mergen
- Bei Konflikten: dem User beschreiben was kollidiert, nicht autonom entscheiden
- `git push --force` niemals verwenden
