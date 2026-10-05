# Contributor instructions

Hotkey Forge is a static browser application in index.html with assets alongside it. Verify keyboard and touch practice, local progress, search and reset when changing behaviour.

## Every code change updates the manual

`docs/MANUAL.md` is the plain-English manual for this project, written for the people who use and operate it. Every code change must update the manual in the same commit. Update the affected tasks, exact labels or commands, access rules, limits, troubleshooting and reference entries, and the **Last updated:** line. When a code-only change leaves behaviour unchanged, record that fact and what was checked in the manual's maintenance record rather than inventing a user-facing change. Add a dated, plain-English entry to `docs/RELEASES.md` in that same commit. The file in this repository is the only edition of the manual; there is no separate build or publishing step.

Before a change is ready for review, compare the manual with the final code, verify examples and page/command references, run the project's relevant checks, and name the manual sections updated in the pull request and handover. A code change is not complete until its documentation is current. Preserve the project's existing approval and release rules.
