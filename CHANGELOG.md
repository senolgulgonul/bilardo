# Changelog

All notable changes to Physics Billiards are listed here.
Versioning: MAJOR.MINOR (e.g. 1.1 for new features, 2.0 for big changes).

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
