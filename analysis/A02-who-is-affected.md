# A02 — Who is affected by a major change?

> **Status:** Final
> **Date:** 2026-11-27
> **Asked by the owner:** how the game knows which characters are affected when something big happens
> (e.g. a lover is killed)
> **Related plan documents:** [EVENTS.md §1.2–1.5](../EVENTS.md)

## 1. The question
When something changes a character's life in a big way (EVENTS.md §1.3), how does the game find out **who** is
affected, and **how** they react?

## 2. What we already know
- Major changes have a high chance of triggering an event (EVENTS.md decision 9).
- The shared character data already stores relationships: lover, friend, family, lord, mentor
  ([AI_CHARACTERS.md §3](../AI_CHARACTERS.md)).
- The golden rule: the AI proposes, the game decides ([AI_CHARACTERS.md §4.2](../AI_CHARACTERS.md)).

## 3. Options and analysis

| Way | How it works | Good | Bad |
|---|---|---|---|
| **A. Rules only** | Each kind of change has a rule. When something happens, the rules look at the relationship data to find who is affected. Example: X is killed → Y is X's lover → Y gets a major event | Cheap (no AI cost), fast, always the same, works for background characters too, easy to test | Each kind of change needs its own rule; may miss unusual cases nobody wrote a rule for |
| **B. AI judges** | After each thing that happens, the AI is asked: *"Is this a major change for anyone?"* | Can notice unusual cases | Many AI calls, so costly and slow; may judge differently each time; can't serve background characters; harder to test |
| **C. Mix** | **The rules find** who is affected (as in A). **The AI decides how** an AI-played character reacts. Background characters react by rules | Cheap and reliable detection; rich, personal reactions where they matter | The reaction for background characters is simpler |

## 4. Recommendation
**Way C.** It follows the golden rule, and the relationship data it needs already exists.

## 5. The owner's decision
**2026-11-27: way C** (EVENTS.md decision 13).

## 6. Changes made to the plan documents
- [EVENTS.md §1.4](../EVENTS.md): decision 13, with a short summary and a link to this report.
