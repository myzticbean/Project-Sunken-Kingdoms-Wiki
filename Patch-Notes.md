# Patch Notes

Every update, newest first. Each one opens with what every delver will feel, then lifts the lid in
**Under the hood**: the numbers, the odds and the work that keeps the halls smooth.

## 0.0.2 — 2026-10-10

### For delvers

**We tore the halls down and raised them again, bigger.** Step through a gate and look up. The
kingdoms' caverns now climb as high as 48 blocks to a domed roof, their walls stepped into ledges
and overhangs, their floors broken across three and four levels. Most cradle a pool at the bottom;
some lie bone dry. The dead have more ways to come at you. You have more places to make your stand.

**The companies left their mark.** The tunnels between rooms run longer now, and they bend, so you
never quite see what waits past the turn. The companies who stripped each kingdom as it sank left
their timber behind: frames still propping the rock, half of them snapped, a lantern lying lit where
a beam came down. Their works crowd the shallows and thin out as you descend, and on the road to a
throne there is nothing at all. Watch for cart lines, collapses, small dead portals at the cave
doors, and geysers that burst from the floor.

**Every heirloom now carries its kingdom.** Every heirloom you pull from the deep holds something
of the kingdom that drowned it, and luck decides how much:

- **Blessed**, about one in seven: both of its kingdom's gifts, and no flaw.
- **Plain**: one gift.
- **Flawed**: one gift at its very strongest, paid for with a mild flaw of the kingdom that drowned
  it. Flaws haunt the shallow kingdoms, which fell last and poorest, and grow rarer the deeper you
  dare.

| Kingdom | Gifts | Flaw |
|---|---|---|
| The Greenwood | more health, or quicker in water | a little slower on your feet |
| The Stonemark | tougher armour, or harder to knock back | falls hurt a little more |
| The Hush | quicker while sneaking, or falls from higher without harm | one heart less |
| The Ashen Hold | the flames go out sooner, or faster on your feet | a little slower to swing |

A flaw only costs you while you wear or hold the piece, so whether it's worth it is up to you. And
because heirlooms never wear, they no longer waste a roll on Unbreaking or Mending.

**Hoards worth the robbing.** The dead no longer sit on bread, beef, arrows, torches, bones or
string. That's what your Crowns are for, and the Provisioner stocks the lot. Break into a hoard now
and you'll find ingots, raw gold, coal, emeralds, now and then a diamond, spectral arrows, bottles
o' enchanting, and the holds' own stew to keep you on your feet. A chest's prize can now be a
shield, a bundle of spectral arrows or bottles o' enchanting, right alongside the potions and
golden apples you already chase.

**Travel light.** Drink a potion or finish a stew below and there's no empty bottle or bowl left
clogging your pack.

**Your fortune stays in your hands.** The purse can no longer be thrown, so no more fumbling your
Crowns onto the floor. It still goes in a chest, and it still falls with you.

### Under the hood

Bigger halls only matter if they run smooth. Here's how we made that happen.

- **Smoother building.** A hold's rooms are now carved in parallel instead of one after another,
  and the blocks are written a slice at a time, spread across ticks, so a new hold no longer stalls
  the server when a gate opens. Chunks a hold needs are loaded gradually rather than all at once,
  and nothing (clearing old delves, waking the dead, rising spawns) forces a chunk to load on the
  spot any more. Fewer lag spikes when you drop in.
- **Lighter server.** The dead crowding a tunnel no longer push each other in every pairing: two
  collisions per mob per tick, not eight. Dropped items and experience gather from further apart, so
  fewer of them lie about, and missed arrows sink into the rock after 15 seconds instead of a minute.
  The halls no longer make every mob rethink its path while a hold is being written. Inside the
  dungeon the server sends you 6 chunks around you, not 10: nothing further can be seen in a cave.
- **The dead stay awake in big rooms.** A dead now stays fully active up to 48 blocks from you
  (was 32), the same distance it can notice you from, so one that has seen you never dozes off
  across a wide room.
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
- **Hoard pools.** Bulk rolls by weight: iron ingots 8, copper ingots 7, gold ingots 6, stew 5, raw
  gold 4, coal 4, emeralds 3, spectral arrows 3, bottles o' enchanting 3, healing potions 2,
  diamond 1. Everything there but the potions, the stew, the arrows and the bottles sells to the
  Assayer. A chest's prize is now about half potions.

## 0.0.1 — 2026-10-04

Where it all began. The first playable build: Bellmouth and its wells, three tiers of sunken
kingdoms with their kings, the Hush's Listening, kingdom veins, Crowns, the factors and the purse.
