---
name: website-starter
description: Fill-in starting prompt and MUST-pass launch checklist for building a website with a coding agent. Use when asked to build, redesign or launch a website, landing page, portfolio, blog or small-business site, or to check whether an existing site is ready to go live. Covers the brief to paste, the build order, and the must-haves for SEO, AEO (answer engine optimisation), legal pages (privacy policy, terms, cookies), accessibility, performance and security.
license: MIT
---

# Website starter

Two parts, used together:

1. **The starting prompt.** A brief to fill in and paste to a coding agent, so it builds the
   right site instead of guessing.
2. **The checklist.** Everything the site must have before it is called done, in
   [`checklist.md`](checklist.md): SEO, AEO, legal pages, accessibility, performance, security and
   the launch steps.

For an agent reading this skill: the prompt template is what you receive from the person. The
steps below are how to turn it into a finished site and prove it against the checklist.

## When to use

- A new website, landing page, portfolio or blog is being built.
- An existing site is being redesigned or relaunched.
- Someone asks whether a site is ready to launch, or asks for an SEO or pre-launch check: run
  `checklist.md` against it and report.
- The site is content plus a few forms. For a product with accounts and payments the checklist
  still applies; the build order below does not cover the backend.

## Step 1: Start from the prompt

Copy the template, replace every `[bracketed]` field, and paste it to the agent.

The four fields marked **(required)** are the ones to answer before starting. Any other field can
stay as "you choose": the agent decides and reports what it assumed.

```text
Build my website end to end. Follow the website-starter skill: build from this brief, then run
checklist.md and report every MUST item as PASS or FAIL with its proof.

## Project
- Name: [site or business name] (required)
- What it is, in one sentence: [e.g. a portfolio where I publish tutorials on building AI agents] (required)
- Who it is for: [the one kind of visitor you care about most] (required)
- The one thing a visitor should do: [e.g. email me / book a call / read the latest post / buy] (required)
- Why they should believe me: [2-3 true facts: years doing this, clients, projects, credentials]

## Pages
- [Every page and its one job. e.g. Home - the pitch and the call to action; Work - six case
  studies; About; Contact]
- Legal pages, always included: Privacy policy and Terms and conditions, plus a Cookie policy if
  the site sets non-essential cookies.

## Content
- Copy I already have: [file paths or links, or "none - write a first draft for every page and mark it DRAFT"]
- Facts you may use about me: [contact email, city or country, social profiles, real project names]
- Do not invent testimonials, client names, numbers, prices or legal entity details. Write
  [REPLACE: what is needed] instead and list every one for me at the end.

## Look and feel
- Voice: [e.g. plain and direct, no jargon / warm / technical]
- Palette: [hex codes, or "choose one neutral and one accent"]
- Typefaces: [names, or "choose a readable pairing"]
- Logo and images: [file paths, or "none - leave labelled placeholders"]
- Hero or section backgrounds: [a style keyword such as "grainy gradients" or "fluted glass", or "none"]
- Sites I like: [URLs] - for layout and tone only; do not copy them.

## Stack and limits
- Stack: [e.g. Next.js / Astro / plain HTML and CSS / "choose the simplest stack that meets the goal"]
- Region and languages: [e.g. Malaysia, English]
- Deadline: [date, or "none"]
- Must not change: [e.g. keep my current domain and URLs / keep the copy from the old site]

## Rules
- Ask me before buying anything, creating an account, deploying in public, or deleting existing content.
- Otherwise make sensible choices, write down each assumption, and keep going.
- Done means every MUST item in checklist.md passes, with its proof written next to it.
```

The 22 background keywords and a full prompt for each are in this hub's `DESIGN-KEYWORDS.md`. Outside
the hub, any style word the person names will do.

If you are the agent receiving it:

- If a **(required)** field is missing or contradicts the content you were given, ask once, in a
  single message, and wait. Who the site is for and what a visitor should do there are not things
  to guess.
- Everything else: choose sensibly, write each choice on an "Assumptions" list, and keep going.
- Never fill a gap with an invented fact, whether a legal entity, an address, a statistic, a
  testimonial or a price. Leave `[REPLACE: what is needed]` and collect them for the hand-back.
- Stop and ask before buying anything, creating an account, deploying in public, or deleting
  existing content.

## Step 2: Plan on one screen before any code

Write the plan first and keep it to one screen: every page with its goal and its primary call to
action, the navigation, the stack, and any checklist item that will be out of scope, with the
reason.

## Step 3: Build in this order

1. **Content.** Real headings, paragraphs and calls to action for every page. Where the brief has
   no copy, write a first draft and mark it `DRAFT`.
2. **Structure.** Semantic HTML: one `h1`, headings in order, `header`, `nav`, `main`, `footer`,
   all working before any CSS or JavaScript is added.
3. **Style.** Layout, type scale, spacing and colour, built at phone width first and then widened.
4. **Search and answer metadata.** Titles, descriptions, canonical URLs, Open Graph tags, JSON-LD,
   the sitemap and `robots.txt`, placed in the page templates rather than added afterwards.
5. **Legal pages.** Privacy, Terms and, where the site sets non-essential cookies, the Cookie
   policy, written from the outlines in [`legal-pages.md`](legal-pages.md) and from what the site
   actually collects.
6. **Motion and polish, last.** Only where it helps the visitor, and it respects
   `prefers-reduced-motion`.

## Step 4: Prove it against the checklist

1. Copy [`checklist.md`](checklist.md) into the project as `LAUNCH-CHECKLIST.md`.
2. Go through every **MUST** item and replace its proof cell with evidence: a measured value, a
   URL with its status code, a command's output, or the path of a screenshot.
3. An item is done only when its proof is written. `N/A` needs a one-line reason.
4. Fix every FAIL, then re-run only those items.

## Step 5: Hand back

Finish with one message containing:

- **Placeholders to replace**: every `[REPLACE: …]` still in the site, with the page it is on.
- **Decisions for the owner**: anything only they can decide, such as the cookie and analytics
  choice, the governing law, and whether AI crawlers may read the site.
- **Launch steps that need a human**: domain, hosting, Search Console, backups, listed in section
  10 of the checklist.
- **The result**: the checklist with PASS, FAIL and N/A counts, and nothing marked done without its
  proof.

## Design rules for the build

- The first screen answers, in this order: what is this, is it for me, what do I do next.
- One job and one primary call to action per page.
- Real content over filler: no lorem ipsum, no generic claims, no invented social proof.
- Hierarchy through size, weight and spacing first; colour last.
- Motion has a job, such as showing what changed or where something moved to, and never holds up
  reading.
- Consistent over clever: the same spacing scale, type scale and component behaviour on every
  page.
