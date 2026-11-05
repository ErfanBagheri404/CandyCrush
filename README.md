# Candy Crush (vanilla JS)

A 9x9 match-3 board in plain JavaScript. Drag a candy onto a neighbour to swap
them; runs of three or more in a row or column are crushed, everything above
slides down and new candies drop in from the top.

## How it works

- `board` is a 9x9 grid of tiles; `startGame()` fills it with six candy types
  (`Blue`, `Orange`, `Green`, `Yellow`, `Red`, `Purple`) at random.
- A single `setInterval` (100 ms) runs the cycle: `crushCandy()` -> `slideCandy()` -> `generateCandy()`.
- Scoring: +30 per crushed tile, written straight into `#score`.
- Swapping uses native HTML5 drag-and-drop events on each tile.

## Run

```bash
git clone https://github.com/ErfanBagheri404/CandyCrush.git
cd CandyCrush
```

Open `index.html`. No build step, no dependencies.

## Files

| file | role |
|---|---|
| `index.html` | board container, score, tiles are generated at runtime |
| `candy.js` | game loop, crush/slide/refill, drag handlers |
| `style.css` | 9x9 grid layout and candy sizing |
