# Corruption System

## Concept
The museum exists inside a malfunctioning build; corruption isn't just a narrative element but an active system. Each wing and room has a **stability rating** that drops over time or when the player triggers certain events.

## Manifestations
- **Visual Distortion**: Textures smear, polygons jitter, and geometry warps. This effect takes inspiration from the limitations of early 3D consoles where fixed-point math caused vertices to "snap" and textures warp【849677326735927†L74-L96】【849677326735927†L121-L134】.
- **Audio Glitches**: Soundtracks detune or loop incorrectly, voice lines stutter, and static creeps into ambient noise. Bitcrushed artifacts emphasise the retro aesthetic.
- **Behavioral Anomalies**: NPCs become unpredictable; doors teleport the player to the wrong location; physics behaves erratically.

## Instability Mechanics
- Every room has an **instability meter** that gradually fills. Environmental triggers like solving puzzles incorrectly or staying too long in a high-corruption zone accelerate the meter.
- When the meter maxes out, a **corruption event** occurs: new obstacles emerge, geometry reshuffles, or hidden passageways open. This rewards exploration but also increases risk.
- Players can reduce instability by applying **patch keys** at designated terminals or by completing optional debugging tasks within the room.

## Gameplay Impact
The corruption system creates dynamic tension. Players must decide whether to let instability climb to access secret content or stabilise zones to safely progress. This fail-forward design means no area ever locks the player permanently; instability simply changes the environment, pushing the narrative that the game is unfinished.

## Technical Notes
Under the hood, corruption effects are modular. Designers tag objects with corruption states and define what changes at each threshold. This allows the system to scale from subtle visual noise to full-fledged level transformations.
