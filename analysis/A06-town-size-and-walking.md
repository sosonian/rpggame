# A06 — The size of the town, and how long walking takes

> **Status:** Draft
> **Date:** 2026-11-27 (updated the same day with the owner's size decisions)
> **Asked by the owner:** "I would like to continue the design of the map of town. And we continue to plan the
> size of this town. I would like the number of the inhabitants is 100, and the soldier is also 100."
> **Related plan documents:** [MAP.md §1.1, open question 2](../MAP.md), [AI_CHARACTERS.md §7](../AI_CHARACTERS.md)
> (the time unit), [EVENTS.md §1.7](../EVENTS.md) (seeing and hearing ranges), [WARFARE.md §4](../WARFARE.md)

## 1. The question

The people are already decided: **about 100 inhabitants and about 100 soldiers** ([MAP.md](../MAP.md) decision 7).
Now:

1. **How big is the town in metres?** How many houses and buildings?
2. **How long does it take to walk across it,** in game time and in real time?

Question 2 turns out to be the hard one, because of the speed of the game clock (§2).

## 2. What we already know

- **The time unit:** 10 game minutes = 5 real seconds. So **game time runs 120 times faster than real time**
  (1 real second = 2 game minutes) ([AI_CHARACTERS.md §7](../AI_CHARACTERS.md)).
- **Battles use finer time steps** ([WARFARE.md §5](../WARFARE.md)), so in battle the clock is slower.
- **The map has a real scale in metres,** because seeing and hearing use metres: whisper 1 m, talk 3–5 m,
  see who it is 10–20 m, see that something happens 50–100 m ([EVENTS.md §1.7](../EVENTS.md)).
- **Characters walk in real time** on the map, with `go_to` ([ACTIONS.md §2.1](../ACTIONS.md)).
- A person walks at about **5 km/h = 1.4 metres per second** (real life).

## 3. How big is the town?

### 3.1 Buildings (proposal)

| Part | How many | Why |
|---|---|---|
| **Homes** | **30 households** (owner's decision, §8) | 100 inhabitants, so about 3–4 people per household |
| **Workshops** | 8–10 (smithy, bakery, brewery, butcher, tannery, carpenter, weaver, mill…) | [ITEMS.md §8](../ITEMS.md). Many craftsmen live in their workshop, so some homes and workshops are the same building |
| **Market square** | 1 | Market day |
| **Tavern / inn, shrine, storehouse** | 1 each | [ACTIONS.md §3.1](../ACTIONS.md) |
| **Garrison** for 100 soldiers | 2–4 barracks, a yard for training, stables, an armoury | 100 soldiers need beds, food and a place to train |
| **The keep** (the lord's small castle) | 1 | [WARFARE.md §4](../WARFARE.md) |
| **Town wall with 1–2 gates** | 1 | If the town has walls (MAP.md open question 4) |

About **50–55 buildings** in all.

### 3.2 Size in metres (owner's decision, §8)

| Area | Size |
|---|---|
| **The town** | **1 km × 1 km** (1 km², 100 hectares) |
| **The whole Chapter 1 map** (the town, fields, forest, river, roads, the border, room for the enemy camp) | **4 km × 4 km** (16 km²) |

The first draft proposed 150 m × 150 m for the town. The owner chose a much bigger town.

### 3.3 What a 1 km town means (notes for the owner)

- **The town is spread out.** Real medieval towns held about 100–200 people per hectare inside the walls, so
  200 people would fill about 2–3 hectares. A 1 km town has 100 hectares, so most of it is **not houses**: it is
  gardens, fields, orchards, pasture, yards and empty ground between the buildings.
- **Walls:** a wall around the whole 1 km square is **4 km long**. With 100 soldiers, that is **1 soldier every
  40 m**: too thin to defend. **Possible ways (proposals):**
  - **a small walled core** (keep, barracks, market, some houses) inside the 1 km town, with the rest open; or
  - **a wooden fence or ditch** around the whole town, and a stronger wall only around the keep; or
  - **no wall,** and the soldiers defend from the keep and chosen places (bridge, ford, streets).
  This is part of MAP.md open question 4 (walls or no walls).
- **Seeing and hearing:** with buildings far apart, most of the town is **out of sight and hearing** of most
  people (you see *that* something happens at 50–100 m). Good for secrets, crimes and hiding. Bad for alarms:
  a bell or horn (heard for hundreds of metres) becomes important.
- **Map size for the computer (note):** 4 km × 4 km with 1 m tiles is 16 million tiles; with 2 m tiles, 4 million.
  Godot can handle this if the map is split into **chunks** (pieces loaded as needed), but it needs care.

## 4. The walking problem

Because game time runs **120× faster** than real time, walking is either **very fast on screen**, or it **takes a
long time in game time**. It cannot be both natural on screen and realistic in game time.

| | Crossing the town (1 km) | Across the whole map (4 km) |
|---|---|---|
| **Real-life walking** (1.4 m/s) | 12 game minutes | 48 game minutes |
| …which on screen takes | **6 real seconds** | 24 real seconds |

So with realistic walking, a person crosses the whole town in **about 6 real seconds**. On screen they move at
about 170 m per second.

## 5. Options

### Option A: Realistic walking time (people move very fast on screen)
Walking takes the real-life game time. On screen, people zip across the town in a second.

| Good | Bad |
|---|---|
| **Realistic daily life.** A trip across town takes about 12 game minutes, so work and schedules make sense | **Hard to watch people move.** Following someone, sneaking up, or walking next to someone while talking is hard to see and control |
| **Simple and consistent** with the metre ranges | **Looks strange** if people are drawn walking |
| **The 1-month chapter stays full of activity,** not of walking | Battle (with slower time steps) looks very different from daily life |

### Option B: Natural walking on screen (walking takes a long time in game time)
People walk at a natural speed on screen (about 1.5–2 m per real second). The clock keeps running.

| Good | Bad |
|---|---|
| **Looks natural.** Easy to follow, sneak, eavesdrop and fight, the same in daily life and battle | **Walking eats the days.** Crossing the town (1 km) takes about 10 real minutes = **about 19 game hours**. Crossing the whole map (4 km) takes about **3 game days** |
| | Daily schedules (work, market, tavern) no longer fit into one day |
| | The 1-month chapter is mostly spent walking |

### Option C: A middle speed (proposal)
People move **fast but visibly** on screen, for example about **10 m per real second** (like the quick walking in
many top-down games). The game clock keeps running.

| | Crossing the town (1 km) | Across the whole map (4 km) |
|---|---|---|
| Real time | 100 seconds | 6.7 minutes |
| Game time | 3.3 hours | 13 hours |

| Good | Bad |
|---|---|
| **You can still see and follow people** | **With a 1 km town, too slow:** crossing the town takes 3.3 game hours, so only one or two trips fit in a day |
| | Trips outside the town (to the forest, the border) take most of a game day, so they need **a faster travel mode** |
| Battle can use the same speed, with the finer time steps | |

### Option D: Two modes of walking
- **Walking you watch** (following, sneaking, battle, the player controlling his character directly): natural
  speed on screen.
- **Travelling with `go_to`** to a place (click the smithy, go): the character moves very fast on screen, and
  the game time is the realistic walking time, as in option A.

| Good | Bad |
|---|---|
| **Both realistic and watchable** where each one matters | **More complex:** two speeds, and the game must decide which one is used |
| Fits the "click a place to go there" control of [ACTIONS.md](../ACTIONS.md) | Two characters moving at different speeds near each other can look odd |

## 6. Recommendation (proposal)

- **Size:** decided by the owner (§8).
- **Walking:** with a **1 km town and a 4 km map**, **option D** (two modes) now looks best. Option C was
  suggested for the first, small town; at 1 km it is too slow (3.3 game hours to cross the town).
  With option D, clicking a place uses realistic time (12 game minutes across town, 6 real seconds), and
  following, sneaking and fighting use a natural speed.
- **Another possible way** (not an option here, because it changes a decided rule): slow the game clock while
  characters walk. This would change the time unit, which is already decided.

## 7. Questions for the owner

1. ~~Size~~: decided (§8).
2. Which **walking option**: A, B, C or D?
3. ~~Walls~~: decided: a walled core, plus a market area (§8).
5. **Necessary parts** of the random map: market, barracks, and what else?
4. ~~One map or two~~: decided: one 4 km × 4 km map for Chapter 1 (§8).

## 8. The owner's decision (filled in when Final)

**Decided so far (2026-11-27), while the report is still a Draft:**
- **The town is 1 km × 1 km.**
- **The whole Chapter 1 map is 4 km × 4 km.**
- **The town has 30 households** (for about 100 inhabitants).
- **The town has a walled core,** and **also a market area** (§3.3; where the market is, inside or outside
  the walled core, is to be confirmed).
- **The map is generated randomly,** but some **necessary parts must always be generated**: the **market** and
  the **barracks**, and more to be listed by the owner (MAP.md open question 7).
- Still open: the walking option (§5), and the full list of necessary parts. The plan documents will be updated
  when the report is Final.

## 9. Changes made to the plan documents (filled in when Final)
