# Imikan Technologies - SEO Summary

## Website: https://www.imikan-technologies.com/
## Last updated: 2026-07-11

---

## 1. ON-PAGE SEO

### Title Tag (current)
`Imikan Technologies | RAG & AI Chatbots | Nigeria & Africa`

### Meta Description (current)
`Imikan Technologies is a self-hosted RAG and AI chatbot vendor for banking, legal, healthcare, and government clients across Nigeria, Africa & worldwide.`

Both are trimmed to spec length and reflect the actual, verifiable business description — no inflated claims.

### Keywords
Meta keywords tag includes relevant terms: RAG, Retrieval-Augmented Generation, AI chatbot, Shopify AI, enterprise AI, vector search, AI solutions Nigeria/Africa, pgvector, NLP, LLM, OpenAI, GPT, Claude, tech company Nigeria, AI startup Africa, digital transformation AI. (Note: meta keywords carry negligible ranking weight with modern search engines — kept mainly for internal reference and legacy crawlers.)

---

## 2. STRUCTURED DATA (JSON-LD)

Six schema.org blocks are live in `index.html`:

1. **Organization** — name, logo, RC-registered description, Lagos/NG address, areaServed (Nigeria, Africa, Global), real social profiles (X, LinkedIn, YouTube), contact point (real email + phone), knowsAbout topics.
2. **WebSite** — site-level entity with a SearchAction pointing at the homepage query param.
3. **SoftwareApplication (RAG Engine)** — product entity with feature list; no user ratings or review counts included.
4. **SoftwareApplication (Shopify AI Chatbot)** — same pattern, no fabricated ratings.
5. **Service** — RAG-as-a-service entity with an offer catalog linking the two product lines.
6. **WebPage** — page-level entity with `datePublished` / `dateModified` for freshness signals.

**Explicitly removed in an earlier pass and confirmed absent from the current build:**
- Fake `AggregateRating` schema (no review data existed to back it)
- Unearned SOC 2 compliance claim
- Inflated usage statistics
- Fabricated client logos

**Open item worth a look:** both `SoftwareApplication` blocks currently list `"price": "0", "priceCurrency": "USD"` — a placeholder from the original build. Since these aren't actually free products, this is a candidate for either removing the `offers` field entirely or replacing it with accurate pricing language, to stay consistent with the authenticity standard applied elsewhere on the site.

---

## 3. GEO-TARGETING

- Organization schema addressCountry/addressRegion set to Nigeria/Lagos
- areaServed covers Nigeria, Africa, and Global
- Content copy explicitly targets Nigeria/Africa market language throughout (RC registration number, NDPR references, local pricing context)

---

## 4. CONTENT INTEGRITY

Per the site's authenticity standard, the following were identified as liabilities and removed:
- Hidden `sr-only` keyword-stuffing block (confirmed: no hidden keyword div exists in the current build — the only `.sr-only` reference is Tailwind's own compiled utility-class definition, unused for content)
- Fake AggregateRating schema
- Unearned SOC 2 claim
- Inflated usage stats
- Fabricated client logos

Replaced with real, verifiable elements:
- Real client logos (Gratiam Dei, NACPFA, Snicks, TechStore, Tita Learning) as properly sized WebP images with descriptive alt text
- RC 9535211 registration number as a credibility marker
- Accurate 12–24 week enterprise RAG deployment timeline (corrected from an earlier underestimated 8–16 week figure)

---

## 5. TECHNICAL SEO

### Sitemap (`sitemap.xml`)
Four URLs currently indexed: homepage, FAQ, privacy, terms — with `lastmod`, `changefreq`, and `priority` set appropriately. (Note: `about.html` is not currently listed in `sitemap.xml` — worth adding if it should be indexed.)

### Robots.txt
- Allows all major crawlers (Googlebot, Bingbot, DuckDuckBot, Yandex, Baiduspider) explicitly
- References `sitemap.xml`
- Includes a `Content-Signal: search=yes, ai-input=yes, ai-train=yes` directive — AI crawlers are intentionally allowed for maximum visibility
- Sets a 1-second crawl delay

### llms.txt
Present and validated with proper Markdown link syntax. Summarizes services, key pages, published Medium articles, and social links for LLM-based crawlers/answer engines.

### Accessibility
- Proper heading hierarchy (H1 → H2 → H3)
- Descriptive alt text on all images, including client logos
- WCAG AA color contrast corrected
- Focus-visible styles for keyboard navigation

---

## 6. SOCIAL / SHARE METADATA

Open Graph and Twitter Card tags reflect the same accurate title/description used in the primary meta tags — no separate inflated copy for social shares.

---

## 7. SECURITY (supports SEO trust signals)

- Cloudflare (Bot Fight Mode, client-side security)
- `security.txt` published at `.well-known/security.txt`
- GitHub repo kept private with 2FA and branch protection on `main`

---

## 8. CONTENT MARKETING (off-site, supports domain authority)

Five Medium posts published, each cross-posted to LinkedIn and X:
1. What is Retrieval-Augmented Generation (RAG)? A Complete Guide for Businesses
2. Natural Language Processing (NLP) for Business
3. How to Deploy AI in Your Business: A Step-by-Step Guide
4. Nigeria-specific RAG pricing piece
5. Vector Search vs Keyword Search

All three of these are linked from `llms.txt`; index.html links to at least the RAG and NLP posts directly.

---

## 9. FILES CURRENTLY LIVE

| File | Purpose |
|------|---------|
| `index.html` | Main landing page |
| `about.html` | Company background (not yet in sitemap) |
| `faq.html` | FAQ page, in sitemap |
| `privacy.html` | NDPR-compliant privacy policy, in sitemap |
| `terms.html` | Terms of service, in sitemap |
| `sitemap.xml` | 4 URLs |
| `robots.txt` | Crawler rules incl. AI crawlers |
| `llms.txt` | LLM-facing summary |
| `.well-known/security.txt` | Security contact/disclosure |

---

## 10. NEXT STEPS

### Short term
1. Decide on the `offers.price: "0"` placeholder in the two `SoftwareApplication` schemas — remove or correct
2. Add `about.html` to `sitemap.xml` if it should be indexed
3. Continue Medium cadence; link newest posts into `index.html` and `llms.txt` as they publish
4. Submit refreshed sitemap to Google Search Console and Bing Webmaster Tools if not already done this cycle

### Medium term
5. Monitor Core Web Vitals / PageSpeed Insights and cross-reference against RankMath (watching for stale-crawl false negatives)
6. Consider testimonials or case studies — only with real, permissioned client input, consistent with the authenticity standard
7. Evaluate whether additional JSON-LD (e.g. BreadcrumbList) would help as more pages are added

---

**Maintained by:** Imikan Technologies
**Contact:** contact@imikan-technologies.com
**Website:** https://www.imikan-technologies.com/
