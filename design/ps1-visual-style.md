# PS1 Visual Style Guide

The **PlayStation 1** aesthetic is a major influence on **The Glitch Museum**. This guide summarises the technical characteristics of the PS1 era and explains how to evoke them using modern tools. Rather than imitating limitations blindly, we selectively apply quirks that support the narrative and mood.

## Key Characteristics of PS1 Graphics

- **Low Polygon Counts:** Original PS1 games used very few polygons per model due to hardware constraints. Characters and environments were blocky but expressive. David Colson notes that typical PS1 models ranged from hundreds to a few thousand triangles【281010470623685†L70-L99】.
- **Vertex Snapping & Jitter:** The PS1 performed geometry calculations using fixed‑point integers, leading to vertices snapping to 1/16th or 1/4th pixel boundaries. This caused characteristic jitter when the camera moved【849677326735927†L74-L96】.
- **Affine Texture Mapping:** The console did not correct perspective across polygons; textures were mapped affinely, leading to texture wobble and warping as objects rotated or moved【849677326735927†L121-L134】.
- **No Z‑Buffer:** The PS1 sorted polygons manually without a hardware depth buffer, resulting in rendering artifacts like polygons drawing in the wrong order and textures bleeding through【281010470623685†L52-L60】.
- **Limited Colour Depth & Dithering:** The system output 15‑bit colour (32,768 colours), so games often used dithering patterns and colour banding to simulate more shades【849677326735927†L157-L167】.
- **Depth Cueing Fog:** Many games used fog not just for atmosphere but to hide pop‑in due to limited draw distance. Fog colours often matched the environment to blend objects seamlessly【281010470623685†L52-L60】.

## How to Recreate the Look

### 1. Models & Geometry

- **Simplify Meshes:** Design characters and props with low triangle counts and exaggerated silhouettes. Avoid modern smoothing or subdivision. Imperfections add charm.
- **Apply Vertex Jitter:** In shaders, add subtle random offsets to vertex positions each frame or on player movement to simulate fixed‑point snapping. This should be optional for comfort.
- **Deliberate Clipping & Sorting Errors:** In certain corrupted zones, intentionally draw polygons in the wrong order or allow textures to bleed through to evoke the absence of a Z‑buffer. Use sparingly so the game remains playable.

### 2. Textures

- **Low Resolution:** Limit texture sizes to 256×256 or smaller. Use simple palettes and avoid high‑resolution photographic detail.
- **Affine Distortion Simulation:** Introduce a shader pass that slightly skews UV coordinates based on camera angle to mimic affine mapping wobble.
- **Colour Banding & Dithering:** Use dithering filters or ordered dithering patterns to approximate 15‑bit colour depth. Provide a toggle for players sensitive to flickering.

### 3. Lighting & Effects

- **Per‑Vertex Lighting:** Avoid per‑pixel dynamic lighting; instead calculate lighting at vertices and interpolate across polygons. This yields a flat, retro look.
- **Depth Fog:** Add fog starting at a moderate distance to hide pop‑in and create atmosphere. Colour the fog to match the environment (e.g., greenish for the Corrupted Files wing).
- **Screen Space Effects:** Use CRT scanlines, slight vignetting, and film grain to emulate playing on old hardware. Combine with glitch effects like RGB channel separation when the corruption system activates.

### 4. Audio & UI Integration

- While this document focuses on visuals, pairing low‑fidelity graphics with **bitcrushed audio** and **retro UI** will enhance immersion. See the `audio-design.md` and `ui-and-hud.md` documents for details.

## Balancing Nostalgia and Modern Expectations

- Provide options to adjust the intensity of PS1 effects so players can prioritise comfort or authenticity.
- Maintain responsive controls and fluid movement; we emulate aesthetics, not clunky gameplay.
- Use high‑fidelity effects (e.g., particle systems, real‑time shadows) sparingly to accentuate important moments, contrasting them with the otherwise retro presentation.

By understanding the technical limitations that defined PS1 visuals and selectively recreating them, **The Glitch Museum** can evoke nostalgia while leveraging modern engine capabilities. These stylistic choices serve the game's themes of lost media and corrupted memories.
