# Glitch Effects

The Glitch Museum’s hallmark is its portrayal of digital decay through visual and auditory glitches. This document lists types of glitch effects to include, when to trigger them, and technical considerations for implementation.

## Categories of Effects

- **Visual Distortions**  
  - *Vertex Jitter*: Randomly offset vertices on meshes, causing walls to wobble or characters to stretch.  
  - *Texture Corruption*: Swap or scramble texture UVs to mimic corrupted image files.  
  - *Color Channel Shift*: Offset RGB channels independently, creating a chromatic aberration effect.  
  - *Scanline & VHS Noise*: Overlay horizontal lines, grain, and tape tracking errors.  
  - *Frame Skips*: Drop or repeat frames to give animations a stuttering feel.

- **Time & Space Anomalies**  
  - *Slowdown/Speedup*: Adjust the local timescale to warp player movement and physics.  
  - *Object Duplication*: Briefly duplicate props or NPCs before snapping them back.  
  - *Spatial Loops*: Place two doors that lead to the same room, causing players to loop until they alter reality with the Glitch Lens.

- **Audio Glitches**  
  - *Bitrate Reduction*: Temporarily reduce the bitrate of music and voices, making them sound muffled or robotic.  
  - *Reverse Playback*: Play snippets of ambient audio backward at random intervals.  
  - *Pitch Bending*: Gradually detune sounds as corruption increases.

- **UI Corruption**  
  - *Garbling Text*: Replace random characters in UI strings with symbols or hex codes.  
  - *Offset Meters*: Slightly misalign HUD elements or invert progress bars.  
  - *Fake Error Messages*: Display placeholder pop-ups like “TODO: add tooltip” or commit hashes.

## Triggering Conditions

- **Environmental Corruption Level**  
  The stability meter dictates the intensity of glitch effects. At low levels, effects are subtle; at high levels, they become overwhelming and may hinder navigation.

- **Puzzle Events**  
  Solving or failing certain puzzles can trigger scripted glitch sequences (e.g., walkway collapses, NPCs reset).

- **Lens Interactions**  
  Using the Glitch Lens can momentarily amplify or suppress glitches. For example, focusing the lens on a corrupted console might temporarily stabilize it.

## Implementation Tips

- **Shader-Based Effects**  
  Implement visual distortions via shaders for performance. Use noise textures and time variables to control randomness.

- **Parameterization**  
  Expose glitch intensity parameters to designers. This allows tuning for each wing and for accessibility options (some players may be sensitive to flashing visuals).

- **Sequencing**  
  Chain multiple effects to build toward major narrative moments. Ensure there are calm periods to prevent player fatigue.

## Safety Considerations

- Avoid rapid strobing or high-contrast flashing that could trigger photosensitive epilepsy. Provide settings to reduce or disable intense effects.

- Limit camera shakes and ensure motion blur can be toggled off.

## Future Experiments

- **Physics Glitches**: Temporarily break physics constraints, causing objects to float or pass through walls.  
- **AI Glitches**: NPCs speak out of character or recall dialogue from other games.  
- **Player Avatar Glitches**: Allow the player’s hands to disappear or swap models to emphasize that they are part of the corrupted build.
