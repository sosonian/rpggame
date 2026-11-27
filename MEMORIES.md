# Crowns of Ashvale — Memories (information storage)

> Plan document for the **memory system**, also called the **information storage system**: how every
> character stores what they saw, heard, did and were told, and how they forget it.
> **Status: started.** Items marked **(proposal)** are suggestions waiting for a decision.
> Related: [ACTIONS.md §3.1](ACTIONS.md) (the `recall` action), [TRAITS.md](TRAITS.md) (Good Memory, Forgetful),
> [EVENTS.md §1.7](EVENTS.md) (who notices), [EVENTS.md §8](EVENTS.md) (perception), [IDEAS.md](IDEAS.md),
> [AI_CHARACTERS.md §3](AI_CHARACTERS.md).

## 0. Decisions so far

| # | Decision | Source | Date |
|---|----------|--------|------|
| 1 | Every character has a **memory storage** (information storage) | Owner | 2026-11-27 |
| 2 | **Memories come from what the character saw, heard and did** | [ACTIONS.md](ACTIONS.md) decision 13 | 2026-11-27 |
| 3 | **Each belief is stored with how it was learned** (seen, told, rumour) and **how sure** the character is | [EVENTS.md](EVENTS.md) decisions 33, 35 | 2026-11-27 |
| 4 | **Memories fade over time. Important memories last longer; small things don't** | Owner | 2026-11-27 |
| 5 | **Good Memory** makes memories fade more slowly; **Forgetful** makes them fade faster | [TRAITS.md](TRAITS.md) decision 5 | 2026-11-27 |
| 6 | **The player can check his memory inventory**, e.g. *does he still remember the scene of the murder?* | Owner | 2026-11-27 |
| 7 | The `recall` action: talking to yourself about a memory can **make an idea jump out**. It **costs stamina and time** | Owner, [ACTIONS.md](ACTIONS.md) decision 15 | 2026-11-27 |
| 8 | **AI-played characters also store and forget memories**; for them `recall` is only an event option or an action inside an idea | [ACTIONS.md](ACTIONS.md) decision 14 | 2026-11-27 |
| 9 | **One storage holds everything a character knows:** memories of events, knowledge, beliefs about others, rumours (§1) | Owner | 2026-11-27 |
| 10 | **Details fade first**; the main fact lasts longest (§3) | Owner | 2026-11-27 |
| 11 | **Recalling a memory refreshes it** (§3, §5) | Owner | 2026-11-27 |
| 12 | **The fading check happens at night** (§3) | Owner | 2026-11-27 |

## 1. What a memory is

A **memory** is one piece of information a character holds. Proposal for what each memory records:

| Part | Example |
|---|---|
| **What** | "A man stabbed the miller behind the tavern" |
| **When and where** | Day 12, evening; behind the tavern |
| **Who** | The miller (victim); the killer: "a tall man, maybe Brann" |
| **How it was learned** | Seen / heard / did / told / rumour (decision 3) |
| **How sure** | Sure / fairly sure / unsure (decision 3) |
| **Importance** | How much it matters to this character (§3) |
| **Strength** | How clearly it is still remembered; falls as it fades (§3) |
| **Details** | Smaller facts: "he wore a red scarf", "he ran towards the river" |

**One storage for all information (decision 9).** Besides memories of events, the same storage holds
**knowledge** ("the smith sells swords for 3 silver"), **beliefs about other characters** (their perception,
[EVENTS.md §8](EVENTS.md)) and **rumours**. Everything a character "knows" lives here, and all of it can fade.

## 2. Where memories come from

- **Seeing and hearing** (decision 2), by the rules of [EVENTS.md §1.7](EVENTS.md): closer means more detail,
  and what is learned is stored with how sure the character is.
- **Doing:** what the character did themselves, e.g. "I lied to the shopkeeper".
- **Being told:** conversations, news and rumours. A rumour may be false.
- **Events:** every event can add a memory ([EVENTS.md §3](EVENTS.md)).

## 3. Forgetting

**Important memories last longer; small things fade quickly (decision 4).**

| Kind of memory | How long it lasts (proposal) | Example |
|---|---|---|
| **Life-changing** (a major change, [EVENTS.md §1.3](EVENTS.md)) | Almost never fades | "My lover was killed" |
| **Important** | Months to years of game time | "I saw a murder"; "the captain promised me a promotion" |
| **Ordinary** | Days to weeks | "Hobb owes me 2 silver" |
| **Small** | Hours to a day or two | "A cart passed by the market at noon" |

**What makes a memory important (proposal):**
- It touches the character's **intents** (goals) or a **vital person** (family, lover, lord, best friend).
- **Strong feelings:** fear, anger, joy, shame.
- **Danger to oneself.**
- **Seen or done oneself** is usually more important than **heard from others**.

**How fading works (proposal):**
- **Details fade first (decision 10).** The main fact stays longest. After a while the character still remembers *"I saw a
  murder behind the tavern"*, but no longer *"the killer wore a red scarf"*. That can matter later, e.g. as a
  witness.
- **Traits** (decision 5): **Good Memory** fades more slowly; **Forgetful** fades faster.
- **Recalling** a memory refreshes it (decision 11), so it fades more slowly afterwards (see §5).
- **The fading check happens at night** (decision 12), e.g. while the character sleeps.
- **Old age** may make characters more forgetful (proposal).
- **What happens to a faded memory is being analysed** in [analysis/A05](analysis/A05-memory-storage.md)
  (Draft). The owner's idea: a faded memory is **not deleted**; the storage **marks** which parts have faded,
  or that the whole memory has faded.

**A useful side effect:** forgetting keeps the storage small. Characters don't collect endless memories over a
long chapter, which keeps the game fast and the AI calls short ([analysis/A04](analysis/A04-event-check-performance.md)).

## 4. The memory inventory (for the player)

The player can **check his memory inventory** at any time (decision 6), like an item inventory.

Proposal for what it shows:
- the list of memories, newest or most important first
- for each memory: what, when, where, who, how learned, how sure, and **how clear** it still is
  (e.g. *clear*, *fading*, *vague*)
- **faded details shown as gone**, e.g. *"the killer wore … (forgotten)"*

**Example:** on day 20 the lord asks the player about the murder on day 12. The player opens his memory
inventory: *"Saw a murder behind the tavern (fading). The killer: a tall man, maybe Brann (unsure).
Red scarf: forgotten."* The player knows what he can honestly say, and what he would be guessing or lying about.

## 5. The `recall` action

Details are in [ACTIONS.md §3.1](ACTIONS.md). In short:
- **The player** can `recall` at any time. He chooses a memory from the inventory and **talks to himself**
  about it.
- **An idea can jump out** of this inner talk (decision 7; [IDEAS.md](IDEAS.md)).
- **It costs stamina and time** (decision 7). The amounts are TBD. Stamina is not designed yet.
- **AI-played characters** use `recall` only as an event option or an action inside an idea (decision 8).

## 6. Other characters

- **AI-played characters** store and forget memories like the player (decision 8). Their memories are part of
  what the AI is told ([AI_CHARACTERS.md §4.2](AI_CHARACTERS.md)), so a character can only act on what it still
  remembers.
- **Background characters** (proposal): the same storage, but smaller and simpler, holding only what the
  rules need.
- **Group characters** (proposal): a shared memory for the whole group, e.g. *"the player's men burned our
  mill"* ([AI_CHARACTERS.md §2.3](AI_CHARACTERS.md)).

## 7. Open questions

1. Is the list of parts of a memory in §1 right?
2. **Faded memories:** marked or deleted? Being analysed in [analysis/A05](analysis/A05-memory-storage.md).
3. How long should each kind of memory last (§3)? What makes a memory important?
4. How much **stamina and time** does `recall` cost? How does stamina work in general?
5. How is the memory inventory shown: sorted how, and what does it show (§4)?
6. Do background characters and group characters have memories (§6)?
