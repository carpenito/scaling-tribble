---
title: Request Review
deprecated: false
hidden: false
icon: fad fa-rocket-launch
metadata:
  robots: index
---
<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ReadMe Platform — Criteria Breakdown</title>
<style>
  :root {
    --bg: #f9f8f6;
    --bg-card: #ffffff;
    --text-primary: #1a1a18;
    --text-secondary: #5c5c57;
    --text-tertiary: #9c9a92;
    --border: rgba(0,0,0,0.1);
    --border-strong: rgba(0,0,0,0.18);
    --green-bg: #eaf3de;
    --green-text: #3b6d11;
    --amber-bg: #faeeda;
    --amber-text: #854f0b;
    --red-bg: #fcebeb;
    --red-text: #a32d2d;
    --radius-md: 8px;
    --radius-lg: 12px;
  }
  @media (prefers-color-scheme: dark) {
    :root {
      --bg: #1c1c1a;
      --bg-card: #252523;
      --text-primary: #e8e6de;
      --text-secondary: #b0ae a6;
      --text-tertiary: #6e6c65;
      --border: rgba(255,255,255,0.08);
      --border-strong: rgba(255,255,255,0.14);
      --green-bg: #173404;
      --green-text: #97c459;
      --amber-bg: #412402;
      --amber-text: #ef9f27;
      --red-bg: #501313;
      --red-text: #f09595;
    }
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    font-family: 'DM Sans', 'Helvetica Neue', Arial, sans-serif;
    background: var(--bg);
    color: var(--text-primary);
    padding: 2.5rem 2rem;
    max-width: 960px;
    margin: 0 auto;
    line-height: 1.6;
  }
  header { margin-bottom: 2rem; }
  h1 { font-size: 22px; font-weight: 600; margin-bottom: 4px; }
  .subtitle { font-size: 14px; color: var(--text-secondary); }
  .legend {
    display: flex; gap: 20px; margin-bottom: 1.5rem; flex-wrap: wrap;
    font-size: 12px; color: var(--text-secondary);
  }
  .legend span { display: flex; align-items: center; gap: 6px; }
  .legend-dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }
  .section-label {
    font-size: 11px; font-weight: 600; color: var(--text-tertiary);
    text-transform: uppercase; letter-spacing: 0.07em;
    margin: 2rem 0 0.75rem;
  }
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 12px;
  }
  .card {
    background: var(--bg-card);
    border: 0.5px solid var(--border);
    border-radius: var(--radius-lg);
    padding: 1rem 1.25rem;
  }
  .card-header {
    display: flex; align-items: flex-start;
    justify-content: space-between; gap: 10px; margin-bottom: 8px;
  }
  .card-title { font-size: 13px; font-weight: 600; color: var(--text-primary); }
  .badge {
    font-size: 11px; font-weight: 600; padding: 3px 9px;
    border-radius: 20px; white-space: nowrap; flex-shrink: 0;
  }
  .badge-yes  { background: var(--green-bg); color: var(--green-text); }
  .badge-partial { background: var(--amber-bg); color: var(--amber-text); }
  .badge-no   { background: var(--red-bg); color: var(--red-text); }
  .card-body  { font-size: 12px; color: var(--text-secondary); line-height: 1.65; }
  .card-detail {
    font-size: 11px; color: var(--text-tertiary);
    margin-top: 8px; padding-top: 8px;
    border-top: 0.5px solid var(--border);
    font-style: italic;
  }
  footer {
    margin-top: 2.5rem;
    font-size: 11px;
    color: var(--text-tertiary);
    border-top: 0.5px solid var(--border);
    padding-top: 1rem;
  }
</style>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600&display=swap" rel="stylesheet">
</head>
<body>

<header>
  <h1>ReadMe — Platform Criteria Breakdown</h1>
  <p class="subtitle">Assessment of ReadMe against documentation platform requirements</p>
</header>

<div class="legend">
  <span><span class="legend-dot" style="background:#3b6d11"></span>Native / strong fit</span>
  <span><span class="legend-dot" style="background:#854f0b"></span>Partial / with config</span>
  <span><span class="legend-dot" style="background:#a32d2d"></span>Gap / needs workaround</span>
</div>

<!-- Core platform -->
<div class="section-label">Core documentation platform</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">API reference as code</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">OpenAPI spec as single source of truth — ReadMe renders API reference directly from your spec, auto-updating on schema change. Upload manually, via API, or CI/CD pipeline.</div>
    <div class="card-detail">Supports OAS 3.x. Use the rdme CLI for spec sync in GitHub Actions.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Multi-language code samples</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">Auto-generated code samples from OpenAPI spec in 10+ languages. Custom samples can be added per-endpoint. Language switcher built into the reference UI.</div>
    <div class="card-detail">No hand-maintenance needed if sourced from spec extensions (x-readme).</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Try-it / live sandbox</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">Built-in "Try It!" API explorer on every endpoint. Supports pre-authentication with user-specific API keys for integrators via the ReadMe JWT/OAuth integration.</div>
    <div class="card-detail">Enterprise: personalised variables populated from user login context.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Changelog as content</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">First-class Changelog section with versioning and RSS subscription. Can link changelog entries from API reference pages. Write in markdown or via API.</div>
    <div class="card-detail">Auto-linking from reference requires manual cross-linking — not fully automatic.</div>
  </div>
</div>

<!-- Search -->
<div class="section-label">Search &amp; discoverability</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">Enhanced search</span>
      <span class="badge badge-partial">Partial</span>
    </div>
    <div class="card-body">ReadMe has built-in full-text search. Semantic search and zero-result gap tracking are not native — gap tracking is available via the Search Queries analytics report, but not auto-flagged.</div>
    <div class="card-detail">Search analytics show what people searched for with no results. Semantic ranking is not currently configurable.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Discoverable IA</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">Hierarchical navigation with categories, subcategories, and custom ordering. Supports multiple doc versions and audience-based navigation. IA is managed in the dashboard or via the Guides API.</div>
    <div class="card-detail">Personalised nav by integration type requires custom JS or dynamic content blocks.</div>
  </div>
</div>

<!-- AI -->
<div class="section-label">AI &amp; modern tooling</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">AI-native / LLM-readable</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">Full AI-native stack: LLMs.txt auto-generated with a single toggle (all plans, zero maintenance). Two native MCP servers — one for doc authors to manage docs via AI, one for API users to give their AI tools live access to your spec and docs. ReadMe pages render clean HTML and expose a public sitemap — crawlable by LLMs. Native llms.txt is supported and automatically generates a configuration file at the root of your documentation site based on your existing documentation structure.</div>
    <div class="card-detail">LLMs.txt available on all plans. MCP servers are a built-in, not a custom integration.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Personalisation</span>
      <span class="badge badge-partial">Partial</span>
    </div>
    <div class="card-body">ReadMe supports user variables (e.g. pre-filled API keys, company name) via JWT SSO. Scheme/country/integration-method-based content branching is not native — requires custom logic or separate doc versions.</div>
    <div class="card-detail">Enterprise variable injection is strong for auth context; conditional content blocks are limited.</div>
  </div>
</div>

<!-- Performance -->
<div class="section-label">Performance &amp; governance</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">SSR / fast page load</span>
      <span class="badge badge-partial">Partial</span>
    </div>
    <div class="card-body">ReadMe's hosted platform uses SSR. TTFB and Core Web Vitals are generally good on the default theme, but you don't control the infra directly — sub-100ms TTFB SLAs are not guaranteed or contractually available.</div>
    <div class="card-detail">Custom domain + CDN is supported. Performance tuning is limited vs self-hosted.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Content governance</span>
      <span class="badge badge-partial">Partial</span>
    </div>
    <div class="card-body">Bi-directional GitHub Sync lets teams use PRs for doc reviews. Broken link checking and linting are not native — you'd need a CI step against the live site or exported content.</div>
    <div class="card-detail">GitHub Sync is available on Business/Enterprise plans. Quality gate tooling is a gap.</div>
  </div>
</div>

<!-- Analytics -->
<div class="section-label">Analytics &amp; feedback</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">Developer feedback loops</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">Per-page ratings (thumbs up/down) are built in. Developer CSAT is surfaced in the Metrics dashboard. Comments can be enabled per page for direct feedback.</div>
    <div class="card-detail">Ratings roll up in the analytics dashboard — filterable by page, version, and time range.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Content analytics</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">ReadMe Metrics tracks page views, time on page, search queries, and exit rates. API call analytics are also available when using ReadMe's API logging.</div>
    <div class="card-detail">Full search gap analysis is available. Feeding to external tools requires the Metrics API or webhook.</div>
  </div>
</div>

<!-- Workflow -->
<div class="section-label">Workflow &amp; editing</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">Easy to update</span>
      <span class="badge badge-yes">Native</span>
    </div>
    <div class="card-body">WYSIWYG editor for non-engineers, markdown/MDX for engineers, plus GitHub Sync for code-first teams. Low barrier for both audiences — no build step required for content-only edits.</div>
    <div class="card-detail">Engineers can also use the Guides API or CLI for bulk updates and automation.</div>
  </div>
</div>

<footer>Generated from ReadMe platform evaluation · readme_criteria_breakdown</footer>

</body>
</html>
`}</HTMLBlock>

Here's how to think through the full picture:

Where ReadMe is a strong fit:

* the core of what you're asking for is exactly what ReadMe was built to do. OpenAPI-synced reference, multi-language code samples, Try It sandbox, changelog, page ratings, and content analytics are all first-class features. The WYSIWYG + GitHub Sync combination directly addresses the "easy to update for engineers and non-engineers" requirement.
* AI-native / MCP indexing — ReadMe ships both sides of the MCP story:
  The author-facing MCP server lets your team query, read, and update documentation through AI tools — useful for content workflows, bulk edits, and AI-assisted writing directly against your live docs.
  The user-facing MCP server is the more strategically significant one for this evaluation — it gives your API users' AI tools (Cursor, Claude, Windsurf, etc.) live access to your spec and docs as context while they're coding. That's exactly what the "MCP-indexed" criterion in the original requirements was asking for.
  That actually makes ReadMe's AI-native story stronger than I initially assessed — and stronger than what many competitors offer. The only remaining nuance on that card would be whether llms.txt is generated natively, but the MCP piece is clearly covered. Worth updating the artifact if you're sharing it.

Where it's partial, and what to do about it:

* Semantic search — current search is keyword-based. Zero-result tracking is available in analytics (you can see what returned no results) but isn't auto-surfaced as a queue for content work. If semantic search is hard criteria, this is the biggest gap vs alternatives like Mintlify or a custom Algolia integration.
* Sub-100ms TTFB guarantee — ReadMe's SSR performance is generally solid, but you're on their infrastructure and can't contractually enforce a TTFB SLA. If that's a hard requirement, self-hosted solutions (Mintlify, Docusaurus + Vercel) give you more control.
* Content governance / quality gates — GitHub Sync handles the PR review part well, but broken link checking and linting need to be bolted on in CI (e.g. broken-link-checker against your staging URL on every PR). ReadMe doesn't enforce this natively.
* Personalisation by scheme/country/integration method — user variable injection (API keys, company name) is excellent. True conditional content branching by integration type isn't native and would require either separate versioned doc trees or custom JS blocks.
* On the build vs buy vs open source question — ReadMe sits squarely in the "buy" column with a strong managed-platform story. If strict performance SLAs, deep MCP/AI-native features, or aggressive content conditionals are hard requirements, it's worth putting Mintlify side-by-side (stronger AI-native story, more config flexibility) and Docusaurus + Vercel (full control, more engineering lift). Happy to do a direct comparison against either if useful.
