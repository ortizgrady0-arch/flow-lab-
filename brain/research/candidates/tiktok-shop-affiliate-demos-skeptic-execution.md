---
title: "Skeptic (execution): TikTok Shop affiliate hands-on demo clips with AI off-camera"
tags: [research, skeptic, execution, tiktok-shop-affiliate-demos]
updated: 2026-09-10
lens: execution
target: "[[research/candidates/tiktok-shop-affiliate-demos]]"
overall: weakened
confidence: 0.55
---

## TL;DR

- Overall verdict: **weakened**. The plan is directionally sane (human on camera, AI off-camera), but almost every number in the dossier rests on unfetched vendor blogs, and this session could not reach a single primary page either (WebSearch budget 200/200 exhausted; egress proxy blocked TikTok, IRS, FTC, Copyright Office, n8n, CapCut, Claude, Kalodata, EchoTik, Reddit, Wayback). Only GitHub-hosted content was reachable, so evidence below is mostly "secondary quoted inside GitHub repos".
- **Refuted claim:** "Creator Center marketplace has no public API." A TikTok Shop *Affiliate Creator API* exists with 23+ creator-scoped endpoints (search open-collab products, sample applications, affiliate orders, generate links, upload/precheck/**post shoppable video**), per an API digest in a public repo. Access requires a registered Partner Center app plus creator OAuth; approval friction is unknown (docs blocked). This cuts both ways: more automation is possible than the dossier assumes, but only after an unbudgeted developer-app setup.
- **Hidden manual work the dossier under-counts:** seller-side outreach is industrially automated (tools advertise 3K-7K DMs/day and 4K invites/day), so the creator inbox is a triage job; "refundable" samples require buying the product first and only refund after a sale (recurring cash float, not the one-off $60-120); a creator tutorial says post 1-3 clips/day for 90 days and expect **30-60 days before any money**, with ~90% quitting in that window; the $20 minimum withdrawal and 15-31 day settlement add lag. Realistic all-in time is 14-16 h/wk, not 11-13.
- **Tool costs are unverified and partly wrong:** n8n self-host is genuinely free for internal business use (Sustainable Use License, verified) and the Cloud trial is 1,000 executions of Pro features; the $24 Starter price was not verifiable. CapCut Pro is quoted at both $7.99/mo ($4.99 annual) and $19.99/mo by two 2026 sources (region/platform dependent), so the dossier's "$9.99 Standard / $19.99 Pro" is weakened. Claude Pro $20, EchoTik $10.19 and Kalodata $59-110 could not be verified.
- **Revenue scenarios are internally consistent but built on an unsupported input** (2,000 avg views/post for a sub-5k-follower account; no data found). Commission ranges conflict: one 2026 secondary table puts beauty at 8-12% and fashion 5-8%, versus the dossier's 15-30% beauty; tutorial examples pay $1.00-$7.59 per sale on $5-40 items. Corrected: month-3 $0; month-6 modal $0-150, base $150-300, upside unchanged; implied base hourly ~$3-5, not $8.
- **Time to first dollar (60-100 days) broadly holds** (30-60 days to first sale + 15-31 day settlement + payout cadence + $20 minimum), but time to the 1,000-follower gate is "no data found"; treat 75-120 days as the honest band.
- **Policy is messier than stated:** secondary sources disagree on whether the AI-voice ban covers only LIVE (kaldon, Sept 2026: AI voiceover on shoppable videos allowed with label) or LIVE **and shoppable videos** (viralslice, June 2026, citing a May 22 Content Policy and June 2 Creator Enforcement Policy). Dates quoted range May 22 / May 23 / June 2 / June 16-17 / July 31. A "human in the first frame" rule for US product videos is asserted by one vendor. The design (human voice, human hands) survives all readings, but "AI-assisted captions/scripts exempt" is only vendor-attested.
- **Missed legal/tax items:** OBBBA raised the 1099-NEC threshold to $2,000 for payments after 2025-12-31 (accountant-reviewed secondary), so small earners get no form but still owe self-employment tax (IRS page blocked; verify $400 net threshold); FTC fake-reviews rule penalty was $51,744/violation (2024 figure; the dossier's $53,088 is the 2025 inflation figure, 2026 not found); AI-output copyright is already summarized in a sibling note and is low-risk for human-performed scripts.

## Evidence quality note

Every WebFetch to a primary domain in this session returned `EGRESS_BLOCKED` (seller-us.tiktok.com, www.tiktok.com, business.tiktokshop.com, partner.tiktokshop.com, developers.tiktok.com, irs.gov, ftc.gov, ecfr.gov, federalregister.gov, congress.gov, law.cornell.edu, copyright.gov, blogs.loc.gov, n8n.io, docs.n8n.io, capcut.com, claude.com, anthropic.com, echotik.live, kalodata.com, fastmoss.com, hamstergarage.com, dashboardly.io, affiversemedia.com, branvas.com, autods.com, creatorsagency.co, shortformnation.com, netinfluencer.com, ppc.land, pymnts.com, socialmediatoday.com, skadden.com, medium.com, news.ycombinator.com, wikipedia, duckduckgo, bing). Reddit and web.archive.org are unfetchable by tool policy. The WebSearch budget was already exhausted (200/200) before this lens ran. What *was* reachable: github.com, raw.githubusercontent.com, and the GitHub code/repo search API. Labels used below: **V** = primary text observed directly (a license file, n8n docs source); **G** = secondary or vendor content observed inside a public GitHub repo (a blog's source file, a research brief, an API digest); **A** = anecdotal (creator tutorial transcript, vendor SOP); **U** = unverified (dossier figure that could not be checked). Default verdict when unsupported is "weakened".

## 1. Does the AI stack produce sellable quality today?

| Dossier claim | Verdict | Evidence |
|---|---|---|
| AI scripts/hooks/captions are exempt from AIGC labeling and safe to use | **weakened** | Only vendor-attested. A June 2026 blog (G) says the ban "is specific to promotional livestreams and shoppable videos that use AI-generated voices or pre-recorded audio narration. AI tools for scripting, caption generation, thumbnail design, or post-production editing of non-live content are not covered" ([viralslice AI-voice post](https://github.com/viralsliceco/vsc/blob/main/apps/www/content/blog/tiktok-shop-ai-voice-ban.mdx), 2026-06-23). The official Content Policy page (knowledge_id 6837891779151617) is cited by a research brief as saying "AI-generated content is not allowed if it misleads or deceives viewers, impersonates others, or violates TikTok Shop Content Policy" ([ai-creator-ops brief](https://github.com/joewilsonai/ai-creator-ops/blob/main/docs/research/source-briefs/2026-05-18-tiktok-shop-ai-creator-affiliate-monetization.md), reviewed 2026-05-18, G). No text explicitly exempting scripts was observed. |
| AI scripts "drift into unsupported claims" and need human stripping (dossier's own risk note) | **holds (and is bigger than stated)** | A dedicated compliance product exists precisely for this: BanProof "scans video scripts against TikTok Shop content policies, Amazon Associates Operating Agreement, and FTC disclosure guidelines" across 11 violation categories (medical claims, false certifications, urgency language, fake social proof, income claims, FTC disclosure gaps, price violations, AI voice disclosures, testimonial requirements, product overclaims) ([banproof-mcp README](https://github.com/NimishRangani/banproof-mcp), 2026, G). The dossier budgets 0.4 h/wk for compliance review on 18 clips; one pass per script through an 11-category checklist is closer to 1-1.5 h/wk. |
| AI-generated visuals/voice would be label-suppressed, so keep AI off-camera | **holds, with conflicting scope** | Kaldon (2026-09-05, G): AI voiceover on pre-recorded shoppable videos is *allowed* "provided the narration accurately describes the product and the 'AI-generated content' toggle is enabled"; undisclosed AIGC can trigger "50-90% reach throttling or account suspension"; only "41% of AI product images pass TikTok's detection standards" (Aug 2026). These reach/detection numbers are uncited vendor claims (A). Viralslice (2026-06-11, G) says the May 22, 2026 Content Policy bans AI voices "from promotional livestreams and shoppable videos". Either way the human-voice design is the safe path. |
| Human hands-on demos are "less crowded" because AI entrants are pushed out | **weakened** | No count of human-demo vs AI-demo affiliate videos was found. The only supply-side datum is that ~89 public GitHub repos target "tiktok shop affiliate" tooling and 355 files reference the creator API (observed 2026-09-10), most created June-September 2026, i.e. the tooling wave is still rising, not receding. |
| Sellable quality of the *output* (do AI-scripted human demos convert better/worse?) | **no data found** | No A/B data, buyer complaints, or brand reviews of AI-scripted human UGC were reachable. Treat as unknown. |

Additional constraint asserted by one vendor (A): "TikTok Shop US requires the opening visual to show a real human physically interacting with the product. AI images, avatars, or synthetic scenes cannot serve as the first frame" ([kaldon post](https://github.com/seanpercytravis/kaldon-marketing-site/blob/main/src/content/blog/tiktok-shop-ai-video-compliance-auto-generated-content-control-2026.md), 2026-09-05). If true, CapCut template intros and AI b-roll openers are out; the dossier already avoids AI b-roll, so this is compatible but should be a hard rule in the edit template.

## 2. Hidden manual work the dossier ignored or under-weighted

| Item | Dossier | Reality (evidence) | Added h/wk |
|---|---|---|---|
| Inbound seller spam / target-collab triage | Step 2 "sample requests and seller messaging" 0.9 h human | Seller-side outreach is automated at scale: a seller SOP (last updated April 2026, A) lists Cruva "3K-7K msgs/day", Uptik "4K targeted invites/day", TTinit "1K msgs/day per shop", Euka "1K DMs + 2.5K invites/day", with "10-20%" DM response rates expected ([AdPros creator SOP](https://github.com/AdProsllc/docs/blob/main/tiktok-shop-creator-sop/index.html)). Sellers also scrape the creator marketplace with open-source tools ([creator scraper](https://github.com/1Milkdeliver/tiktok-shop-creator-scraper), Aug 2026). Once an account is visible, invitations arrive in bulk; reading, declining and deduplicating them against the scoring sheet is human work. | +1.0 |
| Refundable-sample cash float | One-off $60-120 for 3-5 products | Tutorial (2025, A): refundable samples mean "purchase the product yourself, create content, if you generate at least one sale the brand refunds your purchase price" ([tutorial extraction](https://github.com/elienevets-max/claude-code/blob/master/tiktok/tiktok-shop-creator-tutorial-knowledge-extraction.md)). With 5 products in flight and no sale yet, that is a rolling $100-200 float, refunded only on the first sale of *each* item; failed items are sunk cost. | cash, not time |
| Posting cadence needed to leave the flat period | 1-3 clips/day, 18/wk | Tutorial (A): "do one post per day every day for the next 3 months", ideally 3/day; "give it at least 30 to 60 days before you even expect to make any money"; "80% of people who watch this video will not actually go out and just make a TikTok" and ~90% of starters quit in the flat period. The dossier's 18/wk matches the *ideal* cadence, so the 4 h/wk filming estimate (13 min per clip incl. setup, retakes, product prep) is optimistic. | +1.5 (filming) |
| Compliance pass per script | 0.4 h/wk | 11-category checklist (BanProof, G) over 18 scripts. | +0.8 |
| Developer-app setup if the API route is used | not mentioned | Creator API needs an app with `app_key`, signed requests, creator OAuth with ~1-hour authorization links and expiring refresh tokens that force re-authorization ([Linkfox auth reference](https://github.com/linkfox-ai/linkfox-skills/blob/main/skills/linkfox-tiktok-selection-and-shoppable-video/references/linkfox-tiktok-video-auth.md), G). Partner Center approval process: **no data found** (blocked). | one-off 4-10 h, or $ for a vendor |
| Tax admin | 0.15 h/wk "mostly full" | Quarterly estimated tax, Schedule C, tracking sample FMV as income (see section 6). | +0.25 |
| CHR monitoring and appeals | in compliance row | CHR is "a dynamic behavioral score... commission freezes can occur before reaching violation thresholds"; recovery requires a "30-day clean posting window" ([viralslice CHR post](https://github.com/viralsliceco/vsc/blob/main/apps/www/content/blog/tiktok-creator-health-rating.mdx), 2026-06-19, G). One bad week can freeze commissions for a month. | +0.2 |

Corrected weekly load: **~14-16 h/wk** at the 18-clip cadence, versus the dossier's 11-13. Automation share by time falls to roughly 40%, not 50%.

## 3. Tool costs and free-tier limits

| Tool | Dossier | Finding | Verdict |
|---|---|---|---|
| n8n self-hosted | "$0 self-hosted" in lean case | **V**: Sustainable Use License: "You may use or modify the software only for your own internal business purposes or for non-commercial or personal use" ([LICENSE.md](https://raw.githubusercontent.com/n8n-io/n8n/master/LICENSE.md)). Community edition lacks only enterprise features (environments, SSO, external secrets, log streaming, git version control, sharing) ([community-edition-features.md](https://raw.githubusercontent.com/n8n-io/n8n-docs/main/docs/deploy/host-n8n/community-edition-features.md)). A VPS ($5-6/mo per sibling notes) is still needed. | **holds** (add ~$6/mo hosting) |
| n8n Cloud Starter $24/mo, 2,500 executions, 14-day trial | | n8n.io pricing blocked. Docs source (V) says the trial "gives you Pro plan features with a limit of 1000 executions", and "Start and Starter plans: max 2500 executions saved and 7 days execution log retention" ([start-your-free-trial.md](https://github.com/n8n-io/n8n-docs/blob/main/docs/deploy/use-n8n-cloud/start-your-free-trial.md), [manage-your-data.md](https://github.com/n8n-io/n8n-docs/blob/main/docs/deploy/use-n8n-cloud/configure-cloud/manage-your-data.md)). The "2,500" in the dossier may be the *log retention* cap, not the monthly quota; price not verified. | **weakened** |
| CapCut free / Standard $9.99 / Pro $19.99 | | Two 2026 secondary sources disagree (G): "CapCut Pro is $19.99 a month" as of August 2026 ([better-shot FAQ](https://github.com/KartikLabhshetwar/better-shot/blob/main/bettershot-landing/components/home/faq.tsx)) vs "Pro at $7.99/month... Annual billing drops it to $4.99/month ($59.99/year)... roughly 200 AI credits per month; credit packs run $4.99-$19.99" and "the free tier is a real, pro-grade timeline editor with captions, transitions, and text-to-speech" ([frankx CapCut workflow](https://github.com/frankxai/frankx.ai-vercel-website/blob/main/content/blog/ultimate-capcut-workflow-2026.mdx)); the same site notes web vs in-app/iOS prices differ. Free tier suffices for the design (no AI credits needed). | **weakened**; budget $0-20 |
| Claude Pro $20 | | claude.com and anthropic.com blocked; no source observed. | **U** |
| EchoTik free / $10.19; Kalodata $59-79 / $109.99; FastMoss $29-99 | | All vendor sites blocked; no GitHub-hosted price table found. | **U** |
| "Consumer plans allow commercial use of outputs" | | Not verified for Claude or CapCut this session. n8n verified above. | **weakened** |

Corrected monthly tools: lean **$26-35** (Claude $20 U + VPS $6 + CapCut free); base **$55-80** depending on which CapCut price applies; the dossier's $64 base is inside that band but should not be quoted as verified.

## 4. Are month-3 / month-6 numbers realistic for a beginner?

| Input | Dossier | Finding | Verdict |
|---|---|---|---|
| 15% blended commission on sub-$40 kitchen/cleaning/beauty | | A 2026 research report quoting Hamster Garage lists **electronics 2-5%, fashion 5-8%, beauty 8-12%, toys 10-15%, targeted 18-50%** ([researcher report](https://github.com/sepehrnoory/researcher/blob/main/research/reports/tiktok-shop/tiktok-shop-affiliate-slop-rules-risk-strategy.md), 2026-07-05, G), which is *below* the dossier's beauty 15-30% (also Hamster Garage, unfetched). Tutorial examples (A): coffee $30 at 10% = $3.00; supplement $39.95 at 15% = $7.59; dishwashing rags $4.99 at 20% = $1.00. A 10-15% blend on a $20-25 basket gives **$2-3.75 per order**, not $3.75-5.00. | **weakened** |
| 2,000 avg views/post at month 6 for a <10k-follower account | | **no data found**. No median-views-by-follower-tier data for new US affiliate accounts was reachable. | **weakened** (unsupported input) |
| 2% card click x 4.7% closed-loop conversion (= ~0.094% of views become orders) | | The tutorial's illustrative rate is 0.1% of views to sales (1,000 sales from 1M views) ([tutorial extraction](https://github.com/elienevets-max/claude-code/blob/master/tiktok/tiktok-shop-creator-tutorial-knowledge-extraction.md), A), so the funnel arithmetic is coherent; the 4.7% figure itself remains an unfetched vendor stat. | **holds (arithmetic), weakened (source)** |
| Nano tier $200-1,500/mo; 59% churn by month 12 | | Branvas and Dashboardly blocked; no independent earnings reports found. The tutorial's own framing is "a year, two years, 3 years before you are really pumping some serious cash" (A). | **weakened** |
| Named beginner earnings reports in kitchen/cleaning | dossier: no data | Still **no data found** (Reddit unfetchable, search budget zero). | - |

Corrected scenarios (same 60 posts/month, $22 basket, 12% blend, 0.1% view-to-order, 15% clawback): month-3 **$0** (Pilot + settlement lag); month-6 conservative **$0-50** (800 views/post), base **$150-300** (1,200-2,000 views/post), upside unchanged ($1,500+ needs a viral Q4 clip and a targeted plan). Implied base hourly at 14-16 h/wk: **~$3-5/h**.

## 5. Time to first dollar

| Gate | Dossier | Finding | Verdict |
|---|---|---|---|
| 1,000 followers to join affiliate; 5,000 for full access | | Official Creator Eligibility Policy (knowledge_id 6939143037667118) is cited as "Affiliate Creators: 1,000+ followers; Marketing Creators: 5,000+ followers" ([ai-creator-ops brief](https://github.com/joewilsonai/ai-creator-ops/blob/main/docs/research/source-briefs/2026-05-18-tiktok-shop-ai-creator-affiliate-monetization.md), reviewed 2026-05-18, G). | **holds** |
| 30-day Pilot at 3 shoppable videos/day, exit at 5k followers + CHR >= 176 | | A skills reference (G, undated 2025) says creators "with fewer than 5,000 followers are initially enrolled in a 30-day Creator Pilot Program" ([Wbunker shop.md](https://github.com/Wbunker/skills-repo/blob/main/tiktok-expert/references/shop.md)). The 3/day cap and the CHR 176 exit threshold: **no data found** (zero GitHub hits for either). | **weakened** (details unverified) |
| Time to 1,000 followers from zero | anecdotal 3-8 weeks | **no data found**. | **weakened** |
| First sale 30-60 days after starting | implied | Tutorial (A): "Give it at least 30 to 60 days before you even expect to make any money." | **holds** |
| Settlement 15-31 days; $20 minimum withdrawal | dossier omits the minimum | Researcher report (G) quoting Hamster Garage/Dashboardly: "~15 days after delivery (up to ~31 days for newer sellers)"; "Minimum withdrawal commonly ~$20"; one skills prompt notes "Commission settlement hold: 15-31 days post-sale" ([htupycollabs prompt](https://github.com/htupycollabs-spec/Analytics/blob/main/Context/tiktok-system-prompt.html)). Another secondary puts the return window at "7-14 days after delivery" (Wbunker). | **holds**; add $20 minimum |
| Realistic first deposit 60-100 days (base 75) | | Sum of gates: 3-8 wk to 1k followers (U) + 30-day Pilot + first sale + 15-31 days + payout + $20 minimum. | **holds at the top of the band**; quote **75-120 days** |

## 6. Missed policy, TOS, tax and legal risk

| Risk | Finding | Type | Verdict vs dossier |
|---|---|---|---|
| AI-voice ban scope and date | Viralslice (G): "revised Content Policy, published May 22, 2026, explicitly bans AI-generated voices, pre-recorded audio, and static-image content from promotional livestreams **and shoppable videos**"; separate post says policy "published June 16-17, 2026". Kaldon (G): LIVE ban "enforced since May 23, 2026" and AI voiceover on shoppable videos allowed with label. Vault lens [[research/lenses/commerce-arbitrage]] says July 31. Official Policy Pulse page blocked. | G/A | **weakened** (dossier flags the date conflict but not the scope conflict) |
| Six-violation rule | "Under the June 2, 2026 Creator Enforcement Policy, six violations of the same rule within a 90-day window triggers an immediate removal of your e-commerce permissions" (viralslice citing PPC.land, G). | G | **holds** |
| CHR >= 150 and PPS >= 3.5 for gated categories | Researcher report cites the official Affiliate Marketing Policy (2026-06-23): "Creator Health Rating >= 150" and "creator Promotion Performance Score >= 3.5". | G | **holds** |
| CHR mechanics | "started with a baseline score of 200 CHR points"; green tier "700+"; recovery via "30-day clean posting window"; a "soft enforcement period" ran Q1 2026 before full enforcement May/June 2026 (viralslice, G). Suspension ladder "14-30 day suspensions... bans for 'high-risk association'" (researcher report, G). | G | **holds**, adds the 30-day recovery lag |
| Automation / bots TOS | Community Guidelines page blocked. Ecosystem evidence: Selenium posting bots exist and break constantly (19 upload-failure issues on the most-used uploader, 2024-2026: [tiktok-uploader issues](https://github.com/wkaisertexas/tiktok-uploader/issues)); vendor "account warming 7-14 days" and "TikTok links accounts via 50+ device attributes" claims (researcher report, A). Do not use browser bots; the sanctioned route is the Creator API. | G/A | **missed** in dossier |
| Creator API exists | 23+ creator-scoped endpoints incl. "Post Shoppable Video", "Search Sample Applications", "Search Affiliate Orders", "Generate General/Publisher Links"; "Caller Type: Creator applications only"; rate-limit error 36009002 "Too many requests" ([rivonclaw API digest](https://github.com/gaoyangz77/rivonclaw/blob/main/docs/API/TIKTOK_SHOP/AFFILIATE_CREATOR.md), G). | G | **refutes** "no public API"; access friction **no data found** |
| Physical possession | "TikTok Shop requires affiliates to physically possess products they promote" (htupycollabs prompt, A). Consistent with design. | A | new, compatible |
| Sample quotas (5 active under $5k GMV; 14-day post) | Official Guide to Samples blocked; zero GitHub hits for the quota wording. | U | **weakened** |
| FTC | Fake Reviews Rule: "civil penalties up to $51,744 per violation", effective 2024-10-21, covering AI-generated reviews and fake indicators of social-media influence (researcher report citing FTC 2024-08-14 release, G). Dossier's $53,088 is the 2025 adjusted figure (U); 2026 figure **no data found**. Disclosures 101 blocked. | G/U | **holds** in substance; number stale |
| Tax (dossier: silent) | OBBBA: 1099-NEC "Threshold - $600 for 2025 payments (OBBBA raises the threshold to $2,000 for payments after 12/31/2025)... 24% backup withholding (made permanent by OBBBA)" ([openaccountants, reviewed by a licensed accountant 2026-06-03](https://github.com/openaccountants/openaccountants/blob/main/skills/federal/us-1099-nec-issuance.md), G). Implication: a sub-$2,000/yr affiliate receives no 1099 but must still self-report; self-employment tax threshold ($400 net, IRS page blocked) **not verified**; free samples kept are arguably taxable income at FMV (no source found). TikTok's partner terms also state "Each party shall be solely responsible for its own taxes" ([partner campaign T&Cs mirror](https://github.com/lazykern/ecommerce-api-docs/blob/main/data/processed/tiktok/guides/terms-and-policies/terms-and-policies-english/tiktok-shop-partner-campaign-terms-and-conditions.md), 2025-02-24, G). | G | **missed** |
| Copyright of AI output | Not re-fetched; the US Copyright Office Part 2 report (2025-01-29) is summarized in [[research/candidates/linkedin-founder-ghostwriting]] and [[research/candidates/ai-actor-ad-packs-dtc]]: wholly AI-generated text is not copyrightable, prompts alone are insufficient, human modification is protectable case by case. A human-performed, human-edited video is protectable; the raw AI script is not. Low exposure. | prior notes | **holds** (resolves the dossier's "no data found") |
| US JV / algorithm retraining | Not re-examined this session. | - | unchanged |

## 7. Claim-by-claim register

| # | Claim | Verdict | Corrected |
|---|---|---|---|
| 1 | Automation ~50% by time, 11-13 h/wk | weakened | ~40%, 14-16 h/wk |
| 2 | "No public API for the creator marketplace; scoring runs on CSV exports" | refuted | Affiliate Creator API exists (23+ endpoints incl. post shoppable video); needs a registered app + OAuth; approval friction unknown |
| 3 | AI scripts/captions are label-exempt | weakened | vendor-attested only; official text observed says AI content banned if misleading |
| 4 | AI voice ban is LIVE-only (May 2026) | weakened | scope disputed (LIVE vs LIVE + shoppable video); dates May 22 / 23 / June 2 / June 16-17 / July 31 |
| 5 | Tools $30-65/mo; n8n Cloud $24; CapCut $9.99/$19.99; Claude $20; EchoTik $10.19 | weakened | n8n self-host free (verified); CapCut Pro $7.99 or $19.99 by source; Claude/EchoTik/Kalodata unverified; lean $26-35, base $55-80 |
| 6 | Startup $175-285 | weakened | add a rolling $100-200 refundable-sample float |
| 7 | 15% blended commission, $3.75-5.00/order | weakened | 10-15% blend, $2-3.75/order on a $20-25 basket |
| 8 | Month-6 base $400, ~$8/h | weakened | base $150-300, ~$3-5/h; modal outcome $0-150 |
| 9 | First deposit 60-100 days (base 75) | holds | 75-120 days; add $20 minimum withdrawal |
| 10 | 1,000 followers to join; Pilot for <5k | holds | official policy quoted via brief; 3/day cap and CHR 176 exit unverified |
| 11 | CHR >= 150, PPS >= 3.5; six violations/90 days | holds | add 30-day clean-window recovery lag |
| 12 | Sample quota 5 active / 14-day post | weakened | no source reachable |
| 13 | FTC penalty $53,088 (2025) | holds (stale) | $51,744 is the 2024 rule figure; 2026 not found |
| 14 | Tax handled "mostly full" via n8n log | missed | 1099-NEC threshold now $2,000; self-report below it; SE tax and sample FMV to verify |
| 15 | Copyright "no data found" | holds | human-performed video protectable; raw AI script not (Copyright Office 2025 via sibling notes) |
| 16 | Human demos less crowded than they look | weakened | no supply data; tooling wave still rising (89 repos, most Jun-Sep 2026) |

## 8. What would change the verdict

1. Fetch the five official Seller University pages listed in Sources (eligibility 6939143037667118, content policy 6837891779151617, CHR 5054301796321070, affiliate marketing policy 2244964886103809, samples 5764641632306946) and the May 2026 Policy Pulse; if scripts/captions are explicitly exempt and AI voiceover is allowed on shoppable videos with a label, claims 3-4 move to "holds".
2. Confirm Partner Center approval requirements for a creator-scoped app; if a solo creator can self-approve in under a day, claim 1 improves (automation ~55-60%) and claim 2 becomes a design change, not a risk.
3. Three first-person earnings logs from sub-10k US kitchen/cleaning/beauty affiliates (views/post, orders/month, months 1-6) would replace the unsupported 2,000-views input.
4. Live pricing pages for n8n, CapCut (web vs iOS), Claude, EchoTik, Kalodata.

Related: [[research/candidates/tiktok-shop-affiliate-demos]], [[research/lenses/shortform-social]], [[research/lenses/commerce-arbitrage]], [[research/saturated-overhyped]], [[research/shortlist]], [[research/candidates/linkedin-founder-ghostwriting]] (Copyright Office summary), [[research/candidates/ai-actor-ad-packs-dtc]].

## Sources

Observed directly this session (GitHub-hosted):
- [n8n Sustainable Use License (LICENSE.md, observed 2026-09-10)](https://raw.githubusercontent.com/n8n-io/n8n/master/LICENSE.md)
- [n8n docs: Community edition features (source, observed 2026-09-10)](https://raw.githubusercontent.com/n8n-io/n8n-docs/main/docs/deploy/host-n8n/community-edition-features.md)
- [n8n docs: Try free then choose a plan (1,000-execution trial)](https://github.com/n8n-io/n8n-docs/blob/main/docs/deploy/use-n8n-cloud/start-your-free-trial.md)
- [n8n docs: Manage your data (Starter 2,500 saved executions, 7-day retention)](https://github.com/n8n-io/n8n-docs/blob/main/docs/deploy/use-n8n-cloud/configure-cloud/manage-your-data.md)
- [rivonclaw: TikTok Shop Affiliate Creator API digest (2026)](https://github.com/gaoyangz77/rivonclaw/blob/main/docs/API/TIKTOK_SHOP/AFFILIATE_CREATOR.md)
- [TikTokSlop: TikTok Shop API notes (seller scopes, shop_cipher)](https://github.com/Fladdermuz/TikTokSlop/blob/main/docs/TIKTOK_API_NOTES.md)
- [Linkfox skills: TikTok shoppable-video OAuth reference (2026)](https://github.com/linkfox-ai/linkfox-skills/blob/main/skills/linkfox-tiktok-selection-and-shoppable-video/references/linkfox-tiktok-video-auth.md)
- [viralslice blog source: TikTok Creator Health Rating (2026-06-19)](https://github.com/viralsliceco/vsc/blob/main/apps/www/content/blog/tiktok-creator-health-rating.mdx)
- [viralslice blog source: TikTok Shop AI voice ban (2026-06-23)](https://github.com/viralsliceco/vsc/blob/main/apps/www/content/blog/tiktok-shop-ai-voice-ban.mdx)
- [viralslice blog source: TikTok Shop creator enforcement 2026 (2026-06-11)](https://github.com/viralsliceco/vsc/blob/main/apps/www/content/blog/tiktok-shop-creator-enforcement-2026.mdx)
- [Kaldon blog source: TikTok Shop AI video compliance (2026-09-05)](https://github.com/seanpercytravis/kaldon-marketing-site/blob/main/src/content/blog/tiktok-shop-ai-video-compliance-auto-generated-content-control-2026.md)
- [ai-creator-ops: TikTok Shop AI creator affiliate monetization brief (reviewed 2026-05-18)](https://github.com/joewilsonai/ai-creator-ops/blob/main/docs/research/source-briefs/2026-05-18-tiktok-shop-ai-creator-affiliate-monetization.md)
- [ai-creator-ops: sources.yaml (official TikTok Shop policy URLs, retrieved 2026-05-18)](https://github.com/joewilsonai/ai-creator-ops/blob/main/data/sources.yaml)
- [researcher: TikTok Shop affiliate slop rules / risk report (2026-07-05)](https://github.com/sepehrnoory/researcher/blob/main/research/reports/tiktok-shop/tiktok-shop-affiliate-slop-rules-risk-strategy.md)
- [Creator tutorial knowledge extraction (2025 YouTube tutorial, anecdotal)](https://github.com/elienevets-max/claude-code/blob/master/tiktok/tiktok-shop-creator-tutorial-knowledge-extraction.md)
- [Wbunker skills: TikTok Shop reference (Pilot Program, 5-30% commissions)](https://github.com/Wbunker/skills-repo/blob/main/tiktok-expert/references/shop.md)
- [AdPros: TikTok Shop creator recruitment SOP (seller outreach volumes, April 2026)](https://github.com/AdProsllc/docs/blob/main/tiktok-shop-creator-sop/index.html)
- [BanProof MCP: affiliate script compliance checker README (2026)](https://github.com/NimishRangani/banproof-mcp)
- [Reacher skills: seller-side affiliate program automation (2026)](https://github.com/ReacherApp/reacher-skills-public)
- [TikTok Shop creator scraper (open-source, Aug 2026)](https://github.com/1Milkdeliver/tiktok-shop-creator-scraper)
- [tiktok-uploader issues (upload failures 2024-2026)](https://github.com/wkaisertexas/tiktok-uploader/issues)
- [htupycollabs analytics prompt (settlement hold, possession requirement)](https://github.com/htupycollabs-spec/Analytics/blob/main/Context/tiktok-system-prompt.html)
- [openaccountants: US 1099-NEC issuance (OBBBA $2,000 threshold; reviewed 2026-06-03)](https://github.com/openaccountants/openaccountants/blob/main/skills/federal/us-1099-nec-issuance.md)
- [better-shot FAQ: CapCut Pro $19.99/mo as of Aug 2026](https://github.com/KartikLabhshetwar/better-shot/blob/main/bettershot-landing/components/home/faq.tsx)
- [frankx: Ultimate CapCut workflow 2026 (Pro $7.99/mo, $4.99 annual, ~200 AI credits)](https://github.com/frankxai/frankx.ai-vercel-website/blob/main/content/blog/ultimate-capcut-workflow-2026.mdx)
- [TikTok Shop Partner Campaign T&Cs mirror (2025-02-24)](https://github.com/lazykern/ecommerce-api-docs/blob/main/data/processed/tiktok/guides/terms-and-policies/terms-and-policies-english/tiktok-shop-partner-campaign-terms-and-conditions.md)

Official pages cited by the above but blocked this session (verify before committing money):
- [TikTok Shop Creator Eligibility Policy (knowledge_id 6939143037667118)](https://seller-us.tiktok.com/university/essay?knowledge_id=6939143037667118&lang=en)
- [TikTok Shop Content Policy (knowledge_id 6837891779151617)](https://seller-us.tiktok.com/university/essay?knowledge_id=6837891779151617&lang=en)
- [TikTok Shop Creator Health Rating overview (knowledge_id 5054301796321070)](https://seller-us.tiktok.com/university/essay?knowledge_id=5054301796321070&lang=en)
- [TikTok Shop Affiliate Marketing Policy (knowledge_id 2244964886103809)](https://seller-us.tiktok.com/university/essay?knowledge_id=2244964886103809&lang=en)
- [TikTok Shop: What you need to know before becoming a creator (knowledge_id 7608640301074219)](https://seller-us.tiktok.com/university/essay?knowledge_id=7608640301074219&lang=en)
- [TikTok Shop Guide to Samples (knowledge_id 5764641632306946)](https://seller-us.tiktok.com/university/essay?knowledge_id=5764641632306946&lang=en)
- [TikTok Shop Creator program page](https://business.tiktokshop.com/us/creator)
- [n8n pricing](https://n8n.io/pricing/)
- [CapCut pricing](https://www.capcut.com/pricing)
- [Claude pricing](https://claude.com/pricing)
- [FTC Disclosures 101 for social media influencers](https://www.ftc.gov/business-guidance/resources/disclosures-101-social-media-influencers)
- [IRS Self-Employed Individuals Tax Center](https://www.irs.gov/businesses/small-businesses-self-employed/self-employed-individuals-tax-center)
- [US Copyright Office: Copyright and AI](https://www.copyright.gov/ai/)
- [Net Influencer: TikTok Shop bans AI voices from promotional livestreams (2026)](https://www.netinfluencer.com/tiktok-shop-bans-ai-voices-prerecorded-audio-from-promotional-livestreams/)
