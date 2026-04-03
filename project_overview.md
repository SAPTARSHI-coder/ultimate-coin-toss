# 📋 Project Overview — Ultimate Coin Toss

## 🎯 Goal
To build an interactive browser-based coin toss game that demonstrates advanced frontend skills including CSS 3D animations, JavaScript game logic using the module pattern, and Canvas-based particle effects — all in a single self-contained HTML file.

## 🧠 Architecture

### Game State Management
The entire game runs inside a JavaScript **IIFE module** (`const game = (() => {...})()`). This pattern keeps all game state private (wins, losses, mode, round) and only exposes the methods needed by the HTML buttons: `setMode`, `playTurn`, `toggleAuto`, `reset`, and `init`.

```
game state: { wins, losses, mode, targetWins, round, isFlipping, isAuto, gameOver }
```

### Coin Flip Animation
Each flip generates a **unique CSS keyframe animation** at runtime using `document.createElement('style')`. The coin rotates `(4–6 full spins × 360°) + (0° for heads or 180° for tails)`, using CSS `rotateY`. The `backface-visibility: hidden` ensures only one face shows at a time.

### Fireworks System
Uses the **HTML5 Canvas API**. Each particle is an object with position, velocity, color, and decay. On a player win, 3 bursts of 40 particles each are created at different screen positions and animated using `requestAnimationFrame`.

### Auto Mode
When auto mode is enabled, the game randomly selects `'heads'` or `'tails'` and calls `playTurn()` on a repeating `setTimeout` loop (1500ms delay between flips), stopping automatically when the game ends.

## 🎨 UI Design System
| Property | Value |
|---|---|
| Background | `#0f172a` (deep navy) |
| Glass card | `rgba(15,23,42,0.6)` + `backdrop-filter: blur(20px)` |
| Primary glow | `rgba(99,102,241,0.4)` (indigo) |
| Secondary glow | `rgba(168,85,247,0.4)` (purple) |
| Font | Outfit (Google Fonts) |

## 📊 Difficulty Level
| Aspect | Rating |
|---|---|
| HTML Structure | ⭐⭐ (simple, clean) |
| CSS Complexity | ⭐⭐⭐⭐ (3D transforms, glassmorphism, animations) |
| JavaScript | ⭐⭐⭐⭐ (module pattern, Canvas API, state machine) |
| Overall | ⭐⭐⭐⭐ Intermediate-Advanced |

## 💡 Next Steps to Enhance
- Add sound effects (flip sound, win fanfare)
- Add localStorage for persistent high scores
- Add player name input
- Make the coin image dynamic (switch themes)
- Deploy to GitHub Pages
