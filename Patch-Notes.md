# Patch Notes

What changed below, newest first. Each version has a part for every delver, and an **Under the
hood** part for the curious: the numbers, the odds and the work done to keep the halls smooth.

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

### Under the hood

- **Smoother building.** A hold's rooms are now carved in parallel instead of one after another,
  and the blocks are written a slice at a time, spread across ticks, so a new hold no longer stalls
  the server when a gate opens. Chunks a hold needs are loaded gradually rather than all at once,
  and nothing (clearing old delves, waking the dead, rising spawns) forces a chunk to load on the
  spot any more. Fewer lag spikes when you drop in.
- **Room numbers.** Rooms are 64 blocks across and up to 48 tall (they were 48 by 36), with the roof
  peaking about 40 above the doorways. Tunnels are 20 long instead of 12, never narrower or lower
  than 3 by 3, so even the tallest dead fit through. The fall into a room is about 40 blocks.
- **The dead see further.** Bigger rooms meant longer sight: a dead now notices you at 48 blocks and
  calls its room's others from up to 128.
- **Heirloom odds.** Every heirloom first rolls blessed, at 15%. If not, it rolls flawed by tier:
  50% at tier 1, 40% at tier 2, 30% at tier 3, 20% from tier 4 on. Overall that is roughly 42%,
  34%, 25% and 17% flawed. A gift's strength rolls within a range that grows with the hold's
  depth; a flawed piece always takes the top of it. Flaws are attribute modifiers on the item, which
  is why they only apply while it is worn or held, and why they stack across pieces.

## 0.0.1 — 2026-10-04

The first playable build: Bellmouth and its wells, three tiers of sunken kingdoms with their kings,
the Hush's Listening, kingdom veins, Crowns, the factors and the purse.
