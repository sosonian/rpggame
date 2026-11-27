# Crowns of Ashvale — Warfare & Battle System

> Design document for war and battle. **Status: design in progress.**
> The current focus is **Chapter 1** (§4). Later-chapter command (§7) is a direction only.
> Sections marked **TBD** are still to be decided. Items marked **(proposal)** are suggestions waiting for a decision.
> The overview is in [PLAN.md §6.8](PLAN.md).

## 1. Decisions so far

| # | Decision | Date |
|---|----------|------|
| 1 | Battles run in **real time** | 2026-11-22 |
| 2 | **2D map** for the prototype (pure top-down); the final game is **2.5D** | 2026-11-22 |
| 3 | Chapter 1 ends with a **small battle of about 200–300 men** | 2026-11-22 |
| 4 | The player is **one person** in battle: a team leader, a warrior, civilian staff, or a civilian | 2026-11-22 |
| 5 | **Melee and ranged** attacks; characters can equip **weapons, armour, machines and other items** | 2026-11-22 |
| 6 | Later, as a lord, the player is still **an individual on the same map**, with staff and guards around them, and commands other units **through messengers** | 2026-11-22 |
| 7 | Later, a lord has a **sand table** for command, but orders still need **messengers, flags or a plan prepared before the battle** | 2026-11-22 |
| 8 | **Chapter 1 only** for now | 2026-11-22 |

## 2. Core principles

1. **Real time, same map.** Battles are fought on the map the player walks around on, with no separate battle screen.
2. **You are always one person.** The player controls one character who moves, fights, hides or flees as an
   individual, even as a lord. Death in battle means game over.
3. **Command needs communication.** Nobody controls troops directly. Orders spread by voice, flags, horns,
   messengers, or a plan agreed beforehand. Distance, delay and confusion are part of the game.
4. **Every soldier is simulated.** Each person on the field is an individual with their own skills, traits,
   equipment, health and morale, grouped into squads and units.
5. **Morale wins battles.** Most battles end when one side breaks and runs, not when everyone is dead.
6. **Your role decides your battle.** The same battle feels different for a warrior in the line, a squad
   leader, a camp clerk or a villager caught in the middle.

## 3. View: 2D first, 2.5D later

- **Prototype:** pure top-down 2D with simple shapes or sprites, to test the rules, the soldier AI and performance.
- **Final:** 2.5D, e.g. an isometric or angled view with height and depth. The exact style is **TBD**.
- **The rules are kept separate from the drawing.** Battle logic works on positions and numbers only.
  The view just draws them, so moving from 2D to 2.5D does not mean rewriting the rules.
- **Terrain that matters (proposal):** hills (range and morale bonus), forests (cover, broken formations),
  rivers and fords (choke points), walls and buildings (cover, defence), roads (faster movement).

## 4. Chapter 1 battle (current focus)

### 4.1 Scale and setting
- **The final battle of Chapter 1:** about **200–300 men in total** on both sides.
- **Location TBD:** e.g. a ford, a village, a bridge, or the walls of the keep.
- **Smaller fights before it** use the same system: skirmishes, raids, ambushes, bandit fights.
- **Forces TBD:** who is on each side (lord's men, militia, mercenaries, the invaders) and what kinds of troops.

### 4.2 The player's role
The role is set by the player's story and choices earlier in the chapter.

| Role | Example jobs in battle | What the player can do |
|------|------------------------|------------------------|
| Team leader | Leads a squad of about 5–15 men | Fight; give simple orders to their own squad by voice (follow, hold, charge, fall back); carry out orders from above |
| Warrior | A soldier in a squad | Fight; follow, ignore or desert the squad's orders |
| Civilian staff | Clerk, quartermaster, surgeon's helper, messenger, cook | Supply, carry messages, treat the wounded, repair; fight only if needed |
| Civilian | Villager or townsfolk | Hide, flee, protect family, help one side, loot |

- **Consequences:** what you do in battle is seen by others. Holding the line, fleeing, saving a comrade,
  or looting all change fame, opinion and traits.
- **TBD:** the exact list of roles and jobs. Also whether the player can change role during the battle,
  e.g. a warrior taking over when the squad leader falls.

### 4.3 Units and command structure (Chapter 1)
- **Squad:** about 5–15 soldiers with a leader. This is the basic group that moves and fights together.
- **Company / unit (proposal):** a few squads under a captain. The captain is often a story character.
- **Commander:** the lord or captain leading the side. Gives orders before and during the battle.
- **Orders in Chapter 1 (proposal):** mostly **voice** (short range) and a few **horn or flag signals**
  (advance, hold, retreat). The full messenger system is for later chapters, but a player in the messenger
  job already carries orders by hand.

### 4.4 Combat
- **Melee:** swords, spears, axes, clubs, shields.
  - Facing, reach and formation matter. **TBD** how much: from simple ("attack the nearest enemy") to
    detailed (blocking, flanking, shield walls).
- **Ranged:** bows, crossbows, slings, javelins and thrown weapons.
  - Ammunition is limited.
  - Range and accuracy depend on the weapon, skill, and whether the archer is moving.
  - Shots can hit your own side in a crowded melee.
- **Wounds:**
  - Hits cause injuries: light, serious, crippling, deadly.
  - Wounds slow you down and lower your skill.
  - After the battle they can become lasting health traits (Wounded, Maimed, Scarred).
  - Downed soldiers may survive, be captured, or be finished off.
- **Morale:**
  - Things that lower it: fear, losses, a leader falling, being flanked, arrows from an enemy you can't reach.
  - Things that raise it: a leader nearby, a winning fight, defending your home.
  - Traits matter: Brave holds longer, Craven breaks sooner.
  - A squad with low morale wavers, then retreats, then routs.
- **Fatigue (TBD):** running, fighting and heavy armour tire soldiers out. Tired soldiers fight worse.

### 4.5 Equipment and items
- **Weapons:** damage, reach, speed, and whether they are good against armour.
- **Armour:** protection, weight, movement speed, fatigue. **TBD** whether armour comes as pieces
  (helmet, body, shield) or full sets.
- **Machines:** e.g. a small ballista, a battering ram, carts, stakes and barricades.
  Which ones fit a county-scale battle is **TBD**.
- **Other items:** e.g. bandages, torches, horns and flags, food, ropes, horses
  (**TBD** whether mounted combat is in the demo).
- **Where equipment comes from:** the player's gold, their lord, loot, and story events.

### 4.6 Who thinks during battle
- **Soldiers run on rules** (battle AI): move with the squad, pick targets, keep formation,
  react to morale. This is cheap and runs every moment.
- **AI-played characters** (see [AI_CHARACTERS.md](AI_CHARACTERS.md)) are **not called every moment**.
  At most, they are called at key moments, such as a story character deciding whether to retreat,
  or a short exchange of words with the player. **TBD.**
- Their traits still matter through the rules, e.g. a Brave captain charges, an Ambitious one seeks glory.

### 4.7 After the battle
- Result: victory, defeat, or a draw. The story continues differently for each.
- The dead and wounded, including named and story characters.
- Who saw what the player did, with fame and opinion changes and new traits.
- Loot, prisoners and ransom.
- Memories: characters remember the battle, which can unlock dialogue options later.

## 5. Battle time

- The world clock uses a **10-minute basic unit** ([PLAN.md §7](PLAN.md)). A battle needs a much finer pace,
  so it runs on its own **tactical time**, e.g. close to real time for the fighting itself.
- **TBD:**
  - how long a battle lasts in real minutes (proposal for Chapter 1: about 10–20 minutes)
  - how much world time passes during it
  - whether the player can pause or slow the battle. Pausing may not fit the "one person" feel;
    a short slow-motion moment might.

## 6. Technical notes (proposal)

- **Performance:** 200–300 individual soldiers is easily manageable in Godot 4. Each soldier updates a few
  times per second, not every frame. Squads plan, soldiers follow.
- **Battle logic in plain data:** positions, health, morale and orders live in data objects. The 2D or 2.5D
  view only reads and draws them.
- **Testable on its own:** a headless test can run a whole battle without drawing, so the balance can be
  tuned quickly. It can also be repeated with the same random seed.
- **Orders as objects:** every order (who sent it, to whom, content, when sent, how it travels) is a data
  object. In Chapter 1 most orders travel by voice. Later, the same objects are carried by messengers or
  signals (§7), so the system grows without being rewritten.
- **Existing draft code:** `scripts/systems/war_system.gd` moves abstract armies between regions of a map.
  It may later serve realm-scale war (§7.4), but the Chapter 1 battle needs new code.

## 7. Later chapters: commanding as a lord (direction only)

### 7.1 The lord on the field
- The player is still one person on the same map, surrounded by their **staff and guards**: bodyguards,
  messengers, a standard-bearer, advisors.
- **Leading from the front:** fighting in person raises morale and brings prestige, but risks injury or death,
  which ends the game.

### 7.2 Ways to command

| Method | Speed | Limits |
|--------|-------|--------|
| Voice | Instant | Only nearby units |
| Flags, banners, horns | Fast | A small set of signals; must be seen or heard; can be misread |
| Messengers | Slow (they must ride or run) | Can be lost, killed or captured; orders may arrive too late |
| Battle plan | Prepared before the battle | Fixed orders and conditions, e.g. "if the left flank breaks, the reserve advances" |

### 7.3 The sand table
- A planning and command view, like a table map in the lord's tent.
- It shows what the lord **knows** from scouts and messengers. That information may be late or wrong.
- Orders given here still travel by messenger or signal. They are not instant.
- Used before the battle to make the plan, and during it to follow reports and send new orders.
- **TBD:** how it is shown (a separate screen or an overlay), what it shows, and how it is used during battle.

### 7.4 Realm-scale war
- Armies move across the world map, with sieges, occupation, war score, peace and truces.
- When armies meet, the battle is fought on the local map with the battle system above.
- **Reasons for war (TBD):** claims, de jure titles (lands a title rightfully includes), independence,
  and outlaw land grabs.

## 8. Open questions

1. How does the player control their character in battle: mouse, keyboard, or both?
2. How deadly is battle for the player? Can they be knocked down and rescued or captured instead of dying outright?
3. How detailed is melee: facing, formations, blocking and dodging, or simpler?
4. Which equipment, machines and items are in the Chapter 1 battle? Horses or not?
5. Can the player pause or slow time in battle?
6. How long does the final battle last in real minutes?
7. Where is the final battle fought, and what are the two sides' forces?
8. Can the player change role during a battle, e.g. take over a fallen leader's squad?
9. Do duels between named characters use the same system, or a special one?
10. How do civilian roles play: real-time actions, short choice events, or both?
