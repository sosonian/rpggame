# A05 — Storing faded memories: mark, don't delete

> **Status:** Draft
> **Date:** 2026-11-27
> **Asked by the owner:** "The memory fade does not delete this memory from the storage, but marks which part is
> faded, or that all parts of this memory are faded. But I am concerned about the disk storage and performance
> problem. Could you analyse the mark-but-not-delete solution?"
> **Related plan documents:** [MEMORIES.md](../MEMORIES.md), [A04](A04-event-check-performance.md)

## 1. The question
If faded memories are **marked** instead of deleted, the storage keeps growing. Is that a problem for
**disk space** (save files) and **performance** (speed and memory use while playing)? How can it be done well?

## 2. What we already know
- One storage holds everything a character knows (MEMORIES.md decision 9).
- Details fade first (decision 10); recalling refreshes a memory (decision 11); the fading check happens
  **at night** (decision 12).
- Individual characters stay **in the hundreds**; far places are group characters (AI_CHARACTERS.md decision 14).
- Chapter 1 lasts about **1 game month ≈ 6 real hours**.
- **Only a few AI-played characters pass on to the next chapter** (AI_CHARACTERS.md decision 15, 2026-11-27).

## 3. How big could it get? (rough estimate)

The numbers below are guesses to show the size of the problem, not exact figures.

**Assumptions:** 500 individual characters; each one stores about **20–100 memories per game day** (most of them
small: "a cart passed at noon"); Chapter 1 lasts 30 game days.

| | Low | High |
|---|---|---|
| Memories per character in Chapter 1 | 600 | 3,000 |
| **Memories for everyone in Chapter 1** | **300,000** | **1,500,000** |

**Size of one memory:**

| How a memory is stored | Size each | Chapter 1, high case (1.5 million) |
|---|---|---|
| A. As full text and fields (what, where, who, details written out) | about 500 bytes | about **750 MB** |
| B. As compact data (numbers and codes, no text) | about 100 bytes | about **150 MB** |
| C. As a **link to a shared event** plus a few marks (§5) | about 20–30 bytes | about **40 MB** |

**For the whole game** (many chapters), if nothing is ever removed, the storage keeps growing: several chapters
in option A could reach many gigabytes. That is too much for save files and for the computer's working memory.

**Update: only a few characters pass on to the next chapter** (AI_CHARACTERS.md decision 15). So most memories
**do not** carry over: each chapter starts with a mostly new cast and a mostly empty storage. Only the player and
the few characters who pass on bring their memories along. **The storage therefore does not grow from chapter
to chapter;** the size of one chapter is what matters.

**Conclusion: "mark, don't delete" is possible, but only if memories are stored compactly.** Stored naively, it
would cause problems.

## 4. Options

| Option | How it works | Good | Bad |
|---|---|---|---|
| **1. Delete when fully faded** | A memory is removed when every part has faded | Smallest storage | The memory can never come back; the owner doesn't want this |
| **2. Mark, keep everything as it is** | Faded parts are marked; nothing is ever removed or made smaller | Simple; any memory can come back | Storage grows without limit, especially with text (§3, option A) |
| **3. Mark + store compactly + shrink old memories** | See §5 | Keeps the owner's idea; storage stays small; fast | More work to build; storage still grows slowly |
| **4. Option 3 + delete unimportant memories once fully faded** (owner's idea, 2026-11-27) | Like option 3, but a **not important** memory is **deleted** when **all its details** have faded. Important memories are kept and marked | Much smaller storage; it stops growing; simpler than shrinking everything | An unimportant memory can never come back once deleted (§6.1) |

## 5. Option 3 in detail (recommended)

### 5.1 Store each event once, shared by everyone who knows it
Most memories are about **the same events**: thirty people in the market all saw the same brawl. Instead of 30
copies of the full story:
- The world keeps **one event record**: what happened, where, when, who was involved, and all the details.
- Each character's memory is a **small link** to that record, plus their own marks:
  - which details **they** learned (each detail is one on/off mark)
  - which details have **faded** (one on/off mark each)
  - how they learned it, how sure they are, importance, strength, when last refreshed

So "mark which part is faded" costs **one tiny mark per detail**, a fraction of a byte.

### 5.2 Compute fading when it is needed, at night (proposal)
A nightly loop over every memory of every character (up to 1.5 million) could cause a short freeze each night.
Two ways to avoid it:
- **Store when the memory was last refreshed** and how fast it fades (from importance and traits). The strength
  is calculated **only when someone looks at it**: when the player opens the memory inventory, when the AI is
  told the character's memories, or when the rules need it. The result counts **nights** passed, so it still
  follows decision 12 (fading happens at night).
- **Skip memories that are already fully faded.** They don't change any more, so they cost nothing per night.

### 5.3 Shrink old faded memories (proposal)
After a long time, a fully faded memory keeps only its **skeleton**: the link to the event, and the mark
"faded". Text and per-detail marks can be dropped, because they are all faded anyway. The event record itself
can be removed when **nobody** remembers it any more and it has no story importance (proposal).

### 5.4 Not everything needs to be stored (proposal)
- **Background characters** (rules only) store only what the rules need: e.g. important and ordinary memories,
  not every passing cart.
- **Group characters** keep one shared memory for the group.
- **At the end of a chapter**, very small memories that faded long ago can be merged into a summary
  ("days 3–9: ordinary market days").

### 5.5 Keep old memories out of the way
- **AI calls:** the AI is told only memories that are **still clear and relevant**, so faded memories add
  nothing to AI cost.
- **Working memory:** faded skeletons from earlier chapters can be kept in the save file and loaded only when
  needed (e.g. when something reminds the character of them).
- **Save files** can be compressed; compact data compresses well.

### 5.6 Option 4: delete unimportant memories once fully faded (owner's idea)

**The rule:** when a **not important** memory has faded completely (all its details are marked faded), its
record is **deleted**. **Important** memories are never deleted; they stay marked as in option 3.

**What counts as "not important"** (proposal): the **small** and **ordinary** memories in
[MEMORIES.md §3](../MEMORIES.md) (e.g. "a cart passed at noon", "Hobb owes me 2 silver"). **Important** and
**life-changing** memories are kept.

**What it costs: storage.** Most memories are small or ordinary; a rough guess is **85–90%**. They fade within
hours to weeks, so they don't pile up: each character only holds the recent ones.

| | Option 3 (keep all, compact) | **Option 4 (delete unimportant)** |
|---|---|---|
| Memories held per character at one time | Grows all chapter: up to 3,000 | Roughly **a few hundred** recent ones, plus the important ones |
| Chapter 1, everyone | about 40 MB | about **5–15 MB** |
| Over many chapters | Mostly reset each chapter (only a few characters pass on) | Mostly reset each chapter; the few who pass on keep only their important memories |

**What it costs: speed.** Deleting is very cheap. The game can even know **in advance** on which night a
memory will be fully faded (from its importance and the character's traits), and put it in that night's list.
That night, the list is deleted in one go; if the memory was refreshed by `recall` in the meantime, it simply
moves to a later night's list. There is no need to search through all memories.

**What it costs: the game.** This is the real trade-off:
- **A deleted memory is gone for good.** A reminder can't bring it back; the character would learn it as new.
- **Something small can turn out to matter later.** Example: a cart passed at noon, a small memory, and it
  faded. A week later it turns out the killer escaped in that cart. Nobody remembers it any more. This is
  **realistic**, and it can make good stories ("if only someone had remembered").
- **A softer version (proposal):** if an event becomes important later, the memories of it that **still exist**
  are raised to important, so they stop fading towards deletion. Memories already deleted stay deleted.
- **The world's event record** (§5.1) is deleted when nobody remembers the event and it has no story
  importance. While anyone still remembers it, it stays.

## 6. Can a faded memory come back?
Keeping faded memories is useful only if they can **come back**. Proposals:
- **Reminders:** someone tells you about it, or you return to the place where it happened. A faded memory comes
  back more easily than learning it fresh.
- **Recall with help:** `recall` alone can't bring back a fully faded memory, but an event or a conversation can.
- **A memory that comes back may be less sure**, or slightly wrong.

## 7. Recommendation
**Option 4** (the owner's idea, built on option 3): store compactly, mark fading, **keep important memories**,
and **delete unimportant ones once fully faded**. It is cheaper and simpler than keeping everything, and losing
small memories is realistic.

Option 3 alone, for comparison: **mark, don't delete, but store compactly.**
- One shared **event record** per event; each character keeps only a small link and marks (§5.1).
- Fading is **calculated when needed**, counting nights (§5.2).
- Old, fully faded memories shrink to a **skeleton** (§5.3).
- Background and group characters store less (§5.4).

With option 3, Chapter 1 needs roughly **tens of megabytes** at most; with option 4, **about 5–15 MB**. Both
keep the game fast.

## 8. Questions for the owner
1. Option 3 or **option 4** (delete unimportant memories once fully faded)?
1b. If option 4: do **small and ordinary** memories count as "not important" (§5.6)? Should the softer version
    apply (memories of an event that later becomes important are raised to important)?
2. Can a faded memory **come back** (§6)? If yes, how: reminders, places, conversations?
3. Is **calculating fading when needed** (counting nights) acceptable, instead of a real nightly loop (§5.2)?
4. Should **background characters** store fewer kinds of memory (§5.4)?
5. Should very small, long-faded memories be **merged into summaries** at the end of a chapter (§5.4)?

## 9. The owner's decision
*(to be filled in when Final)*

## 10. Changes made to the plan documents
*(to be filled in when Final; nothing has changed yet)*
