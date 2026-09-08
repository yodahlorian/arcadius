# ARCADIUS

**An arcade management game.** Take the lease on a boarded unit, put your name over the door,
licence the machines, and open the doors.

*Devious Developments*

---

## Download

The playable beta is on the [**Releases**](../../releases) page — a single Windows `.exe`,
no installer.

## What's in the beta

- Take a boarded shopfront off the market and name it your own
- Licence arcade games, choose each cabinet's colourway, and site it on your floor
- Open up and watch patrons walk in, pick a machine, pay the coin slot and play it
- **A play pays the machine, not you** — you open the cabinets and collect
- Machines break. Find the fault by looking, order the part, carry it in, fit it
- **Rearrange the floor whenever you like** — pick a placed cabinet back up and set it down
  somewhere else, free
- A wall radio with **six house stations of original music**, or drop your own `.mp3` / `.ogg`
  into your `Music\Arcadius` folder and tune to those instead
- Separate volume faders for music, machines and the room itself
- Rent falls due every 30 days. That is the only way to lose

## What changed in 0.10.5

**Faults you can see.** Every fault tell used to be audio, an absence, or a delayed consequence —
none of which is usable by a player who cannot hear the machine. There are now three redundant
layers: the screen from the aisle (dark / static / black), two coin-door lamps (green power,
red jam), and scorch on the failed unit once the panel is open. Every cabinet also has a free
DIAGNOSTICS menu with a health bar per part.

**The coin mech has two faults.** Jammed — possible on any play once it is worn below 40%, plays
fine but takes no money, cleared by hand for free and does not restore health. Burnt out — a dead
part that needs replacing.

## What changed in 0.10.4

**You can diagnose a fault now.** One unnormalised dictionary lookup was hiding the whole repair
loop: the room registers its walk-up targets under the Title Case machine name, `machine_parts` is
keyed lower case, and a missed lookup falls through to a HEALTHY default — so a dead cabinet
reported no fault at all and offered you "[click] Play". Machine keys are normalised at the door
now, readers and writers, and standing at a faulty machine names the symptom and tells you which
panel to open.

## What changed in 0.10.3

**A broken machine now looks and sounds broken.** The fault table has always described a visible
symptom per part — dark, hashed screen, black tube with sound, coin jam — but only the repair
prompt ever read it. The cabinet itself never asked, so a machine with a dead PSU ran its attract
demo exactly like a healthy one. No power now puts the tube and the cabinet lights out, a board
fault shows static, a dead tube goes black BUT KEEPS ITS SOUND (that is how you tell the two
apart), and a jammed coin mech stays completely normal — only the day's take reveals it.

## What changed in 0.10.2

**The NPCs.** The play cycle now runs to completion: the performance and the economy were on two
different clocks, and at the default 2x speed a patron was released 52% of the way through the beat
— they paid for a game and never played it. The hold is also rolled per go now, one to five seconds
with a per-patron temperament behind it, so a busy floor stops pulsing in unison.

**Queues.** Patrons will line up for any machine rather than only their favourite type, and wait
four times as long before giving up — previously a full floor emptied out, which made a busy arcade
behave like a bad one. They keep their personal space while standing (it only applied while walking,
which excluded everybody actually in a line), and they look around while they wait.

**Comings and goings.** Nobody appears or vanishes in view of the shop any more; arrivals and
departures happen off the ends of the block. The doors close when the day ends and open when you do,
employees let themselves in of a morning, and you can still walk in and out with the doors shut.

**Faults.** The scripted repair lesson fires from day two ONWARDS rather than on day two only, and
it announces itself — a player still on one cabinet used to get no fault at all, and nothing to
diagnose.

## What changed in 0.10.1

- Buttons say what they do. The rename dialog is **Confirm / Cancel**, and the console's save,
  staff and hire buttons follow the same rule
- Fixed the staff hire button showing a raw number instead of a price

## What changed in 0.10.0

**The back-room computer is a computer.** It was a grid of rounded tiles &mdash; a phone's settings
screen wearing an arcade's colours. It is now the machine a shop office actually had in 1985: an
amber monochrome tube running a text-mode program.

- A ruled panel, a numbered menu you read down, the selection in **inverse video**, a blinking
  `READY` prompt and a reverse-video function-key strip along the bottom
- Scanlines, phosphor wash and the corner falloff of a curved tube
- Locked entries say `[LOCKED]` and what to do first, in plain English
- The task card no longer draws over the menu while you are sitting at the screen

**Naming your arcade &mdash; the first thing the game asks you to do &mdash; looks like part of the
game now.** It was a bare label, a default grey text box and two identical grey buttons. It has a
heading, a caption, a framed input in the shopfront's own colours, a live character count, and one
clear primary action.



- **String fix.** A few readouts still counted your takings in "gold" &mdash; the day summary and
  the facade tool among them. Everything that shows money now shows money

## What changed in 0.9.8

**The arcade runs on quarters.** A play used to cost a whole dollar while the machines were called
quarter cabinets. Now a quarter cabinet takes an actual 25&cent;, and every price in the game is
denominated to match &mdash; machines, rent, licences, spares, wages and your own bank balance.

- **A play is 25&cent;**, or 50&cent; and 75&cent; on the bigger cabinets, and the coin readout on a
  machine says so
- Money reads in dollars and cents everywhere &mdash; **$225.00**, not `225`
- The balance is unchanged: every figure was rescaled by the same amount, so the shop earns and
  spends exactly as it did. Only the denomination is different
- **Existing saves are converted automatically** the first time they load

**Patrons walk all the way to a machine before they play.** They were starting the
grip-the-controls, feed-the-coin routine while still short of the cabinet, and reaching for
controls they could not have touched. They now finish the walk, stand on the mark, and play.

**The prize shelf is an arcade prize shelf.** Its collectibles described bonuses for games this
game does not have, and none of them altered anything. They now offer takings, custom and
experience &mdash; and they work.

## What changed in 0.9.7

- **String fix.** The demo notice named the wrong game and offered content this one does not have.
  It now names Arcadius, and offers what Arcadius actually has

## What changed in 0.9.6

**Three fixes to how the arcade behaves and sounds.**

- **Patrons play at human speed again.** The whole grip-the-controls, feed-the-coin, work-the-stick
  performance was running at the day-clock's speed — and the day runs at 2x by default, 4x on the
  fast setting. So a patron walked to a machine at a normal pace and then played it at double
  speed. The performance is now real-time, and looks the same at 1x, 2x and 4x
- **The house music is a background bed, not a support act.** Our own soundtrack was mixed
  fractionally *louder* than the machines themselves and played continuously, so it sat on top of
  the whole room. It is now about 10 dB under the arcade floor — present, but never in the way.
  Your own radio is untouched: if you put your music on, it stays where it was
- Machine and room volumes are unchanged; the faders still work the same way

**Repairing a machine is a job now, not a click.**

- **The dead part has to come out first.** Open the panel a machine's fault is behind and you pull
  the failed unit — the power supply, the board, the tube, the mech. The bay is then visibly
  **empty**, and only then will a replacement go in. Trying to fit one on top of the old unit is
  refused, and tells you why
- The bay you empty is the real one: every cabinet already has its board on a shelf, its power
  supply, its coin mechs and its tube behind the doors that open, and it is that unit which
  disappears — brackets, loom and all still there around the gap
- The prompts follow the two beats, so the machine always tells you which one you are on

## What changed in 0.9.5

**The parked cars are rebuilt.** They were the last blocky thing on the street — literally stacked
boxes, and shorter and taller than any car of the decade. Every vehicle is now built from
looked-up 1980s dimensions and shaped rather than stacked.

- **Five vehicles instead of two** — a full-size sedan, an estate, a compact hatchback, a van and
  a pickup, each to its own measured length, width, height and wheelbase
- **Bodies are shaped, not boxed.** Each one is swept from cross-sections, so every edge is
  chamfered, the nose and tail draw in, and the flanks are flat slab sides with a hard crease —
  no right angles anywhere on the car
- **Real glasshouses.** A raked windscreen you can see the dashboard and steering wheel through,
  dark side glass set into chrome-framed openings, a solid roof and a wide rear sail pillar
- **Built like a car** — chassis rails, silencer and exhaust under the floor; wheels with rims,
  hubs and lug nuts tucked up into their arches; an engine under the bonnet; and a fitted
  interior with a dash, a steering wheel, front seats and a rear bench
- **Period detail** — quad rectangular headlamps flanking a slatted chrome grille, amber lenses
  set into the bumper, wrapped tail lamps and a number plate, 5 mph bumpers with rubber strips,
  body-side mouldings, door shut lines, mirrors and full wheel covers
- The rank outside cycles all five, so no two cars in a row are the same

**Fixes**
- **You could see straight through the parked cars.** The whole cabin was one transparent volume,
  so a car read as a wireframe with furniture inside it. The cab is bodywork now, and only the
  windscreen is glass
- Wheels no longer hang below the bodywork like castors — the rocker sits under the axle line and
  the tyres tuck into the flanks
- Wheel arches read as openings with a rim and a shadow, instead of a flat plate painted on

## What changed in 0.9.4

**The block outside is a real street.** Ten businesses with names, lit signs, interiors you can look
into, flats above them, and both ends closed by real buildings.

- **Studio Cinema** stands opposite your door — marquee with bulb runs, a vertical blade sign,
  poster cases, and a served ticket booth with somebody behind the glass
- **Diner Dash · Soap N Suds · Tower Records · Slices Pizza · Cutz Barber · Rusty's Lounge ·
  Pay & Pawn · Groceries Galore**, and a boarded **For Lease** unit — the frontage your own shop
  started as
- **You can see inside all of them**: booths and a stool counter in the diner, chairs facing mirrors
  in the barber, washer drums and folding tables in the laundromat, browsing bins and a listening
  booth in the record shop. Each has a tiled floor, a ceiling grid, a clock, price boards and a back
  door standing ajar with the back room lit behind it
- **Period signage** — internally-lit acrylic lightboxes, neon for the bar and diner, painted wall
  signs and rooftop hoardings above the shops
- Flats over the shops: sash windows with sills and blinds, string courses, fire escapes, water towers

**Fixes**
- ⛔ **You could fall out of the world.** The pavement was laid in separate strips with nothing under
  the gaps between buildings. The block now has one continuous floor, no slots to walk into, both
  ends closed by buildings rather than an invisible wall — and a body that ends up below the world
  anywhere is put back on the last ground it stood on
- **Placed cabinets can be picked up and moved** — MOVE THIS CABINET on the machine's own panel
- Street furniture no longer stands in front of shop windows

## What changed in 0.9.3

**The arcade has a soundtrack.** Every note of it is generated by our own engine — no samples, no
licensed audio, nothing that can get a stream muted.

- **Six house stations** on the wall radio, in the 80s synth idiom the shop is set in: bright
  attract music, a warm floor bed, late-night synthwave with rain on it, and more
- **Your own music always wins.** Drop files in `Music\Arcadius` and tune to them; the game's own
  soundtrack stands down the moment your radio is on, and comes back when you switch it off
- **A fader for each thing** — master, music, machines, and the arcade's own room noise — reachable
  from the main menu as well as the pause screen
- Every reward, coin and impact sound was re-checked; the ones that hissed were rebuilt

**Fixes**
- ⛔ **You could fall out of the world.** The pavement outside was laid in strips and the gaps
  between the buildings had nothing under them at all. The whole block now has a continuous floor,
  the terraces have no slots to walk into — and, as a backstop, a body that ends up below the world
  anywhere is put back on the last ground it stood on
- **Placed cabinets can be picked up and moved.** MOVE THIS CABINET, on the machine's own panel;
  click to set it down, `R` turns it, `Esc` puts it back where it was. Nothing is charged

## What changed in 0.9.2

**Every one of the 70 machines was checked against a source for the game it is based on** — not
against our own earlier notes, which turned out to be wrong in both directions. Roughly forty
divergences were fixed. The ones a player will actually feel:

**Games that were missing a rule**
- **Missile Command** — the wave multiplier did not exist. Every point is now ×1 up to ×6, plus
  MIRVs that split, smart bombs that dodge your blasts, and bombers crossing the middle
- **Frogger** — there was nowhere to go. Five home bays, the fly, the lady frog, level completion
- **Warlords** — castles died when their bricks went; the warlord *behind* the wall is the target
  now, and there are up to four fireballs
- **Joust** — the pterodactyl arrives if you camp, and egg / survival waves
- **Pengo** — a stunned Sno-Bee can be walked over (it used to kill you back), eggs hatch, and
  crushing several under one block pays far more than crushing them one at a time
- **Track & Field** — the hammer throw was missing, and the card now comes round again, harder
- **Simon** — the tempo steps at the 5th, 9th and 13th signal, five seconds a signal, and the
  8/14/20/31 skill targets, so the game can be *won*
- **Dance mat** — freeze arrows, with a tail you have to hold

**Games that ended wrongly**
- **Tank** now runs on a clock — a knockout costs a point, it does not end the round
- **Blockade** scores a crash and plays on; a match runs to three
- **Head On** restarts the maze instead of ending your run

**Sequels that were wearing the wrong game**
- **Joust 2**'s transform is a button and a *trade* — the horse is bigger and flies worse
- **Time Pilot '84**'s silver craft really are immune to your gun now; you must lock on
- **Hyper Sports** has its own seven events, and **'88 Games** its own eight with heats and finals
- **Tank II** runs a different board setting each round; **Sprint 2** has five real circuits

**Fixes**
- **High scores now exist.** The machines kept a score and never recorded it; every cabinet
  files its own high score and shows it on the glass
- Scoring bugs on two machines where a new record wiped everything else you had earned
- Skee-ball's high score was filed under a name nothing else used

## Controls

| | |
|---|---|
| `W A S D` | move |
| `SHIFT` | sprint |
| `CTRL` / `C` | crouch |
| **left click** | use — machines, the console, the OPEN sign, the radio |
| **right click** | open the build menu |
| `ESC` | step back one page, or open the pause menu |

## Beta notes

**Current build: 0.10.5-beta.** An early build for playtesting. Three things the team most wants
feedback on:

1. **The music.** It is generated rather than composed, so the question is whether it sounds like
   an arcade you would stand around in — and whether any station wears out over an hour.
2. **The mix** — the arcade's own noise against the radio, and whether the faders let you fix
   anything that annoys you.
3. **How a busy evening feels** — do queues read as queues, does the doorway congest?
