# A06 — The size of the town, and how long walking takes

> **Status:** Draft
> **Date:** 2026-11-27
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
| **Homes** | 20–25 houses | 100 inhabitants, 4–5 people per family |
| **Workshops** | 8–10 (smithy, bakery, brewery, butcher, tannery, carpenter, weaver, mill…) | [ITEMS.md §8](../ITEMS.md). Many craftsmen live in their workshop, so some homes and workshops are the same building |
| **Market square** | 1 | Market day |
| **Tavern / inn, shrine, storehouse** | 1 each | [ACTIONS.md §3.1](../ACTIONS.md) |
| **Garrison** for 100 soldiers | 2–4 barracks, a yard for training, stables, an armoury | 100 soldiers need beds, food and a place to train |
| **The keep** (the lord's small castle) | 1 | [WARFARE.md §4](../WARFARE.md) |
| **Town wall with 1–2 gates** | 1 | If the town has walls (MAP.md open question 4) |

About **40–50 buildings** in all.

### 3.2 Size in metres (proposal)

Real medieval towns held very roughly **100–200 people per hectare** (1 hectare = 100 m × 100 m) inside the
walls. With about 200 people, plus the keep, barracks and the market:

| Area | Size (proposal) |
|---|---|
| **Inside the walls** | about **150 m × 150 m** (2–3 hectares) |
| **Fields and farms around the walls** | out to about **500 m** from the wall |
| **The wider map** (forest, river and ford, roads, the border road, room for the enemy camp) | about **2 km × 2 km** |

This fits the earlier proposal in MAP.md (150–250 m across). At this size, from the market you can **see that
something happens** in most of the town (50–100 m), but you see **who** it is only in your own street (10–20 m).
So walls and houses matter a lot for secrets and eavesdropping. That is good for the game.

## 4. The walking problem

Because game time runs **120× faster** than real time, walking is either **very fast on screen**, or it **takes a
long time in game time**. It cannot be both natural on screen and realistic in game time.

| | Crossing the town (150 m) | Fields to the wall (500 m) | Across the wider map (2 km) |
|---|---|---|---|
| **Real-life walking** (1.4 m/s) | 2 game minutes | 6 game minutes | 24 game minutes |
| …which on screen takes | **1 real second** | 3 real seconds | 12 real seconds |

So with realistic walking, a person crosses the whole town in **about 1 real second**. On screen they move at
about 170 m per second.

## 5. Options

### Option A: Realistic walking time (people move very fast on screen)
Walking takes the real-life game time. On screen, people zip across the town in a second.

| Good | Bad |
|---|---|
| **Realistic daily life.** A trip to the market takes a few game minutes, so work and schedules make sense | **Hard to watch people move.** Following someone, sneaking up, or walking next to someone while talking is hard to see and control |
| **Simple and consistent** with the metre ranges | **Looks strange** if people are drawn walking |
| **The 1-month chapter stays full of activity,** not of walking | Battle (with slower time steps) looks very different from daily life |

### Option B: Natural walking on screen (walking takes a long time in game time)
People walk at a natural speed on screen (about 1.5–2 m per real second). The clock keeps running.

| Good | Bad |
|---|---|
| **Looks natural.** Easy to follow, sneak, eavesdrop and fight, the same in daily life and battle | **Walking eats the day.** Crossing the town (150 m) takes about 1.5 real minutes = **about 3 game hours**. A trip to the fields and back takes most of a day |
| | Daily schedules (work, market, tavern) no longer fit into one day |
| | The 1-month chapter is mostly spent walking |

### Option C: A middle speed (proposal)
People move **fast but visibly** on screen, for example about **10 m per real second** (like the quick walking in
many top-down games). The game clock keeps running.

| | Crossing the town (150 m) | Fields to the wall (500 m) | Across the wider map (2 km) |
|---|---|---|---|
| Real time | 15 seconds | 50 seconds | 3.5 minutes |
| Game time | 30 minutes | 1.7 hours | 7 hours |

| Good | Bad |
|---|---|
| **You can still see and follow people** | Not realistic: crossing a small town takes half a game hour |
| **Daily life mostly fits:** a few trips in town per day | Long trips outside (to the forest, the border) take most of a day, so they need **travel by a faster mode** (see below) |
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

- **Size:** use §3: about **40–50 buildings**, **150 m × 150 m inside the walls**, fields out to **500 m**, and a
  wider map of about **2 km × 2 km**.
- **Walking:** **option C** (one middle speed) is the simplest that still looks and plays well. **Option D**
  is better if realistic daily schedules matter a lot. Either way, long trips outside the town (2 km) probably
  need a faster travel mode.
- **Another possible way** (not an option here, because it changes a decided rule): slow the game clock while
  characters walk. This would change the time unit, which is already decided.

## 7. Questions for the owner

1. Do you agree with the **size** in §3 (150 m × 150 m inside the walls, about 40–50 buildings)?
2. Which **walking option**: A, B, C or D?
3. Should the **wider map** (2 km × 2 km, with the forest, river and border) be part of the same map, or a
   separate map (MAP.md open question 3)?

## 8. The owner's decision (filled in when Final)

## 9. Changes made to the plan documents (filled in when Final)
