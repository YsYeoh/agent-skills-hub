# Stacks: combining skills into pipelines

The index answers "what skills exist". This file answers a harder question: **which ones
work well together, and in what order?**

The pattern across every stack below: **one skill sets direction, one does the work, one
checks it, one distributes it.** Follow the arrows in order — stacking two skills that both
claim the same job (two anti-slop design skills, or `brag` alongside OpenMontage's promo
pipeline) makes them fight each other, not cooperate.

Every skill linked here is indexed in [`README.md`](README.md) by its category.

---

## 1. Ship a feature (coding)

| Stage | Skill | Why it goes here |
|-------|-------|------------------|
| Method first | [superpowers](https://github.com/obra/superpowers) or [mattpocock/skills](https://github.com/mattpocock/skills) | TDD, debugging, planning, review — the discipline the rest of the stack hangs off. |
| Workflow | [gstack](https://github.com/garrytan/gstack) | design → review → QA → ship for a solo builder (~60 skills). |
| Taste | [tasteskill](https://github.com/tasteskill/tasteskill) or [frontend-design](https://github.com/anthropics/claude-code) | Keeps the UI from coming out generic. |
| Guardrails last | [learn-harness-engineering](https://github.com/walkinglabs/learn-harness-engineering) | Writes the verification gates and context budgets that keep the *next* session reliable. |

Why it works: methodology first, taste in the middle, guardrails at the end. Starting with a
checking skill is backwards — there is nothing yet to check.

## 2. Idea → published article (research → writing)

1. [d-research-skill](https://github.com/d-init-d/d-research-skill) — evidence ledger and citations, the factual spine.
2. [last30days](https://github.com/mvanhorn/last30days-skill) — what people are actually saying right now.
3. [scrapling](https://github.com/D4Vinci/Scrapling) or [scraping-skills](https://github.com/thirdwatch-dev/scraping-skills) — reach the pages that block plain fetches.
4. [diagram-design](https://github.com/cathrynlavery/diagram-design) — the figures (45 diagram types, HTML+SVG, no Mermaid defaults).
5. [tasteskill](https://github.com/tasteskill/tasteskill) — how the page looks.
6. [social-media-skills](https://github.com/social-media-skills/skills) — the launch posts.

This is essentially the pipeline this portfolio's own blog runs on: evidence, then figures,
then layout, then distribution.

## 3. Idea → launch video (content → video)

The tool-level chain is documented in [`tools/LINKS.md`](tools/LINKS.md):

> `auto-editor` strips silence → `whisperx` gives word-level timestamps → `moviepy` does the
> edit → `remotion` when the video is templated or data-driven.

Around that chain:

- **Cover art:** [image](https://github.com/coreyhaines31/marketingskills) or [brand-design-skill](https://github.com/ziguishian/brand-design-skill)
- **Share cut:** [brag](https://github.com/latent-spaces/brag) for the 15–25s promo clip
- **Publish:** [social-media-skills](https://github.com/social-media-skills/skills)

⚠️ **Pick one lane:** [OpenMontage](https://github.com/calesthio/OpenMontage) already bundles
most of this as 12 production pipelines with 91 skills. Use OpenMontage *or* the four-piece
stack, not both.

## 4. Reliable agent harness (the meta stack)

1. [agents-best-practices](https://github.com/DenisSergeevitch/agents-best-practices) — agent loops, tool design, permissions, context management, evals.
2. [pydantic-ai-harness](https://github.com/pydantic/skills) — sub-agents, memory, context compaction, guardrails, spend limits.
3. [learn-harness-engineering](https://github.com/walkinglabs/learn-harness-engineering) — AGENTS.md and session handoff.
4. [caveman](https://github.com/JuliusBrussee/caveman) — token efficiency for long runs.

This stack maps almost one-to-one onto the eight design layers of an agent (system prompt →
knowledge → tools → guardrails → router → observability → orchestration → run logs), which is
why it makes a good worked example when explaining that architecture.

## 5. Brand → landing page (design)

1. [brand-design-skill](https://github.com/ziguishian/brand-design-skill) — identity and the style guide.
2. [tasteskill](https://github.com/tasteskill/tasteskill) — reference boards **before** any code.
3. [Impeccable](https://github.com/pbakaus/impeccable) — the polish pass.
4. [ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) — the actual build.

Direction before pixels, always in that order.

---

## The two rules that make stacks work

1. **No overlapping claims.** Two skills that both say "this is how you design" will
   contradict each other in the same context window. Check each skill's description against the
   ones already in the stack; if two do the same job, keep the one with the tighter
   description.
2. **End with a checker, never start with one.** QA, review and audit skills are the last
   stage — they verify output that a worker skill produced.

Related reading: [Skills vs MCP vs Subagents](https://www.yongsen.space/blog/agent-skills-vs-mcp-vs-subagents),
[The Anatomy of a SKILL.md](https://www.yongsen.space/blog/how-to-write-skill-md-anatomy).