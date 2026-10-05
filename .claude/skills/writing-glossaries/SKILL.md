---
name: writing-glossaries
description: How to write, prune and order a glossary of a project's own terms. Use when creating or editing a glossary, reviewing one that has grown into rules or history, or when a design starts using capitalised terms that need defining.
---

# Writing glossaries

A glossary answers one question: *I met a capitalised word here; what does it mean?* Every
choice below serves that reader. A term earns a row only when that reader, knowing the field
but not this project, meets it, would otherwise misread it or not know it, and neither the
field's plain wording nor another term of the glossary already says it. Where the project
already sets conventions for its glossary, they win.

## A good glossary

- Two columns, Term and Meaning, and one sentence per meaning. A meaning that needs a second
  sentence is either two terms or a rule that belongs elsewhere.
- Each sentence says what the thing *is*. What it does, when, and under which conditions lives
  in the documents listed below, where it can change without the vocabulary changing.
- A meaning may use other terms of the glossary, as long as a reader needs to follow at most
  one or two of them to understand it.
- Each term comes after the terms its meaning cannot be read without, and related terms sit
  together, so a reader scanning down meets them in the order they build on each other.
- The terms are the current ones. What a term replaced, and why, belongs to the change log;
  keep an old synonym only while migration work still needs it.
- The meanings stay true when the implementation changes, so they hold no paths, keys,
  routes, flags, durations or sizes.

## Where the rest goes

A glossary attracts content that belongs elsewhere. Use the project's own documents when it
has them; these are the usual homes:

| Content | Home |
| --- | --- |
| Relationships and invariants, such as how one term's value derives from another's | the domain model |
| UI behaviour and copy rules | the design |
| Security guarantees, such as which operations need re-authentication | the security model |
| Why a term was chosen and what it replaced | the change log or a decision record |

Before taking a rule out of the glossary, check that its home already says it, and move it
there if not.

## Pruning an existing glossary

Each step changes what the next one works on, so take them in this order. Show the user every
cut, merge and rename with its reason, and apply them once they agree. Changes reach the
project's current vocabulary; change logs, decision records and quotes keep their words.

1. **Cut** each term that fails the admission test above. Typical cases, as illustrations: a
   standard concept, whether under its usual name or a coined one; plumbing the reader never
   meets; a special case of another term. A coined name for a standard concept is replaced by
   the field's plain wording wherever the project uses it, and any cut term loses its capital
   in the project's documents, so no reader meets a capitalised term the glossary does not
   define.
2. **Merge** two rows when one is only a type, a variant or an alternative route of the other;
   the general row names its types or variants in its one sentence. Terms that look alike but
   name different things, such as a verdict and the observation it is derived from, stay
   apart; telling those apart is what the glossary is for.
3. **Rename** a term whose everyday meaning misleads, such as one that reads as a rank or
   belongs to another field, in one change, everywhere the project uses it.
4. **Order** the remaining rows by relation, then read the table top to bottom as a newcomer
   would and check that no meaning depends on a row further down that it cannot be read
   without.
