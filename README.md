# Act 3 — Dreaming: Make the Memory Maintain Itself

This project demonstrates how to build a self-maintaining AI memory system inspired by Karpathy’s **Dreaming** concept. Instead of allowing an AI memory file to continuously grow with duplicates, contradictions, and outdated information, the system periodically reviews and cleans it.

The project uses **Claude Code, Markdown files, a custom Dream Routine skill, and a scheduler** to maintain `MEMORY.md` while keeping the original project files protected.

### Key Features

* Self-maintaining AI memory system.
* Custom Claude Code `Dream Routine` skill.
* Duplicate memory detection and removal.
* Contradiction detection and conflict handling.
* Newer-source prioritization.
* Conversion of relative dates into absolute dates.
* Removal of stale or unnecessary memories.
* Human approval before memory changes.
* Git-based version tracking and rollback.
* Strict permission boundary for memory updates.
* Automated nightly Dream Routine scheduling.

### Workflow

1. Create `MEMORY.md` and session logs.
2. Add messy, duplicated, and conflicting memories.
3. Build the `Dream Routine` skill.
4. Read logs and compare them against existing memory.
5. Generate a proposed diff before making changes.
6. Review and approve memory updates.
7. Commit changes to Git for version history and rollback.
8. Schedule the routine to run automatically.
9. Keep the skill restricted to `MEMORY.md`.

### Safety & Governance

The Dream Routine can read `logs/` and `MEMORY.md`, but it is only allowed to modify `MEMORY.md`. Conflicting information is surfaced for review rather than silently changing memory, giving the human final control over what is retained.

The goal is to demonstrate how AI memory can **continuously improve and stay organized over time**, creating the foundation for Act 4, where the cleaned knowledge can be used to generate a complete YouTube script.
