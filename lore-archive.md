# Lore Archive

The **lore archive** is the beating heart of the Glitch Museum’s narrative.  As the player explores abandoned wings, corrupted exhibits and hidden developer artefacts, they should slowly piece together a sprawling backstory that connects every fragment.  To make this possible, the design team needs a central repository for all story-related materials — concept documents, transcripts of fake developer meetings, NPC dialogue scripts, cryptic emails, museum exhibit plaques, ARG content and more.  This markdown file outlines how to build and maintain such an archive so that the game’s mythology stays coherent even as we embrace chaos and glitch aesthetics.

## Purpose

The lore archive serves several goals:

- **Document consolidation:** Collect all narrative materials in one place so writers, level designers and audio designers can reference the same canon.
- **Cross-referencing:** Provide clear links between items.  For example, a corrupted journal page found in the AI Experiments wing should reference the developer ghost who wrote it and the broken exhibit it relates to.
- **Timeline tracking:** Maintain a chronological sequence of events leading up to and during the museum’s collapse.  This helps maintain internal logic even when the game intentionally scrambles perception.
- **Version control:** Allow multiple contributors to propose lore entries, update them over time and track changes, using Git.
- **Player-facing resources:** Enable the creation of optional codex entries or terminals in-game that pull from the same base documents.

## Archive Structure

It’s recommended to organize the archive into subdirectories and index files.  Some suggested folders:

- **entries/** – Individual lore pieces.  Each file could contain a diary entry, audio transcript, log file, museum placard text, chat log or glitch snippet.  Naming convention: `YYYY-MM-DD-<title>.md` or `wing-title-id.md`.
- **index.md** – Master index listing all entries with summaries, categories and tags.  Should be periodically generated/updated.
- **timeline.md** – A high-level chronological timeline.  List major events, approximate dates, and links to relevant entries.
- **characters/** – Biographies and backstories for major NPCs like the Glitched Curator, Corrupted Guide, Developer Ghost and any experimental AIs.  Include motivations, arcs and relationships.
- **glossary.md** – Definitions of recurring terms (e.g., **Patch Keys**, **Glitch Lens**, **Stability Meter**, **The Void**, **Developer Archive**).
- **external/** – Materials intended for ARG integration: fake web pages, social media posts, e-mails, puzzles requiring real-world action.  These should be clearly labelled and, if published externally, mirrored here.

## Document Types

Within `entries/` there will be different categories of documents:

1. **Developer Logs:** Internal memos, commit messages, bug reports and postmortems that hint at why the project was abandoned.  These can be written in a realistic style with code snippets or technical jargon.
2. **Museum Exhibits:** Plaques and descriptions for each exhibit in the museum.  They often contain background on lost media, unfinished games and strange experiments.
3. **Personal Notes:** Journals or letters from characters (NPCs, anonymous developers, early testers, even players).  These often provide emotional context and tease hidden areas.
4. **System Anomalies:** Scrambled data, corrupted files, AI-generated poetry, glitchy screenshots.  These can be used for puzzles or worldbuilding.
5. **Transcribed Audio:** Text versions of audio logs, voiceovers and overheard conversations.  These should include notations on speaker identity and tone.
6. **ARG Clues:** Codes, ciphers, web links and meta hints that live outside the game but tie into its story.

Each document should start with a YAML frontmatter block containing metadata like date, author, category, associated wing and tags.  Example:

```markdown
---
title: "Diary of the Curator, Page 7"
date: 2003-09-15
author: "Curator"
wing: "Scrapped Games"
tags: [diary, curator, foreshadowing]
---

The seventh page of the Curator’s diary reveals...
```

## Cross-Referencing

To maintain narrative coherence, every entry should link to related files.  Use relative links within the repository so they work both in GitHub and when imported into in-game systems.  For instance, if `entries/2003-09-15-curator-diary.md` references a bug report, include a link: `[Bug Report #42](entries/bug-report-42.md)`.  In the master `index.md`, include a column for related entries to show the network of lore pieces.

A simple cross-reference table could look like:

| Entry | Wing | Related Items |
| --- | --- | --- |
| 2003-09-15-curator-diary | Scrapped Games | Bug Report #42, Exhibit 12 Placard |
| bug-report-42 | Corrupted Files | Developer Log 08, Curator Diary 9 |

This helps authors see connections at a glance.  Avoid long sentences in the table; keep the table to keywords and phrases.

## Timeline

Create a `timeline.md` that outlines major events:

1. **Project inception (circa 1999):** The fictitious development team starts the Glitch Museum project as an ambitious experimental game.
2. **Early builds (2000-2002):** Various prototypes are developed; some wings like **Scrapped Games** and **AI Experiments** are functional.
3. **Catastrophic corruption (2003):** A major patch introduces the Glitch Lens and triggers uncontrolled environmental corruption; development stalls.
4. **Abandonment (2004):** The game is shelved; developers leave behind logs, prototypes and debug tools.
5. **Rediscovery (Present in-game):** The player (or in-universe archivist) finds the unfinished build and explores the museum.

Use approximate dates for in-universe events; you can adjust them as the story evolves.  Link each timeline entry to relevant documents.

## Implementation Notes

- **Version control:** Use Git branches or pull requests to manage large lore additions.  Conduct editorial passes to ensure consistency.
- **Naming conventions:** Adopt clear, descriptive names to avoid duplicate files.  Use lowercase with hyphens and include date or id.
- **Searchability:** Tag each entry with keywords (wing, character, theme) for easier searching.
- **Privacy and safety:** When creating ARG content, ensure no personal data is used and all interactions are opt-in.  Provide warnings when content blurs reality.
- **Collaboration tools:** Consider generating the `index.md` automatically using a simple script that scans `entries/` and extracts frontmatter.  This can be done in a future prototype repository.

## Future Ideas

- **Interactive Codex:** Develop an in-game codex interface that pulls from the markdown archive.  The codex could unlock entries as players discover clues.
- **Lore Database:** Convert the archive to a database with cross-references and search capabilities, accessible via an in-game terminal or a web-based viewer.
- **Community Contributions:** After release, allow players to submit fan theories or art.  Moderated entries could be added to the archive as apocrypha.
- **Dynamic Lore Updates:** For ARG events, reveal new entries in real-time.  Use commit timestamps to simulate the museum changing while the community solves puzzles.

By maintaining a robust lore archive, the Glitch Museum can support deep storytelling across multiple media while preserving the sense of mystery and discovery that defines the experience.  This document is a starting point; it should evolve as the project grows and new ideas emerge.
