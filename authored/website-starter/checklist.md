# Website launch checklist

Every item here is a **MUST**: the site is not done until each one is true and its proof is written.
The sections follow the order a build goes in, not an order of importance.

**How to use it.** Copy this file into the project as `LAUNCH-CHECKLIST.md` and replace each ☐ with
evidence: a measured value, a URL with its status code, a command's output, or the path of a
screenshot. "Looks fine" is not proof. Where an item genuinely does not apply, write `N/A` and a
one-line reason.

**Free tools the proofs rely on:** the browser's developer tools; [Lighthouse](https://developer.chrome.com/docs/lighthouse/)
or [PageSpeed Insights](https://pagespeed.web.dev/); [axe DevTools](https://www.deque.com/axe/devtools/);
the [Schema.org validator](https://validator.schema.org/) and [Rich Results Test](https://search.google.com/test/rich-results);
`curl -I` for headers; `npm audit` or `pip-audit` for dependencies.

Section 5 is a checklist of what the legal pages must say. It is not legal advice.

## 1. Purpose and content

| # | Must be true | Proof |
|---|--------------|-------|
| 1 | The first screen tells a visitor what the site is, who it is for and what to do next. | ☐ Screenshots of the home page at 1440×900 and 390×844 |
| 2 | Every page has one job and one primary call to action. | ☐ Page list with goal and call to action per page |
| 3 | No placeholder copy or images anywhere: nothing reads "lorem", "coming soon" or "[REPLACE". | ☐ Search of the built site for `lorem`, `TODO`, `REPLACE`, `placeholder`, `coming soon` returns nothing |
| 4 | Nothing is invented: every testimonial, client name, statistic, award and price came from the owner. | ☐ Each claim traced to the brief or a source |
| 5 | A working contact route: an email address, or a form that has been submitted once for real. | ☐ Test message received |
| 6 | Every page is reachable through links from the home page. No orphans. | ☐ Link report: each URL linked at least once |
| 7 | An unknown URL returns a 404 page with a link back. | ☐ URL, status code, screenshot |
| 8 | Favicon set: `/favicon.ico`, a sharp icon for tabs and `apple-touch-icon` for phones. | ☐ `200` for each file, `<link rel="icon">` present |
| 9 | The footer on every page has the name, a contact email, links to the legal pages and the copyright year. | ☐ Screenshot |

## 2. Structure and accessibility

The bar is WCAG 2.2 Level AA. Automated tools catch only part of it, so items 4 to 11 are checked by hand.

| # | Must be true | Proof |
|---|--------------|-------|
| 1 | `<html lang="…">` names the page's language. | ☐ View-source |
| 2 | One `h1` per page, stating the page's topic. Headings nest in order (`h1`, then `h2`, then `h3`) and none is skipped for styling. | ☐ Heading outline |
| 3 | Landmarks present: `header`, `nav`, one `main`, `footer`. A second navigation is labelled. | ☐ Outline |
| 4 | Keyboard only: Tab reaches every link, button and field in a sensible order, focus is always visible, and nothing traps the cursor. A skip link jumps to the content. | ☐ Keyboard-only pass over each page, with notes |
| 5 | Body text has a contrast ratio of at least 4.5:1 against its background; large text and the edges of buttons and form fields at least 3:1. | ☐ Contrast reading for each text and background pair |
| 6 | Text can be doubled in size, and the page holds together at 320 px wide: no horizontal scrolling, clipped text or overlap. | ☐ Screenshots at 200% zoom and at 320 px |
| 7 | Informative images have alt text that says what they show. Decorative ones have empty alt text. | ☐ Image audit |
| 8 | Forms: a visible label for every field, required fields marked, instructions before the field, and errors in text that is linked to the field. | ☐ Submit each one empty, wrong and correct |
| 9 | Tap targets are at least 24×24 CSS pixels and not crowded against each other. | ☐ Mobile pass |
| 10 | Motion respects `prefers-reduced-motion`. Nothing plays sound by itself or flashes more than three times a second. Video has captions and audio has a transcript. | ☐ Reduced-motion setting on; media audit |
| 11 | Link text makes sense on its own ("Pricing", not "click here"), and links are told apart by more than colour. | ☐ Read the page with links only |
| 12 | An automated scan finds no critical or serious issue. | ☐ axe DevTools or Lighthouse accessibility report |

## 3. SEO

| # | Must be true | Proof |
|---|--------------|-------|
| 1 | Every page has a unique `<title>` of 50 to 60 characters: the page's main phrase first, the brand last. | ☐ List of titles from a crawl |
| 2 | Every page has a unique meta description of about 150 to 160 characters that reads as a pitch for that page. | ☐ List from the crawl |
| 3 | One canonical URL per page, in `<link rel="canonical">`, matching the live URL. | ☐ Crawl |
| 4 | One host and one scheme: HTTP redirects to HTTPS, and the other host form (apex or `www`) redirects to the chosen one, with a permanent redirect (`301` or `308`) on every page. | ☐ `curl -I` on each variant: status and `location` |
| 5 | URLs are lowercase words separated by hyphens, with no `?id=` in page addresses. | ☐ URL list |
| 6 | `sitemap.xml` lists every indexable page and nothing else: no redirects, 404s or duplicates. | ☐ Sitemap count against the pages on the site |
| 7 | `robots.txt` points to the sitemap and does not block content, CSS or JavaScript. No stray `Disallow: /`. | ☐ The file, and the robots report in Search Console |
| 8 | Pages are indexable by default. `noindex` appears only where it is meant: staging, previews, admin, internal search results. | ☐ Crawl: list of `noindex` pages |
| 9 | Social preview on every shareable page: `og:title`, `og:description`, `og:image` at 1200×630, `og:url`, and `twitter:card`. | ☐ Link pasted into Slack; [Meta Sharing Debugger](https://developers.facebook.com/tools/debug/) |
| 10 | Structured data in JSON-LD with no errors: `Organization` or `Person`, `WebSite`, and the page's type (`Article`, `BlogPosting`, `Product`, `Service`, `LocalBusiness`, `FAQPage`, `BreadcrumbList`). | ☐ Schema.org validator and Rich Results Test |
| 11 | The main content is in the HTML as sent. It does not depend on JavaScript running. | ☐ `curl` of the page shows the text |
| 12 | Internal links: every page is linked from at least one other page, with descriptive anchor text, and related pages are grouped under an index or hub page. | ☐ Link report |
| 13 | Paid or unvetted external links carry `rel="sponsored"` or `rel="nofollow"`. | ☐ List of external links |
| 14 | When replacing a site: every old URL returns a permanent redirect (`301` or `308`) to its closest new page. | ☐ Redirect map with status codes |

Google stopped showing FAQ rich results for most sites in 2023, so write FAQs for readers first.
The `FAQPage` markup is still useful structure for other search engines and AI tools.

## 4. AEO

Answer engine optimisation: being the source that AI assistants and search AI quote (Google AI
Overviews, ChatGPT search, Perplexity, Copilot). Every item here helps ordinary search as well.

| # | Must be true | Proof |
|---|--------------|-------|
| 1 | Each content page opens with a direct answer of roughly 40 to 60 words, under a heading worded as the question people ask. The detail comes after. | ☐ First screen of each content page |
| 2 | One topic per URL, and the page answers the whole question without needing a second page. | ☐ Page plan |
| 3 | Steps, comparisons, definitions and prices sit in lists or tables, labelled with what they are. | ☐ Page review |
| 4 | Facts are concrete: numbers, dates, versions, prices and names, not "many", "several" or "industry-leading". | ☐ Page review |
| 5 | The site says exactly who is behind it: the same name, contact and location on the site, on the About page and in the `Organization` or `Person` schema, with `sameAs` links to the official profiles. | ☐ The three side by side |
| 6 | Time-sensitive pages show their dates: `datePublished` and `dateModified` in the schema and a visible date on the page. | ☐ Schema and screenshot |
| 7 | Claims name their sources, and the page includes something only this site has: first-hand data, measurements or worked examples. That is what gets cited. | ☐ Page review |
| 8 | Content is readable without a login, a paywall or JavaScript. | ☐ Private window with JavaScript off |
| 9 | `/llms.txt` lists the key pages with a one-line summary each, and is generated from the same source as the sitemap so it cannot drift. It is a proposed convention ([llmstxt.org](https://llmstxt.org/)), not a standard. | ☐ The file, and the script that writes it |
| 10 | AI crawlers are a decision, not an accident: `robots.txt` names the known ones (`GPTBot`, `OAI-SearchBot`, `ClaudeBot`, `PerplexityBot`, `Google-Extended`, `Applebot-Extended`, `CCBot`) as allowed or disallowed, matching what the owner chose. | ☐ The `robots.txt` lines and the owner's decision |

## 5. Legal and privacy

These pages must describe what the site actually does. The outlines are in
[`legal-pages.md`](legal-pages.md). Anything regulated, such as finance, health or children's
data, needs a professional review before launch.

| # | Must be true | Proof |
|---|--------------|-------|
| 1 | Privacy policy is live and linked in the footer. It names the entity and a contact, and lists every personal-data source the site really has: form fields, newsletter, analytics, cookies, logs, each with its purpose and retention period. | ☐ Its "what we collect" table next to the site's forms and scripts: one row per real source |
| 2 | Terms and conditions are live and linked in the footer: what the site offers, acceptable use, intellectual property, disclaimers, liability, termination, governing law, how changes are announced, contact. | ☐ Its sections against the outline |
| 3 | Every cookie and local-storage item is inventoried: name, who sets it, purpose, lifetime. | ☐ The inventory, checked in a private window |
| 4 | Consent comes first: no non-essential cookie or third-party script runs before the visitor chooses. Reject is as easy as Accept, nothing is pre-ticked, and the choice is remembered and can be changed. | ☐ Storage tab is clear on first load; choose Reject, reload |
| 5 | Forms show a link to the privacy policy and, where consent is required, an unticked box beside the submit button. Spam protection (a honeypot or a rate limit) does not block assistive technology. Success and failure messages appear on the page. | ☐ Submit each form empty, wrong and correct |
| 6 | If there is a newsletter: subscribers opt in, and every email carries a working unsubscribe link. | ☐ Test email |
| 7 | Entity details are the real ones, supplied by the owner. | ☐ No `[REPLACE` remains |
| 8 | Fonts, icons, photos and illustrations are licensed for commercial use on the web, and credit is shown where the license asks for it. | ☐ Asset list with license and source |
| 9 | Third-party embeds (video, maps, chat widgets) are named in the privacy policy and, if they set cookies, load only after consent. | ☐ Embed audit with cookies cleared |
| 10 | The owner knows which law applies to their visitors (GDPR and UK GDPR for EU and UK visitors; Malaysia's PDPA 2010 for commercial transactions; any sector rules) and has had the pages reviewed if the business is regulated. | ☐ The owner's confirmation |

## 6. Performance

The first three are Google's Core Web Vitals "good" thresholds, measured for mobile.

| # | Must be true | Proof |
|---|--------------|-------|
| 1 | Largest Contentful Paint at 2.5 seconds or less. | ☐ Lighthouse or PageSpeed Insights, mobile |
| 2 | Interaction to Next Paint at 200 ms or less. At launch, read it from a Total Blocking Time under 200 ms in the lab run. | ☐ Same run |
| 3 | Cumulative Layout Shift of 0.1 or less. | ☐ Same run |
| 4 | Lighthouse performance score of 90 or more on mobile. | ☐ Same run |
| 5 | Every image has `width` and `height` (or an `aspect-ratio`), is served as WebP or AVIF, and comes in a size for each breakpoint (`srcset`). | ☐ Network tab: largest image files |
| 6 | The hero image is not lazy-loaded and is given priority. Images below the fold are `loading="lazy"`. | ☐ View-source |
| 7 | Fonts are WOFF2, subset to the languages used, with the main file preloaded and `font-display: swap` so text shows while they load. System fonts are the fallback. | ☐ Network tab |
| 8 | Only the scripts the page uses are loaded. Analytics and other third-party scripts wait for consent or for idle time. | ☐ Network tab |
| 9 | HTML, CSS and JavaScript are served compressed (Brotli or gzip). Static assets have long cache lifetimes and versioned filenames. | ☐ `curl -I`: `content-encoding`, `cache-control` |
| 10 | The home page's first load on mobile is 1 MB or less. | ☐ Network tab total |

## 7. Security

| # | Must be true | Proof |
|---|--------------|-------|
| 1 | HTTPS on every page with a valid certificate. HTTP permanently redirects. | ☐ `curl -I` on both; certificate details |
| 2 | These headers on every response: `Strict-Transport-Security`, `Content-Security-Policy`, `X-Content-Type-Options: nosniff`, `Referrer-Policy`, `Permissions-Policy`, and `frame-ancestors` (or `X-Frame-Options`). If inline scripts prevent an enforcing CSP, start with report-only and record it as a known gap. | ☐ `curl -I` |
| 3 | No secrets reach the browser: API keys, tokens and passwords live in server-side environment variables only. | ☐ Search of the built client files for `key`, `token`, `secret` |
| 4 | Input is validated on the server and echoed back escaped. State-changing requests are protected against cross-site request forgery. Forms are rate-limited. | ☐ Try markup in a field; try a forged request |
| 5 | No high or critical dependency vulnerabilities are left open. | ☐ `npm audit` or `pip-audit` output |
| 6 | Error pages show a message, not a stack trace or a server version. | ☐ Force a 500 on staging |
| 7 | Admin, preview and staging addresses are not public, and staging is `noindex`. | ☐ The addresses and their protection |
| 8 | Backups run automatically and one restore has been tested. A static site's backup is its pushed repository. | ☐ Restore test, or the repository URL |
| 9 | Two-factor authentication is on for the registrar, hosting, DNS and analytics accounts. | ☐ The owner confirms |

## 8. Screens and browsers

| # | Must be true | Proof |
|---|--------------|-------|
| 1 | At 360, 768 and 1280 px wide there is no horizontal scrolling, clipped text or overlap, and the menu works. | ☐ Screenshots at each width |
| 2 | Current Chrome, Safari, Firefox and Edge all work, and the main path has been walked on a real iPhone and a real Android phone. | ☐ List of devices and browsers tried |
| 3 | Mobile keeps everything essential: content, contact and legal links. | ☐ Phone screenshots |
| 4 | Phone numbers and email addresses are tappable links. | ☐ Tap test |

## 9. Measurement and operations

| # | Must be true | Proof |
|---|--------------|-------|
| 1 | Visits are measured: an analytics tool, or the server's logs. Where consent is needed, the script loads only after it. | ☐ A visit appears in the report. No analytics at all is a recorded owner decision |
| 2 | Errors are reported somewhere: an error tracker, or the host's logs if the site is dynamic. | ☐ The report or log location |
| 3 | The home page is watched by an uptime monitor that alerts someone. | ☐ Monitor status |
| 4 | If the domain sends email, it arrives: SPF, DKIM and a DMARC record are published. | ☐ DNS lookup of the three records |
| 5 | How to deploy, and where each account lives, is written down in the project. | ☐ Path of the README or deploy notes |

## 10. Launch

These need the owner. An agent prepares each one and asks before acting.

| # | Must be true | Proof |
|---|--------------|-------|
| 1 | The domain is registered, set to renew automatically, and DNS covers both the apex and `www`. | ☐ Registrar and DNS settings |
| 2 | Google Search Console and Bing Webmaster Tools are verified, the sitemap is submitted, and indexing is requested for the home page. | ☐ Screenshots of both |
| 3 | The share card was checked in [Meta's Sharing Debugger](https://developers.facebook.com/tools/debug/) and [LinkedIn's Post Inspector](https://www.linkedin.com/post-inspector/), and by pasting the link into Slack or a chat. | ☐ Screenshots |
| 4 | The old site was exported before anything was replaced, and its URLs redirect (section 3, item 14). | ☐ Backup location |
| 5 | Ownership is written down: registrar, hosting, analytics, form and email accounts, each with who holds the login, kept in a password manager rather than the repository. | ☐ The list, outside the repository |
| 6 | The owner has walked the live site on their own phone: home, one content page, contact, each legal page, the footer. | ☐ The owner says it is right |

## Worth having, not launch blockers

- An RSS or Atom feed for a blog.
- `hreflang` tags when there is more than one language.
- A web app manifest and icons so the site can be installed on a phone.
- A print stylesheet for long pages.
- A dark colour scheme.
- A date in the calendar to review the content, prices, dates and legal pages, twice a year.
