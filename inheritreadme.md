# IDENTITRIS

A retro, Tetris-themed sorting game built from two readings on identity, ethnicity,
and race:

- Conzen, Gerber, Morawska, Pozzetta & Vecoli, "The Invention of Ethnicity: A Perspective from the U.S.A." (1992)
- Audrey Smedley, "'Race' and the Construction of Human Identity" (1998)

A historical moment falls toward the floor like a Tetris piece. Steer it into the
**FLUID** lane (identity treated as acquired, situational, changeable — ethnicity
as both articles describe it) or the **FIXED** lane (identity treated as
hereditary, permanent, ranked — the modern invention of "race") before it lands.

Sort correctly for a "line clear." Sort wrong three times and you "top out" —
game over, just like the real thing.

## Controls

- **← / →** or **A / D** — steer between lanes
- **↓** or **S** — soft drop (hold to fall faster)
- **Space** — hard drop
- On-screen buttons work too, for mobile/touch

## Play it

Just open `index.html` in a browser — no build step, no dependencies (it does
pull the "Press Start 2P" pixel font from Google Fonts over the network, so an
internet connection is needed for the full look; everything else works offline).

## Deploy to GitHub Pages

1. Create a new repo (e.g. `identitris`) and push these files to it.
2. In the repo, go to **Settings → Pages**.
3. Under "Build and deployment," set **Source** to `Deploy from a branch`,
   branch `main`, folder `/ (root)`.
4. Save. Your game will be live at:
   `https://<your-username>.github.io/identitris/`

## Structure

- `index.html` — everything: HTML, CSS, and JS in one file, no dependencies
  beyond the Google Font link.
- The `cards` array near the top of the `<script>` tag holds all the game
  content — edit or add entries there to expand the deck. Each card has:
  - `year` — short date label shown on the piece
  - `short` — brief text shown on the falling piece itself
  - `text` — full quote/description shown in the feedback panel after landing
  - `answer` — `"fluid"` or `"fixed"`
  - `explanation` — why, shown after landing
  - `source` — which article it's drawn from

## Possible extensions

- Add more pieces/cards to lengthen a run
- Add a combo/streak multiplier for consecutive correct answers
- Add a leaderboard via `localStorage`
- Add actual tetromino shapes (L, T, I, etc.) instead of a plain rectangle
- Add a "hold" piece or preview of the next card, like real Tetris
