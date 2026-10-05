---
name: writing-glossaries
description: Use when writing, editing or reviewing a project glossary, or when a design or spec starts collecting capitalised domain terms, so each term gets one identity sentence and rules stay out of it.
---

# Writing glossaries

A glossary answers one question: *I met a capitalised word here; what does it mean?* Optimise
for that reader and nothing else.

## Shape

- **Two columns: Term and Meaning.** No avoid-lists, examples, notes or extra columns.
- **One sentence per term.** If it needs two, the term is doing two jobs or the second sentence
  belongs somewhere else.
- **No history.** Drop retired words and old synonyms; the change log keeps them. Keep one only
  while migration work still needs it.
- **Related terms sit together.** Order rows so a reader meets a term next to the ones it
  depends on (who, the things they own, what those are made of, what they show), never
  alphabetically.

## What a definition says

- **Identity, not behaviour.** Say what the thing *is*. What it does, when, and under which
  rules goes elsewhere.
- **Terms from the glossary may be used freely,** but keep chains shallow: a reader should
  never follow more than one or two links to understand a row.
- **No implementation details:** no paths, keys, routes, flags, durations, sizes, section
  references, dates or quotes.

## Where everything else goes

| Content | Home |
| --- | --- |
| Relationships and invariants ("a group's state is its worst member's") | the domain model |
| UI behaviour and copy rules | the design |
| Security guarantees ("this needs re-authentication") | the security model |
| Why a word was chosen, and what it replaced | the change log or a decision record |

Before deleting a rule from the glossary, check that its home already says it; move it there
if not.

## Pass over an existing glossary

Run these in order, and show the user the cuts and merges before applying them:

1. **Cut** a term that is:
   - a standard concept under a coined name (call it what the field calls it, and use that
     plain wording in the design too);
   - internal plumbing the reader never meets (it belongs to the design);
   - a special case of another term (say it with the general term).
2. **Merge** two rows when one is only the type, a variant or an alternative path of the
   other: the general row names its types or variants in its one sentence.
3. **Rename** a term whose ordinary meaning misleads (a word that reads as a tier, a size or a
   different field's concept), and rename it everywhere the project uses it, in one change.
4. **Keep apart** terms that look alike but name different things (a verdict and the state it
   is derived from); the glossary exists for exactly those.
5. **Order** the survivors by relation.
