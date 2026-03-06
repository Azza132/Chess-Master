# Chess Master Pro
### Created by Aaron Sermon

A fully-featured, browser-based chess application with AI opponents, tournaments, post-game analysis, and a personal statistics dashboard. No installation required — open the HTML file in any modern browser and play.

---

## Getting Started

1. Download `chess-ultimate.html`
2. Open it in any modern browser (Chrome, Firefox, Edge, Safari)
3. The game loads instantly — no internet connection required after the page loads

---

## Navigation

The app has three main sections accessible from the top navigation bar:

- **Play** — The chess board and game controls
- **Stats** — Your personal performance dashboard
- **Tournament** — Structured multi-match events

There is also a **Light / Dark mode toggle** in the top-right corner of the nav bar.

---

## Play

### Starting a Game

Use the settings panel on the left side of the board to configure your game before clicking **New Game**.

| Setting | Options |
|---|---|
| Mode | Player vs AI, Player vs Player |
| Side | Play as White, Play as Black |
| Difficulty | Beginner, Intermediate, Advanced, Expert |
| Time Control | 1 Min, 3 Min, 5 Min, 10 Min, Unlimited |

Click **✦ New Game** to begin.

### Moving Pieces

You can move pieces in two ways:

**Click to move**
1. Click a piece to select it — legal moves are highlighted in green
2. Click a highlighted square to move there
3. Rings indicate capture squares, dots indicate empty squares

**Drag and drop**
1. Click and hold a piece, then drag it to your destination square
2. Release to place — works with both mouse and touch input

### Special Moves

- **Castling** — Move your King two squares toward a Rook. The option appears automatically if castling is legal.
- **En Passant** — Highlighted automatically when available after a pawn double-push.
- **Pawn Promotion** — When a pawn reaches the back rank, a dialog appears. Choose Queen, Rook, Bishop, or Knight.

### Board Controls

| Button | Action |
|---|---|
| ↩ Undo | Takes back your last move (and the AI's response in PvAI mode) |
| ⇅ Flip | Rotates the board 180 degrees |
| ↓ PGN | Downloads the current game as a .pgn file |
| 🔍 Analyze | Runs post-game analysis and classifies every move |

### Board Themes

Five board colour schemes are available via the colour swatches in the settings panel:

- **Wood** (default) — warm brown tones
- **Green** — classic tournament style
- **Blue** — steel blue
- **Marble** — grey and white
- **Night** — dark purple tones

### Evaluation Bar and Graph

- The **vertical bar** on the left of the board shifts toward White (top) or Black (bottom) as the position changes.
- The **evaluation graph** in the right panel plots the advantage after every move throughout the game. Gold line above centre means White is ahead; below means Black is ahead.

### Move History and Replay

- All moves are recorded in algebraic notation in the right panel (e.g. Nf3, O-O, exd5+, Qxf7#).
- Click any move in the history list to jump to that position on the board.
- Use the **replay bar** below the board to step through the game:
  - ⏮ Jump to start
  - ◀ Previous move
  - ▶ Next move
  - ⏭ Jump to end
  - Drag the slider to any move
- Click the board while replaying to return to the live position.

### Post-Game Analysis

Click **🔍 Analyze** after a game ends (or during a game) to classify every move:

| Classification | Meaning |
|---|---|
| Best | The strongest move available |
| Good | A sound move, close to best |
| Inaccuracy | A slightly inferior choice |
| Mistake | A significantly weaker move |
| Blunder | A serious error that loses material or position |

Move history entries are colour-coded green through red. A summary of blunders and mistakes is shown in the Analysis panel on the right.

### Sound Effects

The game plays audio cues for:
- Normal moves
- Captures
- Check (two-tone alert)
- Castling
- Pawn promotion (ascending arpeggio)
- Checkmate (dramatic chord)

Sound uses the browser's Web Audio API and requires no audio files.

---

## Stats Dashboard

The Stats tab tracks your performance across every game played and stores the data in your browser's local storage — it persists between sessions.

### Key Statistics

| Stat | Description |
|---|---|
| Games Played | Total number of completed games |
| Wins / Draws / Losses | Results breakdown with percentage bar |
| Avg Accuracy | Estimated accuracy based on move quality across all games |
| Favourite Opening | The opening you have played most often |
| Blunders per Game | Your average blunder count across all games |
| Win Streak | Your current consecutive win or loss streak |

### Charts

- **Opening Frequency** — Bar chart of your most-played openings
- **Results by Difficulty** — Win rate at each AI difficulty level

### Game History Table

A log of your last 20 games showing result, opponent difficulty, opening played, number of moves, blunders, and date.

### Resetting Stats

Click **✕ Reset All Stats** at the bottom of the Stats page to wipe all stored data. A confirmation prompt will appear before anything is deleted.

---

## Tournament

The Tournament tab lets you compete in structured events against four AI opponents:

| Opponent | Difficulty |
|---|---|
| The Squire | Beginner |
| The Knight | Intermediate |
| The Bishop | Advanced |
| The Rook | Expert |

### Tournament Formats

**Round Robin**
Every player faces every other player once. The player with the most points at the end wins. A win earns 1 point, a draw earns 0.5, a loss earns 0.

**Swiss System**
Four rounds are played. Players are paired against opponents with similar scores each round. No one is eliminated — everyone plays all four rounds. Most points wins.

**Knockout**
A four-player elimination bracket:
- Semi-final 1: You vs The Squire
- Semi-final 2: The Knight vs The Bishop
- Final: The two winners face off

Lose once and you are out.

### Running a Tournament

1. Go to the **Tournament** tab
2. Select a format by clicking one of the three format cards
3. Enter your name in the **Your Name** field
4. Choose a time control
5. Click **✦ Start Tournament**

Your matches will automatically switch to the Play view. After each game ends, the result is recorded and the next match begins. AI vs AI matches are simulated automatically.

The standings table updates after every match. Click **✕ Abandon** at any time to exit the tournament and return to the lobby.

---

## Opening Detection

The app recognises 22 common chess openings based on your move sequence. The opening name appears above the board once enough moves have been played to identify it. Examples include:

- Ruy Lopez
- Sicilian Defense
- Italian Game
- Queen's Gambit
- King's Indian Defense
- French Defense
- Caro-Kann Defense
- English Opening
- and more

---

## PGN Export

You can export any game in standard PGN format:

1. Click **↓ PGN** in the left settings panel
2. A `.pgn` file is downloaded automatically
3. The file can be opened in any chess GUI or analysis tool such as Lichess, Chess.com, or ChessBase

---

## Tips

- In **Beginner** mode the AI plays random-ish moves with minimal planning — good for learning.
- **Advanced** (Depth 3) offers a solid challenge for casual players.
- **Expert** (Depth 4) uses deeper search and is considerably stronger — mistakes will be punished.
- Use the **Undo** button freely during casual play to learn from mistakes without restarting.
- After a tough loss, click **🔍 Analyze** to see exactly where the game went wrong.
- The evaluation bar moving sharply in one direction usually means a blunder just occurred.
- In Bullet (1 Min) mode, keep an eye on the clock displayed above and below the board — the timer turns red below 30 seconds.

---

## Browser Compatibility

| Browser | Support |
|---|---|
| Chrome 90+ | Full support |
| Firefox 88+ | Full support |
| Edge 90+ | Full support |
| Safari 14+ | Full support |
| Mobile browsers | Supported (touch drag and drop works) |

All game data is stored in `localStorage`. Clearing your browser's site data will erase your statistics.

---

## Credits

Designed and developed by **Aaron Sermon**

Chess engine built from scratch using Minimax search with Alpha-Beta pruning, piece-square tables, and MVV-LVA move ordering. No external chess libraries used.
