# Changelog

All notable changes to Physics Billiards are listed here.
Versioning: MAJOR.MINOR (e.g. 1.1 for new features, 2.0 for big changes).

## v1.40 (2026-11-07 13:20 UTC)

- The contact-point ball (where the cue tip strikes) sits beside the power slider in the side panel, without a caption; the slider moves left to make room. Its drawing and click picking scale with its displayed size (84 px on desktop, 64 px on narrow screens, 52 px on phones in landscape). The panel below the table keeps the usage note

## v1.39 (2026-11-07 10:39 UTC)

- Default carom break set to the stroke that best reproduces the tracked break: power 37 % (the measured speed), aim 188.27°, right english 0.19, follow 0.39, fitted to the three balls' paths over 15 s (measured directly: 188.37°, 0.21, 0.335). The engine now follows the real break to 5 cm on average (was 20 cm with the measured values); the white and the yellow stop within 1 and 3 cm of their real end positions. It still scores in carom and three-cushion

## v1.38 (2026-11-07 09:48 UTC)

- Carom cushions: two-contact impact (Mathavan, Jackson & Parkin 2010). The ball touches the cushion above its centre and the cloth below it at the same time; the impact is followed in small steps of normal impulse, with Coulomb friction at both contacts and energetic restitution. Restitution 0.90, cushion friction 0.20, cloth 0.20, official 37 mm nose. On 24 object-ball cushion hits measured in the match video the speed and direction balls roll away with show no systematic error (single impulse: 3.1° too wide and 3 % too slow). Nine head-on hits roll away at 0.577 ± 0.002 of their speed in the video; the model gives 0.57–0.59
- Break, four stroke values fitted to the three balls' tracked paths over 15 s: mean error 6.7 → 5.0 cm, median 2.9 → 2.3 cm; yellow ends 0.5 cm and white 1.1 cm from where they stopped in the video. The default break keeps the measured stroke and still scores. Pool keeps the single-impulse cushion

## v1.37 (2026-11-07 09:08 UTC)

- The carom table is laid out as in the overhead broadcast: red on the left, yellow on the right, the cue ball 18.25 cm above the yellow; the default break is now played at 188.37°. Physics is symmetric, so only the view turns. Recordings made with earlier versions replay from the new layout and will differ
- A ball set moving from rest by another ball loses a fixed 0.033 m/s (carom only), measured directly on 34 collisions of the tracked match (0.034 ± 0.004 m/s, independent of the impact speed). Ball–ball restitution 0.98 and the speed-dependent throw were confirmed on the same collisions

## v1.36 (2026-11-07 06:41 UTC)

- Carom rolling resistance 0.005 (was 0.006). Slow-rolling balls in the tracked match decelerate less than the earlier average suggested (0.0047–0.0050 below 0.6 m/s, 34 stretches). In the default break the cue ball now follows the real one to 2.3 cm, and the balls' travel lengths and times come closer to the video (yellow stops at the same moment, the red travels 5.4 m instead of 4.9 m; real 6.4 m)

## v1.35 (2026-11-07 06:26 UTC)

- Fix: in the carom break the cue ball now sits 18.25 cm beside the spot ball, as the rules require (it was 15.25 cm, the old US "six inches"). The tracked match confirms it: the video shows 17.5–18 cm
- Carom cushions recalibrated link by link, with the cue stroke (measured from the cue ball's approach) and the ball–ball impact fixed: restitution 0.76, cushion friction 0.20, contact at the official 37 mm nose (UMB; Kleber P37 / Vector profile). On twelve cushion hits of object balls the error after the cushion drops from 2.4 to 1.9 cm. The higher "effective" contact point of v1.26–v1.34 had been compensating the wrong break position
- Default break set up only from measured values: aim 8.37°, power 37 %, right english 0.21 (from the cue stick), follow 0.335 (from the approach). It follows the real break to about 3 cm over six seconds and scores, in carom and in three-cushion

## v1.34 (2026-11-07 05:41 UTC)

- The Han (2005) reference model is removed from the game again; it stays in the project notes as literature. What it confirms (ball–ball restitution 0.98, a cloth faster than 0.010) was already in the calibrated model; what differs (cloth friction 0.069, frictionless ball impacts, speed- and angle-dependent cushions, two-phase spin decay) did not improve the fit to the tracked match. Physics unchanged from v1.32

## v1.33 (2026-11-07 05:27 UTC)

- Reference model: the physics settings can switch to the published carom model of Han (2005, J. Mech. Sci. Tech. 19, 976–984), with its coefficients as published: cloth friction 0.069, frictionless ball–ball impacts (e 0.98), cushion restitution e = 0.39 + 0.257 V − 0.044 V², cushion friction μ = 0.471 − 0.241 θ, contact point 9.25 mm above the ball centre (as a fraction of the radius), rolling and spin resistance from the measured moments. The sliders do not apply to it; recordings remember which model they were made with
- On the tracked world-championship shots the calibrated model follows the real paths about four times more closely than the reference (break: 2.1 cm vs 8.3 cm; three independent drawn paths over three cushions: 12 mm vs 51 mm). Refitting Han's coefficients to the same table brings it to 5.6 cm and 18 mm, still behind; the video also shows the cloth friction is about 0.2 (not 0.069) and that throw is small but not negligible

## v1.32 (2026-11-07 05:11 UTC)

- Carom cloth: rolling resistance 0.006 (was 0.010), measured on 61 stretches where a ball rolled freely for more than 0.7 s in three parts of the match (median 0.0057, half of the values between 0.0051 and 0.0072). Pool keeps 0.010
- Carom cushions refitted with that cloth to the timing of the real break: restitution 0.76, cushion friction 0.19, effective contact height 0.75 (v1.31: 0.77, 0.19, 0.71). The old values had partly made up for the too-slow cloth. Checked on three independent drawn paths of the broadcast: over three cushions the new set follows them to 12 mm in total (v1.31: 16 mm)
- Default break: aim 7.20°, power 37 %, right english 0.18, follow 0.29. The cue ball follows the real break to 2.0 cm on average, frame by frame over six seconds, and scores; it scores from 6.87° to 7.61°

## v1.31 (2026-11-06 22:00 UTC)

- Throw now depends on the sliding speed at the contact (Alciatore & Marlow curve: about 0.1 when slow, 0.02 at 2 m/s) instead of a fixed 0.09. Over ten tracked shots from three parts of the match the object ball leaves on average about 1° (±2°) closer to the cue ball's direction than the line of centres, which this model predicts; a fixed 0.09 predicts 4–5°
- The carom cushions of v1.26 were re-checked on three independent broadcast traces (the drawn path of the cue ball, accurate to about 2–3 mm): over three cushions they follow the traces twice as closely as the v1.25 cushions; small variations of the parameters do not do measurably better
- The default break is refitted to the first contact with the new throw: aim 7.20°, power 37 %, right english 0.21, follow 0.34. The cue ball follows the real break to 1.5 cm on average (3.5 cm at most) and now scores, without tuning the end of the shot

## v1.30 (2026-11-06 20:08 UTC)

- Every slider and checkbox opens at its default on every load, in every browser (Firefox used to restore the last values on reload). The physics was already identical in all browsers; this makes the starting settings identical too

## v1.29 (2026-11-06 20:06 UTC)

- Ball–ball friction ("throw"): when two balls collide their surfaces rub, which pushes the object ball off the line of centers and changes both spins. Friction 0.09, measured from the first contact of the tracked break: with it the red leaves at −16.9° (video −16.8°, before −21.6°) and both balls' speeds and directions just after the contact match the video
- Carom ball–ball restitution 0.98 (measured; pool keeps 0.95)
- The default carom break is now fitted only to the first contact (aim 7.28°, power 38 %, right english 0.21, follow 0.34). In the engine it misses the yellow by a hair: small differences grow over six seconds, and we deliberately do not tune the break to the later part of the shot
- Fix (v1.28): in carom, New game during a moving shot did not reset the moving state

## v1.28 (2026-11-06 19:49 UTC)

- The carom break is now set up as Tran Quyet Chien played it in the 2019 World Championship quarter-final (tracked from the overhead video): aim 7.32°, power 36 % (2.8 m/s), right english 0.21, follow 0.34. Press Shoot and the engine follows the real cue ball path to about 2 cm. It scores from about 7.01° to 7.57°, a window five times wider than a center-hit break. After the break, power and spin go back to 65 % and center hit
- With the rule rack position (white 15.25 cm beside the yellow) the break aim agrees with the cue stick measured in the video (7.2°–7.7°); the 8.10° of v1.27 came from a 2.7 cm error in the measured start position

## v1.27 (2026-11-06 19:41 UTC)

- Fix: side spin was applied the wrong way round since v1.0. Left english now spins the cue ball clockwise seen from above (the left side is pushed forward) and it comes off a cushion to the left, right english to the right. Found while checking the tracked match: the cue stick in the video shows right english of 0.22 R, and the earlier fit had found the same amount with the opposite label. The cushion calibration of v1.26 is unaffected; recordings made with side spin in older versions replay with the spin reversed

## v1.26 (2026-11-06 19:20 UTC)

- Carom cushions recalibrated on real match data. A world-championship break was tracked frame by frame; with its aim (8.10°, from two independent video measurements) and speed (2.8 m/s) fixed, the cushion model was fitted to the cue ball's path: restitution 0.77, cushion friction 0.19, effective contact height 0.71. The engine now follows the real break to about 2–3 cm over six seconds (before: about 30 cm), and reproduces a different shot of the same match with half the error (RMS 9 cm instead of 22 cm). Cloth friction from the video matched the existing defaults. Pool cushions unchanged
- Because the cushions changed, carom aim recipes change too: at 65 % the break now scores at about 7.94°–8.04° and 8.30°–8.39° (7.80° no longer scores)

## v1.25 (2026-11-06 18:48 UTC)

- Cushion restitution now depends on the table: 0.85 on carom tables (calibrated from 28 cushion impacts tracked in an overhead video of a world-championship three-cushion match), 0.75 on pool tables. The default is set when the table type changes; your own setting survives New game. Replays restore the recorded physics. The 65 %, 7.80° break still scores (window about 7.68°–7.86°)

## v1.24 (2026-11-04 07:30 UTC)

- The game now opens in carom (straight rail, three balls) instead of 8-ball

## v1.23 (2026-11-04 07:28 UTC)

- Physics is now identical in every browser: the engine no longer uses the browser's sin, cos, atan2, hypot and pow (they differ between Chrome, Firefox and Safari in the last digit, and billiards amplifies that). It uses its own formulas built only from +, −, ×, ÷ and square root, which are exact in every browser. Recordings and aim recipes now replay the same everywhere. Results differ from v1.22 only in the last digits, but recordings made with older versions may play differently after a few shots

## v1.22 (2026-11-04 06:46 UTC)

- Default power is now 65% (5.2 m/s) instead of 45%: with a center hit the cue ball still slides when it reaches the first ball almost anywhere on the table, so paths are clean and predictable

## v1.21 (2026-11-04 06:42 UTC)

- Recordings as files: "Download recording" and "Load recording" below the table (Game panel). The file name has the mode and the local date and time, e.g. physics-billiards-carom-20261104-0645.json
- Pressing ● when a game is already saved asks before overwriting it
- Removed the live readout row under the table (cue ball speed, motion state, spin)

## v1.20 (2026-11-04 06:34 UTC)

- Title and version always stay on one line: the title shrinks to fit the column, whatever the font
- Slightly shorter power slider, so the recorder buttons fit on screen on shorter laptop screens

## v1.19 (2026-11-04 06:32 UTC)

- Recorder: ● records every shot of a game from a fresh rack (aim, power, spin, cue ball position), ▶ replays the whole game exactly, ❚❚ pauses the balls (also during normal play), ■ stops. The last recording is kept in the browser. During a replay the shot controls are locked
- Title and version share one line in the right column

## v1.18 (2026-11-04 06:20 UTC)

- Aim readout: the cue angle is shown between the two rotate buttons (↺ 7.63° ↻), in degrees with two decimals, 0° toward the right short rail and counter-clockwise. Each button press changes it by exactly 0.1°, so a shot can be written down and repeated exactly

## v1.17 (2026-11-03 19:22 UTC)

- Fix (carom and three-cushion opening rule): the opening shot must hit the red ball directly, with no cushion before it (UMB world rules art. 23.3, USBA). Before, a cushion-first shot that reached the red before the yellow was wrongly counted as legal. The predicted path's "point ✓" follows the same rule

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
