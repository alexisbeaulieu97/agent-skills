---
name: writing-documentation
description: How to decide what a project documents, which document owns each fact, and how much detail each gives. Use when writing, restructuring or reviewing documentation such as a README, design, spec, decision record, runbook or glossary, or when the same fact appears in several places.
---

# Writing documentation

Every document answers one question, and owns the facts that answer it. Put each fact in the
narrowest document whose question it answers, at the detail that question needs; everywhere
else, apply or point to it rather than restate it. A fact with two owners becomes two facts
the first time one copy changes. The project's own conventions for its documents win over
anything here.

For each piece of information, settle three things:

- **Right information:** is it worth writing down? Leave out what a reader finds faster in
  the code, a tool's help or the live system, unless the reader needs an interpretation of
  it, and what nobody will act on. If software can check it, a check beats a sentence.
- **Right place:** which document's question does it answer? Confirm with *if this fact
  changed, which document would change first?* Projects split their questions differently;
  as an illustration only: a glossary answers what a term means, a domain model what concepts
  exist and how they relate, a design what the system should do, a security model what must
  stay true for it to be secure, an architecture document how it is built, a runbook how to
  perform or recover an operation, a decision record why a choice was made, and a README what
  this is and where to go next. Follow the documents the project already has.
- **Right resolution:** how much of it belongs here? The same concept appears at different
  depths: its meaning in one place, its relationships in another, its implementation in a
  third. Each document carries only the depth its own question needs. A rule goes at the
  narrowest level where it stays true: a general principle in shared guidance, a house rule
  in the project, an exact rule in a check.

## Applying and redefining

Centralise definitions and governing rules; distribute their consequences where readers need
them. "Deleting this needs re-authentication" applies a rule; restating what
re-authentication involves, or which operations need it, redefines it and creates a second
authority. A document still answers its own question without a chain of links: a sentence of
context and a pointer to the owner, not a bare "see elsewhere", and not a copy of the owner.

When moving a fact to its owner, check that the owner already says it, and add it there if
not, before removing the copy.

## Change together, live together

Keep information with information that changes for the same reasons at the same pace. A
concept that holds for years and a layout that changes next month, written side by side, tie
the stable document to the volatile one's edits. Volatile detail lives with the design or
implementation it describes.

## New documents

A new document is another place to search and another place for truth to drift. Give
information its own document only when it has its own boundary: a different owner of the
truth, different readers or moments when it is needed, or a different reason and pace of
change. Being a distinct topic is not enough; a section of an existing document is usually
the right home until one of those boundaries appears.

## Specific documents

- Read [references/glossaries.md](references/glossaries.md) when creating, reviewing or
  pruning a glossary.
