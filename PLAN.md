# Crowns of Ashvale — Game Guideline

> Working title. This is the vision and guideline document for the game.
> Sections marked **TBD** are to be designed step by step. Update this file whenever a decision changes.

## 1. Vision

**One life. From nobody to crowned ruler.**

You play **one person**, a young man or woman of common birth in a medieval-style fantasy world. You start with
nothing but a sword, a name and a few friends: a common soldier or a low-ranking officer. Over a single lifetime,
you rise. You might earn your place by loyal service to a lord, or seize it by gathering a band of followers and
taking land by force. Your first goal is to become a small lord with land of your own. Beyond that lie duchies,
crowns, and whatever you can hold before your time runs out.

**You play a person, not a dynasty. When your character dies, the game is over.**

The game blends two kinds of play:

- **A personal life story (Taikō Risshiden–style).** Jobs and missions, skills, rank and promotion,
  played at the scale of one person living in the world from the ground up.
- **Crusader Kings–style characters and realms.** Rich characters defined by **traits**, and a web of
  **personal relationships** (friends, rivals, lovers, mentors). Later you add realm play: land, vassals,
  intrigue and war.

The game is about the **journey between these two scales**, all within one mortal lifetime.

The game is **story-driven**. A written plot, told in **chapters**, is played out with **designed story
characters**, inside a living world of rule-driven, randomly generated people. Important characters, and anyone
the player gets to know, are brought to life by AI (see §6.3 and [AI_CHARACTERS.md](AI_CHARACTERS.md)).

## 2. Design pillars

1. **Rise from the bottom.** Every player starts as a commoner. Rank, land and titles are earned, never given.
2. **One life, one story.** You are a single person. Death ends the game, so health, danger and age matter.
   Every risk is real.
3. **Many roads up.** You can rise through loyal service or through outlaw ambition, and every path is valid.
   Each has its own risks, allies and enemies.
4. **Character is destiny.** Traits shape what you are good at, how others see you, and how AI characters behave.
   Relationships open and close doors.
5. **The world moves without you.** Lords wage war, die, rebel and scheme on their own.
   You find opportunities in that chaos.

## 3. Setting

- An original medieval-style fantasy continent with invented realms, peoples, names and lore.
- Light fantasy flavour, such as fey folk, rumours of dragons and old faiths. It sits on top of a grounded
  medieval society: lords, vassals, levies, castles, towns and villages.
- **TBD:** history, cultures, religions, the role of magic (if any), the major realms at game start.

## 3.1 Story & chapters

- The game follows a **written plot**, divided into **chapters**. Each chapter has its own setting,
  story characters and key events. Between story beats, the player is free to act in the living world.
- **Story characters** are designed by hand: personality, traits, backstory, secrets and goals.
  There is a limited number per chapter.
- **The plot is fully free.** There are no story locks: AI-played characters, and the player, may change the
  plot, even kill story characters early.
  - The story is written as situations, story roles and branches, so it reacts to whatever happens.
  - Chapter endings come from the state of the world.
  - See [AI_CHARACTERS.md §5.8](AI_CHARACTERS.md).
- **Chapter 1 (first demo):** a single local county facing an **enemy invasion**.
  - The story is centred on a **frontier town** near the border the enemy comes from.
    Townsfolk need food, tools and materials to live and work ([ITEMS.md §8](ITEMS.md)).
  - The player **chooses a starting position**: for example a soldier or low officer, or a more important
    position such as the mayor's secretary or the lord's bodyguard. More important positions come with rivals
    and dangers from the start. The full list is **TBD**.
  - The cast is small: about 8–12 story characters, the people the player meets, and a few dozen
    background characters.
  - **TBD:** the story outline, the cast list, possible endings of the chapter, and how the player's choices
    lead into Chapter 2.

## 4. The player's journey

| Stage | Who you are | What you do | How you move up |
|-------|-------------|-------------|-----------------|
| 1. Commoner | Soldier, militia member or low officer | Take orders, fight, do jobs, make friends | Merit, reputation, a patron's favour |
| 2. Officer / Retainer | Captain or knight in a lord's service | Lead a unit, carry out missions, join court politics | Promotion, being granted a fief |
| 3. Small Lord | Holder of a village, keep or county | Manage land, raise troops, deal with neighbours | Service rewards, marriage, conquest |
| 4. Great Lord | Duke or major vassal | Command vassals, intrigue at court | Wars, claims, usurpation, independence |
| 5. Ruler | King or queen of an independent realm | Rule and defend the realm | Expansion, and surviving to enjoy it |

### 4.1 Paths to land

- **The Path of Service:** serve a lord loyally, complete missions, win battles and gain rank.
  Ask for a fief as reward, or be granted one. Your rise is safer but bound by loyalty and your lord's fortunes.
- **The Path of the Band:** gather a group of fighters, outcasts or angry peasants. Live by raiding, mercenary
  work or protection money. Then seize a weakly held village or keep and declare yourself its lord.
  This path is faster and freer, but it makes enemies. Neighbours may see you as an outlaw until you are
  recognised, for example by swearing fealty, bribing, or winning.
- **Other paths (TBD):** for example marrying into a noble family, mercenary captaincy, a tournament champion
  rewarded with land, or a peasant uprising.

### 4.2 Death and the end of the game

- **When the player character dies, the game ends.** There is no playing on as an heir.
- **Causes of death:** old age, illness, wounds from battle or duels, murder plots, execution, accidents
  and events.
- **Lifespan sets the pace:** the whole journey must fit into one life, starting at about age 16. Ambition is
  a race against time, and good health is a valuable asset.
- **Ending screen (TBD):** a summary of the life lived. For example: highest rank and titles, lands held,
  battles won, friends and enemies made, and a short epitaph from your traits and deeds. Possibly a score.
- **Optional (TBD):** a "retire" ending, e.g. stepping down and passing your lands to a chosen heir as the
  final act of the game.
- **Family still exists** as relationships: a spouse, children, parents and siblings who can help, betray or
  be grieved. They are never playable.

## 5. Core loops

### Personal loop (Stages 1–2)
1. Go to the town, the camp, or your lord's court.
2. Take a job or mission, train, or meet people.
3. Carry it out: a fight, a task, or a social encounter.
4. Earn rewards: gold, skill, reputation, relationships, rank.
5. Use them to unlock better jobs, followers and opportunities.

### Realm loop (Stages 3–5)
1. Read the map: your land, your liege, your neighbours, your vassals.
2. Grow: develop land, forge claims, make alliances, recruit followers.
3. Fight: wars, battles, sieges, peace terms.
4. React: rebellions, plots, events, and threats to your own life.

**TBD:** how the two loops blend during the transition (Stage 2–3). For example, a small lord still takes
personal missions from their liege.

## 6. Systems overview

Each system below is a direction, not a final design. Details are **TBD** and will be designed one at a time.
The **trait** and **relationship** systems follow the Crusader Kings model.

### 6.1 Character & skills
- **Core skills:** Diplomacy, Martial, Stewardship, Intrigue, Learning (TBD: whether to add personal combat
  skills such as Prowess).
- Age and health. Health falls with age, wounds and disease, which raises the chance of death.
- **Reputation (TBD):** e.g. *Prestige/Honour* (respected, recognised) and *Notoriety/Dread* (feared, outlaw).
  Different paths build different kinds of reputation.

### 6.2 Traits (Crusader Kings–style)
Traits are the heart of every character, the player and every AI person alike.

- **Personality traits** (e.g. Brave/Craven, Honest/Deceitful, Ambitious/Content, Kind/Cruel, Generous/Greedy,
  Diligent/Lazy, Zealous/Cynical, Paranoid/Trusting, Gregarious/Shy):
  - Each modifies skills.
  - Opposite traits exclude each other.
  - Shared traits raise opinion between people; opposed traits lower it.
  - They drive AI behaviour, such as how likely someone is to scheme, rebel, betray or stay loyal.
- **Education traits:** set during youth or early training, e.g. Strategist, Schemer, Administrator,
  Diplomat, Scholar.
- **Lifestyle traits:** earned through how you live and what you do, e.g. Blademaster, Hunter, Commander,
  Duelist, Mystic, Brawler.
- **Health traits:** e.g. Wounded, Maimed, Ill, Scarred. These affect skills and how long you live.
- **Fame and infamy traits:** earned through deeds, e.g. Hero of a battle, Dragonslayer, Kinslayer,
  Oathbreaker, Bandit-born, Fey-touched.
- **Congenital traits (TBD):** e.g. Strong, Comely, Quick, Sickly. Possibly picked at character creation.
- **Gaining and losing traits:** through events, choices, training, injuries and repeated behaviour.
- **Stress (TBD):** acting against your own personality (e.g. a Kind character executing prisoners) builds
  stress, as in Crusader Kings. Too much stress causes breakdowns and new negative traits.

### 6.3 Relationships (Crusader Kings–style)
- **Opinion:** every character has an opinion of every other, from -100 to +100.
  It comes from traits, deeds, rank, gifts, grudges and favours, and the breakdown is visible.
  Temporary modifiers fade over time.
- **Personal relationships**, formed through events and repeated interaction:
  - **Friend / Best Friend:** strong positive opinion, support and help. Their loss is felt.
  - **Rival / Nemesis:** strong negative opinion, sabotage and plots.
  - **Lover / Soulmate:** romance, possibly secret and dangerous.
  - **Mentor / Student:** skill growth, a patron who opens doors.
  - **Patron / Protégé:** a powerful sponsor in a lord's service.
- **Family:** spouse, children, parents and siblings, linked by marriage and kinship. Kin can help, compete
  or betray.
- **Comrades and followers:** companions from your early days. They may become your officers and vassals.
- **Leverage (TBD):** something like Crusader Kings "hooks", i.e. favours owed and secrets known,
  used to force or persuade.
- **Secrets (TBD):** affairs, murders, crimes and outlaw pasts, which can be discovered and exposed.
- **Every character has their own personality:** their own traits, opinions and memories, which change
  through events over the game.
- **Character tiers:** every character runs on rules; some are also played by AI.
  Details and costs are in [AI_CHARACTERS.md](AI_CHARACTERS.md).

  | Tier | Who | Brain |
  |------|-----|-------|
  | 1. Story characters | Designed characters in the plot | Rules + **AI** |
  | 2. Encountered characters | Randomly generated characters the player has met | Rules + **AI** (capped number) |
  | 3. Background characters | Everyone else, randomly generated by the rules | Rules only |

- **Intents:** every character has a main ambition and a few current aims, born from their traits,
  background and memories. Examples: become famous, take revenge on someone, get rich, protect the family.
  Events create, change or end intents.
- **AI-played characters play like a human player.** They pursue their intents **in real time**, with the same
  actions, limits and knowledge as the player: working, trading, talking, plotting, competing, fighting.
  - The AI decides the **plan**, i.e. the next few **actions**. The player and all characters share one
    list of actions: [ACTIONS.md](ACTIONS.md). How ideas (plans) work: [IDEAS.md](IDEAS.md).
  - The rules carry the plan out moment to moment.
  - The AI only thinks again when the plan ends or fails, or something important happens.
  - Details are in [AI_CHARACTERS.md §5](AI_CHARACTERS.md).
- **The AI proposes, the game decides:** AI-played characters choose only from options the rules allow.
  The game always works without AI, falling back to rules and pre-written lines.
- **Dialogue is choice-based:** the player picks from a few options. The options available depend on the
  traits and backgrounds of the player and the other character. AI-played characters reply in their own voice.

### 6.4 Rank & service
- A ladder of ranks inside a lord's service, for example soldier → sergeant → captain → knight → retainer
  → landed vassal (TBD).
- Missions from your lord: patrols, escorts, collecting taxes, hunting bandits, diplomacy, spying, battles.
- Promotion is earned through merit and favour. Rivals may compete for the same promotion.

### 6.5 Band & followers
- A personal group of named companions plus nameless fighters.
- Upkeep: gold, food, morale. Followers leave if unpaid or unhappy.
- Activities: mercenary contracts, raiding, protection, seizing a keep or village.

### 6.6 Land & realm
- A province map with villages, keeps and towns (granularity TBD).
- A title ladder: Lordship/Barony (TBD) → County → Duchy → Kingdom.
- Income, troops, development, fortifications.
- Vassals and lieges, taxes, opinion, rebellion.

### 6.7 Intrigue & diplomacy
- Gifts, alliances, marriages, claims, plots (including murder), vassalization.
- **Plots go both ways:** others can plot against you, and since your death ends the game, intrigue is
  a constant threat.
- Events with choices, both personal (Stages 1–2) and realm-level (Stages 3–5).

### 6.8 Warfare & battle
War is a core system, so it has its own design document: [WARFARE.md](WARFARE.md) (**design in progress**).
In short:
- **Real-time battles on the same map** the player walks around on. The prototype is pure 2D; the final game is 2.5D.
- **The player is always one person:** a team leader, warrior, civilian staff or civilian, and later a lord
  with staff and guards. Death in battle means game over.
- **Every soldier is simulated**, with melee and ranged combat, wounds, morale, and equipment
  (weapons, armour, machines, items).
- **Command needs communication:** voice, flags and horns, messengers, plans prepared before the battle,
  and later the lord's **sand table**.
- **Chapter 1** ends with a small battle of about 200–300 men. This is the current focus.

### 6.9 World simulation
- AI characters live full lives: they age, marry, have children, scheme, fight and die.
  **Their titles pass to their heirs**; only the player has a single life.
- Opportunities for the player emerge from this, such as a lord dying without an heir, a weak border keep,
  a war that needs soldiers, or a widowed noble seeking a match.
- **Individual characters stay in the hundreds,** even when later chapters make the world larger. **Far places
  are group characters:** a whole town or village counts as one character, with its own traits, mood, needs and
  intents. See [AI_CHARACTERS.md §2.3](AI_CHARACTERS.md).

### 6.10 Items, materials & economy
Items have their own design document: [ITEMS.md](ITEMS.md) (**design in progress**). In short:
- **Categories:** animals (livestock, working and wild), crops and natural products, food and drink,
  handicrafts and tools, weapons, armour, minerals, currency and valuables, and event items such as a
  commission, a secret letter or a signet ring.
- **Every item has value, quality and durability.**
  - Value rises and falls as the story goes on, e.g. weapons and food get dearer when invasion threatens.
  - Durability falls with use and rises when the item is repaired.
- **Everyone has needs:** food to survive, tools to work, materials to make food and weapons.
  Needs drive what characters do.
- **Production chains:** e.g. wheat → flour → bread, and ore + coal → iron → sword.
- **Chapter 1** takes place in a frontier town with its own small economy, which the invasion disrupts.

## 7. Technical direction

- **Engine:** Godot 4.3+ (GDScript), PC first.
- Everything is built in code (one scene, interface from scripts) so it is easy to change through text.
- **Time:** the game runs in **real time**. In normal life, the basic time unit is **10 game minutes = 5 real
  seconds**. So 1 game day ≈ 12 real minutes, and 1 game month (Chapter 1) ≈ 6 real hours.
  - **TBD:** how time moves faster between chapters or in quiet times (time skips, a faster pace, fast-forward),
    since a whole life can't be played at this pace. See [AI_CHARACTERS.md §7](AI_CHARACTERS.md).
  - Dialogue and decision events pause the clock.
  - Battles run on their own finer **tactical time** ([WARFARE.md §5](WARFARE.md)).
- **View:** the prototype is pure top-down 2D. The final game is 2.5D (style TBD). Game logic is kept
  separate from drawing so the view can change.
- **AI characters:** called through a small server (or the player's own API key), never with a key stored
  in the game. All AI-written text is stored in the save file.
- **Testing:** a hidden `--autotest` mode where the AI plays the player's role too, to catch crashes
  and to tune the numbers.
- Proposed folder layout:
  ```
  project.godot
  scenes/main.tscn
  scripts/
    game.gd       # global game state and clock (registered globally as "Game")
    data/         # Character, Traits, Relationship, Item, Recipe, Title, Province, Army, War, Scheme, ...
    gen/          # name, map and world generation
    systems/      # traits, relationships, war, intrigue, AI, events, (later) career, band, missions
    ui/           # interface
  ```

## 8. Roadmap (draft)

Built step by step. Each milestone should end with something you can run and play.
The order and scope are **TBD**.

### Phase 1: Chapter 1 demo (one county, enemy invasion)

| # | Milestone | Focus |
|---|-----------|-------|
| D1 | County map | A small local map: villages, a keep, roads, the border the enemy comes from |
| D2 | Characters & rules | Traits, skills, backgrounds, opinion, relationships, memories, traits changing through events. Random character generation |
| D3 | Player & time | The player character, the real-time clock (10 game minutes = 5 real seconds), basic jobs and orders, death means game over |
| D4 | Items & town economy | Item types with value, quality and durability; needs (food, tools); inventory and equipment; repair; production chains and the frontier-town market ([ITEMS.md](ITEMS.md)) |
| D5 | Dialogue | Choice-based dialogue with options from traits and backgrounds, and hand-written fallback lines |
| D6 | Battle prototype | Pure 2D, real-time battle with 200–300 individual soldiers: squads, melee and ranged, wounds, morale, basic equipment, the player as one person in one of the roles ([WARFARE.md §4](WARFARE.md)) |
| D7 | Story & invasion | The Chapter 1 plot, story characters, the invasion event and its effect on prices and supplies, the skirmishes and the final battle |
| D8 | AI characters | AI-played story and encountered characters through a small server, with the cap and fallbacks |
| D9 | Demo polish | Chapter ending, save/load, basic art and UI (moving towards 2.5D), playtesting |

### Phase 2: Full game (draft)

| # | Milestone | Focus |
|---|-----------|-------|
| M1 | World map | The wider continent and its realms |
| M2 | Living world | AI lords, economy, wars, intrigue, aging, death and inheritance |
| M3 | Service path | Ranks, missions, promotion, being granted a fief |
| M4 | Band path | Followers, raiding and mercenary work, seizing land |
| M5 | Lordship | Playing as a landed lord: realm management, vassals, war; commanding through staff, messengers, signals and the sand table ([WARFARE.md §7](WARFARE.md)) |
| M6 | Later chapters | Further story chapters and characters |
| Later | Polish | Ending summary, art, sound, balance, more paths, traits and events |

## 9. Current status

- Draft code exists for the **realm layer**: the map generator, titles and rulers, the economy, a basic trait
  and opinion model, and the war system. It was written before this vision and **has not been run or tested**.
  It will be reused where it fits.
- **Needs changing:** the draft code continues play as an heir when the player dies. This must become
  **game over** for the player, while AI characters keep inheriting normally.
- The draft generates a whole continent. The Chapter 1 demo needs a small, local county map instead.
- The draft war system (`scripts/systems/war_system.gd`) moves abstract armies between provinces. It may
  later serve realm-scale war, but it does **not** fit the real-time, individual-soldier battle
  planned for Chapter 1, which will be new code (see [WARFARE.md §6](WARFARE.md)).
- The full trait and relationship systems, the player character, dialogue and the AI-character layer have not
  been started.

## 10. Open questions

1. How does time move faster between chapters or in quiet times, so a whole life fits (time skips, faster pace, fast-forward)?
2. How long should a typical journey take from soldier to small lord, in play time and in game years?
3. **Battle:** see the open questions in [WARFARE.md §8](WARFARE.md).
4. **Items & economy:** see the open questions in [ITEMS.md §10](ITEMS.md).
5. Map granularity for the demo: individual villages and keeps as locations?
6. Character creation: can the player choose traits, background and starting location?
7. Should there be a "retire" ending, or only death?
8. Should the game include stress (a mechanic from Crusader Kings) and secrets/leverage?
9. Chapter 1 story outline and cast list.
10. Is AI a core part of the demo or an on/off option, and who pays for AI calls?
11. Art direction for the demo.
