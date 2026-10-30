# Physics Billiards 🎱

**v1.4**, build 2026-10-30 21:34 UTC, by **Şenol Gülgönül**

A browser billiards game built on a real rigid-body model of ball and cloth — no game engine, no install, one HTML file.

**▶ Play:** https://senolgulgonul.github.io/bilardo/

## What makes it different

- **Sliding → rolling physics.** A center-ball hit slides first; cloth friction spins the ball up until it rolls at exactly 5/7 of its initial speed.
- **Follow, draw and english emerge from the physics.** Nothing is scripted: each ball tracks its full 3D angular velocity, and friction converts leftover spin into motion after impact.
- **Exact path prediction.** While aiming, the shot is simulated ahead with the same fixed-step engine, so the drawn path *is* the shot: your ball’s route, contacts, cushion count, and whether the object ball drops.
- **Game modes:** 8-ball (two players), free practice, carom, and three-cushion.
- **Tunable physics:** cloth friction, rolling resistance, cushion and ball restitution.

## How to play

Tap or drag on the table to aim, set power with the slider, pick a contact point on the small cue-ball diagram for spin, then press **Shoot** (or Space). Arrow keys fine-tune the aim.

## Model notes

- 9 ft pool table (2.54 × 1.27 m, 57.2 mm balls); carom table 2.84 × 1.42 m, 61.5 mm balls.
- Sliding friction μ ≈ 0.2, rolling resistance ≈ 0.01, ball–ball e ≈ 0.95, cushion e ≈ 0.75.
- Integrated at fixed 1 ms steps for determinism.
- Not modeled: squirt, throw, airborne balls, pocket jaw rattles.

## Running locally

Just open `index.html` in a browser. To host it: push to GitHub → Settings → Pages → deploy from the `main` branch.

## Credits

Made by **Şenol Gülgönül**. Idea, rules and design direction by Şenol; code written together with Claude (Anthropic).

See [CHANGELOG.md](CHANGELOG.md) for version history.
