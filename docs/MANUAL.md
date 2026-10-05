# Hotkey Forge manual

**Last updated:** October 5, 2026

Hotkey Forge is a single-page Age of Empires II hotkey trainer. It runs in your browser and stores progress in that browser. It has no sign-in, server account or connection to the game. The built-in bindings are practice material; check your game's own hotkey configuration when they differ.

## 1. Open the trainer

**Where:** [Hotkey Forge](https://seldomsilent.github.io/aoe2-hotkey-forge/) or the repository's `index.html` with its adjacent `assets` folder.

**Who can use it:** Any visitor using a keyboard or touch browser.

### What it's for

The three tabs are **Train**, **Codex** and **Stats**. **Sound** toggles the generated feedback tones. There is no installation or build step for the app.

### How to begin

Open **Train**, choose a practice scope and category, and select **Begin Drill**. Enter also starts a drill when Train is visible and no drill is running. Use **Browse the Codex** if you want to study first.

### Good to know

Progress belongs to the current browser origin and profile. The hosted page and a local copy do not share it. Moving devices, using a private session or clearing site data can leave you with a fresh record. There is no built-in import, export or cloud sync.

## 2. Practise on Train

**Where:** **Train** tab.

**Who can use it:** All visitors; advanced drills require the local unlock.

### What it's for

A card shows the action, its context (for example, which building or selection is active) and a short explanation. Supply the required key combination.

### How to answer

1. Start with **Basic 35** and **All in scope**, or choose a category from the dropdown.
2. Choose **Hint** to highlight the expected keys, or **Blind** to practise without those highlights.
3. Select **Begin Drill**. Press the physical key with exactly the required Ctrl, Shift or Alt modifiers. On touch, toggle the displayed **Ctrl** or **Shift** key first, then tap the main key.
4. Read the feedback. A correct answer records reaction time and advances. A wrong answer displays **The forge demands:** and the expected combination before advancing.
5. Use **Skip** to move past a card. A skip counts as an unsuccessful attempt in accuracy and breaks the streak, but is excluded from the basic unlock window.

Changing category or scope while running draws a new question. Changing Hint/Blind changes the keyboard hints. Modifier toggles clear after a touch answer and when a new card is drawn.

### Good to know

Physical letters are interpreted by keyboard position (`KeyboardEvent.code`); Ctrl also accepts the Command/meta modifier. A browser or operating system may reserve a shortcut. Use the on-screen keyboard for available keys if a physical combination is intercepted. Some reference-only mouse/combined actions are not drill questions.

There is no pause/stop button. **Switching tabs does not stop a running drill**: keyboard input outside the Codex search field can still answer the active card. Reload to end the session; saved lifetime progress remains. Time spent away from a card can affect its next reaction time.

## 3. Unlock Full 100 and understand scoring

**Where:** Train's scope buttons and mastery meter; **Stats** unlock card.

**Who can use it:** Anyone practising in the same saved browser profile.

### What it's for

**Full 100** unlocks after at least 20 non-skipped basic-tier answers, with at least 18 of the most recent 20 correct (90%). The window is shared across basic categories. It is not necessary to answer every basic binding once.

### How to progress

Practise basic cards until the meter reports the unlock, then select **Full 100** yourself. The unlock persists even if later accuracy falls. The fully filled meter then indicates that permanent unlock, not your current accuracy.

Correct answers earn XP; faster correct answers earn more. The Train **Score** also applies a streak bonus, so it differs from XP. Wrong answers and skips earn no XP and reset the current streak. **Avg ms** measures correct answers with recorded reaction times, not all attempts.

| Rank | Total XP required |
|---|---:|
| Dark Age | 0 |
| Feudal Age | 25 |
| Castle Age | 120 |
| Imperial Age | 340 |
| Conqueror | 780 |

### Good to know

Train's Score, Streak, Accuracy and Avg ms describe the current session. Best Streak is saved across sessions. The names Basic 35 and Full 100 describe the binding collections; not every reference entry is eligible for a keyboard drill.

## 4. Look up a binding in Codex

**Where:** **Codex** tab.

**Who can use it:** All visitors, including before the Full 100 unlock.

### What it's for

Codex displays all reference bindings with their description, context and keys. Its advanced entries are readable before advanced training is unlocked.

### How to search

Type an action, key, description or context into **Search actions or keys…**, or select a category chip. Search and category filters work together. Clear the search and choose **All** to restore the complete list. Search is case-insensitive substring matching, not a game-settings import.

Categories are **Navigation**, **Town Center**, **Economy**, **Military**, **Selection**, **Camera & UI**, **Unit Production**, **Upgrades & Techs** and **Construction**. Read the context: the same key can perform different actions with different selections.

### Good to know

The Codex search field is exempt from drill key capture, so typing there does not answer cards. If a drill is running, clicking elsewhere and pressing a key may resume answering it. The app does not remap keys in Age of Empires II.

## 5. Review or reset Stats

**Where:** **Stats** → **Your Mastery**.

**Who can use it:** Anyone using that browser profile.

### What it's for

Stats shows the saved rank/XP, unlock status, **Total Drills**, overall **Accuracy**, **Best Streak**, **Avg Reaction**, **Keys Mastered**, and **Mastery by Discipline**. Discipline percentages are lifetime correct answers divided by attempts, including skips.

### How to read the record

Compare accuracy and reaction time over repeated practice. Keys Mastered records a key/category/context after one correct answer; it is not a repeated-proficiency test. Its identity groups by main key, category and context, so it is not necessarily one unique record per Codex card.

### How to start over

Select **Reset all progress** and read the confirmation. Confirming clears XP, ranks, unlocks, lifetime statistics and the basic mastery history, and returns the scope to Basic 35. Sound preference stays as it was. Cancellation keeps progress. There is no undo or built-in backup. Reset does not provide a pause control; reload as well if you want to end a running drill.

## 6. Troubleshoot and maintain the app

**Where:** Browser and repository root.

**Who can use it:** Players and contributors.

| Symptom | What to check |
|---|---|
| Full 100 remains locked at 90% | The meter must contain 20 qualifying answers. Skips do not fill that window. |
| A right-looking key is marked wrong | Check context and every modifier. Physical letters use key position. Compare the on-screen key. |
| Progress disappeared or is not retained | Check browser profile/origin, private browsing and storage restrictions. Storage failures are silently ignored by the app. |
| No sound | Toggle Sound on, interact with the page, and check browser/device audio permissions and volume. |
| Missing icon | Keep the `assets` directory next to the HTML file. Failed icons fall back to an emoji. |
| Game binding differs | Consult the game's own configuration; the trainer's list is fixed in source. |

### How to maintain it

The app's markup, styles, binding data and JavaScript live in `index.html`; images live in `assets`. There is no package manager, compiled build or committed test suite. Preview changes in a browser and check Train's correct/wrong/skip behaviour, the 20-answer unlock, search/category filtering, saved progress after reload, reset confirmation and touch modifiers. Update this manual and [Releases](RELEASES.md) in the same commit as every code change; see [AGENTS.md](../AGENTS.md). No manual-generation command is included.

## Maintenance record

- **October 5, 2026:** Created this manual from the current HTML and JavaScript. Verified tab controls, unlock criteria, score/stat definitions, local storage, reset and the running-drill behaviour across tabs.
