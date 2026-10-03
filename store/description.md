Stop hunting for the body you just killed. **Loot Beam** raises a pillar of light from every NPC corpse
that can still be looted, so the one worth walking to announces itself from across the camp.

The beam is capped at 20 yards by default -- tall enough to spot across a camp, short enough to stay a
marker rather than a light show. It breathes slowly so a live beacon never reads as scenery, and
drifting sparkles twinkle up through the shaft so the light shimmers rather than sits. It draws through
terrain and walls by default, so a body tucked behind a rise is never missed; turn **Through walls** off
if you would rather the world hide it like anything else.

**Every knob is live-tunable** from the in-game overlay panel or from `wxl-loot-beam.ini` next to the
DLL: height, base offset, beam width, colour, opacity, pulse, range, the sparkle field, and whether the
world is allowed to hide it. Prefer to leave already-looted bodies dark? Enable **Only lootable
corpses** and the beacon disappears the moment the body is emptied.

Each gear tier -- currency, poor, common, uncommon, rare, epic, legendary, artifact and heirloom -- has
its own colour and its own on/off switch under **Gear tiers**, so you can recolour them to taste or
hide entire tiers (say, no beam for currency-only or uncommon corpses) while keeping the rest.

Purely visual and entirely client-side: the module sends nothing to the server, and on a stock realm
nothing is retained once a corpse stops counting. Run the companion **mod-loot-beam** server module and
the beacon is tinted by the server's own view of the corpse's best loot -- green for a green, purple for
an epic -- the instant the body dies, before the loot window is ever opened. That server half is not
part of this install: it lives in the repo under `server/mod-loot-beam/` and has to be built into
AzerothCore (see the README's **Server module** section). Without it, a corpse only colours once its
loot window has been opened.
