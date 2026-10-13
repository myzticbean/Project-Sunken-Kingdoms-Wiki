# Patch Notes

Every update, newest first. Each one opens with what every delver will feel, then lifts the lid in
**Under the hood**: the numbers, the odds and the work that keeps the halls smooth.

## 0.0.3 — 2026-10-13

### For delvers

**Everything you do down there now counts.** Meet **Echoes**. Every dead you put down, every gate
you open, every walk home adds to a level that is yours forever. It lives on the XP bar, in every
world, and nothing takes it from you. Hit hard and you hear more: when several delvers bring one of
the dead down, each hears their share of the damage they dealt. Vanilla experience is gone: no
orbs, no bottles o' enchanting, nothing to farm. The enchanting table and the anvil still read your
level, and they spend none of it.

**Hear it ring.** When you reach a new level, it rings out like a bell for everyone near you, and
it rings through you too: every heart comes back, full, right there in the middle of the fight. And
your level travels with you, worn by your name in its bell metal: **Tin**, then **Copper**,
**Verdigris**, **Silver** and **Gold**, ten levels apiece, until at level 50 you wear **the Great
Bell** itself.

**The Bellringer is waiting by the hearth.** Whoever rings the Upper Half hears what each delver
brings home, and now they will teach you what it is worth. Right-click the Bellringer, spend an Echo
on a rank, and carry what you have learned into the dark. Click a learned Way to carry it, and it
shines. Your first Way, Dash, opens at level 2: one delve to learn the deep on your own feet first. Two Ways to begin, a third for every king's
Seal you claim, six at most. Carried Ways are yours from the moment you fall until you walk out.

**The Ways of the Breath.** The first branch, four Ways:

- **Dash.** Jump, then jump again in mid-air, and you launch along your look. Five ranks, each one
  faster, and the last gives you a second dash before you land.
- **Catch.** Sneak in mid-air and you drift down on Slow Falling for 2, 3, then 4 seconds. At its
  third rank, land inside it and the fall does you no harm.
- **Lunge.** Right-click with a sword in hand and you thrust forward. Your first hit within a second
  lands harder: +20%, +35%, then +50%.
- **Second Wind.** Every dead you damaged gives back Nerve when it is put down: 1, 2, then 3. At its
  third rank your Nerve returns a quarter faster.

**Nerve.** Below, your food bar becomes your nerve. Ways and sprinting spend it, it comes back on its
own if you give it a moment, and food tops it up: bread 4, cooked meat 6, stews 8, golden carrots
10, a golden apple the whole bar. Every food tells you what it gives, right at the top of its lore,
and it all stacks to 99, wherever you got it.
Nothing else drains it. Above, in the valley, there is no hunger at all.

**And now you can see it.** Your nerve burns in Bellmouth's own blue lanterns, a row of them where
the drumsticks used to be. A lit lantern is nerve to spend, a guttering one is half gone, a dark one
is spent. Watch them go out as you sprint, and watch them catch again when you stop.

**Run for it.** Below, the deep slows a walking delver: walking is a fifth slower. A sprint shakes
it off and carries you at full pace, and it costs nerve. A full bar buys about five and a half seconds of hard running,
so choose when to break into a sprint. Run dry and your legs won't carry you until your nerve
comes back.

**Words that hold still.** A season's title, its subtitle and the line over your hotbar now arrive
together and fade together, held for 6.5 seconds, with no flicker. Objectives, kings and the hall
falling quiet all hold the same way; a refusal shows once, briefly.

**Your sidebar** now shows your Crowns and any Echoes you have waiting to spend.

**Bellmouth's traders have names.** Walk up to the counters and meet them: **Pell the Provisioner**,
**Ansel the Assayer** and **Aldith the Alchemist**. All three have stood in Bellmouth since the
founding, so nobody waits on a first Cairnfire to come up before a counter opens.

**Some counters are earned.** Aldith deals only with a delver Bellmouth knows by their echoes. Walk
up below level 5 and you are thrown straight back from the counter, with the level Aldith deals from
right there over your hotbar. Reach it, and the whole shelf is yours: brewing stock and finished
draughts, at a price that tells you what the deep is worth. What you carry up yourself will always
be the cheaper way.

**One bell, one side.** No more friendly fire. A wild swing in a crowded tunnel, a stray arrow
across the hall: none of it finds another delver now, below or in the valley. Every delver goes
down under the same bell.

### Under the hood

- **The level curve.** Every delver starts at level 1. Level L to L + 1 takes 20 + 10 × L Echoes:
  30 to reach level 2, 110 from level 9 to 10. Levels stop at 50; Echoes past it still count toward your total.
- **What each deed is worth**, before the tier: a common dead 1, a marked dead 2, a Wight 8, an
  Oathbound 15, a king 60. A met gate objective gives 15 to every delver in the hold. The dead's
  Echoes are split by the damage each delver dealt. Then the tier multiplies it: ×1, ×1.5, ×2, ×2.5
  for tiers 1 to 4. Walking out alive adds 20% of what you heard that delve on top.
- **Nerve, in numbers.** 20 points. One comes back every 1.5 seconds, paused for 2 seconds after any
  Way and for as long as you sprint. Sprinting spends one point every 0.4 seconds, and vanilla stops
  the sprint at 6 points, so a full bar sprints 14 points: 5.6 seconds. Walking below is −20% speed;
  sprinting adds that 20% back, so a sprint below runs at vanilla sprinting speed, 1.6 times your
  walk instead of 1.3.
- **Way costs and cooldowns.**

  | Way | Opens at level | Nerve per use | Cooldown |
  |---|---|---|---|
  | Dash | 2, 4, 8, 14, 20 | 4, 4, 3, 3, 3 | 1.5 s |
  | Catch | 3, 9, 16 | 2 | 3 s |
  | Lunge | 7, 15, 25 | 4 | 4 s |
  | Second Wind | 5, 12, 22 | passive | |

- **Dash and falling.** The second jump borrows vanilla's flight toggle, which would normally spare
  you all fall damage. Fall past your safe distance and the dash is put away, so a long drop hurts
  exactly as it should.
- **Lighter hoards.** Bottles o' enchanting no longer turn up below, in hoards or as a chest's prize.
- **Aldith's prices.** 3 glass bottles for 2 Crowns; 2 nether wart or 2 sugar for 12; gunpowder 8;
  blaze powder 12, twice what the Assayer pays for Rootwart, Ironbark Sap, Blastgrit and Cairnfire.
  Potions: healing 16, swiftness 20, fire resistance 24, strength 30. Brewing stands are no longer
  sold.
- **The Mason has packed up**; the lot stays open for the next trader to come to Bellmouth.
- **Bellmouth's lanterns travel with the server.** The server hands every delver a small resource
  pack as they join, and it is required: six sprites, the full, half and empty lantern and their
  sickly-green twins for when hunger has hold of you. It is served by the game itself, so there is
  nothing else to install.

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
