# Pixel Kick

A simple, lightweight, single-file HTML5 penalty shootout soccer game inspired by retro arcade aesthetics. The entire game—including logic, graphics, and sound—is contained within a single `index.html` file with no external dependencies or CDNs required.

## Features

* **Retro Pixel Art Style:** All visual elements, sprites, and custom fonts are drawn procedurally on an HTML5 Canvas using a limited color palette.
* **Synthesized Web Audio:** Sound effects (kick, goal fanfare, crowd cheer, goalkeeper saves, and misses) are generated programmatically using the Web Audio API. No external `.mp3` or `.wav` files are needed.
* **Mobile-First Design:** Optimized for a 360x640 resolution with touch dragging to aim and a timing-based power bar.
* **AI Goalkeeper:** The keeper reacts with calculated delays and movement speeds mapped to three difficulty settings (Easy, Medium, Hard). Includes a corner-dive visual state.
* **Tiebreakers:** Standard best-of-five format with sudden-death rounds implemented if scores remain tied.
* **In-Game Screenshot Feature:** Includes a "Save Frame" utility that lets players export their current canvas rendering as a PNG directly to their device.

## Controls

### Mobile & Tablet (Touch)
* **Aiming:** Tap and drag anywhere on the bottom half of the screen. A dotted trajectory line and target reticle will appear.
* **Powering Up:** Holding the touch increases the shot power meter on the left.
* **Kicking:** Release your finger to shoot the ball.

### Desktop (Mouse & Keyboard)
* **Mouse Control:** Click and drag to aim, hold to power up, and release to kick (identical to touch controls).
* **Keyboard Control:** 
  * **Arrow Keys:** Adjust the target reticle left, right, up, and down.
  * **Spacebar (Hold):** Charge the power meter.
  * **Spacebar (Release):** Take the shot.

## How to Run

1. Download or copy the `index.html` file to your local system.
2. Double-click the file to open it in any modern web browser (e.g., Chrome, Safari, Firefox, Edge).
3. Select your desired difficulty on the title screen and tap to start.

## Technical Details

* **No Frameworks:** Built purely with Vanilla ES6 JavaScript and CSS.
* **Offline-Ready:** Since all visual and audio assets are generated dynamically, the game functions completely offline.
* **Render Pipeline:** Uses `requestAnimationFrame` for a consistent loop, setting `imageSmoothingEnabled` to `false` to preserve sharp pixel scaling on high-resolution displays.
