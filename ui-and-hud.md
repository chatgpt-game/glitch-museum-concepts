# UI and HUD Design

The user interface of the Glitch Museum must balance immersion with functionality. It should feel like an overlay of a developer’s toolset while still being readable and intuitive for players. This document describes visual style, HUD elements, and interactive menus.

## Visual Style

- **Retro Debug Aesthetic**  
  The UI mimics old development tools: translucent windows, terminal fonts, ASCII borders, and monochromatic palettes. On occasion, UI elements flicker or display fake error codes to reinforce the theme of instability.

- **Minimal Footprint**  
  Keep on‑screen elements minimal to allow the museum environment to shine. When possible, collapse or hide panels unless the player explicitly opens them.

- **Glitch Overlays**  
  When the environment is highly corrupted, the entire UI may distort—text garbles, meters misalign, and buttons “crawl.” These effects are purely cosmetic and should not hinder readability for long.

## Core HUD Elements

- **Stability Meter**  
  Displays the local corruption level. As the bar depletes, textures warp and physics anomalies increase. If it empties completely, players are transported back to a stable area.

- **Glitch Lens Indicator**  
  Shows the current mode of the Glitch Lens (e.g., reveal, swap properties) and its cooldown if applicable. It pulses when hidden data is nearby.

- **Inventory / Patch Keys**  
  A small panel listing collected patch keys and items such as patches or objects used in puzzles. Players can open a full inventory screen to manage items.

- **Context Prompts**  
  When approaching interactable objects or NPCs, unobtrusive prompts appear (e.g., “[E] Inspect,” “[Q] Use Lens”). Prompts fade quickly when the player moves away.

- **Dialogue Box**  
  For conversations, a textbox appears at the bottom of the screen styled like a debugging console. It supports colour-coded speaker names and glitch effects such as scrambled letters.

## Menus

- **Main Menu**  
  Uses the same retro aesthetic with options for Continue, New Game, Options, and Lore Archive. Idle background features a rotating wireframe model of the museum with flickering textures.

- **Pause Menu**  
  Displays options for saving, settings, and patch notes. The pause menu can also show current objectives and hints gleaned through the Glitch Lens.

- **Settings**  
  Players can adjust accessibility options, audio volumes, brightness, and glitch intensity. Include sliders for “VHS noise level” and “UI glitch frequency” to accommodate player comfort.

## Implementation Notes

- **Responsive Layouts**  
  Ensure UI scales appropriately across resolutions and aspect ratios. Use anchors rather than fixed pixel positions.

- **Localization**  
  All text should be loaded from external files to support localisation. Be mindful of dynamic glitch effects that could break in non‑Latin scripts; provide fallbacks.

- **Input Methods**  
  Support keyboard/mouse, controller, and accessibility devices. UI prompts should adjust icons based on the current input device.

## Future Enhancements

- **Diegetic UI**  
  Explore ways to integrate UI elements directly into the world (e.g., wrist-mounted lens device, holographic displays) to increase immersion.

- **Multiplayer HUD**  
  Should multiplayer modes be added, design HUD elements to show other players’ statuses and shared objectives without clutter.
