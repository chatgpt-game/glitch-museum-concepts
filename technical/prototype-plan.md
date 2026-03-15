# Prototype Plan

This document outlines a roadmap for building an early prototype of **The Glitch Museum**. The goal of the prototype is to validate core mechanics, aesthetics, and narrative delivery while remaining small in scope. The prototype will serve as a vertical slice to attract collaborators and test the game’s feasibility.

## Objectives

- Implement core gameplay systems: **Glitch Lens**, **Corruption System**, and **Patch Keys**.
- Build a small portion of the museum (one wing and the lobby) showcasing exploration, puzzles, and NPC interactions.
- Test PS1‑style visuals and glitch effects in a real engine.
- Deliver a playable build that runs on PC and optionally Web.

## Scope

1. **Environment:**
   - Create a simplified version of the **Scrapped Games** wing with 2–3 rooms and a central lobby hub.
   - Include a hidden area to test secret discovery and environmental storytelling.
   - Use placeholder low‑poly assets and textures inspired by PS1 hardware.

2. **Gameplay Systems:**
   - **Glitch Lens:** Implement a tool the player can toggle to reveal hidden objects, debug text, and alternate geometry states. Basic UI overlay and scanning function.
   - **Corruption System:** Track an instability meter per room; apply visual and audio glitches when the meter is high. Include one or two corruption triggers (e.g., failing a puzzle).
   - **Patch Keys:** Create two types of patch keys—one to stabilise an area (reduces instability meter) and one to unlock a blocked path. Integrate inventory management.

3. **NPC & Dialogue:**
   - Implement the **Glitched Curator** as a basic NPC who welcomes the player and offers hints. Use a simple dialogue system with branching choices.

4. **UI & Audio:**
   - Include a rudimentary HUD showing the instability meter, patch key inventory, and Glitch Lens status.
   - Implement placeholder audio: bitcrushed ambience, glitch sounds, and a looping background track that adapts to corruption levels.

5. **Platform & Tools:**
   - Use the engine determined in the `engine-evaluation.md` document (likely Unity or Godot) to build the prototype.
   - Use version control (Git) with the existing GitHub repository for code and asset management.
   - Modularise systems to allow reuse in the full game.

## Milestones & Timeline (Hypothetical)

1. **Week 1: Setup & Research**
   - Choose engine and set up project repository.
   - Experiment with PS1 shader effects (vertex jitter, affine texture mapping, dithering) using prototype assets.
   - Define data structures for corruption system and patch keys.

2. **Week 2: Core Systems**
   - Implement Glitch Lens toggling and raycasting to reveal hidden objects.
   - Create instability meter logic and visual feedback.
   - Build simple inventory system and integrate patch keys.

3. **Week 3: Level Blockout & NPCs**
   - Greybox the lobby and Scrapped Games rooms.
   - Place interactive objects and patch key triggers.
   - Implement the Glitched Curator with basic dialogue and animations.

4. **Week 4: Polish & Playtesting**
   - Refine PS1 visual filters and lighting.
   - Add placeholder audio and UI polish.
   - Conduct internal playtests, gather feedback, and iterate.
   - Package the prototype for distribution.

## Future Considerations

- Expand the prototype to include additional wings once core systems are stable.
- Integrate ARG hooks (e.g., hidden codes linking to real websites) after validating gameplay.
- Transition from placeholder art to production assets while retaining the PS1 aesthetic defined in `ps1-visual-style.md`.

Following this plan will produce a focused prototype that demonstrates the unique mechanics and atmosphere of **The Glitch Museum** while informing further development.
