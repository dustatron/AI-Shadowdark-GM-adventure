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

## Quick Start

1. **Clone this repo**
2. **Open Claude Code** in the repo directory (Mac, iPhone, or web)
3. **Tell Claude to start a new adventure** — Claude sets up the game, picks characters with you, and begins play

---

## How to Play

Claude is your DM. You just tell it what your character does.

- **Claude narrates rooms** — descriptions, atmosphere, what you see and hear
- **Claude rolls dice** — checks, combat, encounters, torch timers
- **Claude tracks everything** — HP, loot, location, game state
- **Claude writes session logs** — summaries saved automatically at session end

**You can ask questions anytime:** What does the room look like? How big is this creature? What's that sound? Claude answers in character as the DM.

### After Each Session

Claude writes a summary in `log/session-NNN.md` covering rooms explored, combat, loot, NPCs encountered, and notes for next session.

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

## Tips for Players

1. **Print or sketch the map.** Keep the keyed map (`Core Rules/keyed-map.png`) on paper next to you while you play. It helps you track where you've been, plan routes, and decide where to explore next.
2. **Light matters.** Your torch has limited time — don't dawdle.
3. **Search carefully.** Secret doors and hidden treasure reward thorough exploration.
4. **Bull statue traps are deadly.** If you see a bronze bull, be cautious.
5. **Talk to NPCs.** Beastmen and Ettercaps have their own goals — alliances are possible.
6. **Be creative.** Clever solutions work. The DM rewards ingenuity.
7. **The Minotaur is real.** The longer you stay, the more likely you'll meet it.

---

## Project Instructions

For project-specific conventions & workflows, see **`CLAUDE.md`**.

---

## Getting Started

1. **Clone this repo**
2. **Open Claude Code** in the repo directory
3. **Say:** "Start a new adventure!"

---

## Questions?

- **"How do I play?"** → Just tell Claude what your character does
- **"Can I ask about the room?"** → Yes! Ask anything — Claude describes it in character
- **"Can I run multiple games?"** → Yes! Claude tracks each game separately in `games/`
- **"Does it work on iPhone?"** → Yes! Clone the repo in the Claude Code app and start playing

---

**The Lost Citadel awaits. Pick your party. Light your torch. Descend into darkness.**
