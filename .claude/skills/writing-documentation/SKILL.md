---
name: writing-documentation
description: How to decide what a project documents, which document owns each fact, and how much detail each gives. Use when writing, restructuring or reviewing documentation such as a README, design, spec, decision record, runbook or glossary, or when the same fact appears in several places.
---

# Writing documentation

Put each fact in the narrowest document that is authoritative for it, at the level of detail
that document's question needs; everywhere else, point to it rather than restate it. A fact
with two owners becomes two facts the first time one copy changes.

Every piece of documentation answers three questions:

- **Right information:** is this worth writing down? Leave out what a reader finds faster in
  the code, a tool's help or the live system, and what nobody will act on.
- **Right place:** which document owns it? Ask: *if this fact changed, which document would
  be changed first?* That one owns it. Projects split ownership differently; as an
  illustration only, a glossary may own what terms mean, a domain model which concepts exist
  and how they relate, a design what the system should do, a security model its trust
  boundaries, an architecture document how it is built, a runbook how to operate and recover
  it, a decision record why a choice was made, and a README orientation and navigation.
  Follow the documents the project already has.
- **Right resolution:** how much of it belongs here? The same concept appears at different
  depths: its meaning in one place, its relationships in another, its implementation in a
  third. Each document carries only the depth its own question needs.

## Repeating and pointing

Repeat consequences where readers need them; do not repeat definitions or governing rules.
"This operation needs re-authentication" applies a rule where it matters; restating what
re-authentication involves, or which operations need it, creates a second authority. A
document still carries enough local context to answer its own question without a chain of
links: a sentence of context and a pointer to the owner, not a copy of the owner.

When moving a fact to its owner, check that the owner already says it, and add it there if
not, before removing the copy.

## Stability

Keep facts that change at the same pace together. A concept that holds for years and a layout
that changes next month, written side by side, tie the stable document to the volatile one's
edits. Volatile detail lives with the design or implementation it describes.

## New documents

Give a fact a new document only when its owner or its readers are actually distinct, not
because it is a distinct concept. A section of an existing document is usually the right home
until it needs its own.

The project's own conventions for its documents win over anything here.

## Specific documents

- Read [references/glossaries.md](references/glossaries.md) when creating, reviewing or
  pruning a glossary.
