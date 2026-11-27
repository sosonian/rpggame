# Crowns of Ashvale — Maps & Places

> Plan document for **maps and places**: the map the player walks on, and the places in it.
> **Current focus: the frontier town of Chapter 1.**
> **Status: started.** This draft collects what the other documents already say about the map and the town.
> Items marked **(proposal)** are suggestions waiting for a decision.
> Related: [STORY.md §2](STORY.md) (Chapter 1), [ITEMS.md §8](ITEMS.md) (the town economy),
> [WARFARE.md §3–4](WARFARE.md) (battles on the same map), [EVENTS.md §1.7](EVENTS.md) (seeing and hearing
> by distance), [PLAN.md §8](PLAN.md) (roadmap item D1: county map).

## 0. Decisions so far

These decisions were made in other documents. They are collected here because they are about the map.

| # | Decision | Source | Date |
|---|----------|--------|------|
| 1 | **Chapter 1 is set in a frontier town** in one county, near the border the enemy comes from | [STORY.md](STORY.md) decision 3 | 2026-11-27 |
| 2 | **The prototype map is pure top-down 2D;** the final game is **2.5D** (style TBD). The rules are kept separate from the drawing | [WARFARE.md](WARFARE.md) decision 2 | 2026-11-22 |
| 3 | **Battles are fought on the same map** the player walks around on, with no separate battle screen | [WARFARE.md §2](WARFARE.md) | 2026-11-22 |
| 4 | **Seeing and hearing depend on distance in metres, walls and chance**, and facing matters for sight. So the map needs a **real scale** (metres) and **walls** | [EVENTS.md](EVENTS.md) decision 39 | 2026-11-27 |
| 5 | Everyone in town needs **food, tools and materials**; the town has its own small economy | [ITEMS.md](ITEMS.md) decision 2 | 2026-11-22 |
| 6 | The map gets **its own plan document** (this one) | Owner | 2026-11-27 |

## 1. What the map must do

From the other documents, the Chapter 1 map must support:

| Need | Why | Source |
|---|---|---|
| **Walking in real time** to places and people | The player and characters move with `go_to`, and click places and people | [ACTIONS.md §2.1](ACTIONS.md) |
| **Places with actions** (click the smithy → `buy`, `repair`…) | Most actions happen at a place | [ACTIONS.md §3](ACTIONS.md) |
| **Workplaces** for the economy | Bread, beer, tools and weapons are made in town | [ITEMS.md §5, §8](ITEMS.md) |
| **Distances in metres, walls, light** | Who sees and hears what | [EVENTS.md §1.7](EVENTS.md) |
| **Private and public spots** | Secrets, eavesdropping, crimes, hiding | [ACTIONS.md §3.6–3.7](ACTIONS.md) |
| **Terrain for battle**: walls, roads, rivers, fords, hills, forest | The final battle (200–300 men) and skirmishes | [WARFARE.md §3–4](WARFARE.md) |
| **The wild** around the town | Hunting, woodcutting, gathering, patrols, scouting | [ACTIONS.md §3.2, §3.5](ACTIONS.md) |
| **The border** and the way the enemy comes | The invasion | [STORY.md §2](STORY.md) |

## 2. Places already mentioned in the documents

None of these are decided as parts of the map yet. They are collected so we can choose.

| Group | Places | Mentioned in |
|---|---|---|
| **Work and economy** | Market (and a market day), smithy, mill, bakery, brewery, butcher, tannery, carpenter, weaver, farms around the walls, storehouse | [ITEMS.md §5, §8](ITEMS.md) |
| **Daily life** | Homes, the tavern / inn, a shrine | [ACTIONS.md §3.1](ACTIONS.md), [AI_CHARACTERS.md §5.3](AI_CHARACTERS.md) |
| **Power and defence** | The town walls, the garrison, the keep (the lord's small castle) | [ITEMS.md §8](ITEMS.md), [ACTIONS.md §3.5](ACTIONS.md), [WARFARE.md §4](WARFARE.md) |
| **Streets** | Tanner Street (from the false tax officer example) | [IDEAS.md §2](IDEAS.md) |
| **Outside the town** | The wild (forest, hunting grounds), a mine, a lumber camp, roads, a river with a ford or bridge, nearby villages, the border | [ITEMS.md §5, §8](ITEMS.md), [WARFARE.md §4](WARFARE.md), [PLAN.md §8](PLAN.md) |

## 3. Open questions

1. **The owner's ideas for the town map:** to be added.
2. **Size and scale:** how big is the town (how many people, how many metres across)? How long does it take to
   walk from one side to the other?
3. **One map or two?** Is there one map for the town and its surroundings, or a town map plus a small county
   map (with villages and the keep, [PLAN.md §8](PLAN.md) D1 and open question 5)?
4. **Layout:** walls or no walls? Where are the gate(s), the keep, the market, the river? Which way is the border?
5. **Buildings:** which places from §2 are in Chapter 1? Can characters go **inside** buildings?
6. **The battle:** where can the final battle happen (a ford, a bridge, the walls, the keep)?
7. **Made by hand or generated?** Is the Chapter 1 town drawn by hand, or made by the map generator
   ([PLAN.md §9](PLAN.md): draft code has a map generator)?
