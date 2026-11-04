# Game Development

Skills and agent harnesses for building games: studio structure, design and production
workflows, engine-specific guidance, QA and release gates.

| Skill | Source | Notes |
|-------|--------|-------|
| claude-code-game-studios | [Donchitos/Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios) | Turns one Claude Code session into a game dev studio: 49 agents in three tiers (creative/technical/producer directors → game-designer, lead-programmer, art/audio/narrative/QA leads → gameplay, engine, AI, network, tools, UI, systems, level, economy, technical-art, sound, world-builder, QA, devops specialists), 74 workflow skills (`/brainstorm`, `/map-systems`, `/design-system`, `/art-bible`, `/create-epics`, `/create-stories`, `/dev-story`, `/qa-plan`, `/regression-suite`, `/release-checklist`, `/team-*` for multi-agent features), 15 hooks for automated validation on commits, pushes, asset and design-doc changes, 14 path-scoped coding rules and 62 document templates (GDD, UX spec, ADR, sprint plan, HUD design). Engine sets for Godot 4, Unity (DOTS, Addressables, UI Toolkit) and Unreal 5 (GAS, Blueprints, replication). Ships as a template, not a finished game; a story touching anything the player sees is not closed until the game has been launched, observed and a screenshot kept in `production/qa/evidence/`. |
