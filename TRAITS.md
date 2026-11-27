# Crowns of Ashvale — Traits

> Plan document for **traits**: the qualities that make up every character's personality, body and history.
> **Status: started. Traits are developed one by one in discussion.**
> Only traits the owner has agreed are in the main table (§2). Traits that other documents mention but that are
> not defined yet are listed as **candidates** (§3).
> Related: [PLAN.md §6.2](PLAN.md) (overview), [AI_CHARACTERS.md §3](AI_CHARACTERS.md) (character data),
> [EVENTS.md §1.6](EVENTS.md) (traits and daily-life events), [ACTIONS.md §2.4](ACTIONS.md) (traits and dialogue
> chances), [analysis/A02](analysis/A02-who-is-affected.md) Part 2 (seeing and hearing).

## 0. Decisions so far

| # | Decision | Source | Date |
|---|----------|--------|------|
| 1 | Traits get **their own plan document** (this one), with a **table of all traits** | Owner | 2026-11-27 |
| 2 | **Chapter 1 traits are developed one by one** in discussion | Owner | 2026-11-27 |
| 3 | **Observant** means a character has **more chance to understand** the information about things, or **the logic behind them**. Its opposite is **Oblivious** | [A02 §10.1](analysis/A02-who-is-affected.md), [EVENTS.md](EVENTS.md) decision 18 | 2026-11-27 |
| 4 | **Hawk Eye** (see further and in more detail) and **Fox Ear** (hear further and in more detail), with opposites **Poor Sight** and **Hard of Hearing** | [A02 §10.1](analysis/A02-who-is-affected.md) | 2026-11-27 |
| 5 | **Good Memory** (memories fade **more slowly**) and its opposite **Forgetful** (memories fade **faster**) | Owner | 2026-11-27 |
| 6 | **Temporary traits, labelled "Emotion":** some traits can be **removed after a short time**. Examples from the owner: **angry, afraid / fear** (§2.2) | Owner | 2026-11-27 |
| 7 | **A second group of temporary traits, labelled "Body status":** **Hot, Cold, Hungry, Thirsty** (§2.3). Cold and Hot moved here from Emotion | Owner | 2026-11-27 |

## 1. What every trait defines

The same properties for every trait, so they can be compared and built the same way:

| Property | Meaning |
|---|---|
| **Name** | e.g. *Hawk Eye* |
| **Group** | Personality, senses and mind, body and health, education, lifestyle, fame (see [PLAN.md §6.2](PLAN.md)), and two groups of **temporary traits**: **Emotion** (§2.2) and **Body status** (§2.3) |
| **Opposite** | The trait it excludes, if any (a character can't have both) |
| **Effects** | What it changes: ranges, chances of events, dialogue option chances, skills, opinions of others |
| **How it is gained** | Born with, learned by practice, given by an event |
| **How it is lost** | Age, wounds, events, acting against it for a long time |
| **Can it be hidden?** | Whether others can be wrong about it ([EVENTS.md §8](EVENTS.md): hiding and seeing through) |

## 2. Defined traits

### 2.1 Senses and mind

| Trait | Opposite | Effects | Gained | Lost |
|---|---|---|---|---|
| **Hawk Eye** | Poor Sight | Sees **further** (about **1.5×** the sight ranges) and in **more detail**. Very useful in battle: archers, scouts, lookouts, spotting ambushes | Mostly **born with**; also by long practice (e.g. hunter, scout) | Old age; wounds |
| **Poor Sight** | Hawk Eye | Sees **less far** and less detail | Born with; old age; wounds | — |
| **Fox Ear** | Hard of Hearing | Hears **further** (about **1.5×** the hearing ranges) and in **more detail**. Very useful in battle: sentries, especially at night; spotting ambushes and sneaking enemies | Mostly **born with**; also by long practice | Old age; wounds (e.g. a blow to the head) |
| **Hard of Hearing** | Fox Ear | Hears **less far** and less detail | Born with; old age; wounds | — |
| **Observant** | Oblivious | More chance to **understand** what is seen and heard: the information about things and **the logic behind them**. Gets daily-life events more often, and helps see through people who hide their true personality. Does **not** make sight or hearing longer | TBD | TBD |
| **Oblivious** | Observant | Rarely understands what is going on; gets fewer daily-life events | TBD | TBD |
| **Good Memory** | Forgetful | Memories **fade more slowly** ([MEMORIES.md §3](MEMORIES.md)) | TBD | TBD |
| **Forgetful** | Good Memory | Memories **fade faster** | TBD (proposal: also old age) | TBD |

The ranges these traits change are in [EVENTS.md §1.7](EVENTS.md) (full analysis in
[analysis/A02 Part 2](analysis/A02-who-is-affected.md)).

### 2.2 Emotions (temporary traits, decision 6)

Most traits last a long time. **Emotions** are traits that come and **go away after a short time**.
They are labelled **Emotion** so the game (and the player) can tell them apart from lasting traits.

**The owner's examples:** **Angry**, **Afraid** (fear). (Cold and Hot are now **Body status**, §2.3.)

**Proposals (not decided):**

| Emotion | Possible causes | Possible effects | Goes away when |
|---|---|---|---|
| **Angry** | Insulted, cheated, hurt; a major event such as betrayal ([EVENTS.md §2](EVENTS.md)) | More chance of rough dialogue options (insult, threaten, `attack`, `challenge`); worse at persuading and at hiding feelings | Time passes; revenge; an apology; `relax` |
| **Afraid** | Danger, threats, a battle, wounds, a dark omen | More chance to `flee`, obey, give in or lie; less chance to fight; Brave characters resist it, Craven ones get it more easily | The danger is gone; time passes; comfort from a friend; `pray` |

**Ideas to decide later (proposals):**
- **Strength:** an emotion could be **weak or strong** (e.g. *a bit angry* / *furious*), and fade step by step.
- **How long:** e.g. minutes to a few game hours for Angry; until the cause is gone for Cold and Hot.
- **Lasting traits change emotions:** e.g. a Vengeful character stays Angry longer; a Brave one is Afraid less.
- **Emotions can become lasting traits:** e.g. being Afraid very often in battle may turn a character Craven
  (like [EVENTS.md §2](EVENTS.md), where events add or remove traits).
- **Others can see emotions** with seeing and hearing ([EVENTS.md §1.7](EVENTS.md)), and some characters can
  **hide** them (Deceitful), like true personality ([EVENTS.md §8](EVENTS.md)).
- **More emotions:** e.g. Sad (grief), Happy, Ashamed, Jealous.

### 2.3 Body status (temporary traits, decision 7)

**Body status** traits are also temporary. They describe how the **body** feels, not the mind. They are labelled
**Body status**, apart from Emotion.

**The owner's list:** **Hot**, **Cold**, **Hungry**, **Thirsty**.

**Proposals (not decided):**

| Body status | Possible causes | Possible effects | Goes away when |
|---|---|---|---|
| **Hot** | Summer sun, heavy armour, hard work | Tires faster; more chance to make mistakes | Rest in the shade, water, taking off armour |
| **Cold** | Winter, rain, night outside, poor clothing ([ITEMS.md](ITEMS.md)) | Works and fights a little worse; more chance to fall ill if it lasts long | Warm clothes, a fire, going inside |
| **Hungry** | Time without food; a siege; poverty ([ITEMS.md §7](ITEMS.md): needs) | Works worse; easier to make Angry; may steal, beg or leave town ([ITEMS.md](ITEMS.md)) | Eating |
| **Thirsty** | Time without water; heat; hard work or battle | Tires faster; worse than hunger if it lasts long | Drinking water or beer |

**Ideas to decide later (proposals):**
- **Strength:** like emotions, e.g. *Hungry* → *Starving*; *Cold* → *Freezing*. A strong status that lasts long
  can wound or kill (e.g. starving in a siege).
- **Body status can cause emotions:** e.g. Hungry makes a character Angry more easily.
- **More body status:** e.g. Tired, Drunk, In Pain.

## 3. Candidates (mentioned in the documents, not defined yet)

These names appear in the documents as examples. Each still needs its effects, gains and losses decided.

| Group | Candidates | Where mentioned |
|---|---|---|
| **Personality pairs** | Brave / Craven · Honest / Deceitful · Ambitious / Content · Kind / Cruel · Generous / Greedy · Diligent / Lazy · Zealous / Cynical · Paranoid / Trusting · Gregarious / Shy | [PLAN.md §6.2](PLAN.md) |
| **Other personality** | Vengeful · Cautious · Patient · Fair | [EVENTS.md](EVENTS.md) §1.2, §7.3 |
| **Education** | Strategist · Schemer · Administrator · Diplomat · Scholar | [PLAN.md §6.2](PLAN.md) |
| **Lifestyle** | Blademaster · Hunter · Commander · Duelist · Mystic · Brawler · Blacksmith | [PLAN.md §6.2](PLAN.md), [ITEMS.md §5](ITEMS.md) |
| **Body and health** | Wounded · Maimed · Scarred · Ill · Strong · Comely · Quick · Sickly | [PLAN.md §6.2](PLAN.md) |
| **Fame and infamy** | Hero of a battle · Dragonslayer · Kinslayer · Oathbreaker · Bandit-born · Fey-touched · Swindler | [PLAN.md §6.2](PLAN.md), [IDEAS.md](IDEAS.md) |

**A clash to fix:** *Cynical* is used in two ways. [PLAN.md §6.2](PLAN.md) makes it the opposite of *Zealous*
(little faith). [EVENTS.md §1.2](EVENTS.md) uses it for "expects the worst of people". These should become two
different traits (proposal: keep **Cynical** as the opposite of Zealous, and use another name, e.g. **Bitter**, for
expecting the worst).

## 4. Open questions

1. Which candidates from §3 are needed for Chapter 1? Which should be defined first?
2. **Observant / Oblivious:** how are they gained and lost?
3. How should the *Cynical* clash in §3 be solved?
4. Are the groups in §1 right (personality, senses and mind, body and health, education, lifestyle, fame, emotion)?
5. **Emotions (§2.2):** are *Afraid* and *Fear* one emotion? (*Cold* and *Hot* are Body status: decision 7.)
6. **Emotions and body status (§2.2, §2.3):** which proposals are accepted: strength levels, how long they last, links to lasting
   traits, and the list of other emotions?
7. **Emotions and mood:** [AI_CHARACTERS.md](AI_CHARACTERS.md) mentions **mood** (e.g. a group's mood: angry
   about high taxes) and [PLAN.md](PLAN.md) mentions **stress**. Are emotions the same thing as mood, or
   separate?
