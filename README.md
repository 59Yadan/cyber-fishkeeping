# Cyber Fishkeeping

An interactive, generative digital aquarium where users can guide a flock of glowing fish, feed them, and watch them scatter. Designed as a meditative, audio-visual interactive experience.

## 🔗 Live Demo
👉 **[Play Cyber Fishkeeping Here](https://59yadan.github.io/cyber-fishkeeping/)**
*(Best experienced on a desktop browser with a mouse and audio enabled)*

## 🎯 Intended User & Idea
This project is designed for anyone looking for a quick, meditative visual break. The idea was to create a "digital pet" experience that feels organic and responsive, rather than a traditional game with winning or losing conditions. The user acts as a caretaker, interacting with a school of digital fish.

## 🖱️ Main Interaction
The program responds to both mouse movement and clicks, providing immediate visual and auditory feedback:
- **Move Mouse**: The fish flock smoothly follows the cursor, creating a fluid, organic movement across the screen.
- **Left Click (Feed)**: Drops white food pellets into the tank. The fish will abandon the cursor and race to eat the food. 
- **Right Click (Scatter)**: Creates a water ripple effect and scares the fish away from the click location.
- **Audio Activation**: Modern browsers block autoplay. Click anywhere to activate the healing ambient background music.

## ✨ Design & Technical Details
- **Flocking Algorithm**: Built using the Boids algorithm (Separation, Alignment, Cohesion) to simulate realistic schooling behavior.
- **Generative Visuals**: 
  - Fish have a streamlined body with a head-to-tail gradient.
  - The entire school smoothly transitions between three custom color palettes (21-second loop) using RGB linear interpolation.
  - Fish leave subtle, fading hollow bubble trails as they swim.
- **Audio Integration**: Uses Tone.js to generate a continuous, healing ambient chord progression (Cmaj7 - Am7 - Fmaj7 - G7) upon user interaction.
- **Performance & Errors**: Implemented `frameRate(60)` lock, audio polyphony limits, and click debouncing to prevent browser crashes during rapid interactions.

## 🚀 How to Run Locally
This is a pure front-end project. No build tools are required.
1. Clone or download this repository.
2. Open `index.html` in any modern web browser.
3. *(Note: You must have an internet connection to load p5.js and Tone.js from the CDN.)*

## ⚠️ Known Limitations
- **Autoplay Policy**: Due to browser security policies, audio cannot play automatically upon page load. The user must interact with the page first (handled via the "CLICK ANYWHERE TO ENABLE AUDIO" prompt).
- **Mobile Support**: The primary interaction is designed for a mouse. While tapping works on tablets, full multi-touch gestures (like two-finger tap for right-click) are not fully implemented.

## 🛠️ Built With
- [p5.js](https://p5js.org/) - Canvas rendering and interaction
- [Tone.js](https://tonejs.github.io/) - Web Audio synthesis

---
*Created for Assignment 3: An Interactive Experience.*