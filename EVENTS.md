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
| 9 | **A major change in a character's life has a high chance of triggering an event for that character.** Example: their **lover** or a **close friend** is killed. The event can give a new intent (e.g. revenge) or **change how the character sees the world** (e.g. a naive character comes to believe the world is cruel) (§1.2) | Owner | 2026-11-27 |
| 10 | **The player character gets major events in the same way** as other characters (§1.2) | Owner | 2026-11-27 |
| 11 | **All 23 candidates in §1.3 are major changes** | Owner | 2026-11-27 |

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
- **TBD:** what else raises or lowers the chance (open question 2). Major changes in a character's life
  are the first known case (§1.2).
- This is like dialogue options, which are also chosen by chance ([ACTIONS.md §2.4](ACTIONS.md)).

### 1.2 Major changes trigger events (decision 9)
When something **changes a character's life in a big way**, the system has a **high chance** of triggering
(starting) an event for that character. The event shows how the character reacts.

**Examples of a major change** (decided):
- the character's **lover** is killed
- a **close friend** of the character is killed

More candidates are listed in §1.3.

**What the event can do to the character:**

| Result | Example | Where designed |
|---|---|---|
| **A new intent** (goal) | *"I want revenge."* | [AI_CHARACTERS.md §5.1](AI_CHARACTERS.md) |
| **A change in how they see the world** | A naive character comes to believe *the world is cruel* | [AI_CHARACTERS.md §3](AI_CHARACTERS.md) (traits change through events) |

**The player character too (decision 10):** the player character gets these events in the same way as other
characters. The event can give the player character a new intent or change their view of the world.
The player still decides what to do next.

**Example:**
> Aldric is young and naive: he trusts everyone. His lover, Wenna, is killed in a raid.
> → The system triggers a major event for Aldric (high chance).
> → He may get the intent *take revenge on the raiders*, and his view of the world changes: he no longer trusts
> easily and believes the world is cruel.
> → The new intent can then start ideas (plans) for his revenge ([IDEAS.md](IDEAS.md)).

**Proposals (not decided):**
- The people who count are the same as those **"vital to you"** in dialogue (family, lover, lord, best friend;
  [ACTIONS.md §2.4](ACTIONS.md)). So the death of a family member or your lord could also trigger a major event.
- "A change in how they see the world" could be done as a **trait change**, e.g. losing *Trusting* or gaining
  *Cynical* (expects the worst of people). The trait list is not designed yet.
- The **chance is high, not certain**, so not every character reacts the same way, and the character's traits
  decide *which* reaction they get. A Vengeful character is more likely to want revenge; a Craven one may
  become afraid instead.

How high the chance is will be decided later (open question 3).

### 1.3 The list of major changes (decision 11)
All 23 rows are accepted as major changes. More may be added later.
"Vital person" means family, lover, lord, mentor or best friend.

| # | Group | Candidate | Possible reactions (examples) |
|---|---|---|---|
| 1 | **Loss** | Lover is killed | Revenge; grief; the world is cruel |
| 2 | Loss | Close friend is killed | Revenge; grief; trusts fewer people |
| 3 | Loss | A family member is killed or dies (parent, child, brother or sister) | Revenge; grief; protect the rest of the family |
| 4 | Loss | Your lord or mentor is killed | Revenge; take their place; lose loyalty to the realm |
| 5 | **Betrayal** | Betrayed by a vital person (lied to, sold out, left to die) | Revenge; becomes suspicious (Paranoid); never trusts again |
| 6 | Betrayal | Your lover is unfaithful | Anger; heartbreak; leaves them; revenge on the rival |
| 7 | **Your own body** | Badly wounded or almost killed | Fear (Craven); or more courage (Brave); wants to quit the army |
| 8 | Your own body | Crippled: loses an eye, a hand, a leg | Bitterness; gives up the sword; finds a new path |
| 9 | Your own body | Captured, imprisoned or tortured | Hatred of the captors; fear; a hard heart |
| 10 | **Violence you do** | Kills a person for the first time | Guilt and stress; or grows used to it (Cruel) |
| 11 | Violence you do | Kills an innocent person, or a vital person, by mistake | Deep guilt; seeks forgiveness; faith |
| 12 | **War** | Survives a lost battle, or a massacre | The world is cruel; fear; wants peace |
| 13 | War | Your home town is captured, burned or looted | Revenge on the enemy; becomes a refugee; loses everything |
| 14 | **Position** | Promoted, or given land or a title | Pride; ambition grows; new rivals |
| 15 | Position | Demoted, dismissed, exiled or shamed in public | Anger at the lord; revenge on whoever caused it; despair |
| 16 | Position | Falsely accused of a crime | Proving innocence; distrust of the law; revenge |
| 17 | **Money and home** | Loses all money, or the home or business | Desperation; crime; starting again |
| 18 | Money and home | Suddenly becomes rich | Greed; generosity; fear of thieves |
| 19 | **Love and family** | Falls in love, or marries | Protect the lover; ambition for the family |
| 20 | Love and family | A child is born | Protect the family; wants a safer life |
| 21 | **Being saved** | Someone saves the character's life | Owes them a debt; loyalty; friendship |
| 22 | **Secrets** | Learns a big secret, e.g. the father is not their real father, or the lord is a traitor | Confusion; a new goal; blackmail |
| 23 | **Faith** | Sees a "miracle" or a dark omen | Becomes faithful; loses faith; fear |

Notes:
- Not all major changes are bad. Rows 14, 18, 19, 20 and 21 are good changes, and they can also change a
  character's goals and view of the world.
- Many of these come from **other characters' actions** (§2), e.g. a murder, a betrayal or a promotion.
- The trait names here (Paranoid, Craven, Brave, Cruel) are examples; the trait list is not designed yet.
- The reactions are examples (proposal), not fixed results.

### 1.4 How does the game know a major change happened? (TBD, open question 4)
Three ways to decide which characters get a major event:

| Way | How it works | Good | Bad |
|---|---|---|---|
| **A. Rules only** | Each kind of change in §1.3 has a rule. When something happens, the rules look at the **relationship data** to find who is affected. Example: X is killed → the rules find that Y is X's lover → Y gets a major event | Cheap (no AI cost), fast, always the same, works for background characters too, easy to test | Each kind of change needs its own rule; may miss unusual cases nobody wrote a rule for |
| **B. AI judges** | After each thing that happens, the AI is asked: *"Is this a major change for anyone?"* | Can notice unusual cases | Many AI calls, so costly and slow; may judge differently each time; can't serve background characters; harder to test |
| **C. Mix (proposal)** | **The rules find** who is affected (as in A). **The AI decides how** an AI-played character reacts. Background characters react by rules | Cheap and reliable detection; rich, personal reactions where they matter | The reaction for background characters is simpler |

**Proposal: way C.** It follows the golden rule of this project: *the AI proposes, the game decides*
([AI_CHARACTERS.md §4.2](AI_CHARACTERS.md)). The relationship data (lover, friend, family, lord) already
exists in the shared character data ([AI_CHARACTERS.md §3](AI_CHARACTERS.md)).

**Proposal: the event starts when the character learns of the change**, not when it happens. Characters know
only what they see or are told ([AI_CHARACTERS.md §5.2](AI_CHARACTERS.md)). If Wenna is killed far away,
Aldric's major event starts when he sees the body, or when news or a rumour reaches him. A false rumour
could even start a major event for something that never happened.

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
(open question 8).

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
3. **Major changes (decision 9):** which candidates in §1.3 should be used, and which are missing?
   **Later:** how high is "a high chance": almost always (like 90%), or just higher than normal?
4. **Detecting major changes (§1.4):** rules only (A), AI judges (B), or a mix (C)? Does the event start when
   the change happens, or when the character learns of it?
5. **Sources:** is the list in §2 right? What should be added or removed?
6. **How events are written:** by hand, made by rules from the situation, made by the AI, or a mix?
7. **How often:** how many events with choices should the player see per hour, so they stay special but the
   world still feels alive?
8. **The clock:** should events with choices always pause the game (§5)?
9. **Traits:** which events and options does each trait open (decision 6)?
10. **Chapter 1:** which story and world events does the demo need (e.g. the enemy's arrival)? Also asked in
   [AI_CHARACTERS.md §12](AI_CHARACTERS.md), question 8.
