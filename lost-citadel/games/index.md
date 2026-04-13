# Lost Citadel Game Registry

Active games and their status. Resume any game or start a new one.

---

## Active Games

| Game | Date | Party | Status |
|------|------|-------|--------|
| game-002-2026-04-13 | 2026-04-13 | Steve (Fighter), Sunscreen (Thief) | **Active** |

---

## Game Archive

*Games will be listed here after completion or long pause.*

---

## How to Add a Game

When starting a new game:

1. Create folder: `game-NNN-YYYY-MM-DD/` (e.g., `game-001-2026-04-12`)
2. Create `state.md` (copy template below)
3. Create `log/` folder
4. Create first session log: `log/session-001.md`
5. Add entry to this index

---

## Game Folder Template

```
game-001-2026-04-12/
├── state.md              (current game state, updated every turn)
└── log/
    ├── session-001.md    (turn log + events)
    ├── session-002.md
    └── ...
```

---

## state.md Template

```markdown
# Game-001 State — Session 1

## Current Status
- **Date Started:** 2026-04-12
- **Date Last Updated:** 2026-04-12, 14:30
- **Location:** Area 1 (Mural Chamber)
- **Turn:** 3

## Party Composition
- **Slot 1:** Fighter "Kael" — 6/8 HP, STR 15, DEX 12, CON 13
- **Slot 2:** Priest "Mira" — 5/6 HP, WIS 15, Deity: Saint Terragnis
- **Slot 3:** Thief "Ren" — 3/3 HP, DEX 15, has 20 arrows
- **Slot 4:** [Vacant]

## Resources
- **Torch Timer:** 4 rounds remaining
- **Light Source:** 1 torch (lit)
- **Ropes/Pitons:** Fighter has 60' rope, 10 pitons
- **Spells Cast:** None yet
- **Luck Tokens:** 0

## Encounters
- **Scarlet Minotaur Status:** Not yet encountered (cumulative penalty = 0)
- **Eska Status:** Still in Area 1 (not alarmed yet)

## Important Notes
- Party just entered citadel
- Heard faint noise from south passage
```

---

## session-001.md Template

```markdown
# Session 001 — Game-001

**Date:** 2026-04-12
**Duration:** ~60 minutes
**Players Present:** 4
**Session Summary:** Party entered citadel, explored mural chamber, heard strange sounds

---

## Turn 1-3: Citadel Entrance → Area 1

**Turn 1:**
- Party enters through SE doors (carved with bucking bulls)
- Kael (Fighter) takes point, torch held high
- Mira (Priest) following, scanning for religious iconography
- Ren (Thief) checking for traps — **DC 12 Perception check**, rolled 14, no traps detected
- Party enters Area 1 (Mural Chamber)

**Description Shared:**
> Towering walls covered in vibrant murals — red pillars banded in black marble. Figures in white robes kneeling before a colossal onyx bull with horns lowered for a charge.

**Turn 2:**
- Kael examines murals closely — **DC 12 INT check**, rolled 10, fails to glean deeper meaning
- Ren searches for valuables — spots **hidden niche behind bull statue**! Retrieves silver bull horn (30 gp)
- Party moves to examine pillars

**Turn 3:**
- Mira attempts to understand religious significance — **DC 12 WIS check**, rolled 16, success!
  - Understands this was a bull cult, likely pre-dates current settlement
  - Bull motifs indicate warrior society
- Torch timer: 4 rounds remain
- **Encounter check (1d6):** Rolled 4 — no encounter yet

---

## Combat Log
*None this session*

---

## Loot Acquired
- Silver bull horn (30 gp) — in Ren's possession

## NPCs Encountered
- None directly (Eska not yet discovered hiding)

## Session Notes
- Party is cautious, good use of light source
- Good roleplay from Mira regarding religious lore
- Ren's thievery skills proving valuable for finding secrets
- Torch timer concerns emerging as players realize time pressure

## Next Steps
- Party likely to explore Area 2 next (west passage)
- Watch for Eska encounter in Area 1 if party returns
```

---

## Quick Commands

When starting a new game:

```bash
mkdir -p lost-citadel/games/game-NNN-YYYY-MM-DD/log
```

Then create `state.md` and `log/session-001.md` using templates above.
