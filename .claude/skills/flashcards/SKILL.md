---
name: flashcards
description: Generate a spaced-repetition deck from a module, paper note, or error log, and run review sessions. Use for "/flashcards <topic>", "turn my error log into a deck", or daily retrieval practice.
---

# Flashcards / Spaced Repetition

Build and review spaced-repetition decks for the topic in the arguments. Decks live as markdown under `research/decks/<topic>.md` so they're git-tracked and portable (offer Anki-importable TSV on request).

## Card generation

Source material, in priority order: the user's error log (misses are the highest-value cards), their paper notes, then the module's content in `curriculum/`.

Card quality rules:

- **Atomic** — one fact, definition, theorem, or distinction per card. Split anything with "and" in the answer.
- **Generative, not recognition** — fronts ask the user to produce ("State the FLP impossibility result and its three assumptions"), never to confirm ("Is FLP about consensus?").
- **Mix card types** — definitions, theorem statements *and* proof sketches (separate cards), complexity bounds, "what breaks if…" edge cases, and cross-module connections.
- **Tag each card** with module + concept so reviews can be filtered.

Deck format, one card per block:

```
Q: <front>
A: <back>
tags: <module> <concept>
ease: 2.5  interval: 1  due: YYYY-MM-DD
```

## Review sessions

1. Select cards due today (or the N most overdue).
2. Show the front only; the user answers from memory before you reveal the back.
3. The user self-grades 0–5 (0 = blank, 5 = instant). Apply SM-2 scheduling: grade <3 resets interval to 1 day; otherwise interval ×= ease, and ease adjusts ±0.1 by grade. Update the card lines in the deck file.
4. Any card failed twice in a row gets escalated: stop reviewing it and route the concept to `/study` — repetition can't fix a conceptual gap.

## Hygiene

- Cap new cards at ~15/day to keep review load sustainable per the roadmap's 2–4 hr/week reinforcement budget.
- During reviews, rewrite any card that proves ambiguous — bad cards teach wrong distinctions.
