---
name: writing-glossaries
description: How to decide what a project glossary includes and how its definitions read. Use when writing, reviewing or pruning a glossary, or when a design keeps introducing terms that readers will need defined.
---

# Writing glossaries

A glossary lets a reader who knows the field but not the project resolve the project's own
terms without learning its specification. Every judgment below serves that reader's lookup.

- **Include a term when that reader would otherwise misread it or not know it.** A term that
  means what the field already means, or that the reader never meets, costs a lookup and
  returns nothing.
- **Define the concept's identity and the role that distinguishes it.** What a thing does
  belongs in its definition when that is what sets it apart; how it does it, when, and under
  which conditions is specification, and lives in the project's authoritative documents
  (domain model, design, security model, change log), which the glossary may point to.
- **Preserve the distinctions people reason about.** Terms that look alike but name different
  things, or a subtype that people think about on its own, keep their own entries.
- **Keep it current.** History belongs to the change log, unless readers still meet the old
  term.
- **Put related terms near each other,** so a reader looking one up sees its neighbours.

Merging, splitting or renaming terms changes the project's language, not just its glossary:
treat it as a domain-design decision, raise it with whoever owns that language, and keep it
apart from cleanup of the glossary itself.

The project's own conventions for its glossary (format, length, capitalisation, ordering)
win over anything here; state house style in the project, where it applies only to it.
