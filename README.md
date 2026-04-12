# Shadowdark RPG — AI Adventure System

Complete, modular framework for running Shadowdark RPG adventures with Claude as Dungeon Master.

---

## Folder Structure

```
AI Adventure/
├── Core Rules/                          (Shadowdark rulebooks)
│   ├── Shadowdark Player Quickstart - Digital.md
│   └── Shadowdark_Game_Master_Quickstart_-_Digital.md
│
└── lost-citadel/                        (The Lost Citadel adventure)
    ├── README.md                        (START HERE)
    │
    ├── rules/                           (Reference files)
    │   ├── characters.md                (4 pre-built templates)
    │   ├── rooms.md                     (27 areas detailed)
    │   ├── encounters.md                (encounters + stat blocks)
    │   ├── npcs.md                      (named NPCs + generators)
    │   └── dm-system-prompt.md          (complete DM guide)
    │
    └── games/                           (Active/archived games)
        ├── index.md                     (game registry)
        │
        ├── game-001-YYYY-MM-DD/         (example game folder)
        │   ├── state.md                 (current game state)
        │   └── log/
        │       ├── session-001.md       (turn log)
        │       └── ...
        │
        └── game-NNN-YYYY-MM-DD/         (more games)
            └── ...
```

---

## Quick Start

### 1. **Read the Intro**
   - `lost-citadel/README.md` — Overview & how to play

### 2. **Start a Game**
   - Copy template: `games/game-NNN-YYYY-MM-DD/` (create `state.md` + `log/` folder)
   - Add entry to `games/index.md`
   - Initialize `state.md` with party info

### 3. **Load DM Mode**
   - Read `rules/dm-system-prompt.md`
   - This is your complete guide for running turns, combat, checks, encounters

### 4. **During Play**
   - **Describe:** Read room from `rules/rooms.md`
   - **Listen:** Ask "What do you do?"
   - **Roll:** Call checks, combat, encounters
   - **Track:** Update `state.md` after each turn
   - **Log:** Write turn summary in `log/session-NNN.md`

---

## Core Files

| File | Purpose |
|------|---------|
| `lost-citadel/README.md` | Adventure overview & how to play |
| `rules/characters.md` | 4 pre-built player characters (Fighter, Priest, Thief, Wizard) |
| `rules/rooms.md` | All 27 areas of the citadel with full descriptions |
| `rules/encounters.md` | Random encounter table + creature stat blocks |
| `rules/npcs.md` | Named NPCs with personalities + generators |
| `rules/dm-system-prompt.md` | Complete DM guide: how to run turns, combat, checks |
| `games/index.md` | Registry of all games (active, paused, archived) |

---

## The Adventure

**The Lost Citadel** is a 1st-3rd level dungeon crawl for 1-4 players.

- **27 explorable areas** (interconnected citadel with secret doors)
- **3 major factions:** Beastmen, Ettercaps, Scarlet Minotaur
- **Torch & light mechanics:** Time pressure & resource management
- **Boss encounter:** Scarlet Minotaur (scales in difficulty as players linger)
- **Multiple endings:** Based on which factions are defeated/allied

---

## Key Features

### Characters
- **4 pre-built templates** ready to play (no character creation needed)
- Fixed stat array (10, 11, 12, 13, 14, 15)
- All starting equipment, abilities, & spells included

### Rooms
- **27 fully detailed areas** with:
  - Player descriptions (safe to share)
  - GM secrets (traps, treasure, NPC locations)
  - Room connections (easy navigation)
  - Encounter mechanics

### Encounters
- **Random encounter table** with d8 roll
- **Scarlet Minotaur scaling:** Becomes easier to find as players spend time
- **Creature stat blocks:** Beastmen, Ettercaps, Wights, Darkman tles, etc.
- **Faction behaviors:** Each group has distinct tactics & goals

### NPCs
- **7+ named NPCs** with personalities & stat blocks
- **d10 generators** for random creatures
- **Faction attitudes:** How each group reacts to players

### Game Tracking
- **adventure-state.md:** Current HP, location, torch timer, resources
- **session logs:** Turn-by-turn record of what happened
- **Multiple games:** Run parallel campaigns in separate folders

---

## Running the Game

### 1. Load the DM System Prompt

Read `rules/dm-system-prompt.md`. This is your complete guide. It covers:
- How to run a turn
- How to call checks
- How to run combat
- Torch & light mechanics
- Encounter checks
- NPC motivations
- Philosophy for good DMing

### 2. Keep References Open

During play, you'll reference:
- `rules/rooms.md` (look up current area)
- `rules/encounters.md` (creature stats, encounter table)
- `rules/npcs.md` (NPC details, tactics)
- `state.md` (current game state)

### 3. Update State After Each Turn

After every major action:
- Update location
- Update HP (if combat)
- Decrement torch timer
- Note resources used
- Check for random encounter

### 4. Log Sessions

At end of each session, write summary in `log/session-NNN.md`:
- Turn-by-turn events
- Rolls made
- Combat summary
- Loot acquired
- NPCs encountered
- Session notes

---

## Example Game Setup

```
Create folder: games/game-001-2026-04-12/

state.md:
---
# Game-001 State

## Current Status
- Location: Area 1 (Mural Chamber)
- Turn: 3
- Torch Timer: 4 rounds

## Party
- Fighter Kael: 6/8 HP
- Priest Mira: 5/6 HP
- Thief Ren: 3/3 HP
- Wizard [Vacant]

## Encounters
- Scarlet Minotaur: Not yet met (penalty = 0)
---

log/session-001.md:
---
# Session 001

**Turn 1-3:** Explored Area 1, found 30 gp silver bull horn

## Combat Log
None

## Loot
- Silver bull horn (30 gp)

## Next Steps
- Likely to explore Area 2 (west passage)
---
```

---

## Scaling: 1-4 Players

The system works for **1 to 4 players**:

- **1 player:** One character. Might struggle in combat. Add NPC allies as needed.
- **2 players:** Two characters. Balanced difficulty. Torch timer creates pressure.
- **3 players:** Three characters. Standard difficulty. Good party composition.
- **4 players:** Four characters (full party). Recommended. All slots filled.

You can adjust encounter difficulty by:
- Adding/removing creature combatants
- Adjusting NPC attitudes
- Making allies more/less willing to help

---

## Multiple Simultaneous Games

Run **multiple campaigns in parallel**:

```
games/
├── game-001-2026-04-12/  (Session 3 — Thief party)
├── game-002-2026-04-13/  (Session 1 — Wizard-heavy party)
└── game-003-2026-04-10/  (Paused — can resume later)
```

Each game has its own `state.md` and `log/` folder. Check `games/index.md` to track which are active.

---

## Tips for Success

1. **Torch timer is key.** Emphasize time pressure so players feel rushed.
2. **Use NPC personalities.** Beastmen are superstitious; Ettercaps are greedy; Minotaur is relentless.
3. **Bull statue traps are deadly.** Creatures use them tactically. Let players discover this.
4. **Secret doors reward searching.** Don't give them away; let persistence & checks find them.
5. **Scarlet Minotaur is the THREAT.** It should feel inevitable if players linger.
6. **Let players be creative.** If they find a clever solution, let it work (within reason).
7. **Failure is interesting.** When a check fails, describe dramatic consequences.

---

## Questions?

- **"How do I start a game?"** → Create folder in `games/`, use index.md template
- **"How do I run a turn?"** → Read `dm-system-prompt.md` section "How to Run a Turn"
- **"What happens in this room?"** → Look up area in `rules/rooms.md`
- **"What are creature stats?"** → See `encounters.md` or `npcs.md`
- **"How does combat work?"** → See `dm-system-prompt.md` "Running Combat"

---

## Ready?

1. ✅ System is modular & flexible
2. ✅ All rules & reference materials included
3. ✅ Game tracking system in place
4. ✅ Multiple games can run in parallel

**Pick 1-4 players, choose characters, create a game folder, and descend into the Lost Citadel.**

Good luck, DM. The darkness awaits.
