# Crowns of Ashvale — Ideas (Plans)

> Design document for **ideas**: the plans that characters make, built from actions.
> **Status: draft, to be worked out together.**
> Items marked **(proposal)** are suggestions waiting for a decision.
> Related: [ACTIONS.md](ACTIONS.md) (the list of actions that ideas are made of),
> [AI_CHARACTERS.md §5.3](AI_CHARACTERS.md) (how AI-played characters plan and act in real time).

## 0. Decisions so far

| # | Decision | Date |
|---|----------|------|
| 1 | **An idea (or plan) is made of several actions.** Ideas are **not limited to a fixed list**: they arise **after an event** and are **produced by the AI**. Impersonation is an idea, not a single action (§1) *(was ACTIONS.md decision 7)* | 2026-11-25 |
| 2 | **The AI also suggests ideas to the player character**, based on the player's traits and situation. The player can follow or ignore them (§3.5) *(was ACTIONS.md decision 9)* | 2026-11-25 |
| 3 | Ideas get **their own document** (this one), moved out of ACTIONS.md §2.3 | 2026-11-27 |

## 1. What an idea is

An **idea** (also called a **plan**) is a goal plus a list of actions to reach it.

- Ideas are **not chosen from a fixed list**. **An event sparks them, and the AI writes them**, from the
  character's traits, intents, knowledge and situation.
- So ideas are **unlimited**, but every action inside them comes from the list in [ACTIONS.md §3](ACTIONS.md)
  and must pass the game's checks.
- Some things that look like one action are really ideas. For example, **impersonation** (pretending to be
  someone else) is an idea made of several actions, not a single action.

## 2. Example: the false tax officer

> **Who:** Hobb, a labourer. Greedy, not very moral (Deceitful), likes to take risks. Ambition: *become rich*.
>
> **The event:** one day Hobb watches the tax officer collect tax from a farmer. The process looks simple: a
> few words, a wax tablet, and the farmer pays. *(The event gives Hobb the knowledge "tax collection seems easy".
> It also unlocks `collect_tax` for him as an event option: [ACTIONS.md](ACTIONS.md) decision 6.)*
>
> **The idea (written by the AI):** *"Nobody on Tanner Street knows me. I could pretend to be a tax officer there
> and collect the money myself."*
>
> | # | Action | Details |
> |---|---|---|
> | 1 | `buy` | A dark coat and a wax tablet, so he looks like an official |
> | 2 | `go_to` | Tanner Street, where nobody knows him |
> | 3 | `talk_to` | A shopkeeper, **lying** that he is the new tax officer |
> | 4 | `collect_tax` | Take the "tax" money; a check of Intrigue against the shopkeeper's suspicion |
> | 5 | `go_to` | Leave before the real officer comes |
> | 6 | `hide` | Hide the money at home |
>
> **What can happen:**
> - It works, and Hobb gets rich, and may try again (repeated fraud builds toward a "Swindler" reputation).
> - The shopkeeper doubts him, and Hobb has to talk his way out or `flee`.
> - The real officer hears of it, and Hobb is hunted. If caught: arrest, a fine or worse, and infamy.
> - The player may see it happen, hear the rumour, or be the one he tries to fool.

Another example, Marta the innkeeper's beer plan, is in [AI_CHARACTERS.md §5.3](AI_CHARACTERS.md).

## 3. How ideas work (proposal)

### 3.1 Sparked by events
- Ideas come from events: seeing something, hearing news, a change in needs ("I'm out of money"), an insult,
  an opportunity.
- Not every event sparks an idea. The game asks the AI only when the event matters to the character's traits
  or intents.

### 3.2 Written by the AI
- For AI-played characters, the AI writes the idea ([AI_CHARACTERS.md §5.3](AI_CHARACTERS.md)).
- The AI may also decide *not* to act: a cautious character may think of the idea and drop it because the risk
  is too high.

### 3.3 Checked by the rules
- Every action in the idea must exist, be possible for this character, and follow the rules.
- Lying happens inside a conversation, as a dialogue option ([ACTIONS.md §2.4](ACTIONS.md)).

### 3.4 Background characters
- Background characters (run by rules only) can't call the AI. They get **simple ready-made ideas** instead
  (e.g. "steal food when hungry").

### 3.5 The player gets ideas too (decision 2)
- After an event, the AI may suggest an idea that fits the **player character's** traits and situation,
  shown as a thought: *"You think: nobody on Tanner Street knows you…"*.
- The player can **follow** it (its actions become available as a plan to carry out) or **ignore** it.
- A Greedy player character gets greedy ideas, a Kind one kind ideas. The player's personality is felt,
  but the player still decides.
- **Proposal:** ideas are suggested only after events that matter, so they stay special
  (perhaps a few per hour of play).

## 4. Open questions

1. **The owner's new ideas for this system:** to be added.
2. How often should the player get ideas? (Proposal above: a few per hour of play.)
3. How many actions may an idea have? (Also asked in [AI_CHARACTERS.md §12](AI_CHARACTERS.md), question 9.)
