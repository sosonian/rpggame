# Crowns of Ashvale — Actions

> Design document for **actions**: everything a character can do in the world.
> **Status: draft list, to be worked out together.**
> Items marked **(proposal)** are suggestions waiting for a decision.
> Related: [AI_CHARACTERS.md §5](AI_CHARACTERS.md) (plans), [IDEAS.md](IDEAS.md) (ideas), [EVENTS.md](EVENTS.md) (events), [ITEMS.md](ITEMS.md) (items and trade),
> [WARFARE.md](WARFARE.md) (battle).

## 0. Decisions so far

| # | Decision | Date |
|---|----------|------|
| 1 | Plan entries are called **actions**. The player and every character share **one list of actions** | 2026-11-25 |
| 2 | The actions marked "Later (or Ch. 1?)" stay in the list as they are | 2026-11-25 |
| 3 | **All actions have the same properties** (§2) | 2026-11-25 |
| 4 | **Two ways to take an action:** some by **clicking places and people**, others as **options in an event** (§2.1) | 2026-11-25 |
| 5 | **Positions give some actions naturally.** Other characters may get the same action as an **event option**, often as a crime. Example: a liar gets the idea to pose as a tax officer and "collect tax" from others (§2.2) | 2026-11-25 |
| 6 | **Some actions exist only through events.** After the event, the action appears as an option when you click the related item, place or character (§2.1) | 2026-11-25 |
| 7 | **An idea (or plan) is made of several actions.** Ideas are **not limited to a fixed list**: they arise **after an event** and are **produced by the AI**. Impersonation is an idea, not a single action ([IDEAS.md](IDEAS.md)) | 2026-11-25 |
| 8 | Which starting positions Chapter 1 has, and which ideas and options each trait opens, will be decided later with the event system | 2026-11-25 |
| 9 | **The AI also suggests ideas to the player character**, based on the player's traits and situation. The player can follow or ignore them ([IDEAS.md](IDEAS.md)) | 2026-11-25 |
| 10 | **Dialogue options are chosen by chance.** Each possible option gets a chance from the character's **personality** and the **situation**. The system shows the **top 5**. Example: lying to someone vital to you has a low chance, so it rarely appears (§2.4) | 2026-11-25 |
| 11 | Dialogue details: options below a **threshold** chance are not shown, so there can be fewer than 5. Very rarely, a **surprising option** appears from outside the top 5. **The player sees only the options, never the chances** (§2.4) | 2026-11-25 |
| 12 | **Every action takes a period of time, including conversations.** An action can cause an event; when the game checks for events is in [EVENTS.md §5](EVENTS.md) | 2026-11-27 |
| 13 | **New action `recall`** (回憶): can be done **at any time**. It opens a **memory screen**; the player chooses one memory and the character **talks to himself** about it. Memories come from what the character **saw, heard and did** (§3.1) | 2026-11-27 |
| 14 | **For AI-played characters, `recall` is not a free action.** It appears only as an **option in an event** or an **action inside an idea**. AI-played characters still **store memories** and **forget** them, like the player (§3.1) | 2026-11-27 |
| 15 | **What `recall` is for:** an **idea can jump out** of the inner talk, and the player can **check his memory inventory** (e.g. does he still remember the scene of the murder?). `recall` **costs stamina and time**. The memory system is in [MEMORIES.md](MEMORIES.md) | 2026-11-27 |

## 1. What an action is

- An **action** is one thing a character does in the world, such as `buy`, `work`, `talk_to` or `steal`.
- **The player and every other character share the same list of actions.**
  - The player chooses actions with the mouse, menus and the dialogue screen.
  - AI-played characters choose them by writing a **plan**: a short list of actions
    ([AI_CHARACTERS.md §5.3](AI_CHARACTERS.md)).
  - Background characters choose them by rules.
- **The rules carry out every action** in real time and decide the result.
- **Two levels of action (proposal):**

  | Level | Examples | Where designed |
  |---|---|---|
  | **Life actions:** what a character decides to do; used in plans | `work`, `buy`, `patrol`, `challenge`, `attack` | This document |
  | **Battle moves:** moment-to-moment control in a fight | Swing, block, shoot, dodge, shout an order | [WARFARE.md](WARFARE.md) |

  A life action like `attack` or `patrol` may lead into a fight, which is then played out with battle moves.

## 2. What every action defines (decision 3: all actions have the same properties)

| Property | Meaning | Example: `steal` |
|---|---|---|
| **Target / details** | Who or what it is done to, and how | Steal *a purse* from *the merchant* |
| **How it is taken** | By clicking a place or person, or as an event option (§2.1) | Click a person, or an event option ("the merchant is distracted…") |
| **Access** | Who has it naturally (from position), and who can get it through an event (§2.2) | Nobody naturally; offered by events to Greedy, poor or desperate characters |
| **Requirements** | Place, items, skills, traits, rank or authority, relationship | Be near the target; nobody watching closely |
| **Duration** | How long it takes. Every action takes time, conversations too (decision 12). Measured in game time, in steps of the 10-game-minute unit; short actions finish within one unit (proposal) | Within one unit |
| **Cost** | Money, items, energy | — |
| **Success check** | Automatic, or a check of skill against difficulty or an opponent | Intrigue vs the target's awareness |
| **Visibility** | Public, private or secret; who might witness it | Secret; witnesses may notice |
| **Legality** | Legal, frowned upon, or a crime | Crime |
| **Results** | Items, money, opinion, memories, trait progress, progress on intents | Gain the purse; if caught: arrest, opinion loss, Thief reputation |
| **Trait reactions** | Who is comfortable doing it, and who suffers stress | Honest characters dislike it; Greedy ones like it |

Even simple actions such as `eat` have all these properties. Most are just short:
`eat` has no access limits, is taken by clicking, takes a moment, is legal, and fills hunger.

### 2.1 Two ways to take an action (decision 4)

| Way | How it works | Examples |
|---|---|---|
| **Direct: click** | Click a place or a person, and pick from the actions available there | Click the smithy → `buy`, `repair`, `seek_job`. Click a person → `talk_to`, `give`, `attack` |
| **Event option** | An event appears with a few choices; each choice is an action | "You see the captain's purse left on the table." → `steal`, `report`, ignore |

- **Events can come from:** the story, the situation (where you are, who is there), your traits and
  background, your needs, or other characters' actions.
- **AI-played characters get the same events and options.** An event option becomes a legal action in their
  plan ([AI_CHARACTERS.md §4.2](AI_CHARACTERS.md)). Background characters choose by rules.
- **Event-only actions (decision 6):** some actions can't be clicked until an event has unlocked them.
  After the event, the action appears as a **new option on the related item, place or character**.
  - Example: after you overhear that the miller hides his savings under the floor, clicking the mill shows
    `steal` (his savings).
  - Example: after watching how tax is collected, clicking a farmer shows `collect_tax`.
- **Proposal:** each action is marked as *direct*, *event only*, or *both*, and an unlocked option stays until
  it no longer makes sense (e.g. the savings were moved).

### 2.2 Access: natural, or offered by events (decision 5)
The same action can be open to a character in two ways:

| Access | Who | Example: `collect_tax` |
|---|---|---|
| **Natural** | Characters whose **position** gives them the action. They can take it directly at any time, legally | A tax officer collects taxes as part of the job |
| **Through an event** | Other characters, when an **event** offers it because of their **traits, background or situation**. Often a crime or a trick | A Deceitful character gets the idea to **pose as a tax officer** and collect "tax", in fact stealing the money |

- **The same action can have different legality** depending on access. Collecting tax is a duty for the
  officer and fraud for the impostor.
- **Impostors face checks:** e.g. Intrigue against the victim's suspicion. Being caught means arrest, a fine
  or worse, plus infamy, and anger from the real tax officer and the lord.
- **Personality shapes which options events open.** A Greedy character notices chances for money; a Kind one
  notices people in need. The details belong to the event system ([EVENTS.md](EVENTS.md)) and will be designed later (decision 8).
- **The starting position** therefore decides the actions the player has naturally. Their **personality**
  decides which other doors events may open.

### 2.3 Ideas: plans made of actions (decision 7)
An **idea** (also called a **plan**) is a goal plus a list of actions to reach it. Ideas now have their own
document: **[IDEAS.md](IDEAS.md)**, with the false tax officer example and how ideas work.

### 2.4 Dialogue options by chance (decision 10)
In a conversation, the game does not show every possible option. It works out a **chance** for each option and
shows the **top 5**.

1. **Collect the possible options.** Only options that make sense right now: e.g. *Remind him of Ashford* needs
   the shared memory; *Pay a bribe* needs money.
2. **Work out each option's chance** (0–100%), from:
   - **personality:** traits and skills, e.g. Deceitful raises *Lie*; Honest lowers it; Cruel raises *Threaten*
   - **the situation:**
     - who the other person is to you: someone vital to you (family, lover, lord, best friend) makes lying
       or threatening much less likely
     - opinion of them
     - what is at stake and the risk of being caught
     - mood and stress
     - place and witnesses
3. **Drop options below the threshold** (decision 11). The exact value is TBD; proposal: about 20%.
4. **Show the 5 options with the highest chance.** If fewer pass the threshold, fewer are shown.
5. **A rare surprise** (decision 11): very rarely, one option from *below* the top 5 (even below the threshold)
   replaces the last option, a sudden temptation or an out-of-character impulse. Proposal: around a 1–2% chance
   per conversation. It may be more likely under high stress or strong emotion.

**Example:** Hobb (Greedy, Deceitful) is asked where he got his new coat.

| Option | To a stranger | To his mother (vital to him) |
|---|---|---|
| *Lie: "I found it."* | 80% | 15% |
| *Tell the truth* | 10% | 60% |
| *Change the subject* | 55% | 50% |
| *Get angry* | 30% | 20% |
| *Bribe them to stay quiet* | 25% | — (makes no sense) |
| *Joke about it* | 40% | 45% |

Hobb lies to a stranger easily. With his mother, the lie falls below a 20% threshold, so it is not shown,
unless the rare surprise brings it up.

- **The same method serves AI-played characters (proposal):** the top options by chance are the legal reactions
  sent to the AI, which picks one and writes the words ([AI_CHARACTERS.md §4.3](AI_CHARACTERS.md)).
- **The chance numbers are hidden from the player** (decision 11). The player sees only the options, which
  simply feel in character.

## 3. The action list

**Ch. 1** means the action is proposed for the Chapter 1 demo. **Later** means a later chapter.
Some names may merge or split as we design them.

### 3.1 Daily life and survival

| Action | What it does | Ch. 1? |
|---|---|---|
| `go_to` | Travel to a place | Ch. 1 |
| `rest` / `sleep` | Recover energy and health | Ch. 1 |
| `eat` / `drink` | Eat food or drink; needed to survive ([ITEMS.md §7](ITEMS.md)) | Ch. 1 |
| `wait` | Wait for a time, or until something happens (e.g. "until Brann is alone") | Ch. 1 |
| `treat` | Treat wounds or illness, your own or someone else's; needs bandages or herbs and skill | Ch. 1 |
| `pray` | Pray at a shrine; comfort, faith, maybe lower stress | Ch. 1 |
| `relax` | Spend time at the tavern or at home; mood and stress, chance to meet people | Ch. 1 |
| `equip` / `unequip` | Put on or take off weapons, armour, clothing | Ch. 1 |
| `store` / `take` | Put items in or take them from home, a storehouse or a cart | Ch. 1 |
| `recall` (回憶) | Look back on a memory: open the memory screen, choose a memory, and talk to yourself about it (see below) | Ch. 1 |

**`recall` (回憶), decision 13:**
- **When:** the **player** can do it at any time. For **AI-played characters** it is only an option in an
  event or an action inside an idea (decision 14).
- **How:** opens the **memory screen**, a list of the character's memories. The player chooses one, and the
  character **talks to himself** about it, as a short inner thought.
- **Where memories come from:** what the character **saw, heard and did** ([EVENTS.md §1.7](EVENTS.md)), stored
  with how sure they are. Memories **fade** over time; **Good Memory** and **Forgetful** change how fast
  ([TRAITS.md](TRAITS.md)).
- **What it is for (decision 15):**
  - **An idea can jump out** of the inner talk ([IDEAS.md](IDEAS.md)).
  - **Checking the memory inventory:** e.g. does the player still remember the scene of the murder?
  - **It costs stamina and time** (amounts TBD).
  - The memory system itself is in **[MEMORIES.md](MEMORIES.md)**.
- **Proposals (not decided):**
  - The memory screen shows for each memory: what happened, when, how it was learned (seen, heard, did, told),
    how sure the character is, and how faded it is.
  - **Recalling refreshes the memory**, so it fades more slowly afterwards.
  - The inner thought is **written by the AI** in the character's voice. Besides an idea, it may give an
    insight, e.g. an Observant character notices something they missed before.
  - It may **change mood or stress**: a sad memory hurts; a proud one comforts.
- **AI-played characters (decision 14):** they don't `recall` freely, but they **store memories** and
  **forget** them in the same way as the player, and Good Memory and Forgetful work for them too. Examples of
  `recall` for them: an event (seeing the place where a friend died) offers *remember him*; an idea for revenge
  starts with *recall what happened at Ashford*.

### 3.2 Work and economy

| Action | What it does | Ch. 1? |
|---|---|---|
| `work` | Do your job for wages or produce (soldier's duty, baker, smith, clerk…) | Ch. 1 |
| `seek_job` | Ask someone for a job or position | Ch. 1 |
| `quit_job` | Leave your job | Ch. 1 |
| `gather` | Collect wood, stone, herbs, berries; needs the right tool | Ch. 1 |
| `farm` | Sow, tend, harvest a field (could be part of `work`) | Ch. 1 |
| `tend_animals` | Feed, herd, milk, shear animals | Ch. 1 |
| `hunt` | Hunt wild animals in the wild; needs a weapon; dangerous | Ch. 1 |
| `fish` | Catch fish; needs a net or rod | Ch. 1 |
| `make` | Craft an item from a recipe ([ITEMS.md §5](ITEMS.md)) | Ch. 1 |
| `repair` | Restore an item's durability | Ch. 1 |
| `buy` / `sell` | Trade items for coin at a shop, the market or with a person | Ch. 1 |
| `barter` | Trade items for items | Ch. 1 |
| `hire` / `dismiss` | Employ someone, or let them go | Ch. 1 |
| `lend` / `borrow` / `repay` | Money between characters, with debts remembered | Ch. 1 |
| `pay` | Pay wages, taxes, fines, debts | Ch. 1 |

### 3.3 Learning and self-improvement

| Action | What it does | Ch. 1? |
|---|---|---|
| `train` | Practise a skill alone (sword practice, archery) | Ch. 1 |
| `ask_to_teach` | Ask a mentor or expert to teach you | Ch. 1 |
| `study` | Read and learn; needs books and literacy | Later |

### 3.4 Talking and relationships
`talk_to` opens the choice-based dialogue ([AI_CHARACTERS.md §4.3](AI_CHARACTERS.md)). Many actions below can
happen as **dialogue options inside a conversation**, or as actions on their own in a plan.

| Action | What it does | Ch. 1? |
|---|---|---|
| `talk_to` | Start a conversation on a topic | Ch. 1 |
| `chat` | Small talk; slowly builds opinion and friendship | Ch. 1 |
| `ask_about` | Ask about a person, place or event; gathers information | Ch. 1 |
| `tell` / `report` | Pass on news, true or false, to someone; report to a superior | Ch. 1 |
| `spread_rumour` | Spread a story, true or false, about someone | Ch. 1 |
| `give` | Give a gift; raises opinion | Ch. 1 |
| `ask_favour` | Ask for help, a loan, a recommendation | Ch. 1 |
| `persuade` | Try to change someone's mind or win them over | Ch. 1 |
| `invite` | Invite someone to a meal, a drink or an event | Ch. 1 |
| `comfort` | Comfort someone grieving or afraid | Ch. 1 |
| `apologise` | Try to repair a damaged relationship | Ch. 1 |
| `insult` / `provoke` | Lower someone's opinion; may start a fight | Ch. 1 |
| `threaten` | Pressure someone through fear | Ch. 1 |
| `bribe` | Offer money for a favour or silence | Ch. 1 |
| `blackmail` | Use a known secret to force someone | Ch. 1 |
| `court` | Romance someone | Ch. 1 |
| `propose_marriage` | Ask someone to marry | Later (or Ch. 1?) |

### 3.5 Service and duty
For characters who serve a lord, the town or the garrison. Some need rank or authority.

| Action | What it does | Ch. 1? |
|---|---|---|
| `ask_for_task` | Ask a superior for a mission or task | Ch. 1 |
| `give_task` | Give a mission or task to someone below you | Ch. 1 |
| `report_back` | Report the result of a task; earns merit | Ch. 1 |
| `patrol` | Patrol an area: roads, walls, the wild | Ch. 1 |
| `guard` | Guard a place or a person (e.g. as the lord's bodyguard) | Ch. 1 |
| `escort` | Escort a person or goods safely | Ch. 1 |
| `scout` | Scout an area to learn what is there (e.g. enemy movements) | Ch. 1 |
| `deliver` | Carry a message or item to someone (messenger work) | Ch. 1 |
| `collect_tax` | Collect taxes or rents (officials) | Ch. 1 |
| `arrest` | Arrest a suspect; needs authority | Ch. 1 |
| `judge` | Judge a case and give a punishment; needs high authority | Later (or Ch. 1?) |
| `ask_promotion` | Ask for a higher rank | Ch. 1 |
| `swear_oath` | Swear loyalty to a lord | Later |
| `desert` | Abandon your post or unit | Ch. 1 |

### 3.6 Information and stealth

| Action | What it does | Ch. 1? |
|---|---|---|
| `watch` | Keep watch on a person or place | Ch. 1 |
| `follow` | Follow someone, openly or secretly | Ch. 1 |
| `eavesdrop` | Listen in on a conversation | Ch. 1 |
| `search` | Search a place or a person for items or clues | Ch. 1 |
| `hide` | Hide yourself, or hide an item (e.g. a secret letter) | Ch. 1 |
| `sneak` | Move without being noticed | Ch. 1 |
| `read` | Read a letter or document; needs literacy | Ch. 1 |
| `forge` | Fake a letter, seal or document; needs skill | Later (or Ch. 1?) |
| `disguise` | Pretend to be someone else | Later |

### 3.7 Crime

| Action | What it does | Ch. 1? |
|---|---|---|
| `steal` | Take an item from a person or place | Ch. 1 |
| `break_in` | Enter a locked building | Ch. 1 |
| `sabotage` | Damage an item, building or plan | Ch. 1 |
| `smuggle` | Move forbidden goods or people | Later (or Ch. 1?) |
| `poison` | Poison food or drink; needs poison and skill | Ch. 1 |
| `murder` | Kill someone in secret; very hard ([AI_CHARACTERS.md §5.6](AI_CHARACTERS.md)) | Ch. 1 |
| `loot` | Take items from the dead, or from an abandoned or captured place | Ch. 1 |
| `escape` | Escape from arrest or prison | Ch. 1 |

### 3.8 Conflict and fighting
These start fights, which are then played with battle moves ([WARFARE.md](WARFARE.md)).

| Action | What it does | Ch. 1? |
|---|---|---|
| `brawl` | A fist fight; usually not deadly | Ch. 1 |
| `challenge` | Challenge someone to a duel | Ch. 1 |
| `attack` | Attack a person or group openly | Ch. 1 |
| `ambush` | Attack from hiding | Ch. 1 |
| `defend` | Protect a person or place | Ch. 1 |
| `flee` | Run from danger | Ch. 1 |
| `surrender` | Give up a fight | Ch. 1 |
| `capture` | Take someone prisoner | Ch. 1 |
| `ransom` / `release` | Ask a price for a prisoner, or let them go | Ch. 1 |
| `execute` | Put a prisoner to death; needs authority | Later (or Ch. 1?) |
| `raid` | Attack and plunder a village or caravan | Later (band path) |

### 3.9 Groups and plots

| Action | What it does | Ch. 1? |
|---|---|---|
| `join` / `leave` | Join or leave a unit, group or plot | Ch. 1 |
| `recruit` | Ask someone to join you, your group or your plot | Ch. 1 |
| `start_plot` | Begin a secret plan with a goal (e.g. ruin a rival); others can be recruited | Ch. 1 |
| `expose` | Reveal a plot or secret to someone (e.g. the lord) | Ch. 1 |
| `betray` | Turn against your group, plot or lord | Ch. 1 |
| `form_band` | Gather followers under your lead | Later (band path) |

### 3.10 Later chapters only (lord and realm), names only

`grant_land`, `declare_war`, `make_peace`, `send_messenger`, `raise_army`, `set_battle_plan`,
`use_sand_table`, `build`, `set_taxes`, `arrange_marriage`, `name_heir`, …
These will be designed with the lordship milestone (PLAN.md M5).

## 4. Count

| Group | Ch. 1 | Later |
|---|---|---|
| Daily life and survival | 10 | — |
| Work and economy | 15 | — |
| Learning | 2 | 1 |
| Talking and relationships | 16 | 1 |
| Service and duty | 12 | 2 |
| Information and stealth | 7 | 2 |
| Crime | 7 | 1 |
| Conflict and fighting | 9 | 2 |
| Groups and plots | 5 | 1 |
| **Total** | **83** | **10 + realm actions** |

Paired actions (e.g. `buy` / `sell`) count as one. This list is long for a demo. We may want to cut or merge
some, or mark them as "AI only" or "player only".

## 5. Open questions

1. **Later:** which actions should be cut or merged for the Chapter 1 demo, and which are missing?
   Also: for each action, is it *direct*, *event only*, or *both* (§2.1)?
2. **Later:** Chapter 1's starting positions and their natural actions; the event system and which options
   traits open (decision 8).
3. **Dialogue (§2.4):** the threshold value and how rare the surprise option is. Tune these in playtesting.
