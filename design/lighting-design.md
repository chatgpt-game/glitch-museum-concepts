# Lighting Design

Lighting plays a critical role in conveying mood and guiding the player through the museum. This document describes the principles and techniques for lighting levels, characters, and events in **The Glitch Museum**.

## Goals

- **Atmosphere & Tone:** Use lighting to evoke curiosity, unease, nostalgia, and wonder. Dark corners, flickering bulbs, and neon glows highlight the game's surreal nature.
- **Gameplay Clarity:** Direct the player’s attention to interactive objects and safe pathways without heavy‑handed waypoints.
- **Reinforce Stability vs Corruption:** Lighting should communicate the state of an area—warm and steady in stable zones; erratic and saturated in corrupted areas.

## Core Techniques

### 1. Base Lighting

- **Ambient Light:** Each wing has a base ambient colour that reflects its theme: e.g., amber hues for the **Scrapped Games** wing, sickly greens for **Corrupted Files**, sterile whites and blues for **AI Experiments**, and soft CRT glow for **Internet Archaeology**.
- **Directional Sources:** Use a limited number of static lights to cast long, soft shadows reminiscent of PS1 pre‑baked lighting. Avoid complex real‑time shadows except in highlight moments.
- **Practical Lights:** Integrate visible light sources (lamps, monitors, neon signs) into environments to justify illumination and enhance immersion. This also grounds the retro aesthetic.

### 2. Dynamic & Reactive Lighting

- **Glitch Flicker:** In corrupted zones, lights occasionally flicker, strobe, or cycle through RGB channels. The frequency and intensity correspond to the area’s instability meter and the player’s actions.
- **Stability Pulses:** When the player uses a **Patch Key**, lights brighten and stabilise, accompanied by a subtle colour shift towards neutral tones. Conversely, using the **Glitch Lens** to corrupt objects causes localised dimming and colour shifts.
- **Trigger Events:** Important narrative moments (e.g., meeting the **Glitched Curator**, discovering a hidden log) are accentuated by spotlights or sudden changes in lighting, drawing the player’s eyes.

### 3. Colour Language

- **Stable = Warm / Neutral:** Soft oranges, whites, and pastel colours signal safety and clarity.
- **Corrupted = Harsh / Cold:** Neon magenta, green, and cyan evoke digital errors and danger. Pair these with glitch effects like RGB channel separation and vertex distortion for maximum impact.
- **Unknown / ARG Elements:** Purple and ultraviolet hues can hint at secrets and puzzles, inviting players to investigate.

### 4. Fog & Volumetrics

- **Depth Fog:** Use fog to mask draw distance and create mystery. The fog colour should fade into the wing’s palette. This also references the PS1’s depth cueing fog, which hid popping geometry【281010470623685†L52-L60】.
- **Volumetric Beams:** Occasionally, shafts of light shine through dust motes or glitch particles, emphasising the museum’s age and digital decay.

### 5. Accessibility & Comfort

- Provide settings to adjust flicker intensity or disable strobing for players sensitive to flashing lights.
- Offer high‑contrast mode options for players with visual impairments, ensuring important objects remain visible.

## Implementation Notes

- Use Godot or Unity’s light layers to separate dynamic and static lights for performance.
- Pre‑bake lighting where possible to maintain the low‑poly, PS1‑era feel while keeping performance high.
- Coordinate with **audio design** so that lighting changes sync with sound cues (e.g., a glitch flicker accompanied by a CRT hum).

Through thoughtful lighting design, **The Glitch Museum** will guide players emotionally and spatially, reinforcing the game’s themes of instability and nostalgia. Balancing retro aesthetics with modern accessibility ensures that lighting enhances rather than hinders the experience.
