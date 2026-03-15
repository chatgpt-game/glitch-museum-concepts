# AI NPC System

Non-player characters (NPCs) in the Glitch Museum are integral to atmosphere and puzzle design. They represent malfunctioning museum staff, rogue AIs, and echoes of developers. This document outlines the desired behaviour, dialogue, and technical implementation approach for these characters.

## NPC Archetypes

- **Glitched Curator**  
  The curator appears human but flickers with static and occasionally switches between different sprites. It offers guidance to the player but sometimes provides corrupted or incomplete information. When the corruption is severe, the curator might speak in code comments or file paths.

- **Corrupted Guide**  
  These guides patrol certain wings and attempt to maintain order. They follow predefined patrol routes but will stop to warn players when an area is too unstable. As corruption increases, guides may become aggressive, blocking doorways or reversing their patrol paths.

- **Developer Ghost**  
  Echoes of developers trapped in the build manifest as ghostly silhouettes. They deliver meta commentary, reading aloud commit messages or bug reports. Players can free them by solving associated puzzles.

- **Experimental AI**  
  Located in the AI Experiments Wing, these characters are chatbots and generative AIs. They can converse with the player using limited vocabulary. Some will generate random textures or sounds when interacted with.

## Behavioural States

NPCs operate on a finite‑state machine with the following primary states:

1. **Idle** – The default state; the NPC plays ambient animations and occasional idle dialogue.  
2. **Interact** – Triggered when the player approaches or uses the Glitch Lens; the NPC focuses on the player and delivers scripted lines.  
3. **Corrupted** – The NPC’s behaviour becomes erratic. Movement may be jerky, dialogue fragments appear out of order, and it may inadvertently reveal hidden information (debug messages, variable names).  
4. **Disabled** – The NPC is temporarily frozen due to environmental corruption. Players can restore them using a patch item or by solving a nearby puzzle.  
5. **Scripted Event** – For important sequences, NPCs execute a unique behaviour path (e.g., leading the player, unlocking a door).

State transitions depend on player proximity, puzzle progress, corruption level of the room, and story triggers.

## Dialogue System

- **Branching Conversations**  
  Conversations use a lightweight branching system. Each node contains:
  - *Trigger conditions* – Which states or environmental flags must be met.
  - *Dialogue text* – Lines with optional placeholders for dynamic values (e.g., player name).
  - *Effects* – Changes to NPC state, environment variables, or puzzle flags.

- **Glitch Lens Interactions**  
  Pointing the Glitch Lens at an NPC overlays debug text such as current state, internal variables, or unused dialogue. This serves both as flavour and as hints to hidden puzzles.

- **Voice & Text**  
  Voices are synthesized using bitcrushed text‑to‑speech to maintain the PS1 aesthetic. Subtitles appear in an old terminal font with occasional character corruption.

## Implementation Notes

- **AI Framework**  
  Use the engine’s built‑in behaviour tree or state machine modules. Each NPC type can share a base class with common states and override specific behaviours.

- **Data‑Driven**  
  Store dialogue and state transition rules in external JSON/YAML files to allow designers to iterate without recompiling.

- **Debug Tools**  
  During development, include hotkeys to toggle NPC state and display full debug data. These tools can later be integrated into the Glitch Lens for players.

## Future Enhancements

- **Learning NPCs**  
  Experimental AIs could adjust their responses based on how players interact, learning to mimic player behaviour or speech patterns over time.

- **Multiplayer Reactions**  
  In future updates, NPCs could comment on the presence of multiple players, reacting differently when more than one avatar enters a room.
