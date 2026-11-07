# Physics Billiards 🎱

**v1.40**, build 2026-11-07 13:20 UTC, by **Şenol Gülgönül**

A browser billiards game built on a real rigid-body model of ball and cloth — no game engine, no install, one HTML file.

**▶ Play:** https://senolgulgonul.github.io/bilardo/

## What makes it different

- **Sliding → rolling physics.** A center-ball hit slides first; cloth friction spins the ball up until it rolls at exactly 5/7 of its initial speed.
- **Follow, draw and english emerge from the physics.** Nothing is scripted: each ball tracks its full 3D angular velocity, and friction converts leftover spin into motion after impact.
- **Exact path prediction.** While aiming, the shot is simulated ahead with the same fixed-step engine, so the drawn path *is* the shot: your ball’s route, contacts, cushion count, and whether the object ball drops.
- **Game modes:** 8-ball (two players), free practice, carom, and three-cushion.
- **Tunable physics:** cloth friction, rolling resistance, cushion and ball restitution.

## How to play

Tap or drag on the table to aim, set power with the slider, pick a contact point on the small ball beside the power slider for spin, then press **Shoot** (or Space). Arrow keys fine-tune the aim.

## Model notes

- 9 ft pool table (2.54 × 1.27 m, 57.2 mm balls); carom table 2.84 × 1.42 m, 61.5 mm balls.
- **The carom table is calibrated on a real match**, the 2019 World Championship quarter-final Tran Quyet Chien – Semih Sayginer, tracked frame by frame in the overhead broadcast and checked link by link:
  - cue stroke and cloth: sliding friction 0.20, rolling resistance 0.005 (171 s of free rolling); from the stroke to the first contact the engine follows the real cue ball to 0.2–1.7 mm and its speed to 1–3 %;
  - ball–ball: restitution 0.98 with a small speed-dependent friction (“throw”, after Alciatore & Marlow), confirmed on 34 collisions; a ball set moving from rest loses a fixed 0.033 m/s;
  - cushions: the ball touches the cushion above its centre and the cloth below it at the same time, and both act together during the impact (two-contact model after Mathavan, Jackson & Parkin 2010), official 37 mm nose, restitution 0.90, cushion friction 0.20; 52 cushion hits of the match are reproduced to 1.4 % of the speed (median).
  - The default break is Tran’s: the engine follows all three balls to about 5 cm over fifteen seconds.
- The pool table keeps textbook values (sliding 0.2, rolling 0.01, ball–ball 0.95, single-impulse cushion 0.75 / 0.14 at the WPA nose height); no pool data was measured.
- Integrated at fixed 1 ms steps for determinism.
- Browser-independent: the physics uses only +, −, ×, ÷ and square root, which JavaScript computes bit-identically everywhere (IEEE 754). Sine, cosine, atan2 and hypot come from the engine’s own short formulas instead of the browser’s Math library, which differs between Chrome, Firefox and Safari in the last digit. So a shot or a recording plays out exactly the same in every browser and on every device.
- Not modeled: squirt and swerve, airborne balls, pocket jaw rattles.

## Running locally

Just open `index.html` in a browser. To host it: push to GitHub → Settings → Pages → deploy from the `main` branch.

## Credits

Made by **Şenol Gülgönül**. Idea, rules and design direction by Şenol; code written together with Claude (Anthropic).

See [CHANGELOG.md](CHANGELOG.md) for version history.
