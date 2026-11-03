# Bar Opening

A single-page tablet checklist for the 7:00 bar opening. It isn't there to pressure the opener. It shows what to do next, makes it easy to go back and forth between customers and prep, and lets an SM or a late starter see at a glance where opening is and help out.

Open `index.html` on the bar tablet ("Add to Home Screen" makes it full screen). Everything is saved on that tablet only, and the list resets itself every morning.

## How it works

- **Four phases** with soft colours based on the time of day: green, then orange, then pastel red (a cue for the SM to help, not an alarm). A phase that's finished turns grey.

  | Phase | Orange | Red |
  |---|---|---|
  | 1. Set up | 7:20 | 7:30 |
  | 2. Drinks prep | 8:30 | 9:00 |
  | 3. Bar prep | 10:00 | 10:30 |
  | 4. Extras | 11:30 | 12:00 |

- **Any order.** "Up next" suggests the most useful next task for each phase.
- **Countdowns for waiting time.** Ticking "Brew 12 tea bags" starts a 12 min timer. When it ends the task comes back as **Ready** with its next step ("put the tea in the fridge"), which then starts the 60 min cooling timer. The tablet plays a soft chime.
- **Learn more / Fiche technique** for each task explains what "done" means, gives tips, and shows the recipe.
- **DLC** dates are calculated automatically (today + 3 days).
- **Note for SM**: one tap ("Bar left dirty", "Piles of deliveries", …) or free text.
- **Weather switch** in Extras: terrace station or back big station.
- **Settings ⚙︎**: chime on/off, reset today, and **Demo mode**: plays 7:00 → 12:00 in 100 seconds (180× speed, timers included: the tea brews in 4 s and cools in 20 s). Demo ticks go into a separate practice list, so a real morning on the tablet is never touched.

## Changing the routine

Everything is in the `PHASES` / `TASKS` block at the top of the script in `index.html`. Each task is plain data: a name, optional `steps` (in order, with an optional `wait` in minutes), `checks` (any order), and `learn` text.
