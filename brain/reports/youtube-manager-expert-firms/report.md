---
title: "Report: Fractional YouTube channel manager for RIAs, law firms and CPAs"
tags: [report, youtube-manager-expert-firms, youtube, b2b-service, regulated-verticals]
updated: 2026-09-11
hustle: youtube-manager-expert-firms
type: report
published_page: https://claude.ai/code/artifact/cbb290c3-b36d-4df0-af13-a7b9313dbf01
---

## TL;DR

- The offer: one 45-60 minute recording per month from a licensed professional (RIA advisor first, estate/business attorney second, CPA opportunistically) turned into 3 long-form episodes, 8-10 Shorts, tested titles/thumbnails, compliance-packaged for CCO or partner sign-off, plus a one-page monthly memo. Price band, skeptic-corrected: **$600-1,000/mo** for one recording; $1,200-1,500 only with a second recording or LinkedIn cutdowns. Entry product: **$150-300 thumbnail + title A/B pack** using YouTube's native Test & Compare.
- Why now: YouTube's 16 Jul 2026 clarification demonetizes "AI personas presenting as experts on health, legal, finance" content, so a real professional on camera is the safe side of the enforcement wave; Test & Compare reached every creator with Advanced Features in Dec 2025, making the packaging service measurable; Idea Decanter's Apr 2026 survey says 88% of advisors think they should make video, 52% do, the top obstacles are time (56%) and hands-on shooting/editing expertise (52%) while cost ranks last (21%), 49% track nothing, and 83% say video helped increase AUM ([Finopotamus, 8 Apr 2026](https://www.finopotamus.com/post/idea-decanter-s-2026-state-of-advisor-video-report-exposes-advisor-roadblocks-shares-best-practice)).
- Skeptic-corrected headline numbers (both skeptics weakened, neither refuted): startup ~$150 budget ($59-124 cash in month 0, see 7.1); tools $112-156/mo (working midpoint $125); first dollar 6-10 weeks (A/B pack); first retainer 2-4 months after 150-300 personalized touches (financial-services cold-email reply 1.5-4%); **16-22 h per client-month**, so **two clients is the ceiling** inside 10-15 h/wk; automation 25-40% of production time, not 58%.
- Revenue: month-6 base **$1,600** (2 x $800), conservative ~$1,000, upside $3,000; month-12 base ~$2,000 (2 x $1,000 after a proof-based price step). Effective rate $21-47/h depending on price and hours (conservative 1-client case $21-25/h, which is below a $25/h floor and is itself a demotion signal); the $35-45/h band in [[decisions/final-selection]] requires $900-1,000/mo and hours near 16 per client by month 6.
- Buyer pool is real but narrow: 16,544 SEC-registered advisers (IAA 2026 snapshot), 92.8% with 100 or fewer staff; the workable subset is SEC/state-registered RIAs with an in-house CCO, not broker-dealer reps (FINRA 2210 principal pre-approval on every retail communication until the proposed risk-based regime in Regulatory Notice 26-14 lands). Law-firm demand exists (30% of firms use video per ABA 2023; video a top channel for 52% per CallRail 2026) but solo-firm budgets are thin and FL/TX filing fees ($250 per ad in Florida from 1 Jul 2026) exclude some markets. CPA video adoption: still no data found.
- Moat is not editing (a $100/mo DIY stack replicates ~60% of the deliverable): it is the compliance packaging, segment judgment on professional-tone content, the memo a partner reads, and reliability. Sell those, not "video editing".
- Kill criteria: fewer than 3 A/B packs sold to channels clearing ~1,000 views per video on recent uploads (with Advanced Features enabled) within 8 weeks, or no RIA retainer at $800+ by month 4. Pivot: LinkedIn-cutdown add-on for the ghostwriting client base, or hand the hours to podcast clipping.
- Published one-page brief ("Channel of Record"): https://claude.ai/code/artifact/cbb290c3-b36d-4df0-af13-a7b9313dbf01 - a reader-facing compression of these three notes; source HTML kept alongside them as `page.html`. Republish from that file to keep the same URL.
- Companion notes: [[reports/youtube-manager-expert-firms/automation-stack]] (workflow, tools, prompts) and [[reports/youtube-manager-expert-firms/plan]] (week 1, 30/60/90, scripts). Research base: [[research/candidates/youtube-manager-expert-firms]], [[research/candidates/youtube-manager-expert-firms-skeptic-demand]], [[research/candidates/youtube-manager-expert-firms-skeptic-execution]].

## 1. Executive summary

**The offer.** A fractional "channel operator" retainer for one regulated professional (a fee-only RIA advisor, an estate/business/PI attorney, or a tax-planning CPA). The client records once a month (45-60 minutes, camera and screen as separate tracks, or a Riverside/Descript remote session). The operator delivers, inside 10 business days plus the client's approval cycle:

| Deliverable | Quantity per month | Notes |
|---|---|---|
| Long-form episodes (8-15 min) | 3 (Core) / 4 (Plus) | Text-based edit in Descript, chapters, lower thirds, disclaimer card |
| Shorts (9:16, captioned) | 8 (Core) / 12 (Plus) | Every caption proofread for statute/form names |
| Titles and thumbnails | 3 title + 2-3 thumbnail variants per episode | Run through YouTube Test & Compare |
| Descriptions, chapters, pinned disclaimer comment, UTM links | per episode | Drafted by Claude, human-edited for compliance |
| Compliance package | 1 per batch | Checklist + approved-version archive for the CCO/partner (SEC recordkeeping helper) |
| Monthly memo | 1 page | Three numbers, one recommendation, one ask for next recording |

**Who pays.** The firm, on a monthly retainer billed in advance by ACH. **Who watches:** prospects researching a specific problem (Social Security timing, Roth conversions, estate basics, entity choice) who arrive by search and suggested video; the business case is one signed client, never AdSense.

**Why now (2025-2026 evidence).**
- YouTube's clarified inauthentic-content policy (16 Jul 2026) names three non-monetizable buckets, the third being "AI personas presenting as experts on sensitive topics like health, legal, finance, or politics" ([TechCrunch, 20 Jul 2026](https://techcrunch.com/2026/07/20/youtube-clarifies-policies-around-ai-slop-and-upsetting-videos/); [AIR Media-Tech timeline, 2026](https://air.io/en/monetization/youtube-monetization-policy-changes-2026-a-complete-dated-timeline)). A licensed human on camera is the opposite pattern.
- Native title/thumbnail A/B testing ("Test & Compare") reached all creators with Advanced Features in Dec 2025, up to 3 variants, winner by watch time, tests end within two weeks ([YouTube Help](https://support.google.com/youtube/answer/16391400?hl=en-GB); [Gyre, 2026](https://gyre.pro/blog/youtubes-new-title-ab-testing-tool-everything-creators-need-to-know)). That makes a $150-300 packaging product provable.
- Advisor appetite versus capacity: 88% think they should make video, 52% do, 73% think it is worth the time and money, 83% say video has helped increase AUM (the pitch line), 80% spend only "a few hours a month" on it, 49% do not track results, 6% quit in the last year. Obstacles, as listed: time 56%, hands-on shooting and editing expertise 52%, fresh ideas 38%, sharing videos successfully 35%, cost 21% ([Finopotamus on Idea Decanter's 2026 report, 8 Apr 2026](https://www.finopotamus.com/post/idea-decanter-s-2026-state-of-advisor-video-report-exposes-advisor-roadblocks-shares-best-practice); [Idea Decanter 2026 report](https://ideadecanter.com/2026report/)). Vendor survey, sample size not published: treat as directional. Two implications: the number that supports outsourcing is the 52% editing-expertise gap, and because cost ranks last (21%) the objection to expect is trust/compliance, not price.

**Headline numbers (skeptic-corrected, see section 7).** Startup ~$150 budget; tools $112-156/mo (midpoint $125); first dollar 6-10 weeks; first retainer month 2-4; retainer $600-1,000; month-6 base $1,600 gross for ~10-15 h/wk (report 7.4: 10-13; plan section 8: 11-15 with the outreach that keeps running); two clients maximum.

## 2. Operator assumptions and what changes them

Baseline operator (per [[research/shortlist]]): one US person, 10-15 h/wk, under $500 capital, fluent with Claude/ChatGPT and n8n/Make, no audience, no credential, no video-editing history.

| If the operator has... | What changes |
|---|---|
| **More time (20-25 h/wk)** | Ceiling rises from 2 to 3 clients (48-66 h/mo production plus 16 h sales, per the execution skeptic); month-6 upside $3,000 becomes the base. Do not add a 4th client without templating steps 8-10 of the workflow. |
| **More money ($1,500+)** | Buy annual tool plans (Descript $24, OpusClip $174/yr, Canva $144/yr: ~$90-100/mo), a $300-500 paid Test & Compare portfolio (pay two friendly firms' filing/ad costs to get case studies), and 2-3 months of Instantly/Apollo paid tiers to lift touch volume from 25 to 60/week. Capital does not shorten the compliance cycle. |
| **Existing video-editing skill** | Per-client hours fall toward 12-14 (the dossier's original estimate), effective rate toward $50/h, and the 3-client ceiling opens. This is the single biggest lever. |
| **A finance/legal credential or network (CFP, JD, ex-paraplanner, ex-paralegal)** | Reply rates move from the 1.5-4% financial-services floor toward the 4-6% top of the range; first retainer can land in 4-8 weeks via warm intros. Also unlocks the "I understand your compliance" pitch without a learning curve. |
| **An existing audience** | Not required and not helpful for this offer; skip building one. |

## 3. Market and demand analysis

### 3.1 Buyer persona

- **Primary: fee-only RIA principal or lead advisor**, firm of 2-15 people, $100M-$1B AUM, SEC- or state-registered, in-house or outsourced CCO who approves marketing monthly. Already runs a quarterly webinar or podcast, or has a YouTube channel with fewer than one upload a month. Client LTV $5-15K/yr in fees (assumption based on 1% of $500K-$1.5M), so one client per year covers a $9,600-12,000 retainer.
- **Secondary: estate-planning, elder-law, business or PI attorney**, 1-5 lawyers, in a state without ad pre-filing fees. Marketing 9% of expenses at solo firms and 5% at small firms ([Clio 2025 Legal Trends for Solo and Small Firms](https://www.clio.com/resources/legal-trends/2025-solo-small-firm-report/); 2026 edition surveyed 1,700+ respondents, [Clio 2026](https://www.clio.com/resources/legal-trends/2026-solo-small-firm-report/)).
- **Opportunistic: CPA firm with a tax-planning/advisory line** (not compliance-only), sold in Q4 for the Jan-Apr content season.

### 3.2 Size proxies (with dates)

| Proxy | Figure | Source |
|---|---|---|
| SEC-registered investment advisers (2025) | 16,544; 92.8% employ 100 or fewer non-clerical staff; >10,500 manage <$1B; advisers focused on individuals average 8 employees and $424M AUM | [IAA 2026 Investment Adviser Industry Snapshot, Jun 2026](https://www.investmentadviser.org/wp-content/uploads/2026/06/Snapshot-2026.pdf); [Yahoo Finance summary](https://finance.yahoo.com/markets/stocks/articles/2026-investment-adviser-industry-snapshot-131500715.html) |
| Advisors making video / wanting to | 52% make video; 88% think they should; top obstacles time 56% and shooting/editing expertise 52%, cost only 21%; 49% track nothing; 83% say video helped increase AUM | [Finopotamus, 8 Apr 2026](https://www.finopotamus.com/post/idea-decanter-s-2026-state-of-advisor-video-report-exposes-advisor-roadblocks-shares-best-practice) (vendor survey, n not published) |
| Law firms using video | 30% (2023, up from 24% in 2020) | [ABA Websites & Marketing TechReport, via ABA Journal](https://www.abajournal.com/magazine/article/why-video-is-the-secret-weapon-for-lawyers-marketing) |
| Law firms naming video a top acquisition channel | 52% (CallRail 2026) | [LEXGRO, 2026](https://lexgro.com/insights/law-firm-marketing-spend-2026/) (secondary) |
| Consumers using YouTube for financial advice | 22% of Americans without an advisor (YouGov 2026, relayed); 28% of Americans who sought financial advice did so on social media (Philadelphia Fed LIFE survey 2025, relayed) | [SmartAsset, 2026](https://smartasset.com/advisor-resources/social-media-for-financial-advisors-5-ways-to-drive-business) |
| CPA firms using video | **no data found** (searched again 2026-09-11; only general "91% of businesses use video" figures, [SellersCommerce 2026](https://www.sellerscommerce.com/blog/video-marketing-statistics/)) | - |

Serviceable market arithmetic (assumption, illustrative): if 10% of the ~10,500 sub-$1B SEC advisers are individual-focused firms with an existing recording habit and a CCO who approves monthly, that is ~1,000 firms; the operator needs 2. The constraint is finding and converting them, not market size.

### 3.3 Trend direction and seasonality

- **Direction: no data found.** The demand skeptic refuted the dossier's "43% (Broadridge 2024) to 52% (Idea Decanter 2026)" comparison as two different surveys with different questions. What is verifiable is supply-side: Test & Compare (Dec 2025), YouTube's AI-persona demonetization (Jul 2026), and FINRA's proposal to move from principal pre-approval to risk-based supervision ([Regulatory Notice 26-14](https://www.finra.org/rules-guidance/notices/26-14); [Holland & Knight, Jul 2026](https://www.hklaw.com/en/insights/publications/2026/07/finra-seeks-to-modernize-rule-2210-communications-with-the-public), comment deadline 11 Sep 2026) which, if adopted, widens the buyer pool to BD-affiliated advisors in 2027.
- **Seasonality:** tax content peaks Jan-Apr ([TVREV on TurboTax](https://www.tvrev.com/news/tube-trends-how-turbotax-owns-tax-season-on-youtube)); CPAs are unavailable exactly then, so their sales window is Oct-Nov. Advisors: Q4 open enrollment and year-end planning, January "new year" estate/retirement resolutions. Law: less seasonal; estate planning spikes January and after market shocks (assumption).

### 3.4 The skeptics' corrections, stated plainly

| Dossier claim | Skeptic verdict | Corrected view used in this report |
|---|---|---|
| Retainer $800-1,500/mo | Weakened (demand): every >$1,000 benchmark is a seller's cost guide; observed anchors are $100 (Upwork post), $250/mo (Attorneys.Media), $1,200/mo full-time offshore editor | **$600-1,000/mo** for one recording; $1,200-1,500 with a second recording or LinkedIn cutdowns |
| CPAs first in the title | Weakened: zero quantitative CPA data; lead math does not close at $500-2,000 per return | **RIAs first, law second, CPAs opportunistic** |
| Trend "up" | Refuted as evidenced | "No data found"; sell on the supply-side changes instead |
| 12 h per client-month, 58% automated, 3 clients in 12-15 h/wk | Weakened (execution): talking-head editing benchmarks 20-30 min per finished minute; 20-40% of AI clips need rework | **16-22 h per client-month, 25-40% automation, two clients maximum** |
| First dollar ~30 days from 30-60 touches | Weakened: financial-services reply rates 1.5-4%, 1-3 meetings per 100 emails | **First dollar 6-10 weeks (A/B pack); first retainer 2-4 months after 150-300 touches** |
| Month-6 base $3,000 | Weakened by both | **$1,000-2,000 (use $1,600); $3,000 is the upside** |
| Tools ~$102-110/mo | Holds on list prices; weakened on limits (Descript metered media minutes, no rollover) | **$112-156/mo including n8n, top-ups and Stripe ACH fees; working midpoint $125** |
| Platform risk low | Holds (both skeptics) | Keep; never synthesize the client's face or voice |
| Compliance as a feature | Weakened as demand: it also shrinks and slows the pool (2-4 week first review, FL/TX filing fees) | Sell it, but exclude BD reps and filing-state law firms from the first cohort |
| Client time ~1 h/month | Weakened | 2-4 h/month including approvals; say so in the pitch |
| Price ladder $1,200 / $1,500 / $2,000 (execution skeptic's "what would make this hold" condition) | Not adopted for cohort one | Observed anchors are $100-250 (demand skeptic, D7: Upwork post, Attorneys.Media Tier 1), so cohort one opens at $800; the ladder is revisited at the two-proof-point price step (section 4), which is why the month-12 step to $1,000 is the base and $1,200+ is the upside. Trade-off accepted: at $800 the 7.4 rate is $26-34/h, below the $35-45/h in [[decisions/final-selection]] |

## 4. Offer design and pricing

| Package | Price | Scope | Benchmark |
|---|---|---|---|
| **A/B Pack** (entry) | $150-300 one-off (assumption inside the corrected band) | For one video on a channel that averages 1,000+ views per video across its last three uploads and has uploaded in the last 90 days (lifetime views on an old video do not generate the ~1,000-5,000 fresh impressions per variant a two-week test needs, [Gyre, 2026](https://gyre.pro/blog/youtubes-new-title-ab-testing-tool-everything-creators-need-to-know)); run on the client's next upload if no recent video qualifies; channel must have Advanced Features enabled (phone plus ID/video verification or channel history, [YouTube Help](https://support.google.com/youtube/answer/9891124?hl=en)): 3 titles + 3 thumbnails, Test & Compare set up, readout after 2 weeks with a one-page recommendation | Fiverr thumbnails avg ~$18 each ([VisualKit, 2026](https://www.visualkit.app/thumbnail-designer-cost)); agency thumbnail/packaging line items sit inside $500-1,500 "basic management" ([Centrics Media, 2026](https://centricsmedia.com/youtube-channel-management-agency-cost-in-2026/)) |
| **Core** | $800/mo (band $600-1,000) | 1 recording, 3 episodes, 8 Shorts, packaging + Test & Compare, compliance package, memo, 2 consolidated revision rounds | Basic channel management $500-1,500/mo ([Centrics](https://centricsmedia.com/youtube-channel-management-agency-cost-in-2026/)); freelance channel managers $25-100/h ([Creator Essentials](https://www.creatoressentials.com/blog/youtube-channel-manager-cost)); Attorneys.Media Tier 1 $250/mo is the low anchor a law firm will cite ([Attorneys.Media](https://attorneys.media/pricing/)) |
| **Plus** | $1,200-1,500/mo | Adds second recording or 8 LinkedIn-native cutdowns (square, different captions to avoid unoriginal-content demotion on Meta/LinkedIn), 4 episodes, 12 Shorts | Agency channel-management-only $3,000-8,000/mo ([MarketerHire, 2026](https://marketerhire.com/blog/youtube-digital-marketing-agency)); Idea Decanter packages from ~$4K to $9-40K annual ([Idea Decanter pricing](https://ideadecanter.com/video-package-pricing/)) |
| **Add-ons** | $200-250 per extra revision round; $250 pass-through per Florida ad filing; $300 one-time onboarding (waive for first two clients) | Codify revision limits: 2-3 rounds is industry standard and unbounded revisions are the top editor complaint ([OneSuite, 2026](https://onesuite.io/blog/video-editing-contract/)) |

Terms: monthly in advance, ACH via Stripe (0.8% capped at $5 versus 2.9% + $0.30 on cards, [FeeCalcPro, 2026](https://www.feecalcpro.com/blog/stripe-ach-guide/)), 30-day cancel, client responsible for regulatory approval, nothing publishes without written sign-off, all deliverables assigned to the client, 5-business-day approval SLA after month 2.

Price step: raise Core from $800 to $1,000 for new clients after two attributable results (a booked consultation from a UTM link, or a Test & Compare win with a CTR lift), which is the demand skeptic's condition for holding price above the $250 anchor.

## 5. Niche selection

| Rank | Sub-niche | Why | Evidence | Watch-outs |
|---|---|---|---|---|
| 1 | **Fee-only RIAs doing retirement / Social Security / Roth content for pre-retirees** | Highest LTV per lead; SEC-registered with a CCO who can approve monthly; the outlier channels (Felix, Sajdak, Carroll) are all in this content lane | 16,544 SEC advisers, >10,500 under $1B AUM ([IAA 2026](https://www.investmentadviser.org/wp-content/uploads/2026/06/Snapshot-2026.pdf)); Ben Felix/PWL: 427K subs, ~1,100 inbound leads/yr, YouTube the #2 lead source, channel cited in the OneDigital acquisition ([Vidpros, 2026](https://vidpros.com/video-marketing-for-financial-advisors/)) | Lowest cold-email reply rates of any vertical (1.5-4%); year-1 channel yields 3-8 leads at the Felix ratio (demand skeptic arithmetic), so sell a 12-month horizon |
| 2 | **Niche-specialist advisors (physicians, tech equity comp, federal employees)** | Search intent is specific and low-competition; clients are high-income; these advisors already write content | Same regulatory profile as #1; specificity raises watch time, which is what Test & Compare optimizes ([YouTube Help](https://support.google.com/youtube/answer/16391400?hl=en-GB)) | Smaller total audience per topic; fewer firms to prospect |
| 3 | **Estate-planning and elder-law firms (1-5 attorneys) in non-filing states** | Evergreen educational topics, seniors watch long-form, matter values $3-10K+ (assumption); ABA 7.1/7.2 rules are lighter than SEC review | 30% of firms use video ([ABA 2023 via ABA Journal](https://www.abajournal.com/magazine/article/why-video-is-the-secret-weapon-for-lawyers-marketing)); marketing 5-9% of expenses at small/solo firms ([Clio 2025](https://www.clio.com/resources/legal-trends/2025-solo-small-firm-report/)) | Florida $250/ad timely, $750 late from 1 Jul 2026 ([The Florida Bar](https://www.floridabar.org/ethics/etad/)); Texas filing within 10 days; exclude FL/TX in cohort one |
| 4 | **Business / tax attorneys and boutique PI firms** | PI has the highest matter value; business law overlaps CPA topics (entity choice, 1031) | Video a top acquisition channel for 52% of firms ([LEXGRO/CallRail 2026](https://lexgro.com/insights/law-firm-marketing-spend-2026/)) | PI is the most ad-regulated practice area and the most agency-served (Esquire Interactive, Attorneys.Media); expect the $250/mo anchor |
| 5 | **CPA firms with an advisory/tax-planning line** | Tax season search volume is enormous and evergreen; busy-season "we run it while you cannot" pitch | TurboTax content reaches 100M+ unique US viewers per tax-season month ([TVREV](https://www.tvrev.com/news/tube-trends-how-turbotax-owns-tax-season-on-youtube)) | **No adoption or spend data found**; lead value too low for compliance-only shops; sell only Oct-Nov, only to firms already publishing |

**Recommended starting niche: #1, fee-only RIAs producing retirement-planning content**, with #2 as the same outreach list filtered by specialty. Reasoning: only this buyer has (a) a client LTV that makes 3-8 year-1 leads pay for the retainer, (b) an in-house approver who can hold a monthly cadence, (c) named 2025-2026 proof points to put in the pitch, and (d) an existing habit (webinars, podcasts) that supplies the monthly recording. Law firms are the second list because their compliance is lighter but their budgets and anchors are lower; CPAs get 20 outbound touches in October as a test and nothing else until data exists.

## 6. Competitive landscape and positioning

**Who the client compares you with (2025-2026):**

| Layer | Examples | Price | What they do |
|---|---|---|---|
| Vertical specialist agencies | Idea Decanter (remote production + annual advisor report), YT Era (advisor YouTube growth), Vireo Video (case study: +762% subs for a wealth firm, Sep 2023-Jan 2025), Attorneys.Media, Esquire Interactive, Madison Media | Idea Decanter ~$4K to $9-40K/yr; Attorneys.Media $250/mo Tier 1; most others $1,500-5,000/mo | Production days, strategy, some editing; rarely month-to-month ops with compliance packaging |
| Generalist agencies | "Channel management only" | $3,000-8,000/mo ([MarketerHire, 2026](https://marketerhire.com/blog/youtube-digital-marketing-agency)); basic $500-1,500 ([Centrics, 2026](https://centricsmedia.com/youtube-channel-management-agency-cost-in-2026/)) | Volume editing, not vertical fluency |
| Marketplace freelancers | Upwork channel managers $300 setup to $8,000+/mo ([Upwork hire page, Aug 2026](https://www.upwork.com/hire/youtube-channel-managers/)); Fiverr gigs $25-990; a $100 fixed-price "channel manager" post (Feb 2026) | $100-1,200/mo | Hands, no compliance, 400-750 proposals per job |
| DIY stack | Descript $35 + OpusClip $29 + Canva $18 + Claude $20 + free Test & Compare | ~$100/mo | Replicates ~60% of the deliverable (demand skeptic) if a coordinator has the hours |

**What the 2025-2026 winners do differently (real examples):**
- **Ben Felix / PWL Capital**: weekly, research-grade, one consistent face; the channel became a line item in the OneDigital acquisition and generates ~1,100 leads/yr ([Vidpros, 2026](https://vidpros.com/video-marketing-for-financial-advisors/)). Lesson: cadence and a single on-camera expert, not production value.
- **Law by Mike (Mike Mandell)**: started on TikTok in Nov 2020 to generate cases after COVID; broke out with "what to say when police pull you over"; ~19.7M YouTube subscribers ([HypeAuditor, Sep 2026](https://hypeauditor.com/youtube/UCKmmERguliWTynG9OIoDhDw/); [Social Blade](https://socialblade.com/youtube/handle/lawbymike); background from [Vidpros lawyer channels, 2026](https://vidpros.com/top-youtube-channels-for-lawyers/) and [Rankings.io, 2026](https://rankings.io/blog/youtube-lawyers/)). Lesson: everyday-situation hooks, short-form as discovery, long-form for trust.
- **Safeguard Wealth Management / Eric Sajdak** and **Carroll Advisory Group**: Social Security and retirement-tax topics, hundreds of thousands of subscribers, AUM growth attributed to YouTube ([YT Era](https://ytera.com/advisor-growth-lab-report/youtube-cited-as-key-driver-in-597m-ria-acquisition); [Paladin](https://blog.paladindigitalmarketing.com/the-ultimate-guide-to-creating-a-financial-advisor-youtube-channel)). All anecdotal, vendor-relayed. Lesson: topic selection by search intent (specific rules, ages, thresholds) beats "market update" content.

**Your angle:** "We run your channel the way your CCO wants it run." Concretely: (1) a compliance package per batch (checklist, approved-version archive, disclaimer placements) that doubles as the adviser's Marketing Rule books-and-records support ([Smarsh on 2026 SEC expectations](https://www.smarsh.com/blog/thought-leadership/sec-marketing-rule-faqs-2026-compliance-guidance/)); (2) editorial restraint (no influencer jump-cuts, no "guaranteed", no performance claims); (3) a memo with three numbers a partner will read; (4) Test & Compare results as proof every month; (5) one recording, one approval batch, nothing published without sign-off.

**Why a beginner can still win:** the specialists are priced 2-10x higher and sell production, the marketplace layer cannot spell the client's compliance vocabulary, and the DIY stack fails on consistency (time is the top obstacle for 56% and hands-on editing expertise for 52%; 80% give it "a few hours a month"; cost, at 21%, is the smallest obstacle, so the sale is trust and compliance, not price). The skill that decides retention, segment judgment plus a partner-readable memo, is learnable in 1-2 months and is not what Upwork sellers compete on. The absence of a visible solo operator at $600-1,000 is a gap the demand skeptic notes may also mean "solo players cannot sustain it" - the 8-week A/B-pack test in [[reports/youtube-manager-expert-firms/plan]] resolves that before real money is spent.

## 7. Unit economics

### 7.1 Startup costs (month 0)

| Item | Cost | Source / note |
|---|---|---|
| Descript Hobbyist, 1 month (10 media hours, 400 AI credits, no watermark; Free is 60 media minutes with 720p watermarked exports, so it cannot hold two 45-60 min portfolio webinars) | $24 | [Sonix, 2026](https://sonix.ai/resources/descript-pricing/); [Castmagic, 2026](https://www.castmagic.io/blog/descript-pricing); [fluxnote, 2026](https://fluxnote.io/guides/descript-pricing-2026). Step up to Creator $35 in the first client month |
| OpusClip Starter, 1 month (150 credits, no watermark) or Free (60 credits, watermarked; trim Shorts in CapCut instead) | $0-15 | [Creatify, 2026](https://creatify.ai/blog/opusclip-pricing-plans-and-what-you-ll-actually-pay-in-2026); [eesel, 2026](https://www.eesel.ai/blog/opusclip-pricing). Step up to Pro $29 at first client |
| Canva Free (Pro $18 at first client) | $0 | [usecarly, 2026](https://www.usecarly.com/blog/canva-pricing/) |
| Claude Pro, 1 month | $20 | [SSD Nodes, Aug 2026](https://www.ssdnodes.com/learn/claude-pro-price-and-limits) |
| Domain + one-page site (Carrd free tier or similar + domain) | $15-25 | assumption |
| Portfolio: two public-domain US federal recordings (IRS Video Portal or SSA retirement video for the financial sample; a federal legal-education recording for the legal sample) re-edited into sample episodes and Shorts, labeled "sample re-edit, not a client" | $0 (time, ~10 h) | Federal works are public domain under [17 U.S.C. 105](https://www.law.cornell.edu/uscode/text/17/105) ([USAGov](https://www.usa.gov/government-copyright)); sources: [IRS Video Portal](https://www.irsvideos.gov/), [SSA YouTube channel, videos "produced at U.S. taxpayer expense" (SSA blog, 18 Aug 2026)](https://www.ssa.gov/blog/en/posts/2026-08-18.html); see [[reports/youtube-manager-expert-firms/plan]] section 1 |
| Business basics: state LLC optional ($50-300, defer), free EIN, Stripe/Wave, free e-sign | $0 in month 0 | assumption; see [[reports/youtube-manager-expert-firms/plan]] |
| Optional USB mic for Loom proposals | $0-40 | assumption |
| **Total** | **$59-124 cash in month 0; budget $150** | The ~$25-50 remainder funds the Descript Creator / OpusClip Pro / Canva Pro step-up (+$43/mo) in the first client month, so the plan's "paid tiers at first client" line and this table agree; holds per execution skeptic; add $250/ad Florida filing exposure only if a FL law firm is signed |

### 7.2 Monthly tool costs (steady state, monthly billing)

| Tool | Monthly | Annual-billing equivalent | Limits that matter |
|---|---|---|---|
| Descript Creator | $35 | $24 | 30 media hours/mo (all uploads count, no rollover), 800 AI credits, top-ups expire in 12 months ([Sonix](https://sonix.ai/resources/descript-pricing/); [Shade, 2026](https://shade.inc/blog/descript-pricing)) |
| OpusClip Pro | $29 | $14.50 ($174/yr) | 300 credits, 1 credit per source minute; 2 clients x ~60 min plus re-runs fits ([eesel, 2026](https://www.eesel.ai/blog/opusclip-pricing)) |
| Canva Pro | $18 | $12 ($144/yr) | AI-use caps per month ([usecarly](https://www.usecarly.com/blog/canva-pricing/)) |
| Claude Pro | $20 | $17 | Rolling 5-hour windows; long transcripts can hit limits ([SSD Nodes](https://www.ssdnodes.com/learn/claude-pro-price-and-limits)) |
| n8n | $0 self-hosted or $24 Cloud Starter (2,500 executions) | $20 | [No Code MBA, 2026](https://www.nocode.mba/articles/n8n-pricing) |
| Descript top-ups / OpusClip re-processing allowance | $0-20 | - | assumption (execution skeptic flags metered minutes) |
| Stripe ACH fees at $1,600/mo | ~$10 | - | 0.8% capped at $5 per payment ([FeeCalcPro](https://www.feecalcpro.com/blog/stripe-ach-guide/)) |
| **Total** | **$112-156** (self-hosted n8n and no top-ups = $112; Cloud Starter plus $20 top-ups = $156; **working midpoint $125**, used in 7.4) | **~$78-118** | Buy annual plans only after the first retainer is paid. The same range is used in [[reports/youtube-manager-expert-firms/automation-stack]] section 3 |

### 7.3 Revenue scenarios (gross, per month)

Assumptions (explicit): 20-30 personalized touches per week from week 2; reply rate 2-4% ([Instantly 2026 benchmark report](https://instantly.ai/cold-email-benchmark-report-2026): 3.43% average; [Reachoutly, 2026](https://reachoutly.com/cold-email/response-rate/): financial services 1.5-3.5%); meetings 1-3 per 100 emails; close 20-30% of meetings (assumption); A/B pack sells ~1 per 50-75 touches to firms already uploading (assumption); Core retainer $800 in months 1-6, $1,000 for new clients after two proof points; churn: one client lost per ~9-12 months (retainer-model agency churn 18%/yr, sub-$1M agencies 32%/yr, [Focus Digital, 2026](https://focus-digital.co/average-marketing-agency-churn/)); no paid ads; no marketplace fees.

| Month | Conservative | Base | Upside |
|---|---|---|---|
| 1 | $0 (setup, portfolio, first 50-75 touches) | $0 | $250 (one A/B pack from a warm contact) |
| 3 | $0-250 (0-1 packs) | $250-500 (1-2 packs) or first Core at $800 starting late month 3 | $800 Core + $250 pack = $1,050 |
| 6 | ~$1,000 (1 x $800 + occasional pack) | **$1,600** (2 x $800) | $3,000 (2 x $1,200 Plus + packs, or 3 x $1,000 if hours allow) |
| 12 | $800-1,000 (1 client, price stepped) | **~$2,000** (2 x $1,000 after price step, one churn replaced) | $3,000-3,400 (2 x $1,500 Plus with LinkedIn cutdowns + $400 packs) |

Months 1-3 are the demand skeptic's "0-1 retainer" window; the base case therefore books its first retainer at the end of month 3 or in month 4.

### 7.4 Hours, effective hourly rate, break-even

| Scenario (month 6) | Production hours | Sales/admin hours | Total h/mo (h/wk) | Net after $125 tools (7.2 midpoint) | Effective rate |
|---|---|---|---|---|---|
| Conservative: 1 client at $800 + ~1 A/B pack/mo (~$200) = $1,000 gross (the 7.3 conservative case) | 16-22 client + ~3 pack | 16 (still prospecting) | 35-41 (8-10) | $875 | $21-25/h |
| Base: 2 clients at $800 | 32-44 | 12 | 44-56 (10-13) | $1,475 | **$26-34/h** |
| Base, priced at $1,000 and templated to 16 h/client | 32 | 8 | 40 (9-10) | $1,875 | **$47/h** |
| Upside: 3 clients at $1,000 | 48-66 | 16 | 64-82 (15-19, over budget) | $2,875 | $35-45/h |

The conservative case sits at or below a $25/h floor; if that is where month 6 lands, it is itself a demotion signal (kill criterion 3 in section 9), not a holding pattern.

Reconciliation with [[decisions/final-selection]]: the "$35-45/h" figure there is the execution skeptic's arithmetic on the dossier's 3-client base; at the corrected 2-client, $800 base the honest number is $26-34/h, rising to ~$47/h only when price reaches $1,000 and per-client hours fall to 16. The plan's 90-day gate therefore checks hours per client, not only revenue.

Break-even: tools ($112-156/mo) are covered by one A/B pack a month; the $75-125 month-0 spend is recovered by the first pack. Cash break-even on time (at a $30/h opportunity cost, assumption) needs two Core clients. Do not buy annual plans, paid outreach tools or an LLC before the first retainer clears.

## 8. Risks and mitigations

| Risk | Likelihood / impact | Evidence | Mitigation |
|---|---|---|---|
| **YouTube policy: inauthentic content / AI personas** | Low / high for the client | 16 Jul 2026 clarification targets generic-repetitive, off-putting, and AI-persona-expert content; "clarification, not an AI ban" ([TechCrunch, Jul 2026](https://techcrunch.com/2026/07/20/youtube-clarifies-policies-around-ai-slop-and-upsetting-videos/); [OutlierKit, Jul 2026](https://outlierkit.com/blog/youtube-updates-july-2026)) | Real professional on camera only; never AI avatars, AI voice, or AI-written scripts read by a synthetic presenter; original human framing in every episode |
| **AI disclosure / likeness detection** | Low | Disclosure required only for realistic altered content; May 2026 auto-detection targets photorealistic synthetic media; AI thumbnails and editing are production assistance ([minimatters, 2026](https://minimatters.com/youtube-altered-or-synthetic-content-disclosure/); [AIR Media-Tech, 2026](https://air.io/en/youtube-hacks/youtube-ai-policy-2026-likeness-detection-and-the-no-fakes-act-what-creators-need-to-know)) | Never synthesize the client's face or voice; non-photoreal AI backgrounds only; keep the disclosure toggle "No" and document why |
| **AI-quality failure (mis-cut clips, mis-transcribed statutes)** | High / medium | ~38% of OpusClip clips needed work in one 76-clip test; Descript 92-95% on proper nouns (execution skeptic relaying 2026 reviews) | Human fix pass on every Short; jargon glossary per client fed to Descript/Claude; separate camera + screen tracks required in the contract |
| **Saturation / DIY substitution** | Medium-high / medium | DIY stack ~$100/mo replicates ~60%; Upwork Q2 2026 GSV -4%, Fiverr buyers -14 to -22% (demand skeptic); YouTube Studio Inspiration tab already suggests titles and thumbnails ([YouTube Help](https://support.google.com/youtube/answer/15575509?hl=en)) | Sell compliance, judgment, memo and reliability; re-price toward $600-800 if YouTube ships native long-to-Shorts auto-clipping for all creators (open risk, no data found) |
| **SEC Marketing Rule (RIA clients)** | Medium / high | All produced content is the adviser's advertisement by entanglement/adoption; FAQs updated 15 Jan 2026; firms must capture, retain and reproduce marketing as used with approvals ([Mayer Brown, Jan 2026](https://www.mayerbrown.com/en/insights/publications/2026/01/sec-staff-publishes-new-marketing-rule-faqs); [Smarsh, 2026](https://www.smarsh.com/blog/thought-leadership/sec-marketing-rule-faqs-2026-compliance-guidance/)) | Contract: client owns regulatory approval; nothing publishes without written sign-off; archive approved versions; no testimonials, no performance claims, no "guaranteed" |
| **FINRA 2210 (BD reps)** | High friction / medium | Principal pre-approval for retail communications to >25 retail investors in 30 days; 14-16 items per client-month; RN 26-14 proposes risk-based supervision (comments due 11 Sep 2026) ([FINRA RN 26-14](https://www.finra.org/rules-guidance/notices/26-14); [Improvado, 2026](https://improvado.io/blog/finra-2210)) | Exclude BD-affiliated advisors from cohort one; revisit in 2027 if the proposal is adopted |
| **State-bar ad rules (law clients)** | Medium / medium | Florida $250 per timely filing, $750 late, from 1 Jul 2026 ([The Florida Bar](https://www.floridabar.org/ethics/etad/)); Texas 10-day filing; ABA 7.1/7.2 | Non-filing states only in cohort one; "Attorney Advertising" label on screen, in description, on embed page; educational-content exemption checked per state before quoting |
| **FTC testimonials rule** | Low / high | Fake/AI-generated testimonials banned since 21 Oct 2024 with civil penalties ([FTC](https://www.ftc.gov/news-events/news/press-releases/2024/08/federal-trade-commission-announces-final-rule-banning-fake-reviews-testimonials)) | No fabricated success stories; client testimonials on advisor channels also trigger SEC testimonial disclosures |
| **Copyright of AI output** | Low / low | Fully AI-generated output not copyrightable; human-authored elements are (US Copyright Office Part 2, Jan 2025, via [Skadden](https://www.skadden.com/insights/publications/2025/02/copyright-office-publishes-report)) | Assign all deliverables to the client; do not promise exclusivity on AI backgrounds |
| **Data / privacy** | Low / medium | Client recordings may contain client names (advisor case discussions) | Contract clause: client scrubs identifying details before recording; Drive folder per client, delete raw files 90 days after approval |
| **Payments / chargebacks** | Low / medium | Services are chargeback-exposed on cards; ACH 0.8% capped $5, $15 dispute fee ([FeeCalcPro](https://www.feecalcpro.com/blog/stripe-ach-guide/)) | ACH invoices in advance, 30-day cancel, written scope; Stripe does not restrict marketing services |
| **Tool dependency** | Medium / low | Descript metered minutes since Sep 2025; OpusClip credits; Canva price rose $12.99 to $18 | Keep raw files and transcripts in Drive; CapCut/DaVinci as fallback editors; monthly billing until proven |
| **Sales tax on digital services** | Unknown / low | 30+ states tax some digital products; treatment of editing services delivered as files: no data found (execution skeptic) | Check home-state rule before first invoice; price "plus applicable tax" |
| **Client-side "too cumbersome" churn** | Medium / high | 6% of advisors quit video in the last year for no value or burden; 2-4 h/month of partner/CCO time is realistic | One recording, one approval batch, memo with an attributable number every month; UTM + booking-link tracking set up in onboarding |

## 9. Kill criteria and pivot options

**Kill / demote triggers (from [[decisions/final-selection]], refined):**
1. Fewer than 3 A/B packs sold to channels clearing ~1,000 views per video on recent uploads (last three videos, uploaded within 90 days, Advanced Features enabled) within 8 weeks of the first outbound send.
2. No RIA (or law) retainer at $800+ by the end of month 4 after 300+ personalized touches.
3. Two retainers running but per-client hours still above 22 at month 6 (the economics do not work at $800 and 22 h).
4. YouTube ships native long-form-to-Shorts auto-clipping plus AI titles/thumbnails for all creators and two prospects cite it as the reason not to buy: re-price to $600-800 immediately; if that fails to close inside 60 days, demote.

**Pivot options, in order:**
- **LinkedIn-cutdown add-on for ghostwriting clients** ([[research/candidates/linkedin-founder-ghostwriting]]): same recording, square clips, no YouTube channel to manage; reuses the stack at ~4 h/client-month.
- **Compliance-and-packaging micro-offer** ($300-500/mo): titles, thumbnails, descriptions, disclaimer placement and the memo for firms that already have an editor; no editing hours.
- **Podcast clipping retainer** ([[research/candidates/podcast-clipping-retainer]]): the designated portfolio alternate; same tools, lower price, faster first dollar.
- **White-label editing for a vertical specialist agency** (Idea Decanter, YT Era, Vireo): trade margin for zero acquisition cost if outbound fails but delivery quality is proven.

## Sources

Platform policy and features
- [TechCrunch: YouTube clarifies policies around AI slop and upsetting videos (20 Jul 2026)](https://techcrunch.com/2026/07/20/youtube-clarifies-policies-around-ai-slop-and-upsetting-videos/)
- [AIR Media-Tech: YouTube monetization policy changes 2026, dated timeline](https://air.io/en/monetization/youtube-monetization-policy-changes-2026-a-complete-dated-timeline)
- [OutlierKit: YouTube updates July 2026](https://outlierkit.com/blog/youtube-updates-july-2026)
- [YouTube Help: A/B test titles and thumbnails (Test & Compare)](https://support.google.com/youtube/answer/16391400?hl=en-GB)
- [Gyre: YouTube's title A/B testing tool in 2026](https://gyre.pro/blog/youtubes-new-title-ab-testing-tool-everything-creators-need-to-know)
- [YouTube Help: Explore Inspiration tab](https://support.google.com/youtube/answer/15575509?hl=en)
- [YouTube Help: Get access to intermediate and advanced features](https://support.google.com/youtube/answer/9891124?hl=en)
- [minimatters: YouTube altered or synthetic content disclosure policy 2026](https://minimatters.com/youtube-altered-or-synthetic-content-disclosure/)
- [AIR Media-Tech: YouTube AI policy 2026, likeness detection and the NO FAKES Act](https://air.io/en/youtube-hacks/youtube-ai-policy-2026-likeness-detection-and-the-no-fakes-act-what-creators-need-to-know)
- [YouTube Help: Channel permissions do not provide API access](https://support.google.com/youtube/answer/9367690?hl=en)

Demand and market size
- [Finopotamus: Idea Decanter 2026 State of Advisor Video Report (Apr 2026)](https://www.finopotamus.com/post/idea-decanter-s-2026-state-of-advisor-video-report-exposes-advisor-roadblocks-shares-best-practice)
- [Idea Decanter: State of Advisor Video Report 2026](https://ideadecanter.com/2026report/)
- [Idea Decanter: The State of Advisor Video Report 2026 (landing page)](https://ideadecanter.com/the-state-of-advisor-video-report-2026/)
- [IAA: Investment Adviser Industry Snapshot 2026 (Jun 2026)](https://www.investmentadviser.org/wp-content/uploads/2026/06/Snapshot-2026.pdf)
- [Yahoo Finance: 2026 Investment Adviser Industry Snapshot summary](https://finance.yahoo.com/markets/stocks/articles/2026-investment-adviser-industry-snapshot-131500715.html)
- [ABA Journal: Why video is the secret weapon for lawyers' marketing (ABA TechReport 30%)](https://www.abajournal.com/magazine/article/why-video-is-the-secret-weapon-for-lawyers-marketing)
- [Clio: 2025 Legal Trends for Solo and Small Law Firms](https://www.clio.com/resources/legal-trends/2025-solo-small-firm-report/)
- [Clio: 2026 Legal Trends for Solo and Small Law Firms](https://www.clio.com/resources/legal-trends/2026-solo-small-firm-report/)
- [LEXGRO: Law firm marketing spend 2026 (CallRail 52%)](https://lexgro.com/insights/law-firm-marketing-spend-2026/)
- [SmartAsset: Social media for financial advisors (YouGov 22%, Philadelphia Fed 28%)](https://smartasset.com/advisor-resources/social-media-for-financial-advisors-5-ways-to-drive-business)
- [SellersCommerce: Video marketing statistics 2026](https://www.sellerscommerce.com/blog/video-marketing-statistics/)
- [TVREV: How TurboTax owns tax season on YouTube](https://www.tvrev.com/news/tube-trends-how-turbotax-owns-tax-season-on-youtube)

Case studies and competitors
- [Vidpros: Video-first marketing playbook for financial advisors 2026 (Ben Felix / PWL)](https://vidpros.com/video-marketing-for-financial-advisors/)
- [Vidpros: Best lawyer YouTube channels 2026 (Law by Mike)](https://vidpros.com/top-youtube-channels-for-lawyers/)
- [Rankings.io: 20 best YouTube channels for lawyers 2026](https://rankings.io/blog/youtube-lawyers/)
- [HypeAuditor: Law By Mike YouTube stats (19.66M subscribers, Sep 2026)](https://hypeauditor.com/youtube/UCKmmERguliWTynG9OIoDhDw/)
- [Social Blade: Law By Mike](https://socialblade.com/youtube/handle/lawbymike)
- [YT Era: YouTube cited as key driver in $597M RIA acquisition](https://ytera.com/advisor-growth-lab-report/youtube-cited-as-key-driver-in-597m-ria-acquisition)
- [Paladin Digital Marketing: Financial advisor YouTube channel guide](https://blog.paladindigitalmarketing.com/the-ultimate-guide-to-creating-a-financial-advisor-youtube-channel)
- [Idea Decanter: Video package pricing](https://ideadecanter.com/video-package-pricing/)
- [Attorneys.Media: Pricing](https://attorneys.media/pricing/)
- [MarketerHire: YouTube digital marketing agency pricing 2026](https://marketerhire.com/blog/youtube-digital-marketing-agency)
- [Centrics Media: YouTube channel management agency cost 2026](https://centricsmedia.com/youtube-channel-management-agency-cost-in-2026/)
- [Creator Essentials: YouTube channel manager cost](https://www.creatoressentials.com/blog/youtube-channel-manager-cost)
- [Upwork: Freelance YouTube channel managers for hire (Aug 2026)](https://www.upwork.com/hire/youtube-channel-managers/)
- [VisualKit: Thumbnail designer cost 2026](https://www.visualkit.app/thumbnail-designer-cost)
- [OneSuite: Video editing contract template 2026 (revision rounds)](https://onesuite.io/blog/video-editing-contract/)
- [Focus Digital: Average marketing agency churn 2026](https://focus-digital.co/average-marketing-agency-churn/)

Outreach benchmarks
- [Instantly: Cold email benchmark report 2026 (3.43% average reply)](https://instantly.ai/cold-email-benchmark-report-2026)
- [Reachoutly: Cold email response rate 2026 (financial services 1.5-3.5%)](https://reachoutly.com/cold-email/response-rate/)
- [Cleverly: Cold email benchmarks by industry](https://www.cleverly.co/blog/cold-email-benchmarks-by-industry)

Tools and payments
- [Sonix: Descript pricing 2026](https://sonix.ai/resources/descript-pricing/)
- [Shade: Descript pricing 2026, media minutes and AI credits](https://shade.inc/blog/descript-pricing)
- [Castmagic: Descript pricing 2026, free plan limits (60 media minutes, watermarked 720p)](https://www.castmagic.io/blog/descript-pricing)
- [fluxnote: Descript pricing 2026 (Hobbyist $24, 10 media hours, 400 AI credits)](https://fluxnote.io/guides/descript-pricing-2026)
- [Creatify: OpusClip pricing 2026](https://creatify.ai/blog/opusclip-pricing-plans-and-what-you-ll-actually-pay-in-2026)
- [eesel: OpusClip pricing 2026](https://www.eesel.ai/blog/opusclip-pricing)
- [usecarly: Canva pricing 2026](https://www.usecarly.com/blog/canva-pricing/)
- [SSD Nodes: Claude Pro price and limits (Aug 2026)](https://www.ssdnodes.com/learn/claude-pro-price-and-limits)
- [No Code MBA: n8n pricing 2026](https://www.nocode.mba/articles/n8n-pricing)
- [FeeCalcPro: Stripe ACH fees 2026](https://www.feecalcpro.com/blog/stripe-ach-guide/)

Regulation
- [Mayer Brown: SEC staff publishes new Marketing Rule FAQs (Jan 2026)](https://www.mayerbrown.com/en/insights/publications/2026/01/sec-staff-publishes-new-marketing-rule-faqs)
- [Smarsh: SEC Marketing Rule FAQs 2026, what compliance teams need to know](https://www.smarsh.com/blog/thought-leadership/sec-marketing-rule-faqs-2026-compliance-guidance/)
- [FINRA: Regulatory Notice 26-14 (Rule 2210 modernization)](https://www.finra.org/rules-guidance/notices/26-14)
- [Holland & Knight: FINRA seeks to modernize Rule 2210 (Jul 2026)](https://www.hklaw.com/en/insights/publications/2026/07/finra-seeks-to-modernize-rule-2210-communications-with-the-public)
- [Improvado: FINRA 2210 compliance guide 2026](https://improvado.io/blog/finra-2210)
- [The Florida Bar: Advertising regulation (fees from 1 Jul 2026)](https://www.floridabar.org/ethics/etad/)
- [FTC: Final rule banning fake reviews and testimonials (Aug 2024)](https://www.ftc.gov/news-events/news/press-releases/2024/08/federal-trade-commission-announces-final-rule-banning-fake-reviews-testimonials)
- [Skadden: Copyright Office report on AI-generated materials (Feb 2025)](https://www.skadden.com/insights/publications/2025/02/copyright-office-publishes-report)
- [17 U.S.C. 105: US Government works are not subject to copyright (Cornell LII)](https://www.law.cornell.edu/uscode/text/17/105)
- [USAGov: Copyright and federal government materials](https://www.usa.gov/government-copyright)
- [IRS Video Portal (webinars and presentations)](https://www.irsvideos.gov/)
- [SSA blog: 5 Social Security YouTube videos everyone should see (18 Aug 2026)](https://www.ssa.gov/blog/en/posts/2026-08-18.html)

Vault
- [[research/candidates/youtube-manager-expert-firms]], [[research/candidates/youtube-manager-expert-firms-skeptic-demand]], [[research/candidates/youtube-manager-expert-firms-skeptic-execution]], [[decisions/final-selection]], [[reports/youtube-manager-expert-firms/automation-stack]], [[reports/youtube-manager-expert-firms/plan]]

Evidence note: as in every prior session, every direct page fetch (techcrunch.com, finopotamus.com, support.google.com, investmentadviser.org, gyre.pro, unipile.com) was blocked by the egress proxy on 2026-09-11; figures are as relayed in search-result summaries of the linked pages (28 searches in the drafting session, 10 more in the review-fix pass) and should be re-verified against primary text before contracts are signed. Review-fix pass (2026-09-11): the Idea Decanter obstacle figures were corrected (time 56%, editing expertise 52%, cost 21%; 83% AUM), Law by Mike updated to ~19.7M, tool-cost and hourly-rate arithmetic reconciled with the companion notes, and the A/B pack re-qualified on recent-upload velocity plus Advanced Features.
