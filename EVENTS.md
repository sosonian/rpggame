# Crowns of Ashvale — Events

> Design document for **events**: the things that happen in the world and give characters choices,
> knowledge and ideas. Events are the **trigger** (the starting point) for ideas.
> **Status: first draft, to be worked out together.**
> This draft gathers what the other documents already say about events. Items marked **(proposal)** are
> suggestions waiting for a decision.
> Related: [IDEAS.md](IDEAS.md) (ideas that events start), [ACTIONS.md §2.1–2.2](ACTIONS.md) (event options
> and event-only actions), [AI_CHARACTERS.md §5.4](AI_CHARACTERS.md) (when the AI thinks),
> [AI_CHARACTERS.md §5.8](AI_CHARACTERS.md) (the free plot and world events).

## 0. Decisions so far

These decisions were made in other documents. They are collected here because they are about events.

| # | Decision | Source | Date |
|---|----------|--------|------|
| 1 | **Events can offer choices**, and **each choice is an action** | [ACTIONS.md](ACTIONS.md) decision 4 | 2026-11-25 |
| 2 | **Events can give actions** that a character's position does not give, often as a crime. Example: a liar gets the idea to pose as a tax officer | [ACTIONS.md](ACTIONS.md) decision 5 | 2026-11-25 |
| 3 | **Some actions exist only through events.** After the event, the action appears as an option on the related item, place or character | [ACTIONS.md](ACTIONS.md) decision 6 | 2026-11-25 |
| 4 | **Events start ideas** (plans), and the AI writes the ideas | [IDEAS.md](IDEAS.md) decision 1 | 2026-11-25 |
| 5 | **The plot is fully free.** The story must react to whatever happens, so story events are written as situations, not a fixed script | [AI_CHARACTERS.md](AI_CHARACTERS.md) decision 9 | 2026-11-24 |
| 6 | Which ideas and options each **trait** opens will be decided together with the event system | [ACTIONS.md](ACTIONS.md) decision 8 | 2026-11-25 |
| 7 | Events get **their own document** (this one) | — | 2026-11-27 |
| 8 | **Events happen by chance.** Each possible event has a chance (probability) of happening (§1.1) | Owner | 2026-11-27 |

## 1. What an event is

An **event** is something that happens to a character, or that a character notices.

- Some events **show a choice** on screen: *"You see the captain's purse left on the table."* →
  `steal`, `report`, ignore.
- Some events happen **quietly**: the character only learns something or changes a little. Example: Hobb
  watches the tax officer at work and learns "tax collection seems easy".
- **The player and AI-played characters get the same events.** Background characters (run by rules only)
  get them too, but react by rules ([ACTIONS.md §2.1](ACTIONS.md)).

### 1.1 Events happen by chance (decision 8)
- Events do not happen on a fixed schedule. **Each possible event has a chance of happening.**
- **TBD:** what raises or lowers the chance (open question 2).
- This is like dialogue options, which are also chosen by chance ([ACTIONS.md §2.4](ACTIONS.md)).

## 2. Where events come from

The documents so far name these sources ([ACTIONS.md §2.1](ACTIONS.md)):

| Source | Examples |
|---|---|
| **The story** | The enemy army reaches the border; the lord calls the militia |
| **The situation:** where you are, who is there | You are at the tavern when a fight starts; you are alone with a rival |
| **Your traits and background** | A Greedy character notices chances for money; a Kind one notices people in need |
| **Your needs** | You are out of money; you are hungry; you are hurt |
| **Other characters' actions** | Someone insults you, helps you, lies to you, or tries to rob you |
| **The world (proposal)** | Prices rise because of the invasion; bad weather; a sickness in town |

**World events** happen on their own unless the world stops them. For example, the enemy army arrives at the
border by a certain time, whatever the characters do ([AI_CHARACTERS.md §5.8](AI_CHARACTERS.md)).

## 3. What an event can do

An event can have one or more of these results:

| Result | Example | Where designed |
|---|---|---|
| **Offer choices** (each one an action) | `steal`, `report`, ignore | [ACTIONS.md §2.1](ACTIONS.md) |
| **Unlock an action** on a place, item or person | After overhearing where the miller hides his savings, clicking the mill shows `steal` | [ACTIONS.md §2.1](ACTIONS.md) |
| **Give knowledge** | "Tax collection seems easy"; "Brann patrols the north road at night" | — |
| **Start an idea** | Hobb's false tax officer plan | [IDEAS.md](IDEAS.md) |
| **Create, change or end an intent** (a goal) | Your brother is killed → you want revenge | [AI_CHARACTERS.md §5.1](AI_CHARACTERS.md) |
| **Add a memory** | "Edric helped me in the brawl" | [AI_CHARACTERS.md §3](AI_CHARACTERS.md) |
| **Add or remove a trait** | Surviving a battle may turn Craven into Brave | [AI_CHARACTERS.md §3](AI_CHARACTERS.md) |
| **Change opinion** between characters | Being helped raises opinion; being insulted lowers it | — |
| **Give or take items** | Finding a secret letter (an event item) | [ITEMS.md §3.9](ITEMS.md) |

## 4. Events and AI-played characters

- An important event **wakes the AI** of an AI-played character, so it thinks again
  ([AI_CHARACTERS.md §5.4](AI_CHARACTERS.md)). Examples: it is attacked, insulted or helped; it sees a crime;
  it hears important news; its target appears.
- **Not every event starts an idea.** The game asks the AI only when the event matters to the character's
  traits or intents ([IDEAS.md §3.1](IDEAS.md)). This keeps AI costs down.
- The choices an event offers become **legal actions** the AI can put in its plan
  ([AI_CHARACTERS.md §4.2](AI_CHARACTERS.md)).
- **Event text (optional):** the rules can use written templates, and the AI can personalise the words
  ([AI_CHARACTERS.md §4.1](AI_CHARACTERS.md)).

## 5. Events and the clock

The game runs in real time. [PLAN.md §7](PLAN.md) says that **dialogue and decision events pause the clock**,
but [AI_CHARACTERS.md §7](AI_CHARACTERS.md) still lists this as an option to consider. This needs a decision
(open question 6).

## 6. Example: from event to idea

> **Event:** Hobb (Greedy, Deceitful) watches the tax officer collect tax from a farmer.
> **Source:** the situation (he was there) and his traits (Greedy characters notice chances for money).
> **Results:**
> - knowledge: "tax collection seems easy"
> - unlocked action: `collect_tax`, as an event option
> - the event matters to his ambition *become rich*, so the AI is asked → it writes the **false tax officer**
>   idea ([IDEAS.md §2](IDEAS.md))

## 7. Open questions

1. **The owner's ideas for events:** to be added.
2. **Chance (decision 8):** what raises or lowers an event's chance? For example: traits, the place, the time, who is nearby, needs, or the story. Is the chance shown to the player, or hidden like dialogue chances?
3. **Sources:** is the list in §2 right? What should be added or removed?
4. **How events are written:** by hand, made by rules from the situation, made by the AI, or a mix?
5. **How often:** how many events with choices should the player see per hour, so they stay special but the
   world still feels alive?
6. **The clock:** should events with choices always pause the game (§5)?
7. **Traits:** which events and options does each trait open (decision 6)?
8. **Chapter 1:** which story and world events does the demo need (e.g. the enemy's arrival)? Also asked in
   [AI_CHARACTERS.md §12](AI_CHARACTERS.md), question 8.
