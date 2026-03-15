# Engine Evaluation

Selecting the right engine is crucial for building a prototype of **The Glitch Museum** that captures its retro aesthetic and supports rapid iteration. This document evaluates several engines—Unity, Godot, Unreal, and Web‑based technologies—based on our needs.

## Evaluation Criteria

1. **Ease of Prototyping:** How quickly can we build and iterate on core mechanics like the Glitch Lens and patch system?
2. **Visual & Audio Capability:** Can the engine produce PS1‑style graphics and dynamic glitch effects? Does it support audio manipulation?
3. **Cost & Licensing:** Are there licensing fees or revenue sharing models? Is the engine open source?
4. **Platform Support:** Does the engine deploy to PC, consoles, and web browsers?
5. **Community & Ecosystem:** Availability of documentation, tutorials, and plugins.

## Unity

**Pros:**

- Widely adopted with a large asset store and extensive documentation. It offers rapid prototyping through prefabs and C# scripting. Wayline’s 2025 comparison notes that Unity excels at cross‑platform support and has a vibrant community【744984677519748†L40-L93】.
- Supports custom shaders and post‑processing, making it feasible to implement PS1 effects like vertex snapping, affine texture wobble, and dithering.
- Robust 2D and 3D tools with flexible UI systems; good integration with audio middleware.

**Cons:**

- Recent licensing and pricing changes have introduced uncertainty【744984677519748†L40-L93】.
- Higher memory overhead compared to lighter engines like Godot.

## Godot

**Pros:**

- Open source and completely free to use, with a permissive MIT licence【744984677519748†L40-L93】.
- Lightweight and easy to learn; uses GDScript (Python‑like) and supports C# and visual scripting. Great for 2D projects and increasingly capable in 3D.
- Small download size; ideal for rapid iteration and modding.

**Cons:**

- 3D features are less mature than Unity or Unreal【744984677519748†L40-L93】. PS1‑style shader support may require more custom work.
- Smaller community and fewer ready‑made assets. May need to implement custom tools (e.g., node‑based dialogue systems).

## Unreal Engine

**Pros:**

- Superior high‑fidelity graphics with robust Blueprints visual scripting system. Good for complex 3D environments【744984677519748†L40-L93】.
- Out‑of‑the‑box support for advanced audio and physics.

**Cons:**

- Heavy installation size and steeper learning curve. Overkill for a retro‑styled indie game【744984677519748†L40-L93】.
- Royalty system (5% after revenue threshold) and high hardware requirements.

## Web‑Based (WebGL / Three.js)

**Pros:**

- Runs directly in the browser, facilitating easy sharing and ARG integration. Web technologies can integrate with real websites to blur game boundaries.
- Lightweight and accessible; no installation for players.

**Cons:**

- Limited performance compared to native engines. Achieving PS1‑style effects and dynamic glitch systems may require significant optimisation.
- Browser security restrictions may complicate file system access or custom shaders.

## Recommendation

Based on the criteria and goals of **The Glitch Museum**, **Unity** and **Godot** are the most suitable engines for prototyping:

- **Unity** offers strong 3D tooling, cross‑platform support, and a wealth of resources, making it ideal for a vertical slice. However, future licensing changes should be monitored.
- **Godot** is appealing for its open‑source nature and ease of use. It may serve as a lightweight alternative for early prototypes, especially if we prioritise 2D ARG components or a stylised 3D look.

Unreal is likely unnecessary given the project’s scope, and web‑based approaches are best reserved for ARG extensions rather than the core game. After an initial prototype, we can reassess engine choice based on team comfort and technical constraints.
