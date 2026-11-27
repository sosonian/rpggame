# Crowns of Ashvale: notes for Claude

This repository holds the **planning documents** for a game called *Crowns of Ashvale* (a working title).
It will be made in Godot 4 with GDScript. The project is in the **planning stage**: only the design documents
are tracked here. Draft code exists on the owner's laptop but is not in this repository.

## The game in one paragraph
You play one person in an original medieval-fantasy world, starting as a commoner or low officer and rising
towards being a ruler. It mixes Taikō Risshiden–style personal life with Crusader Kings–style traits and
relationships. **Death of the player means game over**, with no heirs. The game is story-driven and told in
chapters, and runs in real time. Important characters are played by AI. The first target is a **Chapter 1
demo**: a frontier town in one county, facing an enemy invasion.

## The documents

| File | Contents |
|---|---|
| [PLAN.md](PLAN.md) | Vision, pillars, systems overview, technical direction, roadmap, open questions. Start here |
| [AI_CHARACTERS.md](AI_CHARACTERS.md) | Character tiers, AI-played characters, intents, real-time play, costs |
| [ACTIONS.md](ACTIONS.md) | The shared list of actions, and dialogue options chosen by chance |
| [IDEAS.md](IDEAS.md) | Ideas (plans): how events spark them, how the AI writes them, ideas for the player |
| [EVENTS.md](EVENTS.md) | Events: where they come from, what they do, how they start ideas (first draft) |
| [WARFARE.md](WARFARE.md) | War and battle design (in progress) |
| [ITEMS.md](ITEMS.md) | Items, materials, production and the economy (in progress) |

Each design document starts with a **"Decisions so far"** table and ends with **open questions**.

## How to work on this project
- **Plan before coding.** Do not write game code until the owner approves a plan. The current work is design.
- **The owner designs the game step by step.** Record the owner's decisions; don't decide TBD items yourself.
  - Mark your own suggestions as **(proposal)**.
  - When the owner answers a question, add it to the document's decisions table with the date, update the
    text, and remove or update the open question.
- **Offer options honestly.** When asking the owner to choose, describe the trade-offs fairly. The owner
  often picks bolder options than the "safe" one.
- **Keep the documents consistent.** When something changes, update every document it touches, and the
  links between them (e.g. section numbers like `AI_CHARACTERS.md §5`).
- **Write plainly.** Use short sentences and simple words; the owner reads English as a second language.
  Explain game-design jargon the first time it appears.
- **Never put API keys or secrets in any file.**
- **After updating files, show a link to each changed file**, both the local file and the GitHub page
  (`https://github.com/sosonian/rpggame/blob/main/<file>`), so the owner can check them easily.

## Words used in the documents
The owner sometimes thinks of a term in Chinese. Use these English words:

| Chinese | English word in the documents | Meaning |
|---|---|---|
| 几率 | **chance** (probability) | How likely something is to happen |
| 刺激 | **stimulus** (plural: stimuli) | Something from outside that a character reacts to |
| 认知 | **perception** (not "recognition") | What one character believes about another, e.g. their traits |

