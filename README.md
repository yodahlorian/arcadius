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
- A wall radio: three built-in stations, or drop your own `.mp3` / `.ogg` into the
  game's `music` folder and tune to them
- Rent falls due every 30 days. That is the only way to lose

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

**Current build: 0.9.2-beta.** An early build for playtesting. Three things the team most wants
feedback on:

1. **Do the games feel like the games they are based on?** Every machine on the floor was rebuilt
   this pass against a real source for its original, not from memory.
2. **How a busy evening feels** — do queues read as queues, does the doorway congest?
3. **The sound mix** — the arcade's own noise against the radio.
