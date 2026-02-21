# Test Drive II - Mode 7 Remake Prototype

Playable, browser-only pseudo-Mode-7 racer focused on **in-car perspective** and **working road curvature dynamics**.

## Current status

This version is tuned as a stronger gameplay base:

- Segment-based pseudo-3D road renderer with proper camera projection.
- Curves and hills that both render correctly and affect steering.
- In-car cockpit/HUD presentation inspired by SNES era visuals.
- Traffic opponents with movement, lane drift, and collision crash state.
- Arcade handling loop with throttle, brake, handbrake, off-road penalties.

## Controls

- `Arrow Up` / `W`: accelerate
- `Arrow Down` / `S`: brake
- `Arrow Left` / `A`: steer left
- `Arrow Right` / `D`: steer right
- `Space`: handbrake
- `R`: restart after crash

## Run

Open directly:

1. Open `index.html` in your browser.

Or serve locally:

```bash
python3 -m http.server 8080
```

Then navigate to `http://localhost:8080`.

## Next recommended steps

1. Replace primitive traffic/cockpit shapes with sprite layers (dashboard, mirrors, cars, roadside props).
2. Move track definition into JSON sections (`enter`, `hold`, `leave`, `curve`, `hill`) for easier course design.
3. Add race game loop (checkpoint timer, stage progression, fail/clear conditions).
4. Improve collisions (relative speed damage, knockback, temporary spinout behavior).
5. Add audio layer (engine RPM pitch, skid, collision, ambient desert wind).
6. Build front-end flow (title screen, route select, pause menu, result screen).
