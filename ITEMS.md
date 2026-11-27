# Crowns of Ashvale — Items & Materials System

> Design document for items, materials, animals, production and trade. **Status: design in progress.**
> The current focus is **Chapter 1** (§8).
> Sections marked **TBD** are still to be decided. Items marked **(proposal)** are suggestions waiting for a decision.
> The overview is in [PLAN.md §6.10](PLAN.md). Combat stats of weapons and armour are designed together with
> [WARFARE.md](WARFARE.md).

## 1. Decisions so far

| # | Decision | Date |
|---|----------|------|
| 1 | The world has many kinds of materials and items: animals, crops, food, handicrafts, weapons, armour, minerals, currency and event items (§3) | 2026-11-22 |
| 2 | **Chapter 1** takes place in a **frontier town**. Everyone in town needs **food** to survive, **tools** to gather resources or farm, and **materials** to make food or weapons | 2026-11-22 |
| 3 | A weapon or armour is useful for **hunting or patrolling** in the wild, and needed in the **final battle** if you are a soldier | 2026-11-22 |
| 4 | Every item has **value**, **quality** and **durability** (§4) | 2026-11-22 |
| 5 | **Value changes as the story goes on**, rising or falling (§6) | 2026-11-22 |
| 6 | **Durability falls when an item is used, and rises when it is repaired** (§4.3) | 2026-11-22 |

## 2. Core principles

1. **Everyone needs things.** Every character, the player and every AI person alike, needs food to live and
   tools to work. Needs drive what people do, buy, sell and steal.
2. **Things are made from things.** Most items come from production chains: grain becomes flour becomes bread;
   ore and coal become iron become a sword (§5).
3. **Everything wears out.** Tools, weapons and armour lose durability as they are used and must be repaired
   or replaced. Food spoils (proposal).
4. **The story moves the market.** War, siege, famine or a good harvest change what things are worth (§6).
5. **Items tell stories.** Some items are tied to the plot (§3.9): a secret letter can start a conspiracy;
   a signet ring can prove who you are.

## 3. Item categories

The names below are examples, not the final list.

### 3.1 Livestock and animals
Animals are **living things**, not just items: they need food and care, can get sick or die, and can breed
(proposal). What they produce is an item.

| Animal | Kind | Uses and products |
|--------|------|-------------------|
| Cow | Livestock | Milk, beef, leather, pulling ploughs and carts |
| Horse | Livestock | Riding, carrying, pulling carts, war horses; very valuable |
| Sheep | Livestock | Wool, mutton, sheepskin |
| Pig | Livestock | Pork, lard |
| Chicken | Livestock | Eggs, meat, feathers |
| Dog | Working animal | Herding, hunting, guarding, companionship |
| Pigeon | Working animal | Carrying messages (links to messengers in [WARFARE.md](WARFARE.md)) |
| Eagle (or hawk) | Working animal | Hunting (falconry), a noble's status symbol |
| Wolf | Wild animal | A danger to livestock and travellers; hunted for pelts |
| Bear | Wild animal | Very dangerous; hunted for pelts, meat and fame |

- **TBD:** whether wild animals can be tamed, e.g. a wolf pup raised as a hound.

### 3.2 Agricultural and natural products
- **Crops:** wheat, barley, oats, vegetables, flax (for linen), hops (for beer).
- **Trees and wood:** logs, planks, firewood, charcoal.
- **Fruit:** apples, pears, berries, grapes (for wine).
- **Wild products (proposal):** herbs (for medicine), mushrooms, honey, reeds.

### 3.3 Food and drink
- **Food:** bread, porridge, steak and other meat, cheese, eggs, fish, stew, dried or salted meat.
- **Drink:** clean water, milk, beer, ale, wine, mead.
- **Feed (proposal):** hay and grain for animals.
- **Spoilage (proposal):** fresh food spoils over time. Salted, dried and smoked food keeps much longer,
  which matters during a siege.

### 3.4 Handicrafts and tools
- **Cloth and clothing:** wool, linen, cloth, clothing, cloaks, boots.
- **Tools for daily life:** e.g. axe (woodcutting), pickaxe, hoe, plough, sickle, scythe, hammer, saw,
  fishing net, cooking pot, bucket, rope, needle.
- **Building materials (proposal):** planks, bricks, nails, thatch.
- **Some tools double as weapons:** a woodcutter's axe, a pitchfork, a hunting knife.

### 3.5 Weapons
- **Melee:** knife, dagger, axe, sword, spear, mace, club, pitchfork.
- **Ranged:** bow, crossbow, sling, javelin.
- **Ammunition:** arrows, bolts, sling stones. Ammunition is used up or lost.
- **Combat stats** (damage, reach, speed, use against armour) are designed in [WARFARE.md](WARFARE.md).

### 3.6 Armour
- **Light:** padded cloth (gambeson), leather armour.
- **Medium and heavy:** chainmail, scale, metal plate pieces.
- **Head and shield:** helmets, shields of wood or metal.
- **TBD:** whether armour is worn as pieces (head, body, shield) or full sets. This is also open in
  [WARFARE.md](WARFARE.md).

### 3.7 Minerals and raw materials
- **Stone:** for building and walls.
- **Coal:** fuel for smithing and smelting.
- **Iron ore:** smelted into iron, then steel (proposal).
- **Copper and tin:** smelted together into **bronze**. Bronze is an alloy, so it is a made material,
  not something mined.
- **Asphalt and oil:** e.g. tar for ships and roofs, lamp oil, fire weapons. **TBD** how common they are.
- **Precious metals and gems:** gold, silver, gems, for coins and jewellery.
- **Salt (proposal):** important for preserving food.

### 3.8 Currency and valuables
- **Coins:** gold, silver and bronze coins.
  - Proposed exchange rate: **1 gold = 10 silver = 100 bronze**.
  - Bronze is for daily life, silver for trade, gold for lords.
  - **TBD:** whether exchange rates change.
- **Jewellery and valuables:** rings, necklaces, gems, silverware. These are easy to carry and hide, good for
  bribes, and can be stolen.
- **Barter (proposal):** in a poor frontier town, people often trade goods directly instead of using coin.

### 3.9 Event items
Items tied to the story and quests:
- **Commission:** a written appointment to an officer's rank. It proves your rank and gives authority.
- **Secret letter:** can reveal plots and be used as leverage. It is dangerous to carry.
- **Signet ring:** proves identity or authority and can seal letters. Forged or stolen rings are possible.
- **Other examples:** a map, a key, a seal, a writ of pardon, a holy relic, the enemy's battle plans.

Rules for event items:
- They usually **cannot be bought**.
- They may be worth a lot to the right person, and nothing to others.
- Some are **secret**: being caught with them has consequences.
- Story characters (including AI-played ones) react to them.

## 4. Item properties

Every item has at least these properties:

| Property | Meaning |
|----------|---------|
| **Type** | What the item is, e.g. "iron sword" |
| **Category** | Which category in §3 it belongs to |
| **Value** | What it is worth, in coin (§4.1, §6) |
| **Quality** | How well it is made (§4.2) |
| **Durability** | How worn it is (§4.3) |
| **Weight (proposal)** | How heavy it is to carry |
| **Stack (proposal)** | Whether many can be held as one entry, e.g. 20 arrows or 5 loaves |
| **Owner** | Who owns it. Theft and looting move it between owners |
| **Freshness (proposal)** | For food only: how long until it spoils |

### 4.1 Value
- Each item type has a **base value**.
- The **actual price** depends on:
  - quality
  - durability
  - where you are (town or village, near or far from where it is made)
  - the story situation (§6)
  - who you are dealing with: traits, opinion and skills (proposal)

### 4.2 Quality
- **Proposed quality levels:** Poor, Common, Good, Fine, Masterwork.
- Higher quality means better stats (damage, protection, efficiency of a tool), higher value,
  and often higher maximum durability.
- **Quality depends on the maker's skill** and the materials used (proposal).

### 4.3 Durability
- Each item has a **current durability** and a **maximum durability**.
- **Using an item lowers durability:**
  - fighting with a weapon or being hit wearing armour
  - working with a tool
  - riding a horse hard (proposal: animals have health instead of durability)
- **Low durability makes an item worse:** a dull sword cuts badly, a cracked shield may break.
  At **zero** the item is **broken** and cannot be used until repaired.
- **Repairs raise durability:**
  - by a craftsman (blacksmith, leatherworker, tailor) for coin, or by yourself with the right skill and tools
  - repairs need materials, e.g. iron for a sword, leather for armour
- **Proposal:** each repair slightly lowers maximum durability, so items eventually wear out for good.
  Masterwork items could be exceptions.
- **Food and consumables** are used up instead of wearing out.

## 5. Production chains

Making things takes **materials, tools, a workplace, skill and time**. Examples:

| Product | Chain |
|---------|-------|
| Bread | Wheat (farm, hoe/plough/sickle) → flour (mill) → bread (bakery, oven, firewood) |
| Beer | Barley + hops + water → beer (brewery) |
| Steak | Cow (farm) → beef (butcher, knife) → steak (kitchen, fire) |
| Leather armour | Cow hide → leather (tannery) → leather armour (leatherworker) |
| Iron sword | Iron ore (mine, pickaxe) + coal → iron (smelter) → sword (blacksmith, hammer, anvil) |
| Bow and arrows | Wood (axe) → bow (bowyer); wood + feathers + iron → arrows (fletcher) |
| Cloth | Sheep → wool (shears) → yarn → cloth (weaver) → clothing (tailor) |

- **Workplaces (proposal):** farm, mill, bakery, brewery, butcher, tannery, smithy, carpenter, weaver,
  mine, lumber camp.
- **Who works there:** town characters with jobs. Background characters run on rules; the player may take
  such jobs as part of the personal loop.
- **Skills (TBD):** whether crafting needs new skills (e.g. Smithing, Farming, Cooking) besides the five core
  skills in [PLAN.md §6.1](PLAN.md), or uses traits instead (e.g. a "Blacksmith" lifestyle trait).

## 6. Value and the story

Prices change through **supply and demand**, and the story moves both.

| Story situation | Example price changes |
|-----------------|-----------------------|
| Rumours of invasion | Weapons, armour and horses rise; land and houses fall |
| Siege or blockade | Food and firewood rise sharply; luxuries fall |
| Good harvest | Grain and bread fall |
| Bandits on the road | Goods from outside rise; travel becomes dangerous |
| After the battle | Loot floods the market, so second-hand weapons fall; the wounded need medicine |
| A lord's wedding or feast | Wine, meat and fine cloth rise |

- **Event items** change value through the story, e.g. a secret letter becomes priceless once the plot it
  reveals matters, and worthless after.
- **Proposal:** prices update once per basic time unit (10 real minutes), with big story events causing
  instant jumps.

## 7. Needs, inventory and trade

### 7.1 Needs
- **Food and drink:** every character must eat and drink. Hunger and thirst lower health, skill and mood,
  and in the end can kill. This matters for the player, since death means game over.
- **How often:** depends on what the 10-minute time unit means in game time, which is still open
  ([PLAN.md §10](PLAN.md)).
- **Warmth and shelter (proposal):** clothing, firewood and a roof, especially in winter.
- **Tools:** a farmer without a hoe or a woodcutter without an axe cannot work, so they earn nothing and
  may go hungry.
- **Needs drive behaviour:** hungry characters may steal, beg, leave town or join bandits. This feeds the
  rule-based behaviour in [AI_CHARACTERS.md](AI_CHARACTERS.md).

### 7.2 Inventory
- **Proposal:**
  - The player carries a limited inventory, limited by weight.
  - Items can also be kept at home, in a storehouse, or on a horse or cart.
  - Equipped items (weapon, armour, clothing) are shown in separate slots.
- Stolen goods, secret items and contraband can be hidden, and found by searches.

### 7.3 Trade
- **Buy and sell** at shops, the market, and with travelling merchants.
- **Barter** with anyone, using the dialogue system ([PLAN.md §6.3](PLAN.md)).
- **Haggling (proposal):** traits, skills (e.g. Diplomacy, Stewardship) and opinion change the price.
- **Other ways to get items:** wages, rewards from your lord, gifts, hunting, gathering, crafting, looting,
  theft.

## 8. Chapter 1: the frontier town

- **Setting:** a frontier town in the county, near the border the enemy comes from
  ([PLAN.md §3.1](PLAN.md)).
- **Town economy (proposal):** a small, mostly self-sufficient town:
  - farms around the walls
  - a mill, a bakery and a tavern (beer)
  - a smithy, a few craftsmen, and a market day
  - hunting and woodcutting in the wild
  - occasional merchants
- **The player's needs:** earn enough to eat, get tools for a job, and get a weapon and armour. These are
  needed for hunting and patrols in the wild, and for the final battle if you are a soldier.
- **The invasion changes the town:**
  - Before: normal life and prices.
  - As rumours spread: weapons and food rise, people hoard, some flee.
  - During the battle: supplies run short, and the smithy works day and night.
  - After: loot, losses and rebuilding.
- **Demo item list (TBD):** a short list of about 30–50 item types for Chapter 1, rather than everything
  in §3.

## 9. Technical notes (proposal)

- **Item types in data files:** each item type (name, category, base value, weight, max durability, stats) is
  defined in a data file, not in code, so new items can be added easily.
- **Item instances:** each actual item in the world stores its type, quality, current durability, owner,
  and freshness if it is food. Stackable goods (grain, arrows, coins) are stored as type plus amount.
- **Recipes in data files:** production chains (§5) are recipes: inputs, tools, workplace, skill, time and outputs.
- **Market:** a simple supply-and-demand price per item type per location, with story modifiers.
- **Save files:** all items and their states are stored in the save.

## 10. Open questions

1. What is the final list of item types for the Chapter 1 demo?
2. How detailed are needs: food and drink only, or also warmth, rest and shelter?
3. How often must characters eat? This depends on the time unit ([PLAN.md §10](PLAN.md)).
4. Does food spoil?
5. Is inventory limited by weight, by slots, or not at all?
6. Does crafting use new skills (Smithing, Farming, …) or traits?
7. Can the player craft personally, or only buy, sell and order from craftsmen?
8. Exchange rates between coins: fixed or changing?
9. How simulated are animals: living creatures that eat and breed, or simple items?
10. How deep is the town economy: does every background character produce and consume, or is it a
    simpler market model?
11. Do repairs lower maximum durability over time?
