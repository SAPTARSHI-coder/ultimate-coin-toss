# Ultimate Coin Toss

[![Live Demo](https://img.shields.io/badge/Live%20Demo-ultimate--coin--toss.netlify.app-brightgreen?style=for-the-badge&logo=netlify)](https://ultimate-coin-toss.netlify.app/)

A high-fidelity, interactive browser-based coin toss simulation engineered using core web technologies (HTML, CSS, JavaScript). The interface features a modern aesthetic utilizing glassmorphism, dynamic 3D CSS transform keyframes for realistic coin flipping physics, real-time match state management, and a procedural particle system rendering via the HTML5 Canvas API.

## System Architecture Overview

The system provides competitive match configurations (Best-of-3, Best-of-5, Best-of-7). In each trial, user inputs are validated against randomized outcomes. The application manages score state dynamically and triggers visual feedback mechanisms upon state changes (e.g., match point reached, victory achieved). Additionally, an autonomous execution loop provides simulated match playback.

## Key Capabilities

- **Stochastic 3D Animation:** Procedurally generated CSS keyframes calculate trajectory and spin velocity dynamically per interaction cycle.
- **State Controller:** Real-time multi-variable state tracking encompassing user performance vs. CPU.
- **Match Point Telemetry:** Predictive visual indicators when a conclusive victory is imminent.
- **Canvas Particle Renderer:** Hardware-accelerated fireworks effect deployed upon match resolution.
- **Autonomous Playback:** Configurable automated trial execution loops for simulation.
- **Modern UI Patterns:** Implements translucent frosted-glass aesthetic patterns utilizing backdrop blur filters.

## Technology Stack

| Technology | Implementation Role |
| :--- | :--- |
| **HTML5** | Semantic Document Object Model structure and Canvas integration. |
| **CSS3** | Hardware-accelerated 3D transforms (`preserve-3d`, `backface-visibility`), modular UI design, and dynamic CSSOM mutations. |
| **Vanilla JS** | Application logic encapsulated within an IIFE-based Module Pattern, utilizing requestAnimationFrame and Canvas API rendering. |
| **Typography** | Integration with Google Fonts (Outfit). |

## Environment Setup

The application is deployed as a static file architecture with zero external build dependencies.

1. Clone or download the repository.
2. Execute `index.html` within any modern, standard-compliant automated web browser.

## Technical Implementation Details

- **3D Spatial Rendering:** Employs CSS `perspective` interacting with `rotateY()` to construct 3D space depth during transform animations.
- **Visual Isolation:** Uses `backface-visibility: hidden` to properly render bipartite textural topologies (obverse/reverse interfaces of the coin unit).
- **State Encapsulation:** Implements a JavaScript Module Pattern (`const game = (() => {})()`) to prohibit global scope pollution and ensure state integrity.
- **Procedural Particle Generation:** Uses the HTML5 Canvas API context for rendering stochastic, velocity-based particle trajectories unconstrained by DOM node limitations.
- **Dynamic CSS Injection:** Mutates `styleSheet.textContent` dynamically bypassing static CSS constraints to ensure unique initial-to-terminal rotation vectors per flip task.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
