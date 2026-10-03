---
name: personal-ui-preferences
description: Use when designing, implementing, or reviewing UI/UX for Alexis, or curating personal design preferences from his feedback. Also use it when reviewing screenshots of an interface, brainstorming UX options, or writing UI specs and plans, even when Alexis does not mention preferences.
---

# Personal UI preferences

Confirmed personal defaults. Apply them in context; the user's current direction takes precedence. This shared copy is canonical for Codex and Claude.

## Density and copy

- **Earn visible space.** Favor information density by removing repetition and obvious explanations. Let surrounding context supply meaning; retain wording that clarifies the action or changes interpretation. “Import transactions” can be better than “Import.” Preserve readable text and comfortable targets.
- **Don't ask what the data already says.** When one fixed rule reads every accepted value unambiguously, apply it and drop the setting. When a value can be derived from what the user already gave, show it as an editable fact instead of asking for it. Ask only where the values genuinely cannot decide, and state the accepted shape with an example ("year, month, day, like 2026/08/11"), never a pattern.
- **Truncate to one line, reveal on hover.** Long text in a list or cell keeps one line and shows the full value on hover or focus, never by widening the row or blocking the action that produced it. Use the space before truncating: text is cut only when its container runs out of room, never at a fixed cap while space is free.
- **Hover cards, not browser tooltips.** Information shown on hover or focus (a cut-off value, what an icon means, why a control waits) opens in a styled card, never the browser's `title` tooltip.
- **A layout switches as a whole.** A compact layout (stacked, arrow turned down) replaces the wide one completely; parts never wrap on their own into a mix of the two.

## Placement

- **The simplest wording that carries the message.** Say what happened and what to do, once. Cut words that repeat each other ("updated after being changed") or repeat what the screen already shows (a step already marked current). Prefer one wording that is true in every state over a variant for each state.
- **One cue per meaning.** When layout already tells something apart (a Before section, an After section), don't repeat it with colour, strikethrough or icons. Save colour for the one thing the layout can't show, and give it one meaning everywhere it appears.
- **Match prominence to frequency.** Keep routine actions close to their content. Put occasional settings in a discoverable menu; keep their consequential effects apparent.
- **Place a control beside its effect.** Proximity tells the user what a control changes, before any label does. When several spots compete, the one nearest the thing affected wins, even over grouping with similar-looking fields.
- **A preference lives on the thing it describes.** Store a setting on the entity whose fact it is, not on whichever object is in hand when it comes up. A billing cycle belongs to the account, not to the file format that happens to feed it.
- **A list is a queue or a record, never both.** Items waiting on the user and history that explains something are different kinds. Show the queue where the user acts. Reach a record from the thing it explains, rather than mixing both in one list and filtering them apart with a setting.
- **Give the page to the current work.** Keep persistent navigation and profile controls outside the content header; use that header for context and actions. For sidebar layouts, prefer icon-and-text navigation, collapsible groups, and a profile footer.

## Controls

- **Make appearance and interaction agree.** When a card or row presents one action, its whole surface should activate it. Icons reinforce labels and signal interaction.
- **Switch for instant effect, checkbox for a later submit.** A switch feels mechanical: flipping it changes what is on screen right now, such as a header toggle that repaints a table. A checkbox is a concept: an option collected for a submit, such as "Save this format for next time" or an acknowledgement. Revealing a dependent field is disclosure, not effect, so a checkbox that shows a name input stays a checkbox.
- **Icons when the meaning is universal.** A gear, a pencil, a trash can or a refresh arrow stands alone as a button. Anything less universal gets icon plus text, or text only. Icon-only controls still carry an accessible name and a tooltip.
- **Show, don't tell.** When something can be drawn, draw it instead of describing it: seeing beats reading and decoding. Borrow shapes the screen already uses, so the picture maps onto what it describes without being learned. Stop where the picture would need a legend: keep the words that carry meaning, and fall back to text where a drawing would misstate the thing. The plain sentence stays as the accessible name and tooltip. Examples:
  - A filter or rule drawn in the table's own shape, as the columns it reads over the values it matches, then the columns it writes, not a sentence about them.
  - A change shown as ~~old~~ → new, not "changed from X to Y".
  - A search match highlighted where it occurred, not reported beside it.
  - Alternatives as separate groups joined by an "or" token; conditions that must all hold share one group.
  - Counter-example: a symbol for "contains" or "between" is a code to learn; the word stays.
- **A menu needs more than one item.** A menu holding a single item is a button in disguise. Put the control on the surface, or find what else belongs in the menu.
- **A disabled control says why.** Its tooltip carries the reason it cannot be used, so the user learns what would enable it without guessing.
- **A click lands ready to act.** Click-to-edit opens the field ready: caret at the end for text, list open for a select. One gesture, not two.
- **Every chosen value can be unchosen.** A field that starts empty keeps its empty option after a value is picked.
- **Tables read top-down.** Controls that change what a table shows (page size, paging, filters, view switches) sit in one row above it, right-aligned, with what the table holds on the left; that row stays in view on long pages. What sums up the reading, such as a selection count, sits below the table. Previous and next sit side by side with their state between them, and page size defaults to what fits a screen.

## Flow and order

- **Carry context through the task.** Infer selections already established by the current view and return users to their origin. Avoid making them reselect what the interface already knows.
- **Walk the page in reading order.** Users move left to right, top to bottom. Every control should be answerable with what is already settled above it. A control whose meaning depends on a later choice, or that a later choice resets, is out of order. Review a page by walking it, not by checking its parts, and when the walk exposes friction, question the design before reordering it: the fix may be a different structure, not a different sequence.
- **The current position reads on its own.** The current step marks itself, never only by contrast with its neighbours, and going back marks no later step done.
- **Keep the way forward in view.** The actions that move a flow sit in a bar pinned to the foot of the window, so their availability is seen without scrolling.

## Layout and stability

- **Nothing moves when a setting changes.** Changing a setting changes what is shown, never where the rest of the page sits. Whatever the setting reveals, a control, a count, a notice or a panel, has its place reserved (rendered empty or disabled) or appears after what is already there, so the things the user was looking at stay where they were. People relocate by position before they reread a label.
- **Group by meaning, then let groups breathe.** Related items sit close together. Separate groups spread across the available space instead of piling into one corner. Spread the groups, not the elements inside them.
- **Align rows by centre.** When text and a button share a row, they read as the same height, and the text is vertically centred on the button's centre, never its baseline or top.
- **Whatever shares an edge shares a line.** Elements that sit along the same edge of the window or the same row of a layout, such as a sidebar footer beside a content footer or a header beside a toolbar, match in height and border, reach the edges they sit between, and stay put when the page ends. Two neighbours a few pixels apart read as a mistake.

## Curate

Information density is the admission criterion for this skill: an observation earns a place only when it generalizes beyond the individual correction and changes a design decision. Write every principle generically: this skill is global, so no wording may depend on one project's features, names or data.

Before adding an inferred principle or changing an existing principle's meaning, show the proposed wording and scope to the user and obtain explicit confirmation. Approval to fix the UI, silence, tests, and agent reviews are not preference confirmation. Until confirmed, leave the skill unchanged.

After confirmation, sharpen or merge the relevant principle; remove superseded wording. Editorial compression may preserve already-confirmed meaning. Keep only decision-changing guidance and examples that clarify a boundary. Leave raw corrections and unconfirmed ideas in conversation or existing project history, not companion skill files. Curate this skill without rewriting unrelated workflow policy.
