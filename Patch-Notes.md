# Patch Notes

What changed below, newest first. Each version has a part for delvers and a part for whoever runs
the server.

## 0.0.2 — coming

### For delvers

**The halls are rebuilt.** The kingdoms' caverns are wider and taller now, up to 48 blocks under a
domed roof, their walls stepped into ledges and overhangs, their floors on three or four levels.
Most hold a pool at the bottom; some are dry. The dead have more room to come at you from, and you
have more places to stand.

**The companies came down with them.** The tunnels between rooms are longer and bend, and the
companies who stripped each kingdom as it sank left their timber in them: frames propping the rock,
half of them broken, a lantern lying lit where a beam came down. You'll find their works thickest
near the surface and none at all on the road to a throne. Watch for cart lines, collapses, small
dead portals at the cave doors, and geysers.

**Heirlooms carry their kingdom.** Every heirloom now holds something of the kingdom it was found
in, and luck decides how much:

- **Blessed**, about one in seven: both of its kingdom's gifts and no flaw.
- **Plain**: one gift.
- **Flawed**: one gift at its strongest, with a mild flaw of the kingdom that drowned it. Flaws are
  commonest in the shallow kingdoms, which fell last and poorest, and rarer the deeper you go.

| Kingdom | Gifts | Flaw |
|---|---|---|
| The Greenwood | more health, or quicker in water | a little slower on your feet |
| The Stonemark | tougher armour, or harder to knock back | falls hurt a little more |
| The Hush | quicker while sneaking, or falls from higher without harm | one heart less |
| The Ashen Hold | the flames go out sooner, or faster on your feet | a little slower to swing |

A flaw only costs you while you wear or hold the piece. Heirlooms also no longer waste a roll on
Unbreaking or Mending: they never wear.

### For server owners

- New dungeon generation is on by default (`world-gen-v2: true` in `config.yml`; needs a restart to
  change).
- `loot.yml` is replaced on the next start; your old copy is kept beside it as `loot.yml.v<old version>`. Tune
  heirloom luck with `heirloom.blessed-chance` and `heirloom.bane-chance`.
- The jar is now `SunkenKingdoms.jar`. Delete any older `SunkenKingdoms-<version>.jar` from
  `plugins/` when updating.
- The lobby valley can now be generated with `/delve admin survey` (in progress).

## 0.0.1 — 2026-10-04

The first playable build: Bellmouth and its wells, three tiers of sunken kingdoms with their kings,
the Hush's Listening, kingdom veins, Crowns, the factors and the purse.
