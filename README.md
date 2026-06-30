# APEX // deckbuild

A solo, single-player racing **deckbuilder** prototype. Pick a motorsport category, then race the same field around **Mount Panorama, Bathurst** — managing tyre wear, car damage and a limited hand of cards across two laps.

It's one self-contained HTML file. No build step, no dependencies, no server — just open `index.html`.

## The idea

Racing is resource management stretched over a race distance; a deckbuilder is resource management stretched over turns. They're the same shape. So:

- **Tyre wear is deck degradation.** Push a corner past its grip limit and you jam dead *Worn Tyre* cards into your deck — faster now, weaker later.
- **Each category is an asymmetric faction** drafting from a shared core plus signature cards.
- **The track is the balance lever.** Bathurst is all tarmac, so it favours the circuit cars and leaves the Rally deck out of its element — by design.

## Factions

- **GT3** — the control deck: steady racecraft and tyre management.
- **IndyCar** — the all-rounder: limited Push-to-Pass boost charges and a setup that ignores surfaces.
- **Rally** — the surface specialist: reads the road and gambles for pace, but its weapons backfire on smooth tarmac.

## Mechanics

- **Energy / hand** — draw 5 a sector, spend energy, resolve, redraw.
- **Wear** — Worn cards clog the deck; clear them at the pits or with Lift & Coast.
- **Damage** — a separate meter. The risky **Lunge** card can make contact, and the fragile F1 grounds out down **The Dipper**. Damage drags you back every sector until you box and repair.
- **Pit (Box)** — clears wear (−5) and repairs damage (−9), at a cost in track position.
- **Live timing tower** — gaps shown in seconds to the car ahead.
- **Circuit map** — all cars plotted live, spaced by their gaps.

## Tuning knobs (top of the `<script>` block)

- `LAPS` — race length.
- `GAP_SCALE` — how distance converts to seconds on the timing tower.
- `BATHURST[]` — the track: each sector's type, grip limit and surface.

## Status

Prototype. Single race only — the next step is a between-race draft and a calendar of tracks to turn it into a full roguelike run.
