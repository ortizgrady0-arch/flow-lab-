---
title: "Skeptic (execution): n8n/Claude workflow tutorial channel + $49-99 template pack"
tags: [research, skeptic, execution, workflow-tutorial-channel]
updated: 2026-09-10
lens: execution
target: "[[research/candidates/workflow-tutorial-channel]]"
verdict: weakened
---

## TL;DR

- Overall: **weakened**, not refuted. The channel-as-distribution logic survives; the "Claude drafts the n8n JSON" differentiator and the template-pack economics do not survive contact with what n8n shipped in July 2026.
- **Biggest miss in the dossier:** n8n Assistant (n8n 2.29.9, 2026-07-09, Cloud; self-hosted from 2.35) lets any user "describe an automation in plain language and have n8n Assistant plan, build, test, and iterate on it until it actually runs." A buyer's own n8n now does the thing the $49-99 pack sells. [V: n8n-docs changelog]
- **AI-drafted workflow JSON is not sellable as-is.** The 22.9k-star n8n-mcp project says "default parameter values are the #1 source of runtime failures" and "NEVER edit your production workflows directly with AI"; the 56.6k-star free repo the dossier cites has 1,457 of 1,573 AI nodes silently corrupted to no-op (issue #200, Sep 2026) and a paying n8n subscriber reporting "no workflows working" after import (issue #125). [V]
- **Maintenance is recurring, not "1.0 h amortized".** n8n shipped 8 releases in 4 days (Sep 7-10 2026) across two live major lines (1.123.x and 2.38.x); 2026 issues include "Instance broken by 2.33.4 update", "Workflows disappeared ... after version update", "Updating ... resulted in breaking all of my workflows", and n8n Cloud Code nodes failing fleet-wide (Aug 2026). A paid pack needs a version-support policy and a re-test on every breaking bump. [V]
- **Gumroad fees hold exactly** (verified from Gumroad's open-source code, not a blog): 10% + $0.50 direct, 30% Discover, **plus** 2.9% + $0.30 card processing, $100 minimum payout, 5% at $20k/mo GMV. Net on $49 = $41.88 as the dossier says. But the $100 payout floor means the first *cash* from the pack needs three $49 sales, not one. [V]
- **Every non-GitHub number is unverified this session:** n8n Cloud Starter $24, Claude Pro $20, Descript $24/$35, n8n affiliate 30%/12 mo, Descript $25 flat, tech RPM $8-30, YPP 8,000-hour change, FTC $53,088, Copyright Office Part 2. Pricing/affiliate/help pages for n8n, Descript, Gumroad, YouTube, FTC, IRS, Copyright Office, Anthropic, Reddit, Medium, HN, Trustpilot and G2 were all blocked by the egress proxy and the WebSearch budget was already exhausted (200/200). Default: weakened.
- **Month-6 revenue:** no beginner earnings report could be fetched; the one real seller found (TuguiDragos, EUR 58.99 on Gumroad / $230 on n8n's own library, 14 GitHub stars) publishes prices but zero sales data. Corrected month-6 base [E]: $60-250, not $450; first cash in hand 3-5 months, not ~60 days.
- **Legal: mostly holds.** n8n's license FAQ explicitly allows paid consulting/"building workflows" and only bans white-labeling/hosting for money; Anthropic's consumer terms (eff. 2026-06-14, mirrored copy) assign Outputs to the user and only forbid reselling the Services. Tax (1099-K, hobby-loss) and YouTube policy could not be re-verified.

Related: [[research/candidates/workflow-tutorial-channel]] · [[research/shortlist]] · [[research/lenses/youtube-longform]] · [[research/lenses/digital-products]] · [[research/lenses/emerging-2026]]

## Method and evidence quality

- Run 2026-09-10. WebSearch budget was already exhausted (200/200) before this lens started, so **zero searches** ran; every finding comes from WebFetch of pages the proxy allows (github.com, raw.githubusercontent.com, platform.claude.com) plus GitHub code/issue search. All other domains attempted were blocked: n8n.io, docs.n8n.io, community.n8n.io, descript.com, help.descript.com, claude.com, anthropic.com, support.claude.com, gumroad.com, help.gumroad.com, support.google.com, blog.youtube, youtube.com, ftc.gov, copyright.gov, irs.gov, wikipedia.org, reddit.com, old.reddit.com, web.archive.org, hn.algolia.com, dev.to, indiehackers.com, socialblade.com, trustpilot.com, g2.com.
- Labels: **[V]** fetched this session; **[M]** verified from a third-party mirror on GitHub (text matches the primary but the primary was not opened); **[U]** dossier claim that could not be re-verified (no contrary evidence found); **[E]** my estimate.
- Attack surface: (1) does the AI stack make sellable output, (2) hidden manual work, (3) tool costs and free tiers, (4) month-3/6 revenue realism, (5) time to first dollar, (6) policy/TOS/tax/legal.

## 1. Does the AI stack produce sellable quality today?

| Claim (dossier) | Verdict | Evidence |
|---|---|---|
| "Claude drafts the n8n JSON, code nodes, prompts" (step 2, assisted, 3.0 h/wk) | **weakened** | The most-used bridge between LLMs and n8n, czlonkowski/n8n-mcp (22.9k stars), exists precisely because raw LLM output fails: "Default parameter values are the #1 source of runtime failures. ALWAYS explicitly configure ALL parameters" and "NEVER edit your production workflows directly with AI! Always: Make a copy of your workflow before using AI tools." Coverage even with the tool: 99% of node properties, only 66.5% of operations. [V] |
| Free template supply is a price-compressor (11,700+ official; 4,343 in Zie619 repo) | **holds, and cuts both ways** | Zie619/n8n-workflows issue #200 (2026-09-04): 1,457 of 1,573 AI-named nodes across 2,057 files have their type silently replaced with `n8n-nodes-base.noOp`, i.e. the AI parts of the free repo do nothing when imported. Issue #125 (2025-10-20), from a paying n8n subscriber: "there are no workflows working by downloading then import to n8n". [V] Free supply is large but largely broken, which is the only reason a tested pack can charge anything. |
| Templates are a durable product once built | **refuted as "amortized 1.0 h"** | n8n release cadence observed 2026-09-10: 2.38.6, 1.123.79, 2.39.2-pre, 2.38.5, 2.39.1-pre, 2.39.0-pre, 2.38.4, 2.37.11 all between Sep 7 and Sep 10 (8 releases / 4 days, two supported major lines). [V] 2026 upgrade-regression issues: #30459 "Updating my self-hosted n8n resulted in breaking all of my workflows" (May 2026, Execute nodes, `execve: Operation not permitted`), #35788 "Instance broken by 2.33.4 update, request rollback" (Aug 2026), #35787 "Workflows disappeared and cannot be activated after version update" (Aug 2026), #36249 "Regression: New workflows fail with 404" (Aug 2026), #28572 "2.15.1 -> 2.16.1: Failed to load module breaking-changes" (Apr 2026), #37175 n8n Cloud Code nodes failing across all workflows, task runner unavailable (Aug 2026). GitHub semantic search returns 175 issues matching "regression after upgrade, workflow broke" in n8n-io/n8n. [V] |
| **Not in dossier:** n8n now builds and self-tests workflows natively | **new, material** | n8n-docs changelog: n8n Assistant released 2026-07-09 in n8n 2.29.9 ("n8n Cloud at release. Self-hosted setup followed in n8n 2.35"), "describe an automation in plain language and have n8n Assistant plan, build, test, and iterate on it until it actually runs"; it "supersedes the AI Workflow Builder ... runs what it builds, detects failures, and retries until the automation works", manages credentials progressively, and is in preview ("it can make mistakes"). Billed via n8n Assistant credits, separate from Gateway credits. [V] Implication: the tutorial's "watch me get Claude to write the JSON" segment is a legacy workflow for any viewer on 2.29.9+, and a template pack competes with a one-sentence prompt inside the buyer's own instance. What still sells is the profession-specific integration knowledge (which SaaS, which fields, which edge cases), not the JSON. |

## 2. Hidden manual work the dossier under-counts

| Item | Dossier | Corrected [E] | Evidence |
|---|---|---|---|
| Re-testing the pack on n8n version bumps | 1.0 h/wk amortized (step 10) | 1-3 h per breaking release across every SKU; with ~2 releases/day and periodic breaking changes, budget 2-4 h/wk once 3+ SKUs exist | Release cadence and regression issues above [V]; BREAKING-CHANGES.md in n8n-io/n8n lists node-image and CLI-flag breaks through 2.0.0 [V] |
| Buyer onboarding on the profession's SaaS | 0.5 h/wk support (step 12) | Non-trivial: the one observed seller's "lite" product needs five accounts (n8n, Vapi, Twilio, Google service account, Slack bot) before a test call; the full version adds GoHighLevel. Expect credential/OAuth support to dominate tickets | TuguiDragos/n8n-ai-call-agent README [V] |
| Refund handling | not modeled | Gumroad refunds return the buyer's money but Gumroad retains the processor fee (2.9% + $0.30) from the seller on refund | antiwork/gumroad `app/models/credit.rb`, `purchase_refunds_spec.rb` [V] |
| Demo API/credit costs while recording | not modeled | n8n Cloud Starter/Pro nodes can run on Gateway credits; "when your balance reaches zero, nodes using Gateway credits stop working until you add credit"; trial credits cannot be topped up | n8n-docs gateway-credits README [V] |
| Keeping the free lite template working | not modeled | Same maintenance load as the paid SKU, with zero revenue; broken free templates generate the "nothing works" comments seen in the Zie619 repo | Zie619 issues #125, #200 [V] |
| Account setup and admin | 0.25 h/wk (step 13) | First month adds Gumroad payout/KYC, affiliate applications with review periods (unverified), YouTube channel verification, FTC boilerplate. One-off ~6-10 h [E] | no data found for review periods (pages blocked) |

Corrected weekly hours [E]: 12-15 h/wk once the pack has 3 SKUs, versus the dossier's 10.75 h. Time-weighted automation falls from ~45% to roughly 35%, because the added hours are all manual (testing, support, refunds).

## 3. Tool costs and free tiers

| Claim | Verdict | Evidence |
|---|---|---|
| n8n Cloud Starter ~$24/mo | **weakened (no data found)** | n8n.io/pricing blocked. Docs repo confirms only: 14-day trial "with a limit of 1000 executions and the same computing power as the Starter plan"; Starter = 320 MiB RAM, 10 millicore burstable, max 2,500 executions saved, 7-day log retention; Pro-1 = 10k executions, 640 MiB; docs warn "Exact features, usage limits, and prices for each plan can change." [V] Also: workflows are **permanently deleted 90 days after a trial ends** if not downloaded [V], which matters for a channel that starts on a trial. |
| Claude Pro $20/mo | **weakened (no data found)** | claude.com and support.claude.com blocked. API prices verified: Sonnet 5 $2/$10 per MTok (introductory price made permanent, the Sep 1 2026 increase cancelled), Opus 5 $5/$25, Haiku 4.5 $1/$5; note Claude 4.7+ tokenizer "produces approximately 30% more tokens for the same text". [V: platform.claude.com pricing] |
| Descript Creator $24 annual / $35 monthly | **weakened (no data found)** | descript.com, help.descript.com, G2 all blocked. |
| Gumroad 10% + $0.50 direct, 30% Discover, Stripe 2.9% + $0.30 on top, $100 minimum payout, MoR | **holds (upgraded from [S] to [V])** | antiwork/gumroad source: `GUMROAD_FLAT_FEE_PER_THOUSAND = 100`, `GUMROAD_FIXED_FEE_CENTS = 50`, `GUMROAD_DISCOVER_FEE_PER_THOUSAND = 300`, `PROCESSOR_FEE_PER_THOUSAND = 29`, `PROCESSOR_FIXED_FEE_CENTS = 30`, `Payouts::MIN_AMOUNT_CENTS = 100_00`; help-article template: "we charge a 10% + $0.50 fee + sales tax per transaction. This does not include: Credit card processing (2.9% + $0.30), PayPal fees"; llms.txt: "Gumroad is the merchant of record and handles sales tax collection and remittance worldwide." Bonus: `HIGH_VOLUME_FEE_PER_THOUSAND = 50` once monthly GMV reaches $20,000. [V] |
| Net per sale $41.88 / $68.01 / $85.43 | **holds** | 49 - 4.90 - 0.50 - 1.42 - 0.30 = 41.88 [V arithmetic on verified constants] |
| Startup ~$160-190 | **holds, weakly** | Mic price unverified; all SaaS prices unverified; nothing found that contradicts the total. |

## 4. Affiliate terms

| Program | Dossier | Verdict | Evidence |
|---|---|---|---|
| n8n Cloud 30% for 12 months | [S] | **weakened (no data found)** | n8n.io/affiliates blocked; cookie, payout minimum and schedule still unknown. |
| Descript $25 flat (was 15% recurring) | [S] | **weakened (no data found)** | descript.com/affiliate-terms blocked. Direction (cuts) is plausible; number unverified. |
| ElevenLabs 22% / 12 mo, 90-day hold | [S] | **weakened (no data found)** | elevenlabs.io not attempted after the pattern of blocks; unverified. |
| Anthropic affiliate | none | **holds** | No program referenced anywhere in Anthropic's public docs fetched; treat Claude as non-monetized. |

## 5. Month-3 / month-6 revenue and time to first dollar

| Claim | Verdict | Evidence and corrected numbers |
|---|---|---|
| Base month 6 ~$450 (6-8K views/mo, 12-15 stacked referrals, 6-8 pack sales) | **weakened** | No beginner earnings report was reachable (Reddit, Medium, HN, Indie Hackers, dev.to all blocked; search budget zero). The only real seller observed lists EUR 58.99 (Gumroad) and $230 (n8n template library) with 14 stars and no sales figures. [V] The dossier's own Gumroad base rates (median creator $72/mo; 99.5% of revenue to top 1%; 6-12 months to first $100 without an audience) are third-party [S] and argue against $450 at month 6. Corrected base [E]: **$60-250/month at month 6** (1-3 recurring referrals, 1-3 pack sales), upside unchanged but requires a breakout. |
| Upside month 6 ~$2,500 incl. 25-35 pack sales | **weakened** | 25-35 sales/month of a $79 pack in one profession, six months in, with n8n Assistant now doing prompt-to-working-workflow natively, has no observed comparable. |
| ~60 days to first dollar | **weakened** | Distinguish earned vs received. Gumroad pays nothing below $100 (verified); at $41.88 net per $49 sale that is 3 sales before the first payout. Affiliate payout schedules unverified; ElevenLabs 90-day hold per dossier. Corrected [E]: first dollar *earned* 6-10 weeks is plausible; first dollar *in the bank* ~3-5 months. |
| Implied $9-10/hr base | **weakened** | With corrected revenue ($60-250) and corrected hours (12-15/wk, ~55/month): **$1-4.50/hr at month 6** [E]. |

## 6. Policy, TOS, tax and legal

| Claim | Verdict | Evidence |
|---|---|---|
| n8n Sustainable Use License is silent on selling workflows; practice tolerated | **holds, strengthened** | n8n-docs license FAQ: allowed uses include "Providing consulting services related to n8n, for example building workflows, custom features closely connect to n8n"; not allowed: "White-labeling n8n and offering it to your customers for money", "Hosting n8n and charging people money to access it", and anything whose "value derives entirely or substantially from n8n functionality". [V] n8n's own template library lists paid templates (a $230 listing observed) and the docs say "n8n is working on a creator program, and developing a marketplace of templates." [V] Selling a workflow pack is squarely in the consulting/creator lane; the one line to respect is never hosting/white-labeling for buyers. |
| Anthropic/Claude usage terms: "not researched" | **holds (now researched)** | Consumer Terms effective 2026-06-14: "Subject to your compliance with our Terms, we assign to you all of our right, title, and interest, if any, in Outputs." Restrictions target developing competing products/models and "resell the Services", not selling artifacts made with Outputs. Also: "Outputs may not always be accurate and may contain material inaccuracies", which is the seller's liability, not Anthropic's. [M: three independent GitHub mirrors of the consumer terms; anthropic.com blocked] |
| Copyright Office Part 2: prompt-only output not copyrightable | **[U] not re-verified** | copyright.gov blocked. No contrary evidence; the "if any" hedge in Anthropic's assignment clause is consistent with it. Practical position unchanged: the pack is protected by license terms and human-authored docs/video, not by copyright in the JSON. |
| YouTube inauthentic-content policy is low risk for human-narrated screen recordings | **[U] not re-verified** | support.google.com, blog.youtube, youtube.com blocked. No contrary evidence. |
| YPP rises to 8,000 hours on 2027-02-01 | **[U] not re-verified** | Still secondary-source only; treat as likely, plan to apply before Feb 2027. |
| FTC disclosure, $53,088 per violation | **[U] not re-verified** | ftc.gov blocked. Disclosure requirement itself is not in doubt. |
| Gumroad rules on AI-generated goods | **no data found** | help.gumroad.com blocked; nothing in the open-source repo's help-center templates surfaced on AI goods in this session's searches. |
| Tax: 1099-K threshold, hobby-vs-business, self-employment tax | **no data found** | irs.gov blocked. Verified only that Gumroad is merchant of record for sales tax/VAT [V]; income-tax reporting is the operator's, and the dossier does not budget for it. |
| Profession liability disclaimers | **holds** | Reinforced by n8n Assistant "can make mistakes" and Anthropic "material inaccuracies" language: the template license must disclaim accounting/legal outcomes. |

## 7. What would change the verdict

- Fetching n8n.io/pricing and n8n.io/affiliates (Starter price, execution caps, cookie/payout terms) and descript.com/pricing: converts three "weakened" rows to holds/refuted.
- One verifiable earnings report from a profession-specific automation seller (Gumroad or n8n template library) with sales counts: would anchor the month-6 base.
- n8n Assistant pricing/credits per plan: if it is generous on Starter, the template pack should be repositioned as "installed and maintained against your stack" only, not a file download.

## 8. Corrected numbers (summary)

| Metric | Dossier | Corrected |
|---|---|---|
| Weekly hours (3+ SKUs) | 10.75 | 12-15 [E] |
| Automation share | ~45% | ~35% [E] |
| Gumroad net on $49 / $79 / $99 | $41.88 / $68.01 / $85.43 | unchanged [V] |
| Gumroad minimum payout | $100 | $100 [V] |
| Month-6 base revenue | ~$450 | $60-250 [E] |
| Month-6 base $/hr | $9-10 | $1-4.50 [E] |
| First dollar earned / received | ~60 days | 6-10 weeks earned; 3-5 months received [E] |
| n8n release cadence | not stated | ~2/day, two major lines [V] |
| n8n native prompt-to-working-workflow | not mentioned | shipped 2026-07-09 (Cloud), 2.35 (self-hosted) [V] |

## Sources

Verified this session (GitHub, raw.githubusercontent.com, platform.claude.com)
- [czlonkowski/n8n-mcp README (22.9k stars; "default parameter values are the #1 source of runtime failures")](https://github.com/czlonkowski/n8n-mcp)
- [n8n releases page (8 releases Sep 7-10 2026)](https://github.com/n8n-io/n8n/releases)
- [n8n BREAKING-CHANGES.md](https://raw.githubusercontent.com/n8n-io/n8n/master/packages/cli/BREAKING-CHANGES.md)
- [n8n issue #30459: update broke all Execute-node workflows (May 2026)](https://github.com/n8n-io/n8n/issues/30459)
- [n8n issue #35788: instance broken by 2.33.4 update (Aug 2026)](https://github.com/n8n-io/n8n/issues/35788)
- [n8n issue #35787: workflows disappeared after version update (Aug 2026)](https://github.com/n8n-io/n8n/issues/35787)
- [n8n issue #36249: regression, new workflows fail with 404 (Aug 2026)](https://github.com/n8n-io/n8n/issues/36249)
- [n8n issue #28572: 2.15.1 to 2.16.1 breaking-changes module failure (Apr 2026)](https://github.com/n8n-io/n8n/issues/28572)
- [n8n issue #37175: n8n Cloud Code nodes failing across all workflows (Aug 2026)](https://github.com/n8n-io/n8n/issues/37175)
- [Zie619/n8n-workflows issue #200: 1,457 of 1,573 AI nodes replaced with noOp (Sep 2026)](https://github.com/Zie619/n8n-workflows/issues/200)
- [Zie619/n8n-workflows issue #125: downloaded workflows import but cannot run (Oct 2025)](https://github.com/Zie619/n8n-workflows/issues/125)
- [n8n docs: Sustainable Use License FAQ (allowed and disallowed uses)](https://raw.githubusercontent.com/n8n-io/n8n-docs/main/docs/n8n-community-license/README.md)
- [n8n docs changelog: n8n Assistant, 2026-07-09, n8n 2.29.9](https://raw.githubusercontent.com/n8n-io/n8n-docs/main/docs/changelog/README.md)
- [n8n docs: AI Workflow Builder (beta, credit per interaction)](https://raw.githubusercontent.com/n8n-io/n8n-docs/main/docs/build/ways-of-building-workflows/ai-workflow-builder.md)
- [n8n docs: start your free trial (14 days, 1,000 executions, Pro features)](https://raw.githubusercontent.com/n8n-io/n8n-docs/main/docs/deploy/use-n8n-cloud/start-your-free-trial.md)
- [n8n docs: manage your data (Starter 2,500 executions saved, 7-day retention, 320 MiB)](https://github.com/n8n-io/n8n-docs/blob/main/docs/deploy/use-n8n-cloud/configure-cloud/manage-your-data.md)
- [n8n docs: download workflows (deleted 90 days after trial)](https://github.com/n8n-io/n8n-docs/blob/main/docs/deploy/use-n8n-cloud/download-workflows.md)
- [n8n docs: Gateway credits (nodes stop at zero balance; no top-up on trial)](https://github.com/n8n-io/n8n-docs/blob/main/docs/deploy/use-n8n-cloud/gateway-credits/README.md)
- [n8n docs: submit templates / creator program](https://github.com/n8n-io/n8n-docs/blob/main/docs/reusable-content/.gitbook/includes/workflows/templates/submit-templates.md)
- [antiwork/gumroad purchase.rb (fee constants)](https://github.com/antiwork/gumroad/blob/main/app/models/purchase.rb)
- [antiwork/gumroad user.rb (high-volume 5% fee at $20k GMV)](https://github.com/antiwork/gumroad/blob/main/app/models/user.rb)
- [antiwork/gumroad payouts.rb (MIN_AMOUNT_CENTS = 100_00)](https://github.com/antiwork/gumroad/blob/main/app/business/payments/payouts/payouts.rb)
- [antiwork/gumroad help article template: fees exclude card processing 2.9% + $0.30](https://github.com/antiwork/gumroad/blob/main/app/views/help_center/articles/contents/_66-gumroads-fees.html.erb)
- [antiwork/gumroad llms.txt view: 10% + $0.50 direct, 30% Discover, merchant of record](https://github.com/antiwork/gumroad/blob/main/app/views/llms/index.erb)
- [antiwork/gumroad credit.rb (processor fee retained on refunds)](https://github.com/antiwork/gumroad/blob/main/app/models/credit.rb)
- [Anthropic API pricing (platform.claude.com)](https://platform.claude.com/docs/en/about-claude/pricing)
- [TuguiDragos/n8n-ai-call-agent README (EUR 58.99 Gumroad, $230 n8n library, 5 required accounts)](https://github.com/TuguiDragos/n8n-ai-call-agent)

Mirrored primary text (primary domain blocked)
- [Anthropic Consumer Terms, effective 2026-06-14 (mirror in UPDerechoIA/observatorio-de-licencias)](https://github.com/UPDerechoIA/observatorio-de-licencias/blob/main/data/extracted/anthropic-claude-consumer-terms-2026-06-14.txt)
- [Anthropic Consumer/Commercial Terms output-assignment quotes (mirror in CharlesHoskinson/anthropies)](https://github.com/CharlesHoskinson/anthropies)

Attempted and blocked (no data found)
- https://n8n.io/pricing/ · https://n8n.io/affiliates/ · https://docs.n8n.io/sustainable-use-license/ · https://community.n8n.io/
- https://www.descript.com/pricing · https://www.descript.com/affiliate-terms · https://help.descript.com/
- https://claude.com/pricing · https://www.anthropic.com/legal/consumer-terms · https://support.claude.com/
- https://gumroad.com/pricing · https://help.gumroad.com/article/66-gumroads-fees
- https://support.google.com/youtube/answer/72851 · https://blog.youtube/ · https://www.youtube.com/
- https://www.ftc.gov/ · https://www.copyright.gov/ai/ · https://www.irs.gov/
- https://www.reddit.com/ · https://old.reddit.com/ · https://hn.algolia.com/ · https://dev.to/ · https://www.indiehackers.com/ · https://socialblade.com/ · https://www.trustpilot.com/ · https://www.g2.com/ · https://web.archive.org/ · https://en.wikipedia.org/
