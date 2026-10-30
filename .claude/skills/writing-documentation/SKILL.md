---
name: writing-documentation
description: How to decide what a project documents, which document owns each fact, how much detail each gives, and how to keep it short and clear. Use when writing, restructuring, reviewing or curating documentation such as a README, design, spec, decision record, runbook or glossary, or when the same fact appears in several places.
---

# Writing documentation

Every document answers one question, and owns the facts that answer it. Put each fact in the
narrowest document whose question it answers, at the detail that question needs; everywhere
else, apply or point to it rather than restate it. A fact with two owners becomes two facts
the first time one copy changes. The project's own conventions for its documents win over
anything here.

For each piece of information, settle three things:

- **Right information:** is it worth writing down? See "What to write" below.
- **Right place:** which document's question does it answer? Confirm with *if this fact
  changed, which document would change first?* Projects split their questions differently;
  as an illustration only: a glossary answers what a term means, a domain model what concepts
  exist and how they relate, a design what the system should do, a security model what must
  stay true for it to be secure, an architecture document how it is built, a runbook how to
  perform or recover an operation, a decision record why a choice was made, and a README what
  this is and where to go next. Follow the documents the project already has. A rule goes in
  the narrowest scope that covers every case it holds for: a general principle in shared
  guidance, a house rule in the project, an exact rule in a check.
- **Right resolution:** how much of it belongs here? The same concept appears at different
  depths: its meaning in one place, its relationships in another, its implementation in a
  third. Each document carries only the depth its own question needs.

## What to write

Documentation holds what the code cannot say; a copy of what it can say goes stale the first
time the code changes, and a reader cannot tell the stale copy from a true one.

- **Write why.** The reasons a part is the way it is, the rules it keeps, its trade-offs and
  the options rejected.
- **Leave out what looking answers.** The code, a schema, a tool's help or the live system
  already say what exists and how it behaves. Naming where to start looking, such as the file
  or type that owns a behaviour, is a pointer, not a copy; name it and nothing it contains.
- **Generate reference, or check it.** A list of fields, flags or defaults comes from the
  source or is tested against it, never copied by hand.
- **Write only what stays true.** Plans, statuses and "not yet" belong in the tracker, not
  the docs.
- **Keep a sentence only if it changes what the reader does.** Delete the rest whole rather
  than trimming it.
- **Prefer a check to a sentence.** A rule software can check becomes a check.

## Applying and redefining

Centralise definitions and governing rules; distribute their consequences where readers need
them. "Deleting this needs re-authentication" applies a rule; restating what
re-authentication involves, or which operations need it, redefines it and creates a second
authority. A document still answers its own question without a chain of links: a sentence of
context and a pointer to the owner, not a bare "see elsewhere", and not a copy of the owner.

When moving a fact to its owner, check that the owner already says it, and add it there if
not, before removing the copy.

A fact found in two places usually means the documents are split along the wrong lines: fix
the layout, not only the copy.

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

## Writing it

Readers skim and stop, so a page works only as far as it is read. Make each page as short as
its reader's task allows, and let its form carry what prose would: a table, an example or a
diagram is read where a paragraph is skipped. The ways below are common, not complete.

- **Be direct.** Facts go in bullets and tables, a reason in one clause beside its fact. Leave
  out introductions, summaries and restated context.
- **Show before telling.** An example, such as a command, a snippet or a before and after,
  replaces a paragraph. Prefer examples the project's tests run, since an untested example
  goes stale like any copy.
- **Draw how parts connect.** Connections and flows read better as a diagram in a text format
  the project's viewer renders, such as Mermaid. A diagram that restates a list is another
  copy.
- **Use plain words.** Common terms keep their usual meaning and need no explanation. Only the
  project's own terms are defined, once, in its glossary.
- **Name the reader.** A page opens with who it is for and what it helps them do.
- **Keep always-loaded files small.** A file every agent session loads, such as an
  instructions file, holds rules and pointers that say when to read further, not facts other
  documents own.

## Curating

Documents drift from the code one change at a time, and a reader cannot tell a stale line
from a true one, so curating is part of every edit, not a later chore.

- **Check what you touch.** When a task brings you to a page, check its other claims against
  the code too, and fix or remove what is wrong, stale, copied or misplaced.
- **Delete what you cannot keep true.** A line you cannot check and nobody would miss goes,
  rather than staying in doubt.
- **Read with fresh eyes.** You read your own intent into text you wrote, so a review by
  someone, or an agent, without your context finds what you cannot.

## Specific documents

- Read [references/glossaries.md](references/glossaries.md) when creating, reviewing or
  pruning a glossary.
