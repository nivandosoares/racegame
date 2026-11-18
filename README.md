# Test Drive II - Mode 7 Remake Prototype

Jogo de corrida em estrada feito com JavaScript e HTML Canvas.

**Arquivos principais**

- [index.html](<index.html>)

A playable first-person racing prototype built from this repo as a foundation.

## What this delivers now

- Pseudo-Mode-7 road renderer using per-segment perspective projection.
- In-car style cockpit overlay and SNES-inspired visual palette.
- Curved track segments (left/right), elevation variation, lane strips, rumble edges.
- Basic arcade handling (acceleration, braking, steering, off-road drag).
- Opponent vehicles and simple collision/crash state.
- HUD with speed, distance and current curve value.

## Controls

- `Arrow Up` / `W`: accelerate
- `Arrow Down` / `S`: brake
- `Arrow Left` + `Arrow Right` / `A` + `D`: steer
- `Space`: handbrake
- `R`: restart after crash

## Run

No build step required:

1. Open `index.html` in a browser.
2. Or run a simple static server:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080`.

## Suggested next steps (roadmap)

1. **Replace primitive shapes with sprites**
   - Player dashboard layers, horizon parallax backgrounds, roadside objects, traffic cars.
2. **Track authoring format**
   - Move hardcoded segment generation into JSON (`curve`, `hill`, `length`, biome/theme).
3. **Game rules**
   - Laps/checkpoints, timer, race goals, traffic difficulty curves, damage model.
4. **Vehicle model tuning**
   - Gear simulation, traction loss, weight transfer, per-surface friction.
5. **World systems**
   - Weather/time presets, random encounters (police/traffic), event scripting.
6. **Audio**
   - Engine pitch by RPM, skid sounds, collisions, ambient loops.
7. **UI flow**
   - Title screen, route selection, car select, pause, retry, post-race results.
8. **Production quality**
   - Mobile controls, save/load progression, deterministic replay seeds.

## Code layout (current)

- `index.html`
  - Canvas renderer
  - Mode-7 style road projection and draw loop
  - Car physics/game state
  - UI/HUD and crash overlay

This is intentionally scoped to **core mode-7 driving logic first**, so you can iterate toward a full Test Drive II style game with a clean next-step path.
