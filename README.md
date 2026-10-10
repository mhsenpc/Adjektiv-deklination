# Adjektivdeklination Trainer

A small browser game for practising German adjective endings. It is a single HTML file with no build step and no dependencies.

**Play online:** https://mhsenpc.github.io/Adjektiv-deklination/index.html

Each round loads one declension table with every cell filled in except one. You pick the missing adjective ending from a dropdown, for example `dem rot[▾] Heft` → `-en`.

## Tables

| Table | Columns |
|---|---|
| Nach bestimmtem Artikel | der · die · das · die (Pl.) |
| Nach unbestimmtem Artikel | ein (der) · eine (die) · ein (das) · Plural without article |
| Nach Possessivpronomen | dein (der) · deine (Sg.) · dein (das) · deine (Pl.) |

Each table covers Nominativ, Akkusativ, Dativ and Genitiv, which gives 48 cells across the three tables. The vocabulary is fixed: *blauer Becher*, *grüne Hose*, *rotes Heft*, *blauer Kamm*, plus their plurals.

## How to play

1. Open `index.html` in a browser, or use the online version linked above.
2. Pick the ending in the highlighted cell: `-e`, `-en`, `-em`, `-er` or `-es`. You can also press keys `1` to `5`.
3. You see the correct form and a short rule for that table. Press `Enter` or click **Weiter** for the next round.

Use the **Tabelle** menu to practise all three tables mixed or just one of them.

## Adaptive practice

Every cell has a mastery level from 0 to 5:

- A correct answer raises the level by 1.
- A wrong answer resets it to 0.

The next question is drawn at random, weighted towards weak cells:

- Cells at a low level are picked much more often than mastered ones.
- Cells you have never seen get a high weight, so new material shows up early.
- A higher error rate and a wrong last answer both increase the weight.
- The cell you just answered is almost never repeated right away.

Click **Mein Verlauf anzeigen** to show a colour map of all 48 cells (not seen / weak / improving / mastered) and your most frequent mistakes.

## Data storage

Progress is saved in the browser's `localStorage`. It stays on that browser on that device, and clearing site data or using a private window removes it. **Verlauf löschen** resets everything.
