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
| 12 | **A major event starts only when the character is aware of the change.** It starts **at once** if the character sees it or does it themselves; otherwise it starts when they learn of it. Until then, it is a normal day for them (§1.5) | Owner | 2026-11-27 |
| 13 | **Way C (mix): the rules find who is affected** by a change, using the relationship data. **The AI decides how** an AI-played character reacts. Background characters react by rules (§1.4) | Owner | 2026-11-27 |
| 14 | **False rumours** can start major events; **how the character learns** of a change affects the reaction; **hiding the truth** can become a plan (§1.5) | Owner | 2026-11-27 |
| 15 | **The main principle: every event is triggered by a stimulus**, something from outside that the character reacts to (§1) | Owner | 2026-11-27 |
| 16 | **There are two kinds of stimuli: major changes** (the list in §1.3) and **daily-life stimuli**, small things the character notices in everyday life, like Hobb watching the tax officer (§1.6) | Owner | 2026-11-27 |
| 17 | **Traits change how often daily-life events happen.** An **Observant** character gets them more often than other characters (§1.6) | Owner | 2026-11-27 |
| 18 | **Observant** means **more chance to understand** the information about things and the logic behind them (updated by [A02](analysis/A02-who-is-affected.md)); its opposite, **Oblivious**, gets fewer daily-life events (§1.6) | Owner | 2026-11-27 |
| 19 | **Other traits decide *what* a character notices**, e.g. Greedy notices chances for money, Kind notices people in need (§1.6) | Owner | 2026-11-27 |
| 20 | **Daily-life events are usually small** (knowledge, an option, an idea), but **many small ones over time can change a trait** (§1.6) | Owner | 2026-11-27 |
| 21 | **Every action of a character, and every impact on a character, has a chance to trigger an event** (§1) | Owner | 2026-11-27 |
| 22 | **No script forces story events, not even the final battle of Chapter 1.** The battle comes from a character's event: the **enemy general** (an AI-played major character) receives an **order from the enemy emperor** to take the town, and so he starts the battle (§7) | Owner | 2026-11-27 |
| 23 | **The player can change the story.** For example, the player has a chance to **persuade the general** not to start the war, **surrender the town** to avoid the battle, or choose other options (§7) | Owner | 2026-11-27 |
| 24 | **The emperor's order has a deadline**, e.g. *take the town before June*. The general must act within that time (§7.1) | Owner | 2026-11-27 |
| 25 | **The order is created when Chapter 1 is created**, at the start of the game. No messenger is created: **the general receives the order at once** (§7.1) | Owner | 2026-11-27 |
| 26 | **The emperor is not a character in Chapter 1.** He exists only through his order, and **appears in a later chapter** (§7.1) | Owner | 2026-11-27 |
| 27 | **The deadline is 1 month** of game time after the start. **Chapter 1 lasts about 1 month** of game time (§7.1) | Owner | 2026-11-27 |
| 28 | **What the general does if he misses the deadline depends on his perception of the emperor**: what he believes about the emperor's traits (§7.3) | Owner | 2026-11-27 |
| 29 | **Characters have perceptions of each other.** A character may know some of another character's traits, but not all; it depends on their perception of one another. To be designed in detail later (§7.3) | Owner | 2026-11-27 |
| 30 | **Characters may hide their true ideas and their true personality** from others (§8) | Owner | 2026-11-27 |
| 31 | **To learn another character's true personality, a character needs a way to see through them**, e.g. the **Observant** trait lets them learn more details about the other character (§8) | Owner | 2026-11-27 |
| 32 | **Hiding is a contest:** Deceitful characters hide well, Honest ones badly; the rules compare the watcher's Observant trait with the hider's skill at hiding (§8.3) | Owner | 2026-11-27 |
| 33 | **Each belief is stored with how it was learned** (seen, told, rumour). A belief from a rumour may be wrong (§8.3) | Owner | 2026-11-27 |
| 34 | **Learning a hidden truth is a stimulus** and can start an event, even a major one such as betrayal (§8.3) | Owner | 2026-11-27 |
| 35 | **The player sees other characters through the player character's perception**, not the truth. The character page shows what the player character believes, and how sure they are (§8.3) | Owner | 2026-11-27 |
| 36 | **Every action takes a period of time, including conversations**, and an action can cause an event (§5.1) | Owner | 2026-11-27 |
| 37 | **The time unit:** in normal life, **1 unit = 10 game minutes = 5 real seconds**, so 6 real hours ≈ 1 game month. Battles are different (§5.1) | Owner | 2026-11-27 |
| 38 | **When the game checks for events:** every time unit (10 game minutes), plus **at once** when something big happens, plus **when an action ends** (§5.4) | Owner | 2026-11-27 |
| 39 | **Who notices is decided by distance, walls and chance.** Hearing has short ranges, seeing longer ones; the closer, the more one learns. Facing matters for sight. Details in §1.7 and [A02 Part 2](analysis/A02-who-is-affected.md) | [A02](analysis/A02-who-is-affected.md) | 2026-11-27 |

## 1. What an event is

An **event** is something that happens to a character, or that a character notices.

**The main principle (decision 15): every event is triggered by a stimulus.** A **stimulus** (plural:
*stimuli*; Chinese 刺激) is something from outside that the character reacts to: something they see, hear,
suffer or do. No stimulus, no event.

**In other words (decision 21): every action of a character, and every impact on a character, has a chance to
trigger an event.**

**Two kinds of stimuli (decision 16):**

| Kind | What it is | How often | Example | Section |
|---|---|---|---|---|
| **Major change** | A big change in the character's life | Rare | The character's lover is killed | §1.2–1.5 |
| **Daily-life stimulus** | A small thing the character notices in everyday life | Common | Hobb watches the tax officer collect tax | §1.6 |

- Some events **show a choice** on screen: *"You see the captain's purse left on the table."* →
  `steal`, `report`, ignore.
- Some events happen **quietly**: the character only learns something or changes a little. Example: Hobb
  watches the tax officer at work and learns "tax collection seems easy".
- **The player and AI-played characters get the same events.** Background characters (run by rules only)
  get them too, but react by rules ([ACTIONS.md §2.1](ACTIONS.md)).

### 1.1 Events happen by chance (decision 8)
- Events do not happen on a fixed schedule. **Each possible event has a chance of happening.**
- What raises or lowers the chance:
  - **major changes** have a high chance (§1.2)
  - for **daily-life stimuli**, **traits** change the chance; Observant raises it (§1.6)
  - **TBD:** what else (open question 4)
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

How high the chance is will be decided later (open question 6).

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

### 1.4 How does the game know who is affected? (decision 13: way C)
Three ways were compared in **[analysis/A02](analysis/A02-who-is-affected.md)**. **Way C was chosen:**
- **The rules find who is affected**, using the relationship data. Example: X is killed → the rules find that
  Y is X's lover → Y gets a major event.
- **The AI decides how** an AI-played character reacts.
- **Background characters** react by rules.

**Why way C:** it follows the golden rule of this project: *the AI proposes, the game decides*
([AI_CHARACTERS.md §4.2](AI_CHARACTERS.md)). The relationship data (lover, friend, family, lord) already
exists in the shared character data ([AI_CHARACTERS.md §3](AI_CHARACTERS.md)).

### 1.5 When the event starts: awareness (decision 12)
**A major event starts only when the character is aware of the change.**

| Case | When the event starts | Example |
|---|---|---|
| **The character sees it** | **At once** | Aldric sees something cruel with his own eyes, e.g. the raiders kill his lover in front of him |
| **The character does it** | **At once** | Aldric kills a person for the first time (§1.3, row 10) |
| **It happens somewhere else** | **When the character learns of it:** finds the body, hears the news, hears a rumour | Wenna is killed far away. The event starts when the news reaches Aldric |
| **The character does not know** | **Not yet.** For them it is just a normal day | Aldric goes on working and does not know Wenna is dead |

This fits the rule that characters know only what they see or are told ([AI_CHARACTERS.md §5.2](AI_CHARACTERS.md)).

**More rules about awareness (decision 14):**
- **A false rumour** can start a major event for something that never happened, e.g. a rival spreads the
  lie that Wenna is dead (`spread_rumour`, [ACTIONS.md §3.4](ACTIONS.md)).
- **How it was learned changes the reaction.** Seeing it yourself hits harder than hearing a rumour, and a
  rumour may be doubted at first.
- **Hiding the truth can become a plan.** A murderer may try to keep the lover from finding out
  ([IDEAS.md](IDEAS.md)), and another character may decide when to tell them.

### 1.6 Daily-life stimuli (decisions 16 and 17)
Most events come from **ordinary life**: the character sees, hears or notices something small, and it gives
them knowledge, an option or an idea.

**Examples:**
- Hobb watches the tax officer collect tax and thinks it looks easy → the false tax officer idea
  ([IDEAS.md §2](IDEAS.md))
- someone notices the captain's purse left on the table → `steal`, `report`, ignore
- someone overhears that the miller hides his savings under the floor → `steal` unlocked on the mill
  ([ACTIONS.md §2.1](ACTIONS.md))

**Traits change the chance (decision 17).** An **Observant** character gets daily-life events **more often**
than other characters. Two characters can stand in the same market and see the same thing; only the Observant
one may **understand** what it means and get the event.

**The Observant trait (decision 18, updated by [A02](analysis/A02-who-is-affected.md)).** **Observant** means
more chance to **understand** the information about things and **the logic behind them**. It does **not** make
sight or hearing reach further: that is **Hawk Eye** and **Fox Ear** ([TRAITS.md](TRAITS.md)). Its opposite is
**Oblivious**: an Oblivious character rarely understands what is going on, so they get fewer daily-life events.

**Other traits decide *what* a character notices (decision 19)**, not only how often. A Greedy character
notices chances for money; a Kind one notices people in need ([ACTIONS.md §2.2](ACTIONS.md)). So an Observant,
Greedy character notices many chances for money.

**Small events add up (decision 20).** Daily-life events are usually small: knowledge, an unlocked option, or
an idea. They rarely change traits on their own, but **many small ones over time can**. Example: a character
who sees cruelty again and again may become hard-hearted.

**Proposal (not decided):** **skills may also help** a character notice things, e.g. a high Intrigue skill
helps notice secrets and lies (open question 5).

### 1.7 Who notices: seeing and hearing (decision 39)
A character becomes aware of something (decision 12) by **seeing** or **hearing** it, decided by
**distance + walls + chance**. The full analysis is in [analysis/A02 Part 2](analysis/A02-who-is-affected.md).

| Signal | Sense | Range |
|---|---|---|
| Whisper | Hearing | up to 1 m |
| Normal talk | Hearing | 3–5 m |
| Shouting, an argument | Hearing | 15–30 m |
| Fighting, a scream | Hearing | 30–60 m |
| A horn, a bell | Hearing | hundreds of metres |
| Seeing *that* something happens | Sight | 50–100 m (daylight) |
| Seeing **who** it is and **what** they do | Sight | 10–20 m (daylight) |
| Small details (a coin passed in secret) | Sight | 1–3 m |

**The rules:**
- **The closer, the more you learn.** Far away you see or hear *that* something happens; closer, *who* and
  *what*; very close, the details. The chance also falls with distance.
- **You recognise a voice only if you know that person.**
- **Seeing and hearing add up:** seeing tells you who, hearing tells you what was said.
- **What changes it in Chapter 1:** walls, night (light), noise, attention, traits (**Hawk Eye**, **Fox Ear**,
  about 1.5× the ranges; [TRAITS.md](TRAITS.md)), the actor's stealth, and **facing**: sight is best in front,
  lower at the sides, very low behind; hearing works the same in every direction.
- **What you learn is stored with how sure you are** (decision 35).
- These ranges are starting values, to be tuned in playtesting.

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

**World events** (proposal) happen on their own, without a character causing them: e.g. weather, a bad
harvest, a sickness ([AI_CHARACTERS.md §5.8](AI_CHARACTERS.md)). **Big story events are different:** they
come from characters, not from a script. Even the enemy's attack starts with the enemy general's decision (§7).

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

## 5. Events and the clock: when does the game check for events?

### 5.1 The facts we start from
- The game runs in **real time** (decision 36):
  - **Every action takes a period of time**, and so does a **conversation**.
  - **An action can cause an event** (decision 21).
- **The time unit (decided 2026-11-27):** in normal life, **1 unit = 10 game minutes = 5 real seconds**.
  1 game day ≈ 12 real minutes; Chapter 1 (about 1 game month) ≈ 6 real hours
  ([AI_CHARACTERS.md §7](AI_CHARACTERS.md)). Battles use finer steps.
- An event **starts at once** when the character sees or does the change (decision 12).

### 5.2 How this was decided
Two options were compared in **[analysis/A03](analysis/A03-event-check-timing.md)**: **A.** check after every
action is done, or **B.** check every time unit. Checking after every action leaves gaps during long actions
and misses slow changes. Checking every 10 game minutes works for almost everything, but adds a few seconds of
delay for big, sudden moments. So B was chosen, with two extra checks (§5.4).

### 5.3 (moved)
The detailed comparison is now in [analysis/A03](analysis/A03-event-check-timing.md).

### 5.4 Chosen (decision 38): B, plus checks at once and at the end of actions

| Check | When | What it catches | Example |
|---|---|---|---|
| **1. At once** | The moment something big happens to a character, or in front of them | Major changes (§1.3), being attacked, seeing a crime, hearing shocking news | Aldric sees Wenna killed → the event starts that second |
| **2. When an action ends** | Each time an action finishes or fails | The result of what the character did | Aldric kills a man for the first time; Hobb's fraud succeeds or fails |
| **3. Every time unit** (10 game minutes) | Every 5 real seconds | Daily-life stimuli noticed during any action (§1.6), and slow changes with no action behind them | Hobb notices the tax officer; hunger grows; the general's deadline comes closer; a rumour spreads |

**Rules that make this work (proposal):**
- **Small chances per unit.** The chance of a daily-life event in one unit is small, so over a day a character
  gets only a few events. Because the check is per unit of time, it is fair: ten short actions and one long
  action of the same length get the same number of checks.
- **Spread the checks.** Not every character is checked in the same instant: their checks are spread across
  the 5 seconds, so the game runs smoothly and AI calls don't come in bursts.
- **Conversations:** big news or a lie told in a conversation is a check 1, at once. The general effect of the
  talk (opinion, memories) is a check 2, when the conversation ends.
- **Stimuli for others.** When something happens, the rules also find who **saw** it or was **affected**
  (way C, §1.4). Each of them gets their own check, if they are aware of it (decision 12).
- **Interrupting.** A major event at once (check 1) can **interrupt** the action the character is doing.
  Aldric drops his tools when he hears the news. A small event does not interrupt.
- **The rules check, the AI reacts.** All checks are done by rules, which is cheap. The AI is called only when
  an event happens to an AI-played character and matters to them (§4).

### 5.5 Example: one morning for Hobb

| Game time | Real time from 07:00 | What happens | Check |
|---|---|---|---|
| 07:00 | 0 s | Hobb starts `work` at the market (8 hours = 48 units ≈ 4 real minutes) | — |
| 07:10, 07:20, … | every 5 s | A small check each unit for daily-life stimuli. Being Greedy, he notices chances for money | 3 |
| 10:00 | 1.5 min | He notices the tax officer collecting tax. The event happens: knowledge *"tax collection seems easy"*, and `collect_tax` is unlocked | 3 |
| 10:00 | 1.5 min | The event matters to his ambition *become rich*, so the AI is asked and writes the false tax officer idea. He keeps working while the AI thinks | (AI) |
| 12:00 | 2.5 min | A brawl breaks out in front of him: a stimulus at once. He can watch, join or leave | 1 |
| 15:00 | 4 min | Work ends. He is paid; the end of the action is checked | 2 |
| All day | — | Each unit: his hunger grows a little, and news of the brawl spreads through town | 3 |
### 5.6 Does an event pause the clock?
[PLAN.md §7](PLAN.md) says **dialogue and decision events pause the clock**, but
[AI_CHARACTERS.md §7](AI_CHARACTERS.md) still lists this as an option to consider. This needs a decision
(open question 10).

### 5.7 Performance: is checking hundreds of characters every unit OK?
**Yes, for a PC game this is fine.** The full analysis is in
**[analysis/A04](analysis/A04-event-check-performance.md)**. In short:
- Event checks are done by **rules, not the AI**, so they are cheap: thousands per unit take only milliseconds.
- **The checks are spread** across the 5 seconds of a unit, so the player never feels them (§5.4).
- **The number of characters stays limited** (decision 14 in [AI_CHARACTERS.md](AI_CHARACTERS.md)): individual
  characters stay in the hundreds, and far places are **group characters**.
- **Points for when coding starts (proposal):** find nearby characters by place; never wait for the AI; let old
  memories fade; test with 1,000 fake characters in `--autotest` (milestone D2).

## 6. Example: from event to idea

> **Event:** Hobb (Greedy, Deceitful) watches the tax officer collect tax from a farmer.
> **Source:** the situation (he was there) and his traits (Greedy characters notice chances for money).
> **Results:**
> - knowledge: "tax collection seems easy"
> - unlocked action: `collect_tax`, as an event option
> - the event matters to his ambition *become rich*, so the AI is asked → it writes the **false tax officer**
>   idea ([IDEAS.md §2](IDEAS.md))

## 7. Story events come from characters, not a script (decisions 22 and 23)

Big story events follow the same principle as every other event: **a stimulus reaches a character, and the
character acts.** There is no script that forces them to happen.

### 7.1 Example: the final battle of Chapter 1
The final battle is the big event of Chapter 1's story ([WARFARE.md](WARFARE.md) plans about 300–400 men).
It happens like this:

| Step | What happens | Kind |
|---|---|---|
| 1 | The **enemy emperor** sends an order to his **general**: *take the frontier town within 1 month* | A stimulus for the general |
| 2 | The general, an **AI-played major character**, gets an event from the order | Event |
| 3 | The order gives him the intent *take the town*; his AI makes plans: gather troops, march, attack | Intent and ideas ([IDEAS.md](IDEAS.md)) |
| 4 | The battle starts because of **his** decision, not because of a script | Result |

**When the order comes (decision 25).** The order is created **when Chapter 1 is created**, at the start of
the game. No messenger character is created: **the general has the order from the very start.** So from the
first moment, the general already has the intent *take the town before the deadline*.

**The emperor (decision 26).** The emperor is **not a character in Chapter 1**. He exists only through his
order. He will **appear in a later chapter**.

**The deadline (decisions 24 and 27).** The order says *when*: **within 1 month** of game time.
Chapter 1 lasts about 1 month of game time, so the deadline falls near its end. So the battle is
not forced at a fixed moment, but the general has a reason to act within that time.

**Proposals (not decided):**
- **The deadline puts pressure on the general.** As it comes closer, he is more likely to attack, even if he
  is not fully ready.
- **Missing the deadline has costs for him:** the emperor may be angry, replace him, or punish him. A general
  who fears the emperor will try hard not to miss it. Because the emperor is not a character in Chapter 1
  (decision 26), this would be handled by **rules or a story event**, e.g. a letter of recall.
- **The player can use the deadline.** Delaying the general past it (sabotage, false news, talks) may change
  his choices, or lead to his recall.
- **The town can learn of the deadline** through spies, prisoners or rumours, and plan around it.


### 7.2 The player can change it (decision 23)
Because the battle comes from a character, **the player can act on that character.** Options include:
- **persuade the general** not to start the war
- **surrender the town**, so there is no battle
- other options (to be designed)

**Proposals (not decided):**
- **More ways to change it:** delay the general (sabotage his supplies, spread false news), turn his officers
  against him, warn the town so it is better prepared, or kill the general. Each is a normal action or idea.
- **Reaching the general is hard.** He is in the enemy camp. The player may need a position (messenger,
  officer, the lord's envoy), a disguise, or the help of other characters.
- **If the general is stopped, the story goes on.** Another general may be sent, or the first one punished
  (by rules, since the emperor is not a Chapter 1 character). This uses **story roles** ([AI_CHARACTERS.md §5.8](AI_CHARACTERS.md)): the role *the enemy commander*
  can pass to another character.
- **The general has his own personality.** Whether he can be persuaded depends on his traits, his loyalty to
  the emperor, and what he fears. A loyal, proud general is very hard to persuade; a cautious one who fears
  losing men may listen.
- **Surrender is a choice with costs.** It avoids the battle but may anger the lord, make the player a traitor
  in some eyes, and lead to a different chapter ending.

### 7.3 If the general misses the deadline: perception (decisions 28 and 29)
What the general does if he misses the deadline **depends on his perception of the emperor**.

A **perception** (Chinese 认知) is what one character **believes** about another: which traits they think the
other has, and what they expect the other to do. It may be **right, partly right, or wrong**.

- **Characters know only some of each other's traits** (decision 29). How much they know, and how correct it
  is, depends on their perception of one another.
- So the general's choice comes from **what he believes** about the emperor, not from the emperor's real
  traits.

**The owner's example:** the general believes the emperor is **Ambitious** and **cares about his people**:
a certain kind of ruler. If he misses the deadline, he thinks about this personality to decide what to do.
Two beliefs can pull different ways (proposal):
- *Ambitious:* "He wants this town badly. Failing him is dangerous." → push to attack soon
- *Cares about his people:* "He doesn't want his soldiers wasted." → a careful delay that saves men may be
  forgiven
- The general, played by AI, weighs both, together with his own traits (e.g. Brave or Cautious), and
  chooses. A different general with different beliefs could choose differently.

**More examples (proposal):**

| The general believes the emperor is… | If the deadline is near or missed, he may… |
|---|---|
| **Cruel** (punishes failure harshly) | Attack at any cost; or, if he cannot win, flee or change sides |
| **Patient** or **Fair** | Write to explain the delay and ask for more time |
| **Weak** | Ignore the deadline, or even start his own plans |

**Perception will be designed in detail later.** It probably belongs with the shared character data
([AI_CHARACTERS.md §3](AI_CHARACTERS.md)), and links to hidden intents ([AI_CHARACTERS.md §5.7](AI_CHARACTERS.md)).

## 8. Perception: hiding and seeing through (decisions 29–31)

### 8.1 Characters can hide (decision 30)
A character may **hide their true ideas** (plans, intents) and **their true personality** (traits).
So what others believe about them (their perception, §7.3) can be **wrong**.

- Example: a Deceitful, Ambitious officer acts loyal and humble in front of the captain. The captain's
  perception: *"loyal, humble"*. The truth: *"ambitious, waiting for a chance"*.
- This links to hidden intents ([AI_CHARACTERS.md §5.7](AI_CHARACTERS.md)): intents are hidden until learned.

### 8.2 Seeing through (decision 31)
To learn another character's **true** personality, a character needs a way to see through them.
- The **Observant** trait (§1.6) helps: an Observant character **learns more details** about others.

**More ways to learn the truth (proposal, not decided), many already in [AI_CHARACTERS.md §5.7](AI_CHARACTERS.md):**

| Way | Example |
|---|---|
| **Watching** what they do over time | He says he is brave, but he ran from the brawl |
| **Talking** to them, or to their friends | A friend lets slip that the officer wants the captain's post |
| **Rumours** (may be false) | *"They say the miller cheats on his flour."* |
| **Spying:** `follow`, `eavesdrop`, `search` ([ACTIONS.md §3.6](ACTIONS.md)) | Overhearing the officer's secret meeting |
| **Skills**, e.g. Intrigue (not decided, open question 5) | Noticing a lie in a conversation |
| **Time and closeness** | Family and old friends know each other better than strangers do |

### 8.3 Rules of perception (decisions 32–35)
- **Hiding is a contest (decision 32).** A Deceitful character is good at hiding; an Honest one is bad at it.
  When an Observant character watches a Deceitful one, the rules compare them, and the truth may or may not
  come out.
- **Each belief is stored with how it was learned (decision 33):** seen, told, or rumour, like intents
  ([AI_CHARACTERS.md §5.7](AI_CHARACTERS.md)). A belief from a rumour may be wrong.
- **Learning a hidden truth is a stimulus (decision 34).** Finding out that a friend is not what he seemed
  can start an event, even a major one (§1.3, row 5: betrayal).
- **The player sees through the player character's eyes (decision 35).** The character page shows what the
  player character **believes** about another character, not the truth, and how sure they are.

## 9. Open questions

1. **The owner's ideas for events:** to be added.
2. **Perception (§7.3 and §8):** which of the other ways of seeing through in §8.2 are wanted? Is the example
   table in §7.3 the right idea? How is "how sure they are" shown to the player?
3. **Changing the battle (§7.2):** which of the proposals are wanted? How can the player reach the general?
   What happens if the general is stopped, and what does surrender lead to?
4. **Chance (decision 8):** besides major changes and traits (§1.6), what else raises or lowers an event's
   chance? For example: the place, the time, who is nearby, needs, or the story. Is the chance shown to the player, or hidden like dialogue chances?
5. **Skills (§1.6, not decided):** should skills also help a character notice things, e.g. Intrigue for
   secrets and lies?
6. **Major changes (decisions 9 and 11):** are any major changes missing from §1.3?
   **Later:** how high is "a high chance": almost always (like 90%), or just higher than normal?
7. **Sources:** is the list in §2 right? What should be added or removed?
8. **How events are written:** by hand, made by rules from the situation, made by the AI, or a mix?
9. **How often:** how many events with choices should the player see per hour, so they stay special but the
   world still feels alive?
10. **The clock:** should events with choices always pause the game (§5.6)?
13. **Event checks (§5.4):** the "rules that make this work" are still proposals: small chances per unit,
    spreading the checks, conversations, interrupting. Are they right?
11. **Traits:** which events and options does each trait open (decision 6)?
12. **Chapter 1:** which story and world events does the demo need (e.g. the enemy's arrival)? Also asked in
   [AI_CHARACTERS.md §12](AI_CHARACTERS.md), question 8.
