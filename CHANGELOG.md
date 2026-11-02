# Changelog

All notable changes to Physics Billiards are listed here.
Versioning: MAJOR.MINOR (e.g. 1.1 for new features, 2.0 for big changes).

## v1.16 (2026-11-02 07:32 UTC)

- The "point ✓" label sits above the contact with the second ball instead of at the end of the path, so it no longer lands on top of a ball

## v1.15 (2026-11-02 07:28 UTC)

- Aiming guide: a faint dashed line extends the cue line to the rail and shows the diamond it points at (long rails 0–8, short rails 0–4), so a shot found here can be aimed on a real table

## v1.14 (2026-10-31 07:23 UTC)

- Phones in landscape: shorter power slider so Shoot and New game fit on screen without scrolling

## v1.13 (2026-10-31 07:19 UTC)

- iPhone landscape: score cards use a simple flex layout instead of grid, so the group name and potted balls stay inside their card (Safari drew them far below)

## v1.12 (2026-10-31 07:13 UTC)

- iPhone landscape fixes: the power slider is vertical on iOS Safari too (a rotated horizontal slider, since Safari does not draw vertical sliders); score cards no longer get squeezed, so "Table open" stays inside its card; the right column uses the visible screen height

## v1.11 (2026-10-31 07:07 UTC)

- Phones in landscape: the table fills the screen height with a compact control column on the right (scores, power, fine aim, Shoot, New game; status and mode scroll below). Respects the iPhone notch. Desktop and portrait layouts are unchanged

## v1.10 (2026-10-31 06:13 UTC)

- Carom and three-cushion: official opening rule. The opening shot must hit the red ball first, otherwise it scores no point; the predicted path only shows "point ✓" for a legal opening

## v1.9 (2026-10-31 06:03 UTC)

- Physics: cushions now touch the ball above its center, at the official nose height (pool 63.5% of the ball, WPA; carom 60.2%, UMB 37 mm). Cushion friction (μ ≈ 0.14) now acts on all three spin axes, so cushions also change follow and draw. Balls bend less after a cushion than before, and rebound angles and side-spin effects are based on friction instead of a fixed factor
- The model notes on the page and in the README describe the cushion model

## v1.8 (2026-10-31 05:19 UTC)

- New game button sits right under Shoot; mode menu below it, status message at the bottom of the right column
- Fix: removed a leftover layout rule that broke the layout on screens 901–1000 px wide

## v1.7 (2026-10-31 05:15 UTC)

- Even bigger table: the right column is narrower (150 px) with smaller controls, and the status message moved into it, so the table can use the full screen height (about 10% bigger on a typical laptop)

## v1.6 (2026-10-31 05:09 UTC)

- Bigger table: it now sits on the left and fills the screen; everything else moved to one narrow column on the right (title, compact score cards, power, fine aim, Shoot, mode, New game). The status line sits right under the table. Balls and table keep their true proportions

## v1.5 (2026-10-31 05:03 UTC)

- New layout: the table is as large as the screen allows; title, version, scores, status, mode and a New game button sit on the left, and a vertical power slider, fine aim and Shoot on the right. Spin, settings and explanations stay below the table. On narrow screens everything stacks
- New game button replaces Re-rack, no page refresh needed
- 8-ball: while the table is open, balls already potted (e.g. on the break) are shown under the score cards

## v1.4 (2026-10-30 21:34 UTC)

- Stronger top power: maximum shot speed is now 10 m/s (was 7.5); low and mid power feel the same, only the top of the slider is stronger. Breaks now pocket balls far more often
- Fine aim buttons now turn 0.1° (was 0.2°)
- 8-ball: the status line always says which balls went in, including on the break and on fouls, and notes when the 8-ball is respotted after the break

## v1.3 (2026-10-30 21:12 UTC)

- Removed the head string line from the pool table for a cleaner look; on the break, the shaded area still shows where the cue ball can go

## v1.2 (2026-10-30 21:04 UTC)

- Fix: Shoot did nothing in carom modes when the page loaded straight into carom (e.g. after a browser reload restored the mode menu)
- Reloading the page now always starts in 8-ball

## v1.1 (2026-10-30 20:50 UTC)

- Fix: Shoot button stayed disabled after a finished game when switching mode or re-racking without a page refresh

## v1.0 (2026-10-30 20:30 UTC)

First public release, by Şenol Gülgönül.

- Sliding → rolling ball physics with full 3D spin (follow, draw, english)
- Exact shot path prediction using the same fixed-step engine
- Object ball path and “in” / “scratch” indicators for pool
- Modes: 8-ball (two players), free practice, carom, three-cushion
- Tunable physics: cloth friction, rolling resistance, cushion and ball restitution
