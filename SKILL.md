# SKILL.md — ChatGPT-find-me

## Name

ChatGPT-find-me

## Objective

Transform a standard website into one that is easier to be found, read, understood, cited, and used by ChatGPT, AI search engines, web agents, and semantic crawlers.

This skill does not promise to "rank on ChatGPT." It improves the probability of the site being:

1. discovered;
2. crawled;
3. understood;
4. used as a factual source;
5. cited when supporting a specific claim;
6. accessible to agents that need to navigate, compare, fill out forms, or extract data.

## Core Principle

An AI-findable website needs to be:

* crawlable;
* readable without mandatory JavaScript;
* semantically explicit;
* factual;
* verifiable;
* up to date;
* well-structured;
* easy to cite;
* accessible to humans and agents.

The rule of thumb is:

> If the important fact does not appear in clean textual HTML, with its own URL, clear title, date, context, and semantic relationship, treat it as if the AI will likely not see it reliably.

## When to Use This Skill

Use this skill when the user asks to:

* improve a website to appear on ChatGPT;
* optimize a website for AI Search, GEO, AEO, or LLM discovery;
* make a website more citable;
* prepare landing pages for agents;
* transform a standard website into an agent-readable site;
* improve pricing, product, service, documentation, or company pages;
* create `robots.txt`, `sitemap.xml`, `llms.txt`, `schema.org`, or canonical pages;
* audit whether a website is easily readable by ChatGPT.

## Expected Inputs

Request or use, if already available:

* Website URL;
* Main objective of the website;
* Target audience;
* Main products, services, or concepts;
* City/region, if it's a local business;
* Critical pages: home, pricing, product, services, docs, blog, about, contact;
* Claims the user wants the AI to understand;
* Direct competitors;
* Terms for which the site should be found;
* Whether the site is static, SSR, SPA, WordPress, Next.js, Nuxt, Astro, Laravel, etc.

## Expected Output

The skill must deliver:

1. AI findability diagnosis;
2. Claims map;
3. Technical corrections;
4. Recommended page structure;
5. Auxiliary files;
6. JSON-LD Schema;
7. Publishing checklist;
8. Validation tests;
9. Final report in Markdown.

## Operational Definitions

### Fetched

The page was found and read by the engine, but didn't necessarily appear to the user.

### Cited

The page was used as a clickable source to support a specific sentence.

### Mentioned

The brand, product, or site was mentioned in the response, but not necessarily used as a source.

### Claim

An objective statement that the page wants to support.

Examples:

* "The product costs R$ 99 per month."
* "The company serves Itararé-SP."
* "The system uses passwordless passkeys."
* "The pizzeria delivers to neighborhood X."
* "The API has a REST endpoint for orders."

### Claim page

A strong, canonical, and textual page created to support a claim or a small group of claims.

## Mandatory Critical Stance

Before suggesting optimizations, identify:

### User Assumptions

* The user might assume that just creating `llms.txt` is enough.
* Might assume that ChatGPT works like classic Google.
* Might assume that appearing in AI depends solely on on-page SEO.
* Might assume that the page itself will be cited in opinion-based comparisons.
* Might be ignoring the importance of external sources.

### Common Excuses

* "My site is beautiful, so the AI will understand it."
* "The price appears on the rendered card, so it's fine."
* "It's in a PDF, so it's documented."
* "It's in the video, so the AI will know."
* "The content loads later via API, but the user sees it."
* "I'll do the schema later."

### Stagnation Zones

* SPA site without SSR or useful initial HTML;
* Important data in images;
* Price hidden behind a JavaScript toggle;
* Generic institutional content;
* Pages without an update date;
* Lack of canonical pages per product, service, or location;
* Lack of real external mentions;
* Blog without objective claims;
* Documentation made only for humans, not for agents.

## Workflow

### Step 1 — Crawlability Audit

Verify:

* `robots.txt`;
* `sitemap.xml`;
* HTTP status of main pages;
* Canonical tags;
* Redirects;
* Blocked pages;
* Excessive use of JavaScript;
* Rendering without JS;
* Content in images;
* Content in PDFs;
* Orphan pages;
* Structured data;
* Load time;
* Initial HTML;
* Headings;
* Internal links.

Minimum criteria:

* Critical pages must return a `200` status;
* Main content must appear in the initial HTML or SSR;
* Each important page must have its own URL;
* Internal links must be crawlable via `<a href="">`;
* Do not rely solely on JS buttons for navigation;
* Do not hide price, address, phone number, specs, or policies in images.

### Step 2 — Configure Crawler Access

Create or review `robots.txt`.

Recommended template:

```txt
User-agent: OAI-SearchBot
Allow: /

User-agent: ChatGPT-User
Allow: /

User-agent: GPTBot
Allow: /

User-agent: *
Allow: /

Sitemap: https://example.com/sitemap.xml

```
