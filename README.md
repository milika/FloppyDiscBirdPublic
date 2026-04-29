# Floppy Bird Disc — Community Themes

A collection of `.fdbtheme` files for [Floppy Bird Disc](https://apps.apple.com/app/id6762493898) — available free on the App Store.  
Tap any theme below to install it instantly on your device.

---

## Available Themes

| Theme | Preview | Install |
|-------|---------|---------|
| Default | Complete set of all built-in assets | [Install](https://milika.github.io/FloppyDiscBirdPublic/install.html?theme=default) |

---

## Installing a Theme

Tap **Install** next to any theme — iOS will ask to open it in Floppy Bird Disc, and the theme is applied automatically.

> Don't have the app? [Download it free on the App Store](https://apps.apple.com/app/id6762493898).

---

## Creating Your Own Theme

A `.fdbtheme` file is a standard **ZIP archive** renamed to `.fdbtheme`.  
Only include the assets you want to override — everything else falls back to the built-in default.

### Archive structure

```
my-theme.fdbtheme  (ZIP)
├── manifest.json          ← required
├── textures/              ← optional; override any sprite
├── sounds/                ← optional; override any sound
└── fonts/                 ← optional; override any font
```

### `manifest.json`

```json
{
  "formatVersion": 1,
  "name": "My Theme",
  "author": "Your Name",
  "version": "1.0.0",
  "description": "Short description shown in Settings"
}
```

---

### Texture slots (`textures/<name>.png`)

File names are case-sensitive and must match exactly.  
Images are rendered with nearest-neighbour filtering — provide @1× pixel-art PNGs.

#### Birds

| File | Description | Size |
|------|-------------|------|
| `yellow-bird-1.png` | Yellow bird frame 1 | 34 × 24 px |
| `yellow-bird-2.png` | Yellow bird frame 2 | 34 × 24 px |
| `yellow-bird-3.png` | Yellow bird frame 3 | 34 × 24 px |
| `red-bird-1.png` | Red bird frame 1 | 34 × 24 px |
| `red-bird-2.png` | Red bird frame 2 | 34 × 24 px |
| `red-bird-3.png` | Red bird frame 3 | 34 × 24 px |
| `blue-bird-1.png` | Blue bird frame 1 | 34 × 24 px |
| `blue-bird-2.png` | Blue bird frame 2 | 34 × 24 px |
| `blue-bird-3.png` | Blue bird frame 3 | 34 × 24 px |
| `super-bird-1.png` | Super bird frame 1 | 34 × 24 px |
| `super-bird-2.png` | Super bird frame 2 | 34 × 24 px |
| `super-bird-3.png` | Super bird frame 3 | 34 × 24 px |

#### World

| File | Description | Size |
|------|-------------|------|
| `PipeUp.png` | Upper pipe | 52 × 320 px |
| `PipeDown.png` | Lower pipe | 52 × 320 px |
| `land.png` | Scrolling ground | 336 × 112 px |
| `day-sky.png` | Daytime background | 288 × 512 px |
| `night-sky.png` | Night background | 288 × 512 px |

#### HUD & UI

| File | Description | Size |
|------|-------------|------|
| `floppybird.png` | Title logo | 178 × 48 px |
| `get-ready.png` | "Get Ready!" banner | 174 × 44 px |
| `taptap.png` | Tap instruction | 114 × 98 px |
| `gameover.png` | "Game Over" banner | 192 × 42 px |
| `scoreboard.png` | Result board background | 226 × 116 px |
| `new.png` | "NEW" badge | 32 × 14 px |
| `sparkle.png` | Medal sparkle | 28 × 28 px |
| `copper-medal.png` | Copper medal | 44 × 44 px |
| `silver-medal.png` | Silver medal | 44 × 44 px |
| `gold-medal.png` | Gold medal | 44 × 44 px |
| `platinum-medal.png` | Platinum medal | 44 × 44 px |
| `settings-panel.png` | Settings panel background | 226 × 116 px |
| `settings.png` | Settings gear button | 28 × 28 px |
| `themes.png` | GitHub button (main menu) | 62 × 36 px |
| `leaderboard.png` | Leaderboard button (main menu) | 62 × 36 px |
| `back-button.png` | Back arrow | 26 × 14 px |
| `toggle.png` | Sound/haptics toggle | 36 × 20 px |
| `floppyplay.png` | Play button | 52 × 30 px |

---

### Sound slots (`sounds/<name>`)

Any theme sound may use `.caf`, `.wav`, `.mp3`, or `.m4a` regardless of the key name.

| File (key) | Trigger |
|------------|---------|
| `sfx_wing.caf` | Each tap / flap |
| `sfx_die.caf` | Bird falls off screen |
| `sfx_point.wav` | Passes through a pipe gap |
| `sfx_hit.caf` | Collision with pipe or ground |
| `sfx_swooshing.caf` | UI transitions / result board |

---

### Font slots (`fonts/<name>.ttf`)

| File (key) | Used by |
|------------|---------|
| `pixel.ttf` | Score counter, all game labels, leaderboard |
| `inside.ttf` | Score counter inner stroke, result board |
| `outside.ttf` | Loaded alongside `inside.ttf` |

---

## Sharing a Theme

Once you've created your `.fdbtheme` file, open a pull request adding it to this repository.  
Include a short description and a preview screenshot in your PR.
