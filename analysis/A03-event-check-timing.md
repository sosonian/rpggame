# A03 — When to check for events

> **Status:** Final
> **Date:** 2026-11-27 (revised the same day for the 10-game-minute time unit)
> **Asked by the owner:** "Which solution is better: event check happen after every action done, or every
> time unit go by?"
> **Related plan documents:** [EVENTS.md §5](../EVENTS.md), [ACTIONS.md](../ACTIONS.md)

## 1. The question
The game runs in real time, every action takes time, and actions can cause events. When should the game
**check** whether an event happens (roll the chance)?
- **A.** after every action is done
- **B.** every time a time unit goes by

## 2. What we already know
- Every action takes a period of time, including conversations (EVENTS.md decision 36).
- Every action, and every impact on a character, has a chance to trigger an event (EVENTS.md decision 21).
- An event starts **at once** when the character sees or does the change (EVENTS.md decision 12).
- **The time unit:** 1 unit = 10 game minutes = 5 real seconds (EVENTS.md decision 37).

## 3. Option A: check after every action is done

| Good | Bad |
|---|---|
| **Fits the main principle.** Events come from stimuli, and most stimuli come from actions | **Long actions leave gaps.** A character who works at the market for 8 hours is checked only at the end. If he sees a murder at 9 o'clock, he reacts at 3 o'clock. This breaks "at once" |
| **Clear cause.** The game knows which action caused the event | **Unfair chances.** A character doing many short actions gets many more checks, so many more events, than one doing a few long actions |
| **Reactions are quick** after short actions | **Misses stimuli that are not actions:** hunger growing, a deadline coming closer, news spreading, the weather |

## 4. Option B: check every time unit (10 game minutes = 5 real seconds)

| Good | Bad |
|---|---|
| **Simple, steady and fair.** Everyone is checked at the same rhythm, whatever they do | **A short delay** of up to 10 game minutes (5 real seconds). Fine for small things, odd for a major change seen with one's own eyes |
| **Fine enough.** A unit holds at most one or two actions, so the cause is usually clear | **Order inside one unit is lost** |
| **Catches stimuli that are not actions** | **Many checks** (hundreds every 5 seconds): fine for the rules, but they should be spread out; see [A04](A04-event-check-performance.md) |
| **No gaps in long actions.** An 8-hour job gets 48 checks | |

**Note on the first draft:** the first version of this analysis assumed a time unit could be a whole game
day, which made option B look far too slow. With a 10-game-minute unit, B works for almost everything.

## 5. Recommendation
**B as the base, plus two extra checks:**

| Check | When | What it catches |
|---|---|---|
| 1. At once | The moment something big happens to a character, or in front of them | Major changes, attacks, crimes seen, shocking news |
| 2. When an action ends | Each time an action finishes or fails | The result of what the character did |
| 3. Every time unit | Every 10 game minutes (5 real seconds) | Daily-life stimuli during any action; slow changes (hunger, deadlines, rumours) |

Supporting rules (still proposals in the plan): small chances per unit; checks spread across the 5 seconds;
big news in a conversation counts at once, the rest at the end; a major event can interrupt the current
action; the rules check and the AI only reacts.

## 6. The owner's decision
**2026-11-27:** the recommendation is accepted (EVENTS.md decision 38).

## 7. Changes made to the plan documents
- [EVENTS.md §5](../EVENTS.md): decisions 36–38, the chosen design (§5.4), the example of Hobb's morning (§5.5).
- [ACTIONS.md](../ACTIONS.md): decision 12 (every action takes time).
- Time unit updated in [AI_CHARACTERS.md §7](../AI_CHARACTERS.md), [PLAN.md §7](../PLAN.md),
  [ITEMS.md](../ITEMS.md) and [WARFARE.md](../WARFARE.md).
