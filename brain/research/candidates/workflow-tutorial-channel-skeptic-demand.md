---
title: "Skeptic (demand): n8n/Claude workflow tutorial channel for one profession"
tags: [research, skeptic, demand, workflow-tutorial-channel]
updated: 2026-09-10
---

## TL;DR

- Overall verdict: **weakened**, not refuted. The n8n ecosystem is still growing (verified from GitHub: repos mentioning n8n created per half-year went 11,314 -> 33,104 -> 42,046, and 20,883 in the 10 weeks to Sep 10 2026, i.e. the pace is still rising), but nothing in the dossier proves that a *new* channel captures any of it or that a profession audience pays $49-99 for templates.
- The single biggest hole: the thing a tutorial teaches (how to wire nodes) is being absorbed into n8n itself and into Claude. n8n ships a native `@n8n/ai-workflow-builder` package (v1.39.0 in the monorepo; front-end/back-end PRs opened 2025-04-23 converting natural language to workflows), and `czlonkowski/n8n-mcp` (22,862 stars, "build n8n workflows for you", claims "tens of thousands of developers") plus `n8n-skills` (6,211 stars) let Claude Code generate, validate and deploy workflows. A $49 pack competes with a prompt.
- Free supply is larger than the dossier states and still compounding: 825 GitHub repos match "n8n workflows templates"; collections advertise 10,258+, 8,697+, 7,700+, 5,000+, 4,343, 2,053 and 2,352 workflows; 62,931 n8n template/workflow repos were created in Jan-Sep 2026 vs 44,418 in all of 2025. Free QuickBooks/bookkeeping/real-estate n8n workflows already exist on GitHub (29, 22 and 299 matching repos respectively). n8n's own README says "9,000+" templates, not the 11,700+ the dossier quotes.
- "Profession slot is empty" is absence of evidence: this session (like the dossier's) could not open YouTube, Reddit or vidIQ. What can be observed is that profession-specific n8n repos have near-zero traction (best real-estate repo 10 stars, best QuickBooks repo 2 stars, most created in 2026), which reads as low demand at least as plausibly as under-supply.
- Affiliate math is structurally weak: n8n is fair-code and self-hostable for free, the official `self-hosted-ai-starter-kit` has 15,240 stars, and the audience technical enough to watch node-level tutorials is the audience most likely to self-host. The dossier's "1 paid n8n referral per 2,500-4,000 views" and "pack conversion 0.3-0.8% of views" have no source; treat both as no data found.
- RPM ($8-30 tech) is irrelevant to the six-month case (YPP not reached until month 8-14 in the dossier's own model) and is aggregator-grade; tutorial-specific RPM: no data found. The Feb 2027 8,000-hour YPP change remains unverified from a primary source.
- Corrected planning numbers [E]: month-6 conservative $0-30, base $60-200, upside unchanged but conditional on a breakout; first dollar 60-120 days, not ~60; pack revenue should be modeled off the Gumroad median ($72/mo, third-party scrape) until a real conversion number exists.
- Evidence quality: WebSearch budget was already exhausted (200/200) when this lens ran, so zero new searches happened; only GitHub (github.com, raw.githubusercontent.com, api.github.com) was reachable through the egress proxy. Everything else is re-examination of the dossier's own sourcing. Claims marked "weakened" by default where no evidence either way was reachable.

Related: [[research/candidates/workflow-tutorial-channel]] · [[research/shortlist]] · [[research/saturated-overhyped]] · [[research/lenses/youtube-longform]] · [[research/lenses/digital-products]] · [[research/lenses/emerging-2026]]

## Method and evidence quality

- Run 2026-09-10 as an adversarial demand lens on [[research/candidates/workflow-tutorial-channel]].
- WebSearch: 0 of the planned 14 queries ran; the session-wide budget (200/200) was already spent by earlier lenses. Planned but unrun: saturation complaints on r/n8n, Gumroad n8n pack post-mortems, Google Trends for "n8n", n8n affiliate terms, YPP Feb 2027 primary source, n8n AI Workflow Builder launch coverage, Gumroad 2026 stats, small-channel tech RPM, Nate Herk growth trend, time-to-1,000-subs, n8n pricing changes.
- WebFetch: blocked by the egress proxy for support.google.com, n8n.io, docs.n8n.io, blog.n8n.io, community.n8n.io, gumroad.com, descript.com, socialblade.com, hn.algolia.com, news.ycombinator.com, techcrunch.com, tubefilter.com, wikipedia.org, web.archive.org, reddit.com, duckduckgo.com, bing.com. Reachable: github.com, raw.githubusercontent.com, api.github.com (until a 403 rate limit on the last call).
- Labels: **[V]** verified by fetching this session (GitHub only); **[D]** dossier's own sourcing, re-read critically (snippet-grade); **[E]** my estimate, assumptions stated; "no data found" where nothing reachable supports or refutes.
- A GitHub search "total_count" is a proxy for developer-side interest and free-template supply, not for viewer demand or willingness to pay. I use it that way.

## Claim-by-claim

### 1. "Demand is real and still rising" (n8n $40M ARR, 6x users, 203.9k stars)

Verdict: **holds** (for ecosystem growth), with a scope caveat.

- [V] GitHub repos matching "n8n" by creation date: 2025 H1 11,314; 2025 H2 33,104; 2026 H1 42,046; 2026-07-01 to 2026-09-10 20,883 (~294/day vs ~232/day in H1 2026). Direction is up, not plateauing. Source: api.github.com search queries listed under Sources.
- [V] n8n-io/n8n: 203,945 stars, 60.6k forks; latest stable n8n@2.38.6 released 2026-09-10; pre-release 2.39.x same week (release cadence is healthy).
- [D] $40M ARR, 6x users, $2.5B valuation: Sacra and n8n blog are blocked; unverifiable this session. Vendor and analyst figures, plausible but not checked.
- Caveat: growth of the tool does not imply growth of *unserved* tutorial demand. The same growth attracts creators (see claim 4), and the marginal viewer in 2026 arrives with an AI builder inside the product (claim 6).

### 2. "n8n's community of 200k+ mostly learned via free YouTube tutorials" as evidence YouTube is the acquisition channel

Verdict: **weakened**.

- [D] Source is an n8n integrations landing page (blocked; snippet-grade marketing copy). Even if literally true, it establishes that the audience is trained to expect n8n education for free, which is evidence against the paid layer, not for it.
- [V] n8n's README lists "9,000+ workflow templates" (raw README fetched 2026-09-10). The dossier's "11,700+" comes from an aggregator (connectsafely.ai). Corrected number: "9,000+ per n8n's own README; 11,700+ is an unverified aggregator figure".
- Vendor counts "230,000+ active users" and "1.7M monthly active builders" [D]: no data found to verify; keep as marketing-grade.

### 3. "Tech RPM $8-30 (second-highest tier)"

Verdict: **weakened**.

- [D] All RPM figures are aggregator blogs (FluxNote, vidIQ, OutlierKit, Virlo), none platform-published; the [[research/lenses/youtube-longform]] lens already flags this.
- Irrelevant to the six-month case by the dossier's own model (AdSense $0 in conservative and base at month 6; YPP month 8-14).
- Tutorial-specific and geography-adjusted RPM for n8n content: no data found. n8n's user base skews heavily outside the US (the reachable GitHub template repos include French, Indonesian and Urdu/Hindi-language projects, e.g. `Stirito/N8N_Workflow_Template`, `wahyupepep/nominala-telegram-bot`, `Wajid16/hisaab-whatsapp-agent`) [V], and the lens note records 1M India views at roughly a tenth of US value [D]. Corrected planning assumption [E]: blended RPM for an n8n tutorial channel more likely $3-10 than $8-30 until measured.

### 4. "Generic layer is saturated; the profession-specific slot is thin / no dedicated channel found"

Verdict: **weakened** (the saturation half holds; the "gap" half is unsupported).

- [V] Saturation, creator side: 785 GitHub repos match n8n + youtube/faceless/"youtube automation". At least seven are "workflows for my YouTube channel/course" repos with real traction: `lucaswalter/n8n-ai-automations` 1,622 stars (The Recap AI), `soluckysummer/n8n_workflows` 1,487, `MohElshamy1994/n8n-course-Projetcs` 822, `panaversity/learn-low-code-agentic-ai` 457, `shabbirun/redesigned-octo-barnacle` 413, `joshpocock/Stride-AI-Agents` 364, `gabriel-g2n/workflows` 135. All created 2024-2025. That is the visible tail of a large creator population, beyond Nate Herk.
- [V] Profession side: GitHub "n8n real estate" 299 repos, top result 10 stars (created 2026-02-11), then 6, 5, 3, 2, 2, 2; "n8n quickbooks" 29 repos, top 2 stars; "n8n bookkeeping" 22 repos, top non-node repo 2 stars; most created in 2026. Two readings: (a) under-served gap (dossier), (b) practitioners are not searching for or starring this content. Nothing reachable distinguishes them. The dossier's "no dedicated profession-specific channel was found" came from a session with no YouTube access; this session had none either. Counting channels: still no data found.
- [V] Free profession-specific workflows already exist: `6SHIHAB9/Autobooks-n8n` (invoice PDF -> QuickBooks), `invoice-intelligence-pipeline` (PDF -> extraction -> Slack approval -> QuickBooks), `clickup-quickbooks-invoice-automation` (two separate repos), `Bill-Approval-n8n`, `tabii-dev/accounting-automation-portfolio` (by a chartered accountant, 2026-05-20), `Namanjain723/pixlforge-autobooks-ai` (US accounting firms, n8n + Claude), `real-estate-leads-n8n`, `real-estate-disposition-workflows` (10 workflows, 127 nodes, 2026-07-11). A bookkeeper pack must beat these on install docs and support, not on the JSON.

### 5. "Template pack at $49-99, pack conversion 0.3-0.8% of monthly views, 6-8 sales at month 6"

Verdict: **weakened**; conversion figure effectively **refuted as sourced** (it has no source).

- [V] Free supply and its growth: 825 repos match "n8n workflows templates"; advertised sizes include `zengfr/n8n-workflow-all-templates` 10,258+ (synced monthly), `ScraperNode/awesome-n8n-templates` 8,697+, `EtienneLescot/n8n-as-code` 7,700+ templates with full node schemas for AI agents, `ritik-prog/n8n-automation-templates-5000` 5,000+, `Zie619/n8n-workflows` 4,343 (56,570 stars, MIT, "100% import success rate"), `Danitilahun/n8n-workflow-templates` 2,053, `czlonkowski/n8n-mcp` 2,352 templates with "99.96% AI metadata coverage", `wassupjay/n8n-free-templates` 200+ (6,170 stars), `enescingoz/awesome-n8n-templates` 280+ (25,268 stars, 6,450 forks). Template/workflow repos created: 44,418 in 2025 vs 62,931 in 2026 through Sep 10.
- [D] Gumroad: median creator $72/mo; 99.5% of tracked revenue to the top 1%; 6-12 months to first $100 without an audience (Insight Raider scrape, unaudited; blocked this session). The dossier cites this and then models 6-8 sales/month by month 6 anyway.
- The "0.3-0.8% of monthly views" conversion has no citation in the dossier and no data found here. Corrected: model pack revenue at the Gumroad median ($72/mo gross, ~$60 net) for month 6 until the channel produces its own number; the dossier's base-case $250-340/month from packs is unsupported.
- Copyright: the dossier itself notes prompt-generated JSON is not copyrightable (US Copyright Office, Jan 2025) [D]; combined with the free repos above, the pack's only moat is install support, which is a service, not a product.

### 6. "AI is ~45% of the work; the human build/test/record is the monetization licence" (implicitly: viewers still need tutorials to build workflows)

Verdict: **refuted** as an assumption about durable tutorial demand; the human demo still matters, but for a different reason than the dossier gives.

- [V] n8n has a native AI Workflow Builder: package `@n8n/ai-workflow-builder` v1.39.0 exists in the monorepo (`packages/@n8n/ai-workflow-builder.ee`); GitHub PRs "feat: AI workflow builder front-end" and "feat: AI Workflow Builder backend" (LangGraph, "converting natural language into n8n workflows") opened 2025-04-23; "first-shot evaluation for the T2WF [text-to-workflow]" 2025-07-04; 737 issues/PRs in n8n-io/n8n mention it; 2.39.0 release notes reference the AI Assistant editing workflows. Plan availability (cloud vs self-host): no data found (docs blocked).
- [V] Third-party: `czlonkowski/n8n-mcp` 22,862 stars, created 2025-06-07, "A MCP for Claude Desktop / Claude Code / Windsurf / Cursor to build n8n workflows for you", covers 2,755 nodes, validates and deploys to a live instance, README claims "tens of thousands of developers"; `czlonkowski/n8n-skills` 6,211 stars (2025-10-20), "n8n skillset for Claude Code to build flawless n8n workflows", including deploying self-hosted n8n to a fresh VM; `n8n-as-code` 1,568 stars (2026-01-03); 36 repos match "n8n workflow generator" (top: browser-based generator, 153 stars; `nodemationautomation` "generates n8n workflow JSON from natural language descriptions using Claude AI", 2026-01-03).
- Implication: "how to build the QuickBooks reconciliation flow in n8n" is a prompt away for the viewer, and n8n's own UI is moving to do it in-canvas. What is not commoditized is (a) knowing which profession process is worth automating and (b) the credibility of a practitioner showing it working against real QuickBooks/Follow Up Boss accounts. The dossier's differentiation section gets this partly right; its demand section still leans on n8n mechanics ("learn n8n" viewers) for discovery, and that funnel is the one being eaten.

### 7. "Affiliates first: n8n Cloud 30% recurring for 12 months, first dollar 6-10 weeks, 1 paid referral per 2,500-4,000 views"

Verdict: **weakened**.

- [D] n8n affiliate terms: n8n.io blocked again; still snippet-grade; cookie window and payout: no data found.
- [V] Structural conflict: n8n is fair-code and free to self-host; n8n's official `self-hosted-ai-starter-kit` has 15,240 stars and `n8n-skills` includes a "deploy self-hosted n8n to a VM" skill. Tutorial viewers who can follow a node-level demo are the population most likely to self-host, which pays $0 in affiliate commission.
- The referral-per-views ratio has no source; no data found. Descript's cut from 15% recurring to $25 flat [D] is the dossier's own evidence that AI-tool affiliate terms drift down. ElevenLabs/HeyGen commissions are irrelevant to a bookkeeper or real-estate audience that does not make videos; the dossier's base case counts them anyway ("Descript/ElevenLabs ≈ $50").
- Corrected [E]: model affiliate income at month 6 as $0-40 unless the profession's own SaaS (QuickBooks, Follow Up Boss, HoneyBook, etc.) has a program the operator has actually verified; none were researched in either session (no data found).

### 8. "YPP thresholds reportedly double to 8,000 hours on Feb 1 2027"

Verdict: **weakened** (unverified either way).

- support.google.com and web.archive.org both blocked; the [[research/lenses/youtube-longform]] lens already marks this as a single-secondary-source claim. Keep as a risk flag; do not build the timeline on it in either direction.

### 9. "Policy risk is low; screen-recorded human demos are the counter-example to inauthentic content"

Verdict: **holds** on the reachable evidence, with one note.

- No reachable source contradicts it. Note that 785 n8n-plus-YouTube repos include many faceless/Shorts-automation kits (`aruntemme/n8n-faceless-youtube`, `Hritikraj8804/Autotube`, `mismai-li/n8n-youtube-to-shorts-workflow`) [V]; the n8n-tutorial category sits next to the exact content YouTube is sweeping, so recommendation-system adjacency is a soft risk even if the channel itself is compliant. No data found on whether that adjacency depresses reach.

### 10. Economics: "~60 days to first dollar; month-6 base ~$450; upside ~$2,500"

Verdict: **weakened**.

- Every input to the base case (referral rate, pack conversion, 6-8K views/month at month 6, 500-view average) is [E] in the dossier with no benchmark; time-to-1,000-subscribers and view-growth curves for tutorial channels: no data found in either session.
- Corrected [E], holding the dossier's 10-12 hrs/week: first dollar 60-120 days (a self-hosting audience delays the first paid referral; Gumroad's 6-12-month no-audience benchmark applies to the pack); month-6 conservative $0-30; base $60-200 (Gumroad-median pack revenue plus a handful of referrals); upside unchanged in size (~$2,500) but should be labeled a breakout tail, not a scenario. Implied base hourly rate ~$1-4/hr at month 6.
- The dossier's own "why still do it" (distribution asset for paid installs at $300-800, Upwork n8n $40-100/hr) is where the money is; that is a services business with a content front end, and it should be evaluated under [[research/lenses/freelance-marketplaces]] and [[research/shortlist]] picks 5-7, not as a channel P&L.

## Corrected numbers (summary)

| Dossier figure | Corrected | Basis |
|---|---|---|
| 11,700+ official templates | 9,000+ per n8n README (2026-09-10); 11,700+ unverified aggregator | [V] |
| Free GitHub supply: 4,343 + 280+ | 825 matching repos; collections of 10,258+, 8,697+, 7,700+, 5,000+, 4,343, 2,353, 2,053; 62,931 template/workflow repos created Jan-Sep 2026 | [V] |
| "No profession-specific competition" | 299 real-estate, 29 QuickBooks, 22 bookkeeping n8n repos on GitHub, all low-traction; channel counts still no data found | [V] |
| Pack conversion 0.3-0.8% of views | no data found; plan on Gumroad median $72/mo until measured | [D] |
| 1 paid n8n referral per 2,500-4,000 views | no data found; discount for free self-hosting | [V] structural, [E] |
| Tech RPM $8-30 | irrelevant before YPP; blended n8n-audience RPM likely $3-10 [E]; tutorial-specific: no data found | [D] |
| First dollar ~60 days | 60-120 days | [E] |
| Month-6 base ~$450 | $60-200 | [E] |
| Month-6 conservative ~$60 | $0-30 | [E] |
| "Human build is the moat" | native AI Workflow Builder in n8n + n8n-mcp (22.9k stars) + n8n-skills (6.2k); moat is profession process knowledge and live demo on real accounts | [V] |

## What would change the verdict

- Direct YouTube counts: number of channels with 5+ videos in "n8n for bookkeepers/real estate/photographers" and their median views (needs YouTube or vidIQ access).
- Google Trends for "n8n" and "n8n tutorial" 2024-2026 (flat or falling would push to refuted; still rising keeps weakened).
- A single verified creator earnings breakdown for a sub-50K n8n tutorial channel (affiliate + product split).
- n8n's published affiliate terms and whether the AI Workflow Builder is on the free/self-hosted tier.
- Any Gumroad/n8n Markets listing with visible sales counts for a profession-specific n8n pack.

## Sources

Verified this session (GitHub only, fetched 2026-09-10)
- [n8n-io/n8n repository (203,945 stars, 60.6k forks)](https://github.com/n8n-io/n8n)
- [n8n-io/n8n README (raw; "9,000+ workflow templates")](https://raw.githubusercontent.com/n8n-io/n8n/master/README.md)
- [n8n-io/n8n releases (n8n@2.38.6 stable, 2.39.x pre-release, Sep 2026)](https://github.com/n8n-io/n8n/releases)
- [n8n-io/n8n packages/@n8n/ai-workflow-builder.ee (native AI Workflow Builder package)](https://github.com/n8n-io/n8n/tree/master/packages/%40n8n/ai-workflow-builder.ee)
- [@n8n/ai-workflow-builder package.json (v1.39.0)](https://raw.githubusercontent.com/n8n-io/n8n/master/packages/@n8n/ai-workflow-builder.ee/package.json)
- [GitHub issues/PRs in n8n-io/n8n mentioning "AI workflow builder" (737; front-end/backend PRs 2025-04-23)](https://api.github.com/search/issues?q=repo:n8n-io/n8n+%22AI+workflow+builder%22&sort=created&order=asc&per_page=10)
- [czlonkowski/n8n-mcp README (22,862 stars; 2,755 nodes; 2,352 templates; "tens of thousands of developers")](https://raw.githubusercontent.com/czlonkowski/n8n-mcp/main/README.md)
- [czlonkowski/n8n-skills README (6,211 stars; build/validate/deploy n8n via Claude Code)](https://raw.githubusercontent.com/czlonkowski/n8n-skills/main/README.md)
- [Zie619/n8n-workflows README (4,343 workflows, 15 categories, MIT)](https://raw.githubusercontent.com/Zie619/n8n-workflows/main/README.md)
- [GitHub search: n8n workflows templates (825 repos, by stars)](https://api.github.com/search/repositories?q=n8n+workflows+templates&sort=stars&order=desc&per_page=30)
- [GitHub search: n8n in repo name (83,352 repos, by stars)](https://api.github.com/search/repositories?q=n8n+in:name&sort=stars&order=desc&per_page=50)
- [GitHub search: n8n MCP / Claude Code tooling (111,800 matches, top results)](https://api.github.com/search/repositories?q=n8n+mcp+OR+%22n8n+skill%22+OR+%22claude+code%22+n8n&sort=stars&order=desc&per_page=30)
- [GitHub search: n8n repos created 2025-01-01..2025-06-30 (11,314)](https://api.github.com/search/repositories?q=n8n+created:2025-01-01..2025-06-30&per_page=1)
- [GitHub search: n8n repos created 2025-07-01..2025-12-31 (33,104)](https://api.github.com/search/repositories?q=n8n+created:2025-07-01..2025-12-31&per_page=1)
- [GitHub search: n8n repos created 2026-01-01..2026-06-30 (42,046)](https://api.github.com/search/repositories?q=n8n+created:2026-01-01..2026-06-30&per_page=1)
- [GitHub search: n8n repos created 2026-07-01..2026-09-10 (20,883)](https://api.github.com/search/repositories?q=n8n+created:2026-07-01..2026-09-10&per_page=1)
- [GitHub search: n8n templates/workflows repos created in 2025 (44,418)](https://api.github.com/search/repositories?q=n8n+templates+OR+workflows+created:2025-01-01..2025-12-31&per_page=1)
- [GitHub search: n8n templates/workflows repos created 2026-01-01..2026-09-10 (62,931)](https://api.github.com/search/repositories?q=n8n+templates+OR+workflows+created:2026-01-01..2026-09-10&per_page=1)
- [GitHub search: n8n quickbooks (29 repos)](https://api.github.com/search/repositories?q=n8n+quickbooks&sort=stars&order=desc&per_page=20)
- [GitHub search: n8n bookkeeping (22 repos)](https://api.github.com/search/repositories?q=n8n+bookkeeping&sort=stars&order=desc&per_page=20)
- [GitHub search: n8n "real estate" (299 repos)](https://api.github.com/search/repositories?q=n8n+%22real+estate%22&sort=stars&order=desc&per_page=20)
- [GitHub search: n8n youtube / faceless / youtube automation (785 repos)](https://api.github.com/search/repositories?q=n8n+youtube+faceless+OR+%22youtube+automation%22&sort=stars&order=desc&per_page=15)
- [GitHub search: n8n workflow generator (36 repos)](https://api.github.com/search/repositories?q=%22n8n+workflow+generator%22+OR+%22generate+n8n+workflows%22&sort=stars&order=desc&per_page=15)
- [n8n-io/self-hosted-ai-starter-kit (15,240 stars, via search results above)](https://github.com/n8n-io/self-hosted-ai-starter-kit)

Dossier sources re-examined, not re-fetched (blocked this session)
- [n8n Cloud affiliate program (blocked)](https://n8n.io/affiliates/)
- [YouTube Help: Partner Program eligibility (blocked)](https://support.google.com/youtube/answer/72851?hl=en)
- [Insight Raider: State of Gumroad 2026 (blocked)](https://insightraider.com/en/state-of-gumroad-2026)
- [Descript affiliate terms (blocked)](https://www.descript.com/affiliate-terms)
- [Sacra: n8n revenue and valuation (blocked)](https://sacra.com/c/n8n/)
- [ConnectSafely: n8n templates 2026, 11,700+ (aggregator; contradicts README's 9,000+)](https://connectsafely.ai/articles/n8n-templates-workflow-automation-examples)
- [FluxNote: YouTube RPM by niche USA 2026 (aggregator)](https://fluxnote.io/guides/youtube-rpm-by-niche-usa-2026)
- [AIR Media-Tech: YPP requirements 2026 / Feb 2027 change (secondary)](https://air.io/en/monetization/youtube-partner-program-requirements-2026-the-complete-guide)
