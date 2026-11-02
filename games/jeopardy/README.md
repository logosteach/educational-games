# Jeopardy-Style Review Game

A team quiz game for review days. Load your own clues from a CSV file, make teams, and play. Answered squares disappear and scores update automatically.

![Game board](screenshots/2-board.png)

## Quick start

1. **Download** [`jeopardy-app.html`](jeopardy-app.html): click the file, then click the **Download raw file** button (down-arrow icon).
2. **Open** the downloaded file in **Chrome** or **Edge** (double-click it, or drag it into a browser window).
3. **Make teams:** type a team name and add it. Repeat for each team.
4. **Add students** to each team.
5. **Upload your CSV** of clues (or try one from [`samples/`](samples/)).
6. **Play!** Click a square, read the clue, reveal the answer, and award or deduct points.

Your game is saved in the browser automatically, so refreshing the page will not lose your scores.

![Setup screen](screenshots/1-setup.png)

## CSV format

The first line must be this header:

```
category,value,clue,answer,daily_double
```

| Column | What to put |
|--------|-------------|
| `category` | Category name shown at the top of the column |
| `value` | Point value. Leave blank to use the defaults 200, 400, 600, 800, 1000 |
| `clue` | The clue shown to students |
| `answer` | The correct response |
| `daily_double` | `yes` (or `true`/`1`) to make it a Daily Double; otherwise leave blank |

- Up to **6 categories** with **5 clues** each.
- **Final Jeopardy:** use `final` as the category, or `final:Category Name` to show a category name.
- If a clue contains a comma, wrap it in double quotes: `"Hello, world"`.

Example:

```
category,value,clue,answer,daily_double
Python Basics,200,This function displays text on the screen,What is print()?,
Python Basics,400,This keyword starts a loop over a sequence,What is for?,yes
final:Famous Scientists,,He wrote the laws of motion,Who is Isaac Newton?,
```

Spreadsheets work too: build it in Excel or Google Sheets and choose **File > Download / Save As > CSV**.

## Playing online (Zoom, Adobe Connect, Google Meet)

Open the game in its own browser tab, then share **that tab** (or the browser window):

- **Zoom:** Share Screen > choose the browser window. Check **Share sound** so students hear the effects.
- **Adobe Connect:** in a Share pod, choose Share My Screen > Applications or Windows > your browser.
- **Google Meet:** Present now > A tab > pick the game tab (tab sharing includes sound).

![Clue view](screenshots/3-clue.png)
![Daily Double](screenshots/5-dailydouble.png)
![Scoreboard](screenshots/9-scoreboard.png)

## Troubleshooting

- **CSV won't load:** make sure the first line is exactly the header above and the file is saved as `.csv` (UTF-8).
- **Missing squares:** each category needs its own rows; anything past 6 categories or 5 clues is ignored.
- **No sound:** click anywhere on the page once (browsers block sound until you interact), and check that sound sharing is on in your meeting app.
- **Want a fresh start:** use the reset option in the game, or clear the site data in your browser.
- **Odd behavior in Safari/Firefox:** use Chrome or Edge.

## Disclaimer

This is an independent educational tool. It is not affiliated with, endorsed by, or sponsored by *Jeopardy!*, Jeopardy Productions, Inc., or Sony Pictures Television. *Jeopardy!* is a registered trademark of its owner.

## License

MIT. See the [LICENSE](../../LICENSE) file at the top of the repository.
