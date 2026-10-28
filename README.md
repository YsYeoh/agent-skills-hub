# agent-skills-hub

A curated collection of agent coding skills, organized by category.

## Purpose

Gather agent skills from around the web (GitHub repos, etc.) and group them into
clear categories so they're easy to find and reuse.

## Categories

1. **UI/UX & Frontend Design** (`skills/ui-ux-design/`)
   Interface & visual design, design systems, landing pages, redesigns, image→code, frontend taste/anti-slop, brand kits.

2. **Motion & Animation** (`skills/motion-animation/`)
   Web animation, React Native/Expo animation, gestures/haptics, animation audit/lookup, 'where to animate'.

3. **Video & Motion Video** (`skills/video-motion/`)
   Editing, from-HTML/video generation, templated short-form marketing video (e.g. hyperframe-style 'HTML → video'), video compositing.

4. **Coding & Language Guidance** (`skills/coding-language/`)
   Language-specific best-practices (Swift, etc.), code review, architecture, testing patterns.

5. **Coding Harness & Agent Orchestration** (`skills/coding-harness/`)
   Sub-agent delegation, messaging, context/compaction, goals, memory, skills, heartbeats, evals/environments.

6. **Content & Media Generation** (`skills/content-media/`)
   Image generation for web/mobile, marketing visuals, brand boards.

7. **Research & Web** (`skills/research-web/`)
   Web search, scraping, data gathering.

8. **General / Meta Skills** (`skills/general/`)
   Skill creation, output enforcement, workflow automation, reusable tactics.

## Layout

Skills are grouped under these category folders, each holding a `LINKS.md` index of the
links collected there:

```
skills/
├── ui-ux-design/        # UI/UX & Frontend Design   (LINKS.md)
├── motion-animation/    # Motion & Animation          (LINKS.md)
├── video-motion/        # Video & Motion Video        (LINKS.md)
├── coding-language/     # Coding & Language Guidance  (LINKS.md)
├── coding-harness/      # Coding Harness & Agent Orchestration (LINKS.md)
├── content-media/       # Content & Media Generation  (LINKS.md)
├── research-web/        # Research & Web              (LINKS.md)
└── general/             # General / Meta Skills       (LINKS.md)
```

## How it works

This hub is an **index, not a copy**: each skill is recorded as a linked entry under its
category, pointing back to the source repo. We don't clone repos in — links keep the hub
small and always current with the original.

## Skill index

_Entries get added as skills are gathered. Format: `name` — one-line summary (source)._

| Category | Skill | Source |
|----------|-------|--------|
| UI/UX & Frontend Design | [Impeccable](https://github.com/pbakaus/impeccable) | [pbakaus/impeccable](https://github.com/pbakaus/impeccable) v4.4.0 |
| Motion & Animation / UI/UX | [emilkowalski/skills](https://github.com/emilkowalski/skills) | 13 skills by Emil Kowalski (aiforui.dev): 6 Motion & Animation + 5 UI/UX & Frontend + 2 Coding/Language. Per-skill links in each category's LINKS.md. |
| Video & Motion Video / Motion | [iart-ai/motion-skills](https://github.com/iart-ai/motion-skills) | Umbrella index of 16 packs / 53 motion-video skills (Remotion, Manim, GSAP/SVG, WebGL, canvas). Packs indexed under Video & Motion Video (6), Motion & Animation (9), General (1). |
| UI/UX & Frontend Design | [mattpocock/skills](https://github.com/mattpocock/skills) | Real-engineer skills: code review, TDD, debugging, architecture, domain modeling, research. ~28 skills. |
| Coding & Language Guidance | [superpowers](https://github.com/obra/superpowers) | Dev methodology for coding agents: TDD, debugging, planning, code review, subagents, git worktrees (14 skills). |
| Coding & Language Guidance | [ponytail](https://github.com/dietrichgebert/ponytail) | The 'lazy senior dev' — minimal one-line fixes (6 skills). |
| Coding & Language Guidance | [autoresearch](https://github.com/karpathy/autoresearch) | Autonomous overnight LLM experimentation agent. ML research project. |
| Coding & Language Guidance | [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills) | Single CLAUDE.md fixing Karpathy's LLM coding pitfalls. |
| Coding & Language Guidance | [garrytan/gstack](https://github.com/garrytan/gstack) | Ship like a team of 20: design/review/QA/ship for solo builders (~60 skills). Cross-cuts UI/UX + eng. |
| Motion & Animation | [greensock/gsap-skills](https://github.com/greensock/gsap-skills) | Official GSAP skills: core, timeline, ScrollTrigger, plugins, React/Vue, performance, utils (8). |
| Video & Motion Video | [heygen-com/hyperframes](https://github.com/heygen-com/hyperframes) | Write HTML, render video (shorts, captions, talking-head, Remotion, Figma). ~20 skills. |
| UI/UX & Frontend Design | [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | Great UI/UX skill + CLI: design, brand, design-system, ui-styling, slides. |
| Content & Media Generation | [tt-a1i/archify](https://github.com/tt-a1i/archify) | Turn any idea/plan into an interactive HTML visual (archify + archify-review). |
| General / Meta Skills | [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) | Curated index of 1497+ official agent skills across all categories. |
| Coding Harness & Agent Orchestration | [walkinglabs/learn-harness-engineering](https://github.com/walkinglabs/learn-harness-engineering) | Builds/audits harnesses that make AI coding agents reliable: AGENTS.md/CLAUDE.md, verification gates, scope boundaries, session handoff, memory, context budgets, tool-permission safety, multi-agent coordination. (1 skill) |
| Video & Motion Video | [latent-spaces/brag](https://github.com/latent-spaces/brag) | "You built it. Now brag." Turns a just-built project (or a website URL) into a 15–25s shareable launch video with music, motion and share copy — `/brag` (Hyperframes workflow) and `/brag-slim` (single-file, model-built). (2 skills) |
| General / Meta / Coding & Language / Coding Harness | [JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman) | Terse 'caveman' voice + token-efficiency toolchain for coding agents: /caveman, /ultracave, /megacave output voices, memory/log compression, code-mode Blocks, token-cost analytics — plus lean work patterns (investigate-first, surgical-patch, verify-and-stop…). (22 skills) |
| Video & Motion Video / Motion / Coding Harness | [calesthio/OpenMontage](https://github.com/calesthio/OpenMontage) | Agentic video production studio: 12 production pipelines (93 stage-director skills), 100+ tools, 60+ providers, 91 Agent Skills covering video/image/TTS/motion/Three.js/GSAP/HyperFrames. AGPL-3.0. |
| Research & Web | [d-research-skill](https://github.com/d-init-d/d-research-skill) | Production research workflow for agents: search, browser automation, APIs, archives, extraction, evidence ledgers, citation resolution and reproducible evals. (CC BY-NC 4.0) |
| Research & Web | [scraping-skills](https://github.com/thirdwatch-dev/scraping-skills) | Web scraping playbook for coding agents: anti-bot guidance (Cloudflare, DataDome, PerimeterX, Akamai), build-vs-buy decision tree, and ready-made scrapers for jobs, e-commerce, reviews, real estate and social. |
| Research & Web | [scrapling](https://github.com/D4Vinci/Scrapling) | Official agent skill of the Scrapling stealth-scraping framework: undetected browser automation, Cloudflare/anti-bot bypass, adaptive selectors, structured extraction. Ships SKILL.md plus an MCP server. |
| Research & Web | [last30days](https://github.com/mvanhorn/last30days-skill) | Research any topic across Reddit, X, YouTube, Hacker News, Polymarket and the web over the last 30 days, then synthesize a grounded brief with sources. |
| Research & Web | [agent-reach](https://github.com/Panniantong/Agent-Reach) | One CLI that gives agents eyes on the internet: read and search Twitter/X, Reddit, YouTube, GitHub, Bilibili, Xiaohongshu and Google - no API keys or paid tiers. |
| UI/UX & Frontend Design | [taste-skill](https://github.com/Leonxlnx/taste-skill) | Anti-slop design skill: art direction, real reference photographs instead of generic defaults, and a browser self-check against the rendered result. Plugin packaging for Claude Code and Codex. (1 skill) |
| UI/UX & Frontend Design | [frontend-design](https://github.com/anthropics/claude-code) | Anthropic's official `frontend-design` plugin skill inside Claude Code: distinctive visual design, deliberate layout/typography decisions, anti-templated defaults. |
| UI/UX & Frontend Design | [tasteskill](https://github.com/tasteskill/tasteskill) | The Anti-Slop Frontend Framework for AI agents: layout, typography and motion primitives, plus image-generation skills for building reference boards before coding. |
| Content & Media Generation | [image](https://github.com/coreyhaines31/marketingskills) | `image` skill for AI image generation: blog hero images, social graphics, product mockups and ad banners (repo also carries CRO, copywriting, SEO, analytics and growth skills). |
| Content & Media Generation | [brand-design-skill](https://github.com/ziguishian/brand-design-skill) | Image-first brand identity: Socratic intake, logo exploration, VI systems, industry style guidance and HTML brand manuals. Works in Codex and Claude Code. |
| Content & Media Generation | [social-media-skills](https://github.com/social-media-skills/skills) | 106 social-media skills incl. `design-and-templates` (brand kit + reusable on-brand template system), plus strategy, writing, video, publishing and analytics. |
| Content & Media Generation | [diagram-design](https://github.com/cathrynlavery/diagram-design) | Editorial diagram design for coding agents: 45 diagram types rendered as self-contained HTML+SVG - no Mermaid defaults, no dependency sprawl. |
| Coding Harness & Agent Orchestration | [pydantic-ai-harness](https://github.com/pydantic/skills) | Pydantic's official plugins for Claude Code, Codex and Cursor: `pydantic-ai-harness` (sub-agents, memory, context compaction, guardrails, spend limits), building agents with Pydantic AI, data validation, and Logfire observability. |
| Coding Harness & Agent Orchestration | [langchain-skills](https://github.com/langchain-ai/langchain-skills) | 22 skills for LangChain, LangGraph and Deep Agents: deep-agents-core (planning, sub-agent delegation, long-term memory, skills middleware), human-in-the-loop, persistence, decision models, eval engineering. Early development. |
| Coding Harness & Agent Orchestration | [agents-best-practices](https://github.com/DenisSergeevitch/agents-best-practices) | Provider-neutral agent-skill for Codex, Claude Code and friends: harness design patterns - agent loops, tool design, permissions, context management and evals. |
| Coding Harness & Agent Orchestration | [understand-anything](https://github.com/Egonex-AI/Understand-Anything) | Turn any codebase into an interactive knowledge graph: guided tours, search, and diff impact analysis - understand before you change. |
| Coding Harness & Agent Orchestration | [rea](https://github.com/morluto/rea) | Reverse-engineer anything with agents: app behaviour down to native binaries, JS/Electron bundles and .NET assemblies, with an evidence trail for every claim. |
| Coding Harness & Agent Orchestration | [headroom](https://github.com/headroomlabs-ai/headroom) | Compress tool outputs, logs, files and RAG chunks before they reach the LLM: 20%+ fewer tokens for coding agents with the answers left intact. |
| General / Meta Skills | [agentskills-spec](https://github.com/agentskills/agentskills) | The Agent Skills open specification and documentation: the SKILL.md format, progressive disclosure, reference implementations. The standard this hub indexes against. |
| General / Meta Skills | [anthropics-skills](https://github.com/anthropics/skills) | Anthropic's official public Agent Skills repository: document generation, design assets, web testing, MCP-server generation and more. |
| General / Meta Skills | [agent-skills-creator](https://github.com/mblode/agent-skills) | 28 skills led by `agent-skills-creator` (write, audit and merge skills with a validator), plus `agents-md`, UI/typography/dx audits, PR and release skills - "nobody ships AI slop on purpose". |
| General / Meta Skills | [agent-skills-catalog](https://github.com/magnus919/agent-skills) | 189 skills in the Agent Skills format for Hermes and other frameworks, incl. the `agent-skills` meta skill for creating/reviewing skills, plus evals, governance, production ops and multi-agent patterns. |
| Video & Motion Video | [feitangyuan/onetake](https://github.com/feitangyuan/onetake) | Launch films and feature demos with one continuous take — no cuts, continuity oracle scores every boundary, ~38 camera moves, deterministic 4K60. |
| Motion & Animation | [JohnHeibel/ClaudeAnimationBase](https://github.com/JohnHeibel/ClaudeAnimationBase) | Animate hand-painted cartoons (Clawd, 31 emotions) in p5.js + p5.brush: storyboard → contact-sheet self-check → mp4, with ANIMATION_GUIDE.md. |
| Video & Motion Video | [pyang5166/gbro-collage-broll](https://github.com/pyang5166/gbro-collage-broll) | ~5s voiceover line → editorial halftone paper-collage B-roll clip (9:16) via Gemini Omni Flash first/last-frame video; metaphor → still → video approval gates. |
