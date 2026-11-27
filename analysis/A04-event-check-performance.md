# A04 — Performance of event checks

> **Status:** Final
> **Date:** 2026-11-27
> **Asked by the owner:** "We might have hundreds of characters, so the system must check hundreds of times at
> once, right? Is there any problem, or is it okay for a PC game?"
> **Related plan documents:** [EVENTS.md §5.7](../EVENTS.md), [AI_CHARACTERS.md §2.3](../AI_CHARACTERS.md)

## 1. The question
Events are checked every time unit (5 real seconds) for every character ([A03](A03-event-check-timing.md)).
With hundreds of characters, is that a problem for a PC?

## 2. Analysis
**It is fine for a PC game.**
- An event check is done by **rules, not the AI**: a few quick questions and a dice roll.
- **Example:** 500 characters × about 10 possible events each is about 5,000 small checks per unit. That probably
  takes a few milliseconds in total, even in Godot's own scripting language (GDScript).
- **Spread the checks** across the 5 seconds of a unit (about 300 screen frames): fewer than 2 characters per frame.

**What needs care:**

| Risk | Fix |
|---|---|
| **Finding who is nearby or who saw something.** Comparing every character with every other gets slow (500 characters make about 250,000 pairs) | Group characters by **place** (market, tavern, barracks) and only compare people in the same place |
| **Waiting for the AI.** An AI call takes 1–10 seconds | AI calls always run in the background; the character keeps doing its current action |
| **Memory growing over a long chapter.** Six hours of play means many memories, beliefs and rumours per character | Old, unimportant memories **fade or are summarised** |
| **Battles** are heavier (200–300 soldiers updating several times per second) | Planned in [WARFARE.md §6](../WARFARE.md) |

**If it ever becomes slow:** run quick filters first (someone asleep at home skips market events), or move the
busiest code to a faster language (Godot supports C# and C++). Probably not needed for Chapter 1.

**How to be sure:** once coding starts, `--autotest` can run a test town with 1,000 fake characters and measure
the time (milestone D2 in [PLAN.md §8](../PLAN.md)).

## 3. The owner's decision
**2026-11-27:** the number of individual characters stays **in the hundreds**, even when later chapters make the
world larger. **Far places are group characters:** e.g. the people of a town in a nearby foreign country count as
**one character** (AI_CHARACTERS.md decision 14).

## 4. Changes made to the plan documents
- [AI_CHARACTERS.md §2.3](../AI_CHARACTERS.md): decision 14 and group characters.
- [EVENTS.md §5.7](../EVENTS.md): a short performance summary with a link to this report.
- [PLAN.md §6.9](../PLAN.md): a line on group characters.
