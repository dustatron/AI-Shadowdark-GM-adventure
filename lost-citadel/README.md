# The Lost Citadel — Shadowdark RPG Adventure System

**A complete, modular system for running The Lost Citadel with Claude as DM.**

---

## Quick Start

1. **Start a new game:**
   - Copy `games/game-001-YYYY-MM-DD/` template (create state.md + log/ folder)
   - Pick 4 characters from `rules/characters.md`
   - Initialize `state.md` with party info

2. **During the game:**
   - Reference `rules/dm-system-prompt.md` for how to run turns
   - Look up rooms in `rules/rooms.md`
   - Roll encounters from `rules/encounters.md`
   - Reference NPCs in `rules/npcs.md`
   - **Update `adventure-state.md` after each major action**

3. **Track everything:**
   - `adventure-state.md` = current HP, location, torch timer, resources
   - `log/session-001.md` = detailed turn-by-turn log + what happened
   - Multiple sessions can run in parallel (different game folders)

---

## Folder Structure

```
lost-citadel/
├── rules/
│   ├── characters.md        (4 pre-built character templates)
│   ├── rooms.md             (all 27 areas fully detailed)
│   ├── encounters.md        (random encounter table + creature stats)
│   ├── npcs.md              (named NPCs + generators + tactics)
│   └── dm-system-prompt.md  (complete DM instructions)
│
└── games/
    ├── index.md             (registry of all games)
    │
    ├── game-001-2026-04-12/ (example game folder)
    │   ├── state.md         (current game state — UPDATE EACH TURN)
    │   └── log/
    │       ├── session-001.md   (turn log: what happened)
    │       ├── session-002.md
    │       └── ...
    │
    └── game-002-YYYY-MM-DD/ (another game)
        ├── state.md
        └── log/
```

---

## Files at a Glance

### `rules/characters.md`
- **4 pre-built character templates:** Fighter, Priest, Thief, Wizard
- Fixed stat array (10, 11, 12, 13, 14, 15)
- Ready-to-use HP, abilities, equipment, spells

### `rules/rooms.md`
- **All 27 areas of the citadel** in indexed format
- Player descriptions (safe to share)
- GM notes (secrets, traps, treasure, connections)
- Easy lookup: Area 1, Area 2, etc.

### `rules/encounters.md`
- **Random encounter table** (d8 roll)
- Creature stat blocks (Beastmen, Ettercaps, Scarlet Minotaur, Wights, etc.)
- **Scarlet Minotaur scaling mechanic** (cumulative -2 penalty after first encounter)
- Combat quick-reference

### `rules/npcs.md`
- **Named NPCs** with personalities (Rogath, Eska, Brell, Giuseppe, etc.)
- Stat blocks for each
- **NPC generators** for random creatures (d10 tables)
- Faction attitudes & dialogue examples
- Combat tactics for each group

### `rules/dm-system-prompt.md`
- **Master DM guide (reference during play)**
- Links to operational guides below

### Claude Operating Guides (Use During Play)

**`rules/claude-narration.md`** — How to describe rooms, pacing, atmospheric details

**`rules/claude-combat.md`** — Combat procedures, narrating hits/misses, creature tactics

**`rules/claude-torch-anxiety.md`** — When to mention torch, creating pressure, darkness mechanics

**`rules/claude-failures.md`** — Making failures interesting, not frustrating

**`rules/claude-example-turn.md`** — Full turn example (model your pacing after this)

### `games/index.md`
- Registry of all active/archived games
- Templates for creating new game folders
- Example `state.md` and `session-001.md` formats

---

## How to Play

### Setup (First Time)
1. Create new game folder: `games/game-NNN-YYYY-MM-DD/`
2. Create `state.md` (use template from `games/index.md`)
3. Create `log/` folder with `session-001.md`
4. Add game entry to `games/index.md`
5. Players pick characters from `rules/characters.md`

### During Play

**Quick Reference (Keep These Open):**
1. Current `adventure-state.md` (party status, location, torch)
2. Current room from `rooms.md`
3. One Claude operating guide (based on what's happening):
   - Room description? → `claude-narration.md`
   - Combat? → `claude-combat.md`
   - Torch running low? → `claude-torch-anxiety.md`
   - Check failed? → `claude-failures.md`
   - Unsure about pacing? → `claude-example-turn.md`

**Each Turn:**
1. Describe situation (reference `claude-narration.md` for formula)
2. Ask "What do you do?"
3. Listen to player actions
4. Resolve each action with narration (not just mechanics)
5. Track torch timer (decrement by 1)
6. Every 2 rounds: Roll 1d6 for encounter check
7. Update `adventure-state.md` after session

### Resources & Rules
- **Room descriptions:** Model after examples in `claude-narration.md`
- **Combat:** Follow `claude-combat.md` narration procedures
- **Torch timer:** Follow `claude-torch-anxiety.md` callout schedule
- **Failures:** Follow `claude-failures.md` framework
- **NPC stats/tactics:** Reference `npcs.md` and `encounters.md`

---

## Key Mechanics

### Checks
- Player rolls **d20 + stat modifier**
- You set **DC** (9=easy, 12=moderate, 15=hard)
- Success if **d20 + mod ≥ DC**

### Combat
- **Initiative:** d20 + DEX (all PCs act, then all enemies)
- **Attack:** d20 + ATK bonus vs. target AC
- **Damage:** Roll die + modifier
- **0 HP:** Unconscious. Death timer = 1d4 + CON mod rounds. Each turn: roll d20, on 20 = stabilize with 1 HP

### Torch Timer
- **Duration:** 6 turns per torch (each turn ≈ 10 min exploration)
- **Every 2 rounds:** Roll 1d6. On 1, encounter happens
- **When torch expires:** All light out. Immediate encounter check.

### Scarlet Minotaur Scaling
- **First encounter:** Roll d8 normally
- **After first encounter:** -2 cumulative penalty to all future d8 rolls
- **After encountering Minotaur:** Reset penalty to 0

---

## Running a Full Session

**Time: ~60 minutes**

- **00-05 min:** Set scene, ask what players do
- **05-50 min:** Play through 3-5 turns of exploration/combat
- **50-60 min:** Level up, discuss loot, note any cliffhangers

**Each turn includes:**
- Describe situation
- Ask for actions
- Call checks if needed
- Resolve consequences
- Update torch timer & encounter status
- Roll 1d6 for random encounter (if 2+ rounds since last)
- Log turn in session file

---

## Tips for DMs

1. **Read the room before each area.** Know what treasure/NPCs are present.
2. **Use the NPC generators** if you encounter random creatures not pre-named.
3. **Torch timer creates urgency.** Emphasize time pressure so players feel rushed.
4. **Bull statue traps are deadly.** Beastmen use them tactically against Minotaur.
5. **Let players be creative.** If they find a clever solution, let it work.
6. **Secret doors are a reward.** Searching methodically should pay off.
7. **The Minotaur is a threat that looms.** It should feel like an inevitable danger.
8. **NPC factions have goals.** They don't exist just to fight PCs. Beastmen want the Minotaur dead; Ettercaps want treasure.

---

## Multiple Games

This system supports running **multiple campaigns in parallel**:

```
games/
├── game-001-2026-04-12/  (Active)
├── game-002-2026-04-13/  (Active)
└── game-003-2026-04-10/  (Paused, can resume)
```

Each game has its own `state.md` and `log/` folder. Check `games/index.md` to see which are active or ready to resume.

---

## Files You'll Update

- **`adventure-state.md`** (inside each game folder) — Update after EVERY turn
  - Current location
  - Party HP
  - Torch timer
  - Resources used
  - Encounters triggered

- **`log/session-NNN.md`** (inside each game folder) — Update at session END
  - Turn-by-turn summary
  - Rolls made
  - Combat log
  - Loot acquired
  - NPCs encountered
  - Session notes & next steps

---

## Ready to Play?

1. ✅ Rules ready
2. ✅ Rooms detailed
3. ✅ NPCs defined
4. ✅ Encounters random-generated
5. ✅ Game tracking system in place

**Start a new game in `games/`, pick your party, and descend into the Lost Citadel.**

---

## Questions?

- **"How do I run a check?"** → See `dm-system-prompt.md`
- **"What's in this room?"** → Look up area number in `rooms.md`
- **"What are the creature stats?"** → See `encounters.md` or `npcs.md`
- **"How does the Scarlet Minotaur work?"** → See `encounters.md` Minotaur section + `dm-system-prompt.md`
- **"Can I play multiple games?"** → Yes! Create separate folders in `games/`

Good luck, DM. The darkness awaits.
