# ⚔️ Hotkey Forge

A hyper-slick, zero-dependency web app for mastering **Age of Empires II: Definitive Edition** hotkeys.

**Live:** https://seldomsilent.github.io/aoe2-hotkey-forge/

## What it does
- **Train** — flashcard drills that detect your real key presses, measure reaction time, track streaks, and reward speed. Hint mode lights up the on-screen keyboard; Blind mode tests pure recall.
- **Codex** — a searchable, categorized reference of every binding (Navigation, Town Center, Economy, Military, Selection, Camera & UI).
- **Stats** — accuracy, average reaction time, best streak, per-discipline mastery, and an Age-themed rank ladder (Dark Age → Conqueror) with XP, all persisted in `localStorage`.

## Tech
A single self-contained `index.html` — vanilla JS, Web Audio for SFX, a canvas ember background, no build step, no dependencies. Works on desktop (physical keyboard) and touch (tap the on-screen keys).

## Notes
Bindings reflect AoE II:DE default & competitive-standard hotkeys (Grid layout). In-game hotkeys are fully customizable under **Options → Hotkeys**. Not affiliated with or endorsed by Microsoft, Xbox Game Studios, or Forgotten Empires.
