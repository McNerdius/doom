# BIGMACDECK
## v5.4

![BigMacDeck-screenshot](BigMacDeck-5.4/graphics/decks/BigMacDeck.png)

A large, streaming-friendly deck for [Corruption Cards](https://forum.zdoom.org/viewtopic.php?t=67939).  It disables 58 cards (see below [below](#disabled-cards) for a listing and notes), leaving 197 in play - double the default "Balanced" deck.

Card removal criteria:
  - Potentially map- or run-breaking: making 100% item/kill count impossible, out-of-bounds issues, interfering with advanced mapping techniques, etc.
  - Significant/disproportionate alteration of gameplay, such as "The Ancient One".
  - Adding hostility to the environment in ways that are likely to block progress or eliminate a mapper's intended "safe zones."
  - Reversing or preventing progress due to large or ongoing ressurections/spawns.

Just load the [`BigMacDeck-*.pk3`](BigMacDeck-5.4.pk3) (right click to "Save As") after the Corruption Cards PK3 and the deck will be presented along with the defaults:

![ZDL](ZDL.png)

Voila:

![BigMacDeckScreenshot](BigMacDeck-Screenshot.png)

# Unsolicited Opinions

IMO, variety is what makes Corruption Cards great.  In addition to using a large deck, one can:

- Disable difficulty progression keeps lower tier cards in play throughout the playthrough.  (This deck disables difficulty progression by default, but custom mode settings can override this.)
- Use custom mode to offer eight cards:

![CC-Settings-2](CC-Settings-2.png)

Eight could be a bit much for streaming, maybe six would be more reasonable, combined with "streamer friendly layout":

![CC-Settings](CC-Settings.png)

Which looks like this:

![CC-StreamerLayout](CC-StreamerLayout.png)

# Future Stuff

One feature this deck doesn't take advantage of is custom monster grouping.  This would allow disabling certain buffs on boss monsters.

In time this repository will house "McDeck" (for lack of a better name...), a set of tools i'm working on to simplify creation and sharing of custom decks.  It consists of:
- A CLI to collate and dump assets from Corruption Cards PK3s to a more "consumable" format.  It can be used to generate custom decks but this tedious given 200+ cards.
- A web API to consume dumped data programatically.  For now it has endpoints to provide Decks and Cards (by ID, Base Class, or Type) for the latest version of Corruption Cards.  Search and version selection will be added.
- A site to browse and search Corruption Cards and create custom Decks.  Future versions will allow loading previously customized Decks for further editing, and if there is interest a "Community Decks" page.

# Disabled cards

Some cards i've disabled may seem borderline or "not too bad" but keep in mind that due to eggs, random enchantments, deck modifying cards and so on - any card in the deck could pop up at any time.  Possibly annoying card in a possibly annoying scenario is no bueno.

Scent Of Blood:
------
After taking 100+ damage, extra monsters will spawn.

Notes: Progress-blocking.

Boiling Blood:
------
Players bleed damaging pools of blood.

Notes: Generally annoying.

Wrath Sentries:
------
Add several sentries that fire {species} projectiles.

Notes: Progress-blocking - they could be placed such that intended safe spots or transporter destinations are vulnerable.

Cult Chow:
------
Health items become Priest Porridge (tastes better warm!)

Notes: I've had some weird issues with stacked health potions.

Brutal Totem:
------
Spawn a totem that doubles monster damage.

Notes: A wee bit much...

Frankenstein's Gift:
------
{species} can stitch together two corpses to make a new monster.

Notes: Gets out of control when applied to extra monsters mid-level.

Armageddon:
------
After 1000 kills, all monsters are given the Nuclear Curse.

Notes: Does this cause a chain reaction ?

Mega Deathmatch:
------
An 8-bit warrior will challenge you.

Notes: What's the HP ?


Leaking Soul:
------
Your bonus health drains over time.

Annoying Devil:
------
A devil will follow players and cause mischief.

Unfinished Business:
------
Monsters you left alive in previous levels will return.

Notes: I've had this erroneously add dozens of monsters in.

Marked for death:
------
Monsters begin hunting players from the start.

Notes: Potentially level-breaking.  (Keeping blind playthroughs in mind here.)

Sludge Rain:
------
Sludge rain will fall outside, slowing your movement.

Notes: Super bad combo if a level has challenging hurtfloor areas.

Poultry Hazard:
------
Chickens will appear. Avoid killing them at all costs.

Notes: Amusing as a temporary card, but a nuisance as a permanent card.

Shadows Manifest:
------
A damaging shadow will spawn and trail behind players.

Blade Traps:
------
Spawn several spinning blade traps in the level.

Notes: Much more damaging than other traps and can break invisible-lift style bridges and similar tricks, block intended safe zones, doorways, lifts...

Teleport Shock:
------
When something teleports, a shockwave shoves entities away.

Notes: May make 100% item count unachievable.

Co-operative Evil:
------
Monsters no longer infight.

Notes: 🤔

Breach!:
------
Monsters gain a speed boost when they open doors.

Notes: Potentially level breaking.  I've seen doors opening that shouldn't be, plus they stay open.

Hotter Start:
------
At the start of the level, 20 monsters are teleported near players.

Notes: Nope.

Adaptable Foe:
------
Bosses gain up to 3 random enchantments while in combat.

Notes: This is one where `monstergroup` will be useful.

The Howling:
------
Monsters may transform into a Werewolf when damaged.

Notes: Annoying as hecc, there i said it.

Chain Resurrections:
------
When a monster resurrects, another nearby is also resurrected.

Notes: "Nearby" may be unreachable.

Night Totem:
------
Spawn a totem that makes monsters invisible.

Notes: Completely invisible = completely unreasonable.

Vile Totem:
------
Spawn a totem that resurrects nearby monsters.

Notes: Archvile with higher range and frequency...

Concealed Totems:
------
Totems are invisible until dropped.

Notes: Completely invisible = completely unreasonable.

Lethality Curse:
------
One monster is cursed. Killing it drastically lowers your health.

Resurrection Curse:
------
One monster is cursed. Killing it resurrects nearby monsters.

Notes: Much worse than similar duplication effects, and "one monster" is a starting point - with this in the deck it could be applied randomly in other circumstances.

Mirror Curse:
------
One monster is cursed. Killing it mirrors your world.

Notes: I've heard of weird effects while streaming plus it's kinda meh.

Invisibility Curse:
------
One monster is cursed. It is completely invisible.

Notes: Completely invisible = completely unreasonable.

Miasma Curse:
------
One monster is cursed. Killing it makes nearby floors toxic.

Notes: Progress blocking.

Vegetation Curse:
------
One monster is secretly cursed. Killing it spawns vegetation.

Notes: Visibility is handy

Curse Of Decay:
------
One monster is cursed. When it dies, exploding critters infest nearby corpses.

Notes: SUPER annoying.

Incineration Curse:
------
One monster is cursed. Killing it burns nearby items.

Notes: Burned items means 100% items won't happen.

Curse of Achilles:
------
One monster is cursed. It can only be damaged at very close range.

Notes: Imagine choosing between sniping a cybie or teleporting next to it.

Kleptomania:
------
{species} will steal items off the ground.

Notes: Another potential 100% items killer.

Casali's Watchers:
------
{species} may become an immobile, self-resurrecting sentry.

Notes: Progress blockers, same as sentries.

Forbidden Gaze:
------
Looking at {species} for too long burns the player.

Notes: Annoying

Living Vessel:
------
{species} spawns 3 {species} when killed.

Notes: Can be applied randomly... Progress killer.

Noxious Vials:
------
{species} gain the ability to throw poison gas vials.

Notes: Super annoying.

Barbarity:
------
{species} always deal the highest damage they've ever dealt.

Notes: Can be applied randomly...

Reflect Enchantment:
------
{species} reflect projectiles back at you.

Notes: No

Acid Blood Enchantment:
------
{species} bleeds lethal acid.

Notes: Super annoying.

Leap Enchantment:
------
{species} can leap at their prey.

Notes: No 100% kills if they jump OOB.

High Voltage Enchantment:
------
{species} will electrocute nearby players.

Notes: Super annoying

Infestation Enchantment:
------
Exploding critters may hide inside {species} corpses.

Notes: Super annoying

Bombardment Augment:
------
{species} continuously throw projectiles.

Notes: Progress-blocking.

Electric Augment:
------
{species} projectiles electrocute nearby players.

Notes: Super annoying.

New Hunting Grounds:
------
Remove most monsters, but replace some with Archviles.

Notes: Not too fun eh ?

Curse of Dormin:
------
One monster is cursed. Killing it transforms you into the monster.

Oath to the Old God:
------
5 monsters become disciples. If they all die, the Ancient One is summoned.

Demand / Supply:
------
Items are removed. Stand still and hold USE to spawn them all.

Endless Flow:
------
A green liquid will slowly fill the level, resurrecting monsters.

Angry Bones:
------
Remove all monsters in this level, but an angry Revenant stalks you.

Grace of Lilith:
------
|index entry637:changes manynfDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDD NON-ZDOOM DETECTED, PLEASE START IN REGULAR ZDOOM NON-ZDOOM DETECTED, PLEASE START IN REGULAR ZDOOM NON-ZDOOM DETECTED, PLEASE START IN REGULAR ZDOOM - whoami

Swimming Lessons:
------
One Key is trapped, and will spawn 3 bosses.

Break the Bat:
------
Bane will challenge you to a 1 on 1 fight.

Second Slice:
------
You must do a second lap of the level under a time limit.
