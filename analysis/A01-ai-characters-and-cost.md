# A01 — AI-played characters: approaches and cost

> **Status:** Final
> **Date:** 2026-11-20 (updated 2026-11-24 for real-time play, and 2026-11-27 for the 6-hour Chapter 1)
> **Asked by the owner:** "If we use AI to play other characters, please analyse the possibility and the cost."
> **Related plan documents:** [AI_CHARACTERS.md](../AI_CHARACTERS.md)

Prices are Anthropic Claude API list prices as of November 2026. They change over time; re-check before
deciding anything that depends on them.

## 1. The question
Can AI language models play the characters of the game, and what would it cost?

## 2. What we already know
- Every character has traits, opinions, relationships and memories (Crusader Kings–style).
- The game runs in real time. 1 time unit = 10 game minutes = 5 real seconds; Chapter 1 lasts about
  **1 game month ≈ 6 real hours**.
- AI-played characters have intents and play like a human player, in real time, everywhere
  ([AI_CHARACTERS.md §5](../AI_CHARACTERS.md)).

## 3. Options

| Approach | Description |
|---|---|
| A. Rules only | Crusader Kings–style rules drive every character |
| B. AI plays every character | Every character is played by an AI model |
| C. Hybrid | Rules for everyone; AI also plays the important characters (story characters and those the player meets) |
| D. Local AI model | A small AI model runs on the player's own PC |

## 4. Analysis

### 4.1 Approaches

| Approach | Good | Bad |
|---|---|---|
| A. Rules only | Free, fast, reliable, works offline | Characters feel less alive; dialogue is limited to written lines |
| B. AI for everyone | Every character feels alive | Far too expensive (500+ characters in real time) and too slow |
| C. Hybrid | Rich characters where the player looks; cheap everywhere else | Two systems to build (rules and AI); needs a cap on the AI cast |
| D. Local model | No running cost, works offline | Weaker quality, heavy download, needs a strong PC |

### 4.2 Chapter 1 demo: estimated cast

| Group | Examples | Count | Brain |
|---|---|---|---|
| Story characters | The county lord, the lord's heir or daughter, the player's captain, a mentor, a rival soldier, a friend, the priest or elder, a merchant or spy, the enemy commander, an enemy scout or traitor | ~8–12 | AI |
| Encountered characters | Soldiers in the player's unit, villagers the player helps, refugees, deserters | up to ~15 (cap) | AI once met |
| Background characters | Other soldiers, villagers, enemy officers | ~50–100 | Rules |

The demo's AI cast is about **20–27 characters**.

### 4.3 Estimated AI calls per real hour of play

| Call type | Per hour (estimate) | Notes |
|---|---|---|
| Planning and re-planning | ~520 | ~25 characters × about 3–4 per 10 real minutes, wherever they are |
| Important decisions | ~60 | Only when a decision is pending |
| AI-to-AI exchanges | ~60 | |
| Dialogue exchanges with the player | ~40 | e.g. ~10 conversations × 3–4 exchanges |
| Event text, profile and memory updates | ~30 | |
| **Total** | **~700** | Before real-time play it was ~130 |

### 4.4 Estimated cost

Assumptions per call: about 3,000 cached tokens (rules and world), 1,500 uncached tokens (profile, memories,
situation), 300 output tokens.

| Model | Input | Cached input | Output |
|---|---|---|---|
| Claude Haiku 5.5 (`claude-haiku-5-5`) | $0.10 / MTok | ≈ $0.01 (assumed ~10%) | $0.50 / MTok |
| Claude Sonnet 5.5 (`claude-sonnet-5-5`) | $2.00 | $0.10 | $10.00 |
| Claude Opus 5.5 (`claude-opus-5-5`) | $4.00 | $0.20 | $20.00 |

(MTok = million tokens; a token is about ¾ of an English word.)

| Setup | Cost per call | Per real hour | **Chapter 1 (~6 real hours)** |
|---|---|---|---|
| Haiku 5.5 for everything | ≈ $0.0003 | ≈ $0.23 | **≈ $1.40** |
| Sonnet 5.5 for everything | ≈ $0.0063 | ≈ $4.40 | **≈ $26** |
| Opus 5.5 for everything | ≈ $0.013 | ≈ $8.80 | **≈ $53** |
| **Mix:** Sonnet for dialogue with the player, Haiku for the rest | — | ≈ $0.47 | **≈ $2.80** |

- **Update 2026-11-27:** earlier versions assumed a 2-hour demo (≈ $0.95 with the mix). Chapter 1 now lasts
  about 6 real hours, so the cost per playthrough is about **3× higher**. The cost per hour has not changed.
- Thinking (the model reasoning before answering) can make outputs 1.5–3× longer. Use low effort for planning.
- **Ways to lower cost:** skip the regular review when nothing has changed; let the rules handle obvious
  re-plans; group characters for far places ([A04](A04-event-check-performance.md)).
- **Development and testing** would likely cost a few tens of dollars; `--autotest` runs can use the cheapest model.

### 4.5 Full game
With the tier system the AI cast stays at about 25–35 characters, so costs stay about **$0.25–$6 per real hour**
depending on the model, or about **$0.50 per hour with the mix**. A 40-hour playthrough would cost about
**$20 with the mix**.

## 5. Recommendation
Approach **C, the hybrid**, with the **mix** of models.

## 6. The owner's decision
- **2026-11-20:** rules for every character; AI for important ones (story characters and characters the player
  has met), with a cap. This is approach C.
- **2026-11-24:** AI-played characters have intents and play in real time, everywhere.
- Who pays for AI calls is still open ([AI_CHARACTERS.md §12](../AI_CHARACTERS.md)).

## 7. Changes made to the plan documents
- [AI_CHARACTERS.md](../AI_CHARACTERS.md): decisions 1–3, 7, 8 and 11; the tier system (§2); the cap (§6);
  a cost summary (§8–§10) that links to this report.
