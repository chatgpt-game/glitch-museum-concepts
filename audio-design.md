# Audio Design

Sound plays a crucial role in immersing players in the Glitch Museum. The audio palette should evoke nostalgia for late 90s computing while also communicating the instability of the environment. This document outlines stylistic guidelines, technical considerations, and ideas for using audio as a gameplay mechanic.

## Aesthetic Goals

- **Bitcrushed Fidelity**  
  Most sound effects are downsampled and compressed to emulate PS1-era hardware. This includes subtle tape hiss, hum, and aliasing artifacts.

- **Dynamic Glitches**  
  Areas of high corruption should trigger random skips, static bursts, or stuttering. Audio can be used to foreshadow upcoming instability (e.g., muffled voices before entering a corrupted wing).

- **Musical Minimalism**  
  Music is sparse and ambient, consisting of droning pads, reversed piano notes, and distant reverberant melodies. Each wing features its own motif:  
  - *Scrapped Games Wing* – Overlapping chiptune loops with occasional missing beats.  
  - *Corrupted Files Wing* – Detuned synths, dissonant chords, and static.  
  - *AI Experiments Wing* – Generative music created by in-game AIs; patterns evolve based on player movement.  
  - *Internet Archaeology Wing* – Nostalgic modem handshakes blended with lo-fi IDM rhythms.

## Interactive Audio

- **Environmental Cues**  
  Sounds emanate from exhibits, NPCs, and background systems. The player hears distant footsteps, whirring servers, and museum announcements. These cues guide the player to points of interest or hint at hidden rooms.

- **Reactive Soundscape**  
  The audio engine should adjust layers based on the player's use of the Glitch Lens. For example, pointing the lens at a corrupted wall might reveal a hidden melody or a reversed voice message embedded in the static.

- **Puzzles**  
  Some puzzles rely on audio manipulation. Example ideas:  
  - **Sound Reversal Puzzle** – Players record a distorted audio clip and then play it backward to reveal instructions.  
  - **Frequency Matching** – Align the pitch of different machines to open a door.  
  - **Spatial Listening** – Identify the correct path in a maze by following specific sound patterns.

## Implementation Notes

- **Middleware**  
  Integrate a middleware solution such as FMOD or Wwise to handle interactive audio layers, real‑time effects, and dynamic music transitions.

- **Adaptive Mixing**  
  Use state machines and parameters (e.g., corruption level, current wing, lens usage) to blend audio stems. Ensure transitions are smooth even when sudden glitches occur.

- **Audio Assets**  
  Maintain an organized library of assets grouped by wing and function (UI, ambient, puzzle). Provide designers with a spreadsheet listing file names, descriptions, and tags.

## Future Ideas

- **3D Positional Audio**  
  Implement binaural audio or HRTF filtering for players using headphones to enhance immersion.

- **Player Voice**  
  Allow players to record their voice for specific puzzles, with the game processing and incorporating it into the environment.

- **ARG Integration**  
  Hide phone numbers or spectrogram images in audio tracks that lead to real‑world clues.
