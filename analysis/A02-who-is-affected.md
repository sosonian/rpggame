# A02 — Who is affected, and who notices?

> **Status:** Part 1 **Final** · Part 2 **Draft**
> **Date:** 2026-11-27 (Part 2 added 2026-11-27)
> **Asked by the owner:**
> - Part 1: how the game knows which characters are affected when something big happens (e.g. a lover is killed)
> - Part 2: "Finding who is nearby or who saw something. The principle of this mechanic is determined by the
>   distance. People could hear other people talking, must be in a short distance. People saw other people do
>   something, could have a longer range."
> **Related plan documents:** [EVENTS.md §1.2–1.5](../EVENTS.md), [EVENTS.md §5](../EVENTS.md),
> [A04](A04-event-check-performance.md)

---

# Part 1: Who is affected by a major change? (Final)

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

---

# Part 2: Who notices? Seeing and hearing by distance (Draft)

## 7. The question
Part 1 finds who is **affected** through relationships. But a character can only react once they are **aware**
(EVENTS.md decision 12): they saw it, heard it, or were told. So how does the game find **who saw or heard**
something?

**The owner's principle:** it is decided by **distance**.
- **Hearing** someone talk needs a **short** distance.
- **Seeing** someone do something works over a **longer** distance.

## 8. What we already know
- Awareness starts a major event at once if the character sees or does it; otherwise when they learn of it
  (EVENTS.md decision 12).
- How it was learned matters: seeing it hits harder than hearing a rumour (EVENTS.md decision 14). Beliefs are
  stored with how they were learned (EVENTS.md decision 33).
- **Observant** characters notice more; **Oblivious** ones less (EVENTS.md decision 18).
- Stealth actions exist: `sneak`, `hide`, `eavesdrop`, `watch`, `follow` ([ACTIONS.md §3.6](../ACTIONS.md)).
- Performance: find nearby characters **by place first** ([A04](A04-event-check-performance.md)).

## 9. Senses and distances (proposal)

Every action that others could notice gives off **signals**: something to **see** and/or something to **hear**,
each with its own range. A character notices a signal if they are within range, and pass a chance check.

Distances are in metres on the game map (the map scale is not decided yet).

| Signal | Sense | Proposed range | Example |
|---|---|---|---|
| Whisper | Hearing | **up to 1 m** (owner) | Two plotters whispering in the tavern |
| Normal talk | Hearing | **3–5 m** (owner: 8 m is too far) | Hobb lying to the shopkeeper |
| Shouting, an argument | Hearing | 15–30 m (shortened to match) | A quarrel in the street |
| Fighting, a scream, breaking things | Hearing | 30–60 m (shortened to match) | A brawl; a cry for help |
| A horn, a bell | Hearing | Hundreds of metres | The alarm bell of the town |
| Seeing that something happens (people fighting, someone running) | Sight | 50–100 m (daylight) | Seeing a fight across the square |
| Seeing **who** it is, and **what** exactly they do | Sight | 15–30 m (daylight) | Recognising Hobb taking the money |
| Small details (a hidden knife, a coin passed in secret) | Sight | 2–5 m | Seeing a pickpocket's hand |

**Closer means you know more (owner's decision, question 3).** For both senses, the shorter the distance, the
more you learn. Only when you are close enough do you know **who** you saw or heard.

| Sense | Far (inside the range) | Closer | Very close |
|---|---|---|---|
| **Seeing** | *That* something happens: "two people are fighting" (50–100 m) | **Who** it is, and **what** they do: "Hobb took the money" (15–30 m) | Small details: "he hid a coin in his sleeve" (2–5 m) |
| **Hearing** | *That* someone is talking or shouting, but not the words | **What** is said: the words (normal talk 3–5 m; whisper 1 m) | **Who** is speaking, by the voice (proposal: as close as hearing the words, and only if you know that person's voice) |

- **Seeing and hearing can add up.** If you only **see** a conversation from 20 m, you know *"Hobb talked with
  the shopkeeper"*, but not what was said. If you only **hear** it through a wall, you know the words, and you know
  who spoke only if you know the voice.
- **What you learn is stored with how sure you are** (EVENTS.md decision 35). From far away, the belief is
  uncertain: *"someone, maybe Hobb, was fighting"*.

## 10. What changes the range or the chance (proposal)

| Factor | Effect |
|---|---|
| **Walls and buildings** | Block sight completely. Hearing goes through doors and thin walls, but shorter |
| **Light** | At night, sight is much shorter (e.g. 10–15 m), unless there are torches or a fire |
| **Noise** | A busy market or a loud tavern shortens hearing ranges |
| **Weather** | Rain and fog shorten sight; wind and rain shorten hearing |
| **Attention** | Someone busy with work notices less; someone who is `watch`ing a person or place notices much more |
| **Facing** (proposal, later) | Things behind a character are harder to see than things in front |
| **Traits** | **Observant**: longer range and higher chance. **Oblivious**: shorter and lower |
| **Skills** (not decided) | e.g. Intrigue to notice secret things (EVENTS.md open question 5) |
| **The actor's stealth** | `sneak`, `hide` and whispering make signals weaker; a contest of the actor's stealth against the watcher's attention |

**Chance falls with distance (proposal):** close up, a character almost always notices; at the edge of the
range, only sometimes. Example: normal talk is heard for sure at 1 m, about half the time at 3 m, and rarely at 5 m.

## 11. Options for how to compute it

| Option | How it works | Good | Bad |
|---|---|---|---|
| **A. Same place only** | Everyone in the same place (the tavern, the market) notices everything there | Very simple and fast | Not realistic: in a big market, someone at the other end hears every whisper; no sneaking |
| **B. Distance only** | Circles of range around the action, as in §9 | Simple, follows the owner's principle | Sees through walls; no hiding behind a building |
| **C. Distance + blocking + chance** | Ranges as in §9; walls block sight (and weaken hearing); the chance falls with distance and changes with the factors in §10 | Follows the principle, realistic, makes sneaking and hiding meaningful | More work to build; needs line-of-sight checks (but see §12) |
| **D. Full sound simulation** | Sound spreads and echoes through the map | Most realistic | Far too complex for this game |

## 12. Performance
Option C sounds heavy, but it stays cheap:
1. **Places first** ([A04](A04-event-check-performance.md)): only characters in the same place, or in places
   next to it, are considered. A tavern has maybe 10–20 people, not 500.
2. **Then distance:** a quick distance check removes everyone out of range.
3. **Line of sight last,** only for the few characters left. Godot has built-in tools for this ("raycasts"),
   and for the 2D prototype walls can be simple lines on the map.
4. **Only actions that give off signals are checked.** Walking or sleeping gives off almost nothing worth
   noticing; a fight or a theft does.

## 13. Recommendation
**Option C (distance + blocking + chance)**, with the ranges in §9 as starting values to tune in playtesting.
For the 2D prototype, walls can be simple: inside a building or outside it.

## 14. Questions for the owner
1. Is option C right?
2. Are the starting ranges in §9 about right?
3. Should **seeing** and **hearing** give different knowledge (§9): seeing *who*, hearing *what*?
4. Which factors in §10 are wanted for Chapter 1? For example: walls, night, noise, attention, traits, stealth.
5. Should **facing** (things behind you are harder to see) be in Chapter 1, or later?

## 15. The owner's decision
- **2026-11-27, question 1:** **option C** (distance + walls + chance) is accepted.
- **2026-11-27, question 2 (ranges):** the owner wants **shorter** hearing ranges: a whisper only within
  **1 m**, normal talk **3–5 m** (8 m is too far). Shouting and fighting were shortened to match (proposal).
  Sight ranges are unchanged for now.
- **2026-11-27, question 3:** **closer means you know more.** When seeing, only a short enough distance tells you
  **who** you saw. **The same logic applies to hearing** (§9).
- Questions 4–5: still open. Also open: are the sight ranges fine as they are?

## 16. Changes made to the plan documents
*(to be filled in when Part 2 is Final; nothing has changed yet)*
