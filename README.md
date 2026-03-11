# mrsmith-skills

Öffentliche Skill-Bibliothek für [Mr. Smith](https://mrsmith.app) — die KI-Steuerzentrale.

## Was sind Skills?

Skills erweitern Mr. Smith mit Wissen und Verhaltensweisen:

- **Task-Skills** — Wissen für den Brain (Mr. Smith). Wird in den System-Prompt eingebettet.
- **Persona-Skills** — Anweisungen für Ausführer (Codex, Claude Code, …). Wird dem Prompt vorangestellt.

## Verfügbare Skills

| Skill | Typ | Beschreibung |
|-------|-----|--------------|
| [git-flow](git-flow.md) | Task | Git-Flow-Konvention: Feature-Branches, Commits, Review vor Merge |
| [roadmap](roadmap.md) | Task | Roadmap & Milestone-Management: Status-Tracking, Checkpoint-Updates |
| [code-review](code-review.md) | Task | Code-Review-Checkliste: Qualität, Sicherheit, Lesbarkeit |
| [tdd](tdd.md) | Task | Test-Driven Development: Red-Green-Refactor-Zyklus |
| [conventional-commits](conventional-commits.md) | Task | Conventional Commits Standard: feat/fix/chore/docs/refactor |

## Installation

Im Mr. Smith Skill-Manager → „Skills durchsuchen" → Skill auswählen → Installieren.

Oder manuell: Skill-URL einfügen unter „Importieren".

## Eigene Skills beitragen

1. Fork erstellen
2. Neue `.md`-Datei mit YAML-Frontmatter anlegen (siehe Vorlage unten)
3. Pull Request erstellen

### Skill-Vorlage

```markdown
---
name: Skill-Name
type: task
executor:
description: Kurze Beschreibung was dieser Skill bewirkt
enabled: true
source: https://optional-link-to-source-or-docs
---

# Skill-Name

Inhalt des Skills — Markdown, Anweisungen, Beispiele.
```

## Lizenz

MIT
