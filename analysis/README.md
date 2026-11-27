# Analysis reports

This folder holds the **analysis reports**. Each piece of analysis work gets its own report.
The **plan documents** in the main folder (PLAN.md, AI_CHARACTERS.md, ACTIONS.md, IDEAS.md, EVENTS.md,
WARFARE.md, ITEMS.md) hold only the **agreed design**.

## How it works

1. **The owner asks a question** that needs analysis, e.g. *"Should events be checked after every action, or
   every time unit?"*
2. **A new report is written** in this folder, with status **Draft**. The plan documents are **not** changed yet.
3. **The owner reads it, asks questions, and decides.** The report is revised as needed.
4. **When the owner decides, the report becomes Final.** It records the decision and the date.
5. **Only then are the plan documents updated.** They get the decision, a short summary, and a link to the report.

## Report status

| Status | Meaning |
|---|---|
| **Draft** | Being worked on. Nothing in the plan documents has changed because of it |
| **Final** | The owner has decided. The plan documents have been updated |
| **Replaced** | A later report took its place (the report says which) |

## Reports

| # | Report | Date | Status | Plan documents updated |
|---|---|---|---|---|
| A01 | [AI-played characters: approaches and cost](A01-ai-characters-and-cost.md) | 2026-11-20 (updated 2026-11-27) | Final | AI_CHARACTERS.md |
| A02 | [Who is affected, and who notices?](A02-who-is-affected.md) | 2026-11-27 | Part 1 Final · Part 2 (seeing and hearing by distance) **Draft** | EVENTS.md §1.4 (Part 1 only) |
| A03 | [When to check for events](A03-event-check-timing.md) | 2026-11-27 | Final | EVENTS.md §5 |
| A04 | [Performance of event checks](A04-event-check-performance.md) | 2026-11-27 | Final | EVENTS.md §5.7, AI_CHARACTERS.md §2.3 |

## Template for a new report

```markdown
# A00 — Title

> **Status:** Draft | Final | Replaced
> **Date:** YYYY-MM-DD (updated YYYY-MM-DD)
> **Asked by the owner:** "the question, in the owner's words"
> **Related plan documents:** links

## 1. The question
## 2. What we already know (facts and earlier decisions)
## 3. Options
## 4. Analysis (good and bad of each option)
## 5. Recommendation
## 6. The owner's decision (filled in when Final)
## 7. Changes made to the plan documents (filled in when Final)
```
