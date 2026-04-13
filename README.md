# The Lost Citadel — Shadowdark RPG Adventure System

**A complete, modular framework for running The Lost Citadel with Claude as Dungeon Master.**

---

## What Is This?

This is a fully-playable **Shadowdark RPG dungeon adventure** designed to run with Claude as your DM.

### Source & Credits

The core Shadowdark RPG rules and DM guidelines in this repo are converted from the free **Shadowdark RPG Quickstart Set** PDFs provided by **The Arcane Library**:
[https://www.thearcanelibrary.com/products/shadowdark-rpg-quickstart-set-pdf](https://www.thearcanelibrary.com/products/shadowdark-rpg-quickstart-set-pdf)

These materials have been reformatted to Markdown for easy reference during play.

### What's Included

This repo includes:

- **27 explorable rooms** in an interconnected citadel
- **3 factions** with distinct goals (Beastmen, Ettercaps, Scarlet Minotaur)
- **4 pre-built player characters** (Fighter, Priest, Thief, Wizard)
- **Complete DM system** with encounter tables, NPC generators, combat rules
- **Torch & light mechanics** for time pressure & resource management
- **Game tracking** so you can run multiple campaigns in parallel

**Play solo or with friends. Run from Mac, iPhone, or web.** Claude handles the dungeon.

---

## Quick Start (5 Minutes)

1. **Pick characters** from `lost-citadel/rules/characters.md`
2. **Create game folder** `lost-citadel/games/game-NNN-YYYY-MM-DD/` (copy state.md template)
3. **Open in Claude Code** (or Claude iPhone app)
4. **Load these files in the conversation:**
   - `lost-citadel/rules/dm-system-prompt.md` ← How to run the game
   - `lost-citadel/rules/rooms.md` ← What the citadel looks like
   - `lost-citadel/rules/encounters.md` ← Creature stats
   - Your game's `state.md` ← Current location, HP, torch timer
5. **Start playing** — Ask Claude to describe the citadel entrance. Then: "What do you do?"

---

## How to Play

### Setup (First Time)

- **Pick 1-4 characters** from `lost-citadel/rules/characters.md`
- **Create game folder:** `lost-citadel/games/game-001-2026-04-12/` (use today's date)
- **Copy template state.md** (example in `lost-citadel/games/index.md`)
- **Create `log/` folder** with empty `session-001.md`

### During Play

**Each turn:**
1. **Describe** the room (Claude references `rooms.md`)
2. **Ask** "What do you do?"
3. **Listen** to player actions
4. **Call checks** (d20 + mod vs. DC 9/12/15)
5. **Resolve consequences** with narration
6. **Update state.md:** location, HP, torch timer
7. **Roll for encounters** every 2 rounds (1d6, on 1 = encounter)

**References (keep open):**
- Current room from `rooms.md`
- `state.md` (your game state)
- `encounters.md` (creature stats for combat)
- `npcs.md` (NPC details)

### After Each Session

Write a summary in `log/session-NNN.md`:
- What rooms you explored
- Combat that happened
- Loot acquired
- NPCs encountered
- Notes for next session

---

## The Adventure

### Setting

**The Lost Citadel** is a sprawling underground fortress, partially flooded and overrun by competing factions. You're a party of adventurers seeking treasure and glory in its depths.

### What's Inside

- **27 interconnected areas** (rooms, corridors, caverns, treasure chambers)
- **Secret doors** that reward careful searching
- **Torch timer** (6 rounds per torch = constant time pressure)
- **Random encounters** (every 2 rounds of exploring)

### Map

![The Lost Citadel — Keyed Map](Core%20Rules/keyed-map.png)

*27 areas, interconnected layout. Reference this during play to plan routes and understand the citadel's geography.*

### The Factions

**Beastmen** — Led by Rogath, they want the Scarlet Minotaur dead so they can rule the citadel.

**Ettercaps** — Leaderless spiders. Greedy. Want treasure. Will trade or fight depending on mood.

**Scarlet Minotaur** — An unstoppable beast roaming the citadel. Gets easier to find the longer players stay (cumulative -2 penalty after first encounter).

### Victory

Multiple endings based on your choices:
- Defeat the Minotaur
- Ally with Beastmen to defeat Minotaur
- Flee with treasure
- Solve the citadel's mysteries

---

## Files at a Glance

### Rules & References

| File | Purpose |
|------|---------|
| `rules/characters.md` | 4 pre-built player characters (Fighter, Priest, Thief, Wizard) |
| `rules/rooms.md` | All 27 areas with descriptions, treasures, secrets, connections |
| `rules/encounters.md` | Random encounter table + creature stat blocks |
| `rules/npcs.md` | Named NPCs + personality profiles + generators |
| `rules/dm-system-prompt.md` | Complete DM guide (reference during play) |

### Claude Operating Guides (Reference During Play)

| File | Purpose |
|------|---------|
| `rules/claude-narration.md` | How to describe rooms & set atmosphere |
| `rules/claude-combat.md` | How to narrate combat (hits, misses, tactics) |
| `rules/claude-torch-anxiety.md` | When to mention torch & create time pressure |
| `rules/claude-failures.md` | How to make failed checks interesting |
| `rules/claude-example-turn.md` | Full walkthrough of what a turn looks like |

### Game Tracking

| File | Purpose |
|------|---------|
| `games/index.md` | Registry of all games (active, paused, archived) |
| `games/game-NNN/state.md` | Current game state (UPDATE AFTER EACH TURN) |
| `games/game-NNN/log/session-NNN.md` | Turn-by-turn session logs (WRITE AT SESSION END) |

---

## Key Mechanics

### Checks
- **Roll:** d20 + stat modifier
- **You set DC:** 9 (easy), 12 (moderate), 15 (hard)
- **Success if:** d20 + modifier ≥ DC

### Combat
- **Initiative:** d20 + DEX (PCs roll together, enemies roll once)
- **Attack:** d20 + ATK bonus vs. AC
- **Damage:** Roll weapon die + modifier
- **0 HP:** Unconscious. Death timer = 1d4 + CON mod rounds. Each turn: Roll d20 (on 20 = stabilize with 1 HP)

### Torch Timer
- **Duration:** 6 turns per torch (each turn ≈ 10 min exploration)
- **Pressure:** When torch expires, all light goes out. Immediate encounter check.
- **Action:** Light a new torch to reset timer to 6

### Encounters
- **When to roll:** Every 2 non-combat exploration rounds
- **Roll:** 1d6. On 1 = encounter occurs
- **Table:** Reference `encounters.md` (d8 roll for which creatures appear)

### Scarlet Minotaur Scaling
- **First encounter:** Roll d8 normally
- **After first encounter:** Apply cumulative **-2 penalty** to future rolls
- **After meeting Minotaur:** Reset penalty to 0

---

## Running Multiple Games

This system supports **parallel campaigns**:

```
lost-citadel/games/
├── game-001-2026-04-12/  (Active — Session 3)
├── game-002-2026-04-13/  (Active — Session 1)
└── game-003-2026-04-10/  (Paused — can resume)
```

Each game has its own `state.md` and `log/` folder. Check `games/index.md` to see status.

---

## Tips for DMs

1. **Torch timer creates urgency.** Emphasize time pressure so players feel rushed.
2. **Read the room before each area.** Know what treasures & NPCs are present.
3. **Bull statue traps are deadly.** Creatures use them tactically. Let players discover this.
4. **Secret doors reward searching.** Don't give them away; let persistence & checks find them.
5. **The Minotaur is a threat that looms.** It should feel inevitable if players linger.
6. **Let players be creative.** If they find a clever solution, let it work (within reason).
7. **Failure is interesting.** When a check fails, describe dramatic consequences (not "nothing happens").
8. **NPCs have goals.** Beastmen want the Minotaur dead; Ettercaps want treasure. They're not just obstacles.

---

## Project Instructions

For project-specific conventions & workflows, see **`CLAUDE.md`**.

---

## Getting Started

1. **Read this README** (you're doing it!)
2. **Pick your players** (1-4)
3. **Create game folder** in `games/`
4. **Pick characters** from `rules/characters.md`
5. **Initialize state.md** with party info
6. **Open in Claude Code** (Mac or iPhone app)
7. **Ask Claude:** "Start the adventure!"

---

## Questions?

- **"How do I run a turn?"** → See `rules/dm-system-prompt.md`
- **"What's in this room?"** → Look it up in `rules/rooms.md`
- **"What are creature stats?"** → See `rules/encounters.md` or `rules/npcs.md`
- **"How does combat work?"** → See `rules/claude-combat.md`
- **"How do I track game state?"** → See `rules/dm-system-prompt.md` "Managing Player Resources"
- **"Can I run multiple games?"** → Yes! Create separate folders in `games/`

---

**The Lost Citadel awaits. Pick your party. Light your torch. Descend into darkness.**

Good luck, DM.
