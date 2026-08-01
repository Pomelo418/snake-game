# Snake

A browser-based Snake game built with vanilla JavaScript and the Canvas 2D API. No frameworks, no dependencies — open the file and play.

**[Play it live →](https://Pomelo418.github.io/snake-game/)**

---

## Features

- **Neon theme** — glowing snake, pulsing food, dark grid
- **Fixed-timestep game loop** — consistent speed independent of frame rate
- **Progressive difficulty** — speed increases every 5 points
- **Pause / Resume** — hit Space at any time
- **High score** — persists across sessions via `localStorage`
- **Input safety** — direction changes are queued and validated to prevent instant reversal

## Controls

| Key | Action |
|-----|--------|
| `↑ ↓ ← →` or `W A S D` | Move |
| `Space` | Pause / Resume |

## Run locally

No build step required — just open the file:

```bash
open index.html
```

Or clone and serve:

```bash
git clone https://github.com/Pomelo418/snake-game.git
cd snake-game
open index.html
```

## How it works

| Concept | Implementation |
|---------|---------------|
| Game loop | `requestAnimationFrame` with delta-time accumulation |
| Rendering | Canvas 2D API — `shadowBlur` for glow, radial gradients for food |
| Snake color | Per-segment hex interpolation from neon green (head) to cyan (tail) |
| Collision | Wall bounds check + O(n) self-intersection scan each tick |
| Persistence | `localStorage` for best score |

## Tech

- HTML5 Canvas
- Vanilla JavaScript (ES2020)
- CSS3

## License

MIT
