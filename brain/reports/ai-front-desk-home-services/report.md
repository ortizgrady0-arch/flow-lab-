---
title: "Report: Inbound AI front desk for 1-5-truck HVAC, plumbing and electrical shops"
tags: [report, ai-front-desk-home-services, home-services, voice-ai, mrr]
updated: 2026-09-11
hustle: ai-front-desk-home-services
type: report
---

# Report: Inbound AI front desk for 1-5-truck HVAC, plumbing and electrical shops

Business report for the conditional third finalist in [[decisions/final-selection]]. Built on the dossier [[research/candidates/ai-front-desk-home-services]] and its two skeptic notes ([[research/candidates/ai-front-desk-home-services-skeptic-demand]], [[research/candidates/ai-front-desk-home-services-skeptic-execution]]). Companion notes: [[reports/ai-front-desk-home-services/automation-stack]] (how it runs) and [[reports/ai-front-desk-home-services/plan]] (what to do, day by day).

## TL;DR

- **Offer:** a per-shop AI phone receptionist on Retell + Twilio + n8n that answers after-hours and overflow calls, triages the trade emergency, books into the shop's calendar or CRM, texts back missed calls, alerts the owner, and emails a weekly "jobs recovered" report. Sold locally, inbound-only, at **$149-249/mo + $250-500 setup** (skeptic-corrected from the dossier's $199-499 + up to $1,000).
- **Why now:** the trades are being sold AI answering by 15+ SaaS vendors, four field-service suites (Jobber $29 add-on, Housecall Pro CSR AI, Workiz ~$200 add-on, ServiceTitan) and a $1B-valuation entrant (Avoca, $125M+ raised across Seed/A/B, Apr 2026, ~$1,000-3,000/mo). The wedge is the 1-5-truck shop that is on none of those suites and will not self-configure a SaaS trial; the operator is the local human who makes it work.
- **Demand is real but smaller than the headline:** the 62% missed-call figure is a vendor relay of ServiceTitan; CallRail's 1.1M-lead dataset says 14% for home services. New this session: ServiceTitan's own State of the Trades puts residential HVAC *off-hours* call share at 9.8% (Oct) to 14.1% (Jun 2025), not the 47% vendors cite. Plan on the pilot shop's carrier log, not any of these.
- **Unit economics hold and are better than the dossier said:** ~110 billable minutes per shop per month at $0.11-0.15/min on Retell = $12-17 platform cost; all-in variable **$30-45/shop incl. Stripe fees (~$20-35 before payment fees)**; **~77-85% gross margin at $199 before operator time**. Startup ~$150, fixed overhead ~$50/mo.
- **Revenue is the weak leg:** first dollar at ~day 35-60 in the plan's base ramp (skeptics: 60-90 days if pilot 1 slips); month-3 base **2 shops, $398 MRR** (the minimum that clears the day-60 kill gate); month-6 base **$250-750 MRR** (3 shops x $199 = ~$600), upside ~$1,300; month-12 base ~$1,000 MRR only if one new shop a month offsets churn, and only if churn stays <=10%/mo (the vendor-claimed 15-25%/mo would need the upside acquisition rate just to stand still). Implied hourly ~$9-10/hr at month 6 base (demand skeptic: $10-15).
- **The only documented beginner attempt (ClawOps, Feb-Mar 2026) made $0** after 4-16 contacts and zero replies, pitching $2-3k setup + $400-500/mo by email. The corrected plan is local, in-person, cheaper, and counts *replies* not touches.
- **Recommended starting niche:** residential plumbing and drain shops (year-round emergencies, $57 LSA cost per lead, $1,714 average ticket, 127k US firms), adding HVAC in Feb-Apr ahead of the June after-hours spike. Electrical is third (251k firms but a scheduled, not emergency, call mix).
- **Kill criterion (binding):** fewer than 2 paying shops after 60 days of 30+ local touches/week, or pilot transcripts under ~80% correct intake; on kill, swap to [[research/candidates/podcast-clipping-retainer]] per [[decisions/final-selection]].

## 1. Executive summary

**The offer.** "Never miss a job call again": a trade-specific AI receptionist that picks up when the shop does not (after hours, on the job, second line ringing), captures name/address/problem/urgency, applies the shop's rules (service area, no-heat/no-cool/burst-pipe escalation, gas-smell safety script), books a window into Google Calendar/Jobber/Housecall Pro, sends the caller a confirmation text, texts back any call that still goes unanswered, and pings the owner with a one-line summary. The operator builds it once per trade, clones it per shop, and bills monthly through Stripe.

**Who pays.** Owner-operators of residential HVAC, plumbing and electrical companies with 1-5 trucks where the owner or spouse answers the phone. The alternative they actually compare you against is not a $1,500/mo human receptionist; it is voicemail (free), a $29 Jobber add-on, or a $49-149 Rosie/Goodcall/Dialzara tier they never finish configuring.

**Why now.** Voice AI reached "usable on the phone" in 2025 (Retell G2 4.8/5; the G2 listing showed ~2,638 reviews in a 2026-09 search snippet, vs 780 in the execution skeptic's Apr 2026 snapshot, a jump that is plausible but not reconciled this session; Trustpilot 4.9/5 on 815 per CloudTalk's 2026 comparison, not re-fetched), and every vendor in the category is now selling into this vertical, which both validates the demand and commoditizes the agent. The 2026 differentiator is not the AI; it is booking into the shop's real calendar, trade triage rules, a working text-back with carrier-approved SMS, and a person 20 minutes away who fixes it.

**Headline numbers (skeptic-corrected, see section 3 and 6):**

| Item | Dossier | Corrected (used in this report) | Basis |
|---|---|---|---|
| Startup cash | ~$150 | ~$150 | execution skeptic; 10DLC cheaper than modelled ($4.50 + $15) |
| Fixed monthly before clients | ~$50 | ~$50 | dossier, holds |
| Price | $199-499/mo + $250-1,000 setup | **$149-249/mo + $250-500 setup** | both skeptics; Jobber $29, Rosie $149, Goodcall $129-249 benchmarks |
| Platform cost per shop | $45-90 (300 min) | **$12-17 Retell minutes; $30-45 all-in incl. Stripe (~$20-35 before payment fees; ~110 billable min)** | operator call log, 774 calls, Aug-Sep 2026; itemized in 7.2 |
| Gross margin | 60-85% | **~77-85% at $199 after payment fees (85-90% before)** | arithmetic on corrected cost |
| First dollar | ~40 days | **~35-60 days in the plan's base ramp (pilot 1 converts week 5-8); 60-90 days if it slips** | both skeptics (60-90); ClawOps zero-reply data; plan section 3 |
| Month-6 base MRR | ~$1,650 incl. setup | **$250-750** | both skeptics |
| Automation share | 65% | **45-55% overall; delivery 85-90% machine** | execution skeptic |
| Monthly churn | ~7% | **15-25% (vendor claim, unverified)** | Trillet via execution skeptic |
| Hours at 5 shops | ~7 h/wk | **10-12 h/wk** | execution skeptic |

## 2. Operator assumptions and what changes them

**Assumed:** one US operator, 10-15 h/wk, under $500 cash, fluent in Claude/ChatGPT and n8n, willing to learn light JavaScript for date handling, no audience, no trade background, no sales network. Day job permits short calls or drop-ins in owner-available windows (7-8 am, 12-1 pm, 4-6 pm local). If that last condition fails, [[decisions/final-selection]] says swap to podcast clipping without running the 60-day test.

**If the operator has more time (20+ h/wk):** the binding constraint is outreach, not build. Double the local touches (60/wk) and the base case moves toward the dossier's original 5 shops by month 6. Nothing else changes; delivery time per shop stays ~3-6 h/mo.

**If the operator has more money ($2-3k):** do not buy ads (contractors are already cold-pitched by every vendor). Spend on (a) a $200-300 Retell minute reserve so pilots 2-4 can run concurrently without a cash gap, (b) a $99-299/mo white-label wrapper only once past 5 shops, (c) a part-time local appointment setter at $15-20/hr for 5 h/wk, which is the one purchase that attacks the acquisition bottleneck directly [assumption: no data on setter conversion for this offer].

**If the operator has an existing skill or asset:** a trade background (worked in HVAC/plumbing, family in the trades) is the single biggest accelerator because it removes the trust gap that killed ClawOps; a local business network (Chamber, BNI, church, sports league) converts the cold walk-in into a warm referral. A YouTube habit helps only as a demo channel ("watch the agent take a 2 am no-heat call"), not as an acquisition channel for this buyer.

## 3. Market and demand analysis

### 3.1 The pain, with the skeptics' corrections stated plainly

| Claim in dossier | Evidence found (date) | Corrected view |
|---|---|---|
| 62% of home-service calls are missed (ServiceTitan, 50k+ lines) | Still only available as vendor relays: Contractor In Charge, Dialfyne, AIRA, CallJolt (all 2026). AIRA's own page also relays CallRail's Jan 2025 analysis of 1.1M leads: **14%** missed for home services. | **Weakened.** Use a 14-62% range; the population behind the 62% is undefined. The pilot shop's carrier call log is the number that matters. |
| 47% of calls arrive after hours | ServiceTitan State of the Trades (primary, via search snippet 2026): **14.1%** of inbound calls to residential HVAC shops arrived off-hours in June 2025, **9.8%** in October, a ~45% relative swing. AgentZap's "47%" is not supported by ServiceTitan's own published series. | **Refuted as stated.** After-hours share is roughly 10-15% for residential HVAC; overflow during business hours (lunch, on the job) is the larger pool. Sell "every call, not just night calls." |
| 78% abandoned a business after an unanswered call; 82% would call a competitor (CallRail, Sept 2025, n=1,000) | Confirmed as described by Quo/OpenPhone and OnCrew (2026). | **Holds as a survey; weakened as a per-call loss rate.** It is a lifetime attitude statistic, not the share of trade calls lost per miss. |
| Replacement cost $51-57 per lead | Google LSA 2026 benchmarks: HVAC $51, plumbing $57, electrical $39, overall $53, range $25-90+; HVAC 44.0% book rate and $2,110 average ticket; plumbing 44.5% book rate, $1,714 ticket (Skill Mammoth, Valley Marketing Group, Searchlight, 2026). | **Holds for shops that buy leads; weakened for shops that rely on referrals.** Use it in the pitch only after asking whether the owner runs LSAs. |
| "Recovered $X" case studies | Kaizen AI Consulting (Nottingham plumber, ~34 jobs/mo), Newo, RingReady, Jobber testimonial ($4,800 first month) are all self-reported (2026). | **Weakened.** Quote none of them to a prospect; run your own 2-week pilot and report the shop's own numbers. |

### 3.2 Buyer persona

- **Who:** owner of "Mike's Plumbing" or "Comfort Air Heating & Cooling", 1-5 trucks, $300k-1.5M revenue [assumption], answers the phone personally or through a spouse, uses Google Calendar, QuickBooks and maybe the free/cheap tier of Jobber or Housecall Pro; no CSR.
- **Trigger events:** a customer review saying "never called back"; a summer/winter surge where the phone rang while he was under a sink; a spouse who wants out of phone duty; a quote for a human answering service ($292.50/mo for 30 calls at Smith.ai, per Loman 2026).
- **What he distrusts:** "AI", anything that calls his customers, anything that quotes prices, and vendors who email him (he gets several a week). What he trusts: another owner's referral, hearing the agent take a call live, and a person he can call back.
- **Budget reality:** Census BTOS (May 2026) reports 19.8% of US businesses using AI in production and under 20% of firms with four or fewer employees; Housecall Pro's May-June 2026 survey (n=248) says 70%+ of pros use AI tools, ~40% "actively", 29% not at all, and active users save ~3.2 h/week. Awareness is high; paid, operational use in the smallest firms is the minority. Pitch time saved and jobs booked, never "AI".

### 3.3 Size proxies

| Proxy | Figure | Source (date) |
|---|---|---|
| US HVAC contractor businesses | 118,433 (2025, +2.3% YoY) | IBISWorld (dossier relay, 2025) |
| US plumbing businesses | **127,324** (2025, +0.8% YoY) | IBISWorld (search snippet, 2026) |
| US electrician businesses | **251,789** (2025, +2.6% YoY) | IBISWorld (search snippet, 2026) |
| Share that is 1-5 trucks, off-suite, no CSR, misses enough calls to feel it | **no data found** | demand skeptic |
| Avoca customers (upmarket, $1,000-3,000/mo) | 800+ | Fortune / PRNewswire (Apr 2026), Contractor ToolStack (2026) |
| Jobber Receptionist conversations at GA | 200k+ | PRNewswire Aug 2025 (execution skeptic relay) |

Reading: ~500k firms across the three trades, of which a local operator needs 5-10. Addressable size is not the constraint; reaching and convincing them is.

### 3.4 Trend direction

- Supply: Avoca $125M+ raised in total (Seed, A, B) at a $1B valuation, Apr 2026; Series B led by Meritech and General Catalyst, Series A by Kleiner Perkins; 800+ customers (PRNewswire / Dealroom, 2026-04-27). Jobber, Housecall Pro, Workiz, ServiceTitan all shipped native AI answering 2025-2026; Retell's G2 listing shows ~2,638 reviews (search snippet, Sept 2026; 780 in Apr 2026 per the execution skeptic, unreconciled). The category is being validated and bundled at the same time.
- Demand: Jobber's 2026 Home Service Trends report says 88% of its "high-confidence" cohort uses AI daily and that leads are still referral-led (Facebook 32%, Google organic 20%, LSAs 19% for high performers). The execution skeptic's relay that 80% of surveyed businesses are fully booked and only 13% name lead volume as a constraint could not be re-verified this session (**treat as unconfirmed**); its implication stands: "more calls" is not every owner's pain, "not answering the phone at dinner" is.
- Pricing: entry tiers fell from $149-299 (2025) to $29-49 (2026): Jobber $29 for 30 conversations ($0.79 each after; help center updated 2026-07-09), Dialzara $29 for 60 minutes (CloudTalk 2026). Expect continued compression.

### 3.5 Seasonality (this is the sales calendar)

- ServiceTitan State of the Trades: residential HVAC off-hours call share 9.8% (Oct) to 14.1% (Jun 2025). Vendors report peak-week HVAC volume 2-4x average in first heat waves (KaiCalls, Call Experts 2026; vendor figures).
- Plumbing: emergency mix is year-round with a winter freeze and holiday sewage-backup spike; a 2 am burst-pipe call runs $450-1,200 and a holiday mainline clear $1,200-1,800 (PipelineOn 2026, vendor pricing guide).
- Implication for a September 11 start: first go-lives land in November-December. Plumbing carries winter demand; HVAC's heating-season calls exist but its big after-hours spike is June. Sell plumbing now, line up HVAC pilots in February-April, and expect HVAC churn attempts in October and March when the owner "can answer it myself again."

## 4. Offer design and pricing

### 4.1 Packages

| Package | Price | What is included | When to sell it |
|---|---|---|---|
| **Pilot** | $0 for 14 days (pilot start = day 1), then auto-converts at go-live (day 15) | After-hours + overflow answering, SMS confirmation to caller, owner SMS alert, daily summary email; no booking writes yet | Every first shop; pilot is the demo |
| **Front Desk** | **$199/mo** ($149 if the shop signs annual or is a referral from a paying shop) + **$250 setup** | Everything in Pilot + booking into Google Calendar or a shared calendar, missed-call text-back (after 10DLC approval), weekly recovered-calls report | Default close for shops with no suite |
| **Front Desk + Integration** | **$249/mo + $500 setup** | Front Desk + writes into Jobber / Housecall Pro / ServiceTitan or a two-calendar dispatch rule, warm transfer to on-call tech for emergencies, monthly review call | Shops on a suite's cheap tier who will not pay the suite's Plus/Grow upgrade; 2+ truck shops with an on-call rotation |
| Add-ons | $49/mo second phone line or Spanish agent; $99 one-time re-scoping | | Only after month 3 |

**Definitions used in all three notes:** *pilot start* = day 1, the agent is answering the shop's after-hours line for free; *go-live* = day 15, when the pilot auto-converts; the $250 setup fee and the first $199 are invoiced together on go-live, never on signature or on pilot day 1. The pilot is free because the dossier's 6-10 h first build drops to ~4 h once templated and the fee only clears when the shop has heard it work.

### 4.2 Benchmarks the buyer will hold you against

| Product | 2026 price | Source |
|---|---|---|
| Jobber Receptionist (native) | $29/mo, 30 conversations, $0.79 each after; unlimited on Plus | Jobber Help Center (updated 2026-07-09) via search; Beside, Morgan Systems 2026 |
| Workiz Genius Answering (native) | ~$200/mo add-on on top of ~$100 phone add-on and a $225-325 plan | Carly, Tooled Up Pro, checkthat.ai (2026) |
| Housecall Pro CSR AI (native) | quote-only; third parties estimate $200-500+/mo | Projul (2026) |
| Dialzara | $29/60 min, $99/220, $199/500, $349/1,000; $0.35-0.48 overage | CloudTalk (2026) |
| Goodcall | $79 / $129 / $249 per mo, unlimited minutes, by unique callers | execution skeptic, verified July 2026 |
| Rosie | $49 / $149 / $299 for 250 / 1,000 / 2,000 min; booking from $149 | dossier relay (2026) |
| Smith.ai (human) | from $292.50/mo for 30 calls (~$9.75/call) | Loman (2026) |
| Avoca | ~$1,000-3,000/mo | Contractor ToolStack (2026) |
| Fiverr "build me a Vapi/Retell receptionist" gigs | $10-90 | Fiverr listings (2026) |

The Fiverr line matters: an agent alone is worth $10-90 on a marketplace. The $250-500 setup fee is for call forwarding on the shop's carrier, the calendar/CRM write, 10DLC registration for the shop (Twilio ISV flow: a secondary customer profile under the shop's legal name and EIN, then brand and campaign), 20-50 scripted test calls and an owner walkthrough; say so in the proposal.

### 4.3 Why $199 and not $99 or $299

- Below $149 you are a SaaS with worse marketing than Jobber; above $249 you are anchored against Rosie $299 or a Workiz bundle and lose without an integration. The demand skeptic refutes $499 for this segment and the execution skeptic sets the corrected band at $149-249.
- At $199 with $30-45 all-in variable cost (incl. Stripe fees) the contribution is ~$155-170/shop/mo; 5 shops cover the whole fixed stack 15x over. Margin is not the problem; volume and retention are.

## 5. Niche selection

| Rank | Sub-niche | Why | Evidence | Risk |
|---|---|---|---|---|
| 1 | **Residential plumbing and drain shops, 1-5 trucks, metro or exurban** | Year-round emergency calls, highest LSA cost per lead ($57), $1,714 average ticket, 44.5% LSA book rate, 127k US firms; a missed 2 am burst pipe is a $450-1,200 job | Valley Marketing Group / Skill Mammoth LSA 2026; IBISWorld 2025; PipelineOn 2026 | Many already on Housecall Pro; screen for suite use |
| 2 | **Residential HVAC in hot-climate metros (TX, AZ, FL, GA, NV)** | Off-hours share peaks in June (14.1%), peak weeks 2-4x volume, $2,110 average ticket, $51 CPL; the best "you missed calls last summer" story | ServiceTitan State of the Trades (2025 data); LSA 2026 | Strong shoulder-season churn; sell Feb-Apr, expect pause requests in Oct |
| 3 | **Combined HVAC + plumbing shops** | Two call types, higher volume per line, less seasonality; often 3-5 trucks with an owner who is done answering | assumption, no separate data | More likely to already have a CSR or suite |
| 4 | **Residential electricians (panels, EV chargers, service calls)** | Largest count (251k firms, +2.6%), lowest CPL ($39), scheduled work fits booking | IBISWorld 2025; LSA 2026 | Fewer emergencies, so the after-hours pitch is weak; sell overflow + booking |
| 5 | **Water-heater / sewer / restoration specialists** | Restoration CPL up to $150 (dossier relay), highest urgency | dossier relay 2026 | Small population; restoration usually multi-truck with dispatch already |

**Recommended start: residential plumbing/drain (rank 1), with HVAC (rank 2) as the second template built in January for a February-April selling window.** Reasoning: the September start puts first go-lives in November-December, when plumbing demand is steady and HVAC's after-hours share is at its annual low; plumbing has the highest replacement cost per lead and the least seasonal churn pressure; and the same n8n intake works for both, so the HVAC template is a two-evening fork, not a rebuild.

## 6. Competitive landscape and positioning

**What the 2025-2026 winners do differently (named examples):**

- **Avoca** (YC; 800+ customers; $125M+ raised across Seed, A and B at a $1B valuation, Apr 2026; Series B led by Meritech and General Catalyst, Series A by Kleiner Perkins): sells an "AI front office" (answer, book, follow up on estimates) at $1,000-3,000/mo to 10+-person shops on ServiceTitan; wins on integration depth and outcome reporting ("on track to book $1B in jobs in 2026" per Fortune). Not your customer, but its sales team is calling your prospects' bigger neighbours.
- **Jobber Receptionist** ($29): wins on distribution (already inside the app) and price; loses when the shop is not on Jobber or wants booking into a non-Jobber calendar.
- **Rosie / Goodcall / Dialzara** ($29-349): win on self-serve and free trials; lose when the owner will not sit down and configure a trial, which is exactly the 1-5-truck owner.
- **Retell certified partners** (e.g. The AI Agency USA, listed on retellai.com/partners) and small consultancies (Kaizen AI Consulting's Nottingham plumber): win on build-and-run for one vertical with the client's own calendar; Retell's partner tiers are earned by onboarding 1-8 customers in 6 months (higher tiers 9-16), which is achievable for a solo operator and gives referred leads and priority support (Retell partner blog via search, 2026).

**Your angle:** "the plumber's front desk, run by the guy down the road." One trade at a time, in-call booking into whatever calendar the shop actually uses, a text-back that carriers actually deliver (10DLC done for them), disclosure and recording rules handled, a weekly one-page report, and a phone number that reaches a human when it breaks. Compete on being local and on integration, never on price or on "AI".

**Why a beginner can still win:** the SaaS incumbents cannot walk into a shop, sit with the owner for 40 minutes, set up conditional call forwarding on his carrier and register his EIN with the campaign registry; Avoca will not sell a $199 account; the suites only serve their own users. The addressable gap is small per shop and large in aggregate, and nobody in the category is competing for the 6th plumber in a mid-size county.

## 7. Unit economics

### 7.1 Startup costs (one-time)

| Item | Cost | Source / note |
|---|---|---|
| Retell test minutes beyond the $10 free credit (~60 min) | $30 | Retell pricing relays (Cekura, CloudTalk 2026) |
| Twilio local number + voice/SMS credit | $22 | ~$1.15/mo number + $20 credit (Lumentra/Seldon Frame relay, 2026) |
| A2P 10DLC Low-Volume Standard: brand $4.50 + one campaign vetting $15 (your own demo line) | $19.50 | Twilio docs / Sociocs (2026); client shops re-billed in setup fee |
| n8n self-hosted on a $5-7 VPS, first month | $7 | ExpressTech 2026; n8n Cloud Starter is EUR 20-24/mo if preferred |
| Domain + one-page site with the demo number and a privacy/terms page (needed for 10DLC) | $15 | assumption |
| Claude Pro (already paying per profile) | $0-20 | profile |
| Stripe account | $0 | Stripe: no monthly fee |
| **Total** | **~$95-115; ~$150 with a $40 reserve for pilot minutes** | matches the corrected ~$150 |

### 7.2 Monthly tool costs

| Tier | Fixed (before clients) | Variable per shop | Notes |
|---|---|---|---|
| Fixed stack | Claude Pro $20; n8n VPS $7; Twilio demo number $1.15; demo minutes ~$10; Stripe $0; domain ~$1 | | **~$40-50/mo** |
| Per paying shop | | Retell minutes ~110 billable x $0.11-0.15 = **$12-17**; Retell phone number $2 or Twilio number $1.15; 10DLC campaign $1.50-10; SMS ~$5; Stripe 2.9% + $0.30 + 0.7% Billing (~$8 on $199) | **~$30-45 all-in incl. payment fees (~$20-35 before Stripe); this is the figure used everywhere in the package** |
| At 5 shops | ~$50 | ~$150-225 | Total ~$200-275/mo against $995-1,245 MRR |

Sources: operator call log (774 calls, 20 days, median 16 s, 60/60 rounding 2.3x; execution skeptic, Sept 2026); Retell $0.07/min engine and $0.13-0.31 all-in (Cekura, CloudTalk 2026); Twilio 10DLC (Twilio docs, Sociocs 2026); Stripe 2.9% + $0.30 and 0.7% Billing (Checkout Page, Flexprice 2026).

### 7.3 Revenue scenarios

Assumptions (all labelled): price $199 base, $249 with integration; setup $250 (base) / $500 (integration); 30+ local touches/wk from week 3; reply rate and close rate **no data found**, so scenarios are defined by shop count, not by a conversion funnel; churn 15-25%/mo year one is a vendor claim (Trillet via execution skeptic), modelled as one lost shop per quarter in base (~8-10%/mo at 3-5 shops) and one per two months in conservative; at the vendor-claimed 15-25%/mo the month-12 base would need ~10-12 closes to hold 5 shops, i.e. the upside acquisition rate, so treat the month-12 base as contingent on churn <=10%/mo; hours 10-12/wk, which at 4+ shops only holds if outreach drops to ~3 h/wk (see plan section 8). The base ramp follows the plan: pilot 1 live week 3, converts week 5-6; pilot 2 converts week 7-8; so the base clears the day-60 kill gate (2 paying) with no margin, and the conservative column is what the gate is designed to catch (it is shown only to bound the downside).

| Month | Conservative | Base | Upside |
|---|---|---|---|
| 1 | $0 (build + first touches) | $0 | $0 |
| 3 | $0-199 MRR; 1 pilot running (fails the day-60 gate) | 2 shops: **$398 MRR** + $500 setups banked (= day-60 gate) | 3 shops: $597 MRR + $750 setups |
| 6 | 1 shop: $199 MRR (one closed, one churned) | 3 shops: **$597 MRR** (2 + 2 closed in the Nov-Jan trough, 1 churned), cumulative setups $1,000 | 6 shops (2 integrated): **$1,294 MRR** (4 x $199 + 2 x $249), setups $2,000 (4 x $250 + 2 x $500) |
| 12 | 2 shops: $398 MRR | 5 shops (1 integrated): **$1,045 MRR**; ~8 closed, 3 churned; setups ~$2,250 cumulative (7 x $250 + 1 x $500) | 10 shops (4 integrated): **$2,190 MRR**; setups ~$3,500 |

Net monthly at month 6 base: $597 - 3 x $40 - $50 = **~$427**. Month 12 base: $1,045 - 5 x $40 - $50 = **~$795**.

**Hours and effective hourly:** 10-12 h/wk (~45 h/mo). Month 6 base ~$427 / 45 h = **~$9-10/hr** (demand skeptic: $10-15; the difference is the skeptic's lower hours assumption); month 12 base ~$795 + a $250 setup / 45 h = **~$23/hr**; upside month 12 ~$1,750 net / 50 h = ~$35/hr. Cumulative over the first six months is near $0-8/hr (execution skeptic) because months 1-2 are unpaid.

**Break-even:** fixed $50/mo is covered by one shop. Cumulative cash (startup $150 + $50/mo burn) is recovered by the first setup fee plus first month, i.e. at the first go-live (pilot day 15), around day 35-60 in the base ramp and day 60-90 if pilot 1 slips. The asset case only starts at 5+ retained shops.

## 8. Risks and mitigations

| Risk | Likelihood / impact | Evidence | Mitigation |
|---|---|---|---|
| **Platform reliability** (agent breaks after a vendor update; webhooks not firing) | Medium / high | Vapi: 63 incidents in 90 days, silent breaking changes, 14-day transcript purge (execution skeptic, Mar 2026 snapshot); Retell: StatusGator lists a multi-outage history (2026, egress-blocked and unverified this session; do not rely on the count); Retell's own docs claim >99.9% uptime | Build on Retell; keep prompts, tools and intake in n8n (portable); nightly transcript export; a scripted 5-call smoke test after any platform changelog; fallback = ring the owner's cell |
| **Suite bundling** (Jobber $29, HCP CSR AI, Workiz ~$200, ServiceTitan) | High / medium | help.getjobber.com (2026-07-09); Projul, Carly (2026) | Qualify for off-suite or cheap-tier shops; sell the Integration tier as "the AI that books into your suite"; expect and price for churn |
| **Acquisition failure** | High / high | ClawOps: 0 replies, $0 in ~6 weeks (Feb-Mar 2026); contractors cold-pitched by 15+ vendors | Local and in-person only; free 14-day pilot; count replies; 60-day kill gate |
| **Seasonal churn** | High / medium | ServiceTitan off-hours share 9.8% Oct vs 14.1% Jun | Plumbing first; annual discount ($149) offered in month 2; "pause at $49" option instead of cancel [assumption] |
| **AI quality / caller rejection** | Medium / high | 37% of real inbound calls hung up on a machine; 8.7% spam (operator log, Sept 2026) | Human-sounding voice, first-sentence disclosure that is short, callback-within-60-seconds text-back for hang-ups; weekly transcript QA; kill at <80% correct intake |
| **TCPA / FCC** | Low if inbound-only / severe if not | The TCPA restricts *making* calls or texts with an artificial voice or autodialer; answering an inbound call is outside it (a vendor-blog reading, JustCall / AIemply 2026; no primary FCC statement found). FCC 24-17 (Feb 2024) makes AI voices "artificial", so any outbound AI-voice call needs prior express consent. **SMS counts as a call under the TCPA** (FCC interpretation relayed by ActiveProspect and Infobip, 2026), and consent for calls does not automatically extend to texts; informational texts need prior express consent, marketing texts prior express *written* consent (Wipfli 2026). NPRM 24-84 (Aug 2024) still a proposal as of Aug 2026; $500-1,500 per violation | Agent never dials out. The missed-call text-back is **one informational SMS to a consumer-initiated inbound contact** (the defensible "consumer-initiated, informational" reading; this is the weakest compliance point in the stack and the part carriers scrutinize at campaign vetting, Twilio error 30909): never a marketing message, includes the shop name and STOP, rate-limited to 1 per number per 24 h, and this exact flow is described verbatim in the 10DLC campaign's message-flow/CTA field. Log the inbound call (number, timestamp) as the consent event. No reactivation campaigns; any caller callback request is logged verbatim and returned by a human |
| **State bot-disclosure and recording consent** | Medium / medium | Utah SB 149 AI Policy Act (disclose if asked; regulated occupations proactively); **Maine LD 1727 Chatbot Disclosure Act (in force 2025-09-24, covers "textual or aural" bots, i.e. voice callbots; disclosure at the start of the interaction; Verrill 2025)**; California B.O.T. Act (unsettled for voice); Colorado AI Act **delayed to 2027-01-01 and narrowed by SB 189, signed 2026-05-14, not in force** (Hunton, Holland & Knight, May 2026). Recording: 11 clear all-party states for phone calls plus 4 mixed/unsettled (Recording Law, NextPhone, Viirtue 2026) | Greeting discloses AI and recording in every state, which satisfies all of the above. Recording: treat as all-party **CA, DE, FL, IL, MD, MA, MT, NV, NH, PA, WA** (11 clear; Nevada is all-party for phone calls under NRS 200.620) **plus CT, MI, OR, VT** (mixed or unsettled; treat as all-party to be safe). When the caller may be in another state, the stricter law applies. If the owner refuses the recording disclosure in any of these 15, disable recording in Retell and keep the transcript only; cross-check against questionnaire field 14 (states served) |
| **10DLC rejection blocks text-back** | Medium / medium | Twilio errors 30882/30908/30934; TermsAndConditionsUrl required from 2026-06-30; cached rejections need a ticket (execution skeptic case, Jun-Jul 2026) | Publish a compliant privacy/terms page on the shop's site (template in the plan) before submitting; submit on day 1 of the pilot; voice goes live without SMS |
| **FTC / advertising** | Low / medium | FTC has no AI-disclosure rule; fake-testimonial/endorsement rule applies | Report only jobs the agent actually booked; never publish vendor case studies as yours; disclose AI in the shop's own "24/7 answering" marketing |
| **Liability for what the bot says** | Low / medium | Moffatt v. Air Canada (company owns bot statements) | Guardrails: no prices beyond the owner's published dispatch fee, no safety advice beyond the gas/CO script; "AI may err" and limitation clauses in the agreement |
| **Payments / chargebacks** | Low / low | Stripe disputes $15 (2026); processor rules for AI telecom services: no data found | Monthly card on file, setup invoiced on go-live, 30-day cancel in writing |
| **Copyright of AI output** | Negligible | not a revenue factor | Transcripts belong to the shop by contract; prompts and workflows are the operator's trade secret |
| **Tool dependency / price change** | Medium / medium | Retell added Fast-Tier LLM at 1.5-2x rates (2026) | Portable design; price contracts with a 30-day repricing clause |

## 9. Kill criteria and pivot options

**Kill (binding, from [[decisions/final-selection]]):** fewer than 2 paying shops after 60 days of 30+ local touches per week, or first-pilot transcripts under ~80% correct intake on real calls. Execution-skeptic additions adopted here: any client whose agent breaks twice in a month from a platform update; a 10DLC campaign not approved within 30 days of go-live; and count replies (target 10% of touches) as the leading indicator, since ClawOps' failure mode was zero replies, not zero closes.

**Pivot options, in order:**
1. **Swap to podcast clipping** (designated alternate) if the schedule condition fails or the 60-day gate is missed.
2. **Narrow to integration-only work** for shops already on Jobber/HCP that want booking into a second calendar or dispatch rule: $500-1,000 projects, no MRR, uses the same n8n skill.
3. **Sell the template, not the service**: package the plumbing agent + n8n intake as a Retell "app partner" listing or a $99-199 template for other resellers (validated only by the existence of five white-label platforms; demand not measured).
4. **Move up-market as a subcontractor** to a Retell certified partner or a local marketing agency that wants a voice line but has no builder.

## Sources

Demand and market
- [Contractor In Charge: Missed call statistics for home service companies (62%, 2026)](https://contractorincharge.com/blog/missed-call-statistics-for-home-service-companies)
- [AIRA: 62% of business calls go unanswered; also relays CallRail Jan 2025 14% home services (2026)](https://www.getaira.io/blog/missed-business-calls-statistics)
- [ServiceTitan State of the Trades: HVAC off-hours summer call spike (June 2025 14.1%, October 9.8%)](https://www.servicetitan.com/toolbox/state-of-the-trades/trends/hvac-summer-after-hours-call-spike)
- [AgentZap: HVAC phone statistics 2026 (source of the 47% claim)](https://agentzap.ai/blog/hvac-phone-statistics)
- [Quo (OpenPhone): Small business callback statistics 2026 (CallRail Sept 2025 survey)](https://www.quo.com/blog/small-business-callback-statistics/)
- [OnCrew: Missed call statistics, verified sources (2026)](https://oncrew.ai/resources/missed-call-statistics)
- [Valley Marketing Group: Google LSA cost per lead 2026, HVAC/plumbing/electrical](https://thevalleymarketinggroup.com/blog/google-lsa-cost-per-lead-home-services-2026/)
- [Skill Mammoth: Local Services Ads cost 2026 by trade](https://skillmammoth.com/blog/local-service-ads-cost)
- [Searchlight Digital: Google LSA cost per lead by trade (2026)](https://searchlightdigital.io/google-local-service-ads-cost-per-lead/)
- [IBISWorld: Plumbers in the US, number of businesses (127,324 in 2025)](https://www.ibisworld.com/united-states/number-of-businesses/plumbers/1946/)
- [IBISWorld: Electricians in the US, number of businesses (251,789 in 2025)](https://www.ibisworld.com/united-states/number-of-businesses/electricians/189/)
- [IBISWorld: Heating and air-conditioning contractors in the US (118,433 in 2025)](https://www.ibisworld.com/united-states/number-of-businesses/heating-air-conditioning-contractors/1945/)
- [US Census Bureau: Large firms with at least 20 employees biggest AI users (BTOS, May 2026)](https://www.census.gov/library/stories/2026/05/ai-use-businesses.html)
- [Omago: How many US small businesses use AI in 2026 (BTOS 19.8%)](https://www.omago.ai/blog/us-small-business-ai-adoption-2026)
- [Plumbing & Mechanical: 70%+ of home service pros use AI, Housecall Pro report (2026)](https://www.pmmag.com/articles/106575-70-of-home-service-professionals-now-use-ai-to-cut-admin-work-not-field-jobs-housecall-pro-report-finds)
- [Jobber: 2026 Home Service Trends Report](https://www.getjobber.com/home-service-trends-report/)
- [Marketing Code: Jobber 2026 trades report, four-channel stack (May 2026)](https://www.marketingcode.com/jobber-2026-trends-four-channel-stack-trade-marketing-may-2026/)
- [PipelineOn: Plumbing emergency service pricing 2026](https://pipelineon.com/blog/plumbing-emergency-service-pricing/)
- [KaiCalls: How many calls do HVAC companies miss (seasonal)](https://www.kaicalls.com/blog/how-many-calls-do-hvac-companies-miss)

Competitors and pricing
- [Fortune: Avoca, Kleiner Perkins-backed $1B AI startup for HVAC, plumbing, roofing (2026-04-27)](https://fortune.com/2026/04/27/avoca-ai-agents-missed-calls-hvac-plumbing-roofing-kleiner-perkins-chen-shrivastava-braswell/)
- [PRNewswire: Avoca raises $125M+ at $1B valuation; Series B led by Meritech and General Catalyst, Series A by Kleiner Perkins (2026-04-27)](https://www.prnewswire.com/news-releases/avoca-raises-125m-at-1b-valuation-to-power-americas-services-economy-with-ai-302753962.html)
- [Dealroom: Avoca raises $125M+ across three rounds at $1B valuation (2026-04-27)](https://dealroom.co/news/127930-avoca-raises-125m-at-1b-valuation-to-bring-ai-to-service-businesses/)
- [Contractor ToolStack: Avoca AI review 2026 ($1,000-3,000/mo)](https://contractortoolstack.com/software/avoca-ai/)
- [Jobber Help Center: Receptionist powered by Jobber AI ($29/mo, 30 conversations, updated 2026-07-09)](https://help.getjobber.com/hc/en-us/articles/25315927533847-Receptionist-powered-by-Jobber-AI)
- [Beside: Jobber AI phone answering, what it costs (2026)](https://www.beside.com/blog/jobber-ai-phone-answering)
- [Carly: Workiz AI in 2026, Genius Answering (~$200/mo)](https://www.usecarly.com/blog/workiz-ai/)
- [Tooled Up Pro: Workiz pricing 2026 with add-ons](https://tooleduppro.com/guides/workiz-pricing/)
- [Projul: Housecall Pro pricing 2026 (CSR AI quote-only)](https://projul.com/blog/housecall-pro-pricing-analysis-2026/)
- [CloudTalk: Dialzara pricing 2026 ($29-349)](https://www.cloudtalk.io/dialzara-pricing/)
- [Loman: Smith.ai pricing 2026 ($292.50/30 calls)](https://loman.ai/blog/smith-ai-pricing)
- [CloudTalk: Rosie AI answering service pricing 2026](https://www.cloudtalk.io/blog/rosie-ai-answering-service-pricing/)
- [CloudTalk: Goodcall pricing 2026](https://www.cloudtalk.io/blog/goodcall-pricing/)
- [Fiverr: build AI receptionist voice agent with Vapi or Retell ($90 gig, 2026)](https://www.fiverr.com/ethxn787/make-an-ai-voice-agent-using-vapi-or-synthflow)
- [Fiverr: AI voice agent and receptionist with Vapi, Retell, n8n ($20 gig, 2026)](https://www.fiverr.com/gigpilot_33/build-make-com-n8n-automation-ai-voice-agent-vapi-ai-receptionist-retell-ai)
- [Upwork: hire AI receptionist builders (Jul 2026)](https://www.upwork.com/hire/ai-receptionist-builders/)
- [Retell AI: Find a solution partner](https://www.retellai.com/partners)
- [Retell AI: How the certified partner program works (2026)](https://www.retellai.com/blog/how-retell-ais-certified-partners-work)
- [Retell AI: Best answering service for HVAC, 8 tools ranked (June 2026)](https://www.retellai.com/blog/best-answering-service-for-hvac-company)
- [Kaizen AI Consulting: Nottingham plumbing company AI receptionist case study (self-reported)](https://kaizenaiconsulting.com/nottingham-plumbing-company-ai-receptionist-books-jobs-24-7/)
- [Trillet: Voice agent client retention strategies 2026 (churn claims, vendor)](https://trillet.ai/blogs/voice-agent-client-retention-strategies)
- [VoiceAI Connect: How to reduce AI receptionist client churn 2026 (vendor)](https://www.myvoiceaiconnect.com/blog/reduce-ai-receptionist-client-churn-rate)

Platform costs and reliability
- [Cekura: Retell AI pricing per minute, what you actually pay in 2026](https://www.cekura.ai/blogs/retell-ai-pricing-per-minute)
- [CloudTalk: Retell AI pricing 2026](https://www.cloudtalk.io/retell-ai-pricing/)
- [Layer3 Labs: Retell AI pricing 2026](https://www.layer3labs.io/guides/retell-ai-pricing)
- [CloudTalk: Retell AI vs Vapi AI 2026 (G2 4.8; Trustpilot 4.9/815 vs 2.4; page date not captured, egress-blocked 2026-09-11)](https://www.cloudtalk.io/retell-ai-vs-vapi-ai/)
- [G2: Retell AI reviews (4.8/5, ~2,638 reviews per search snippet, 2026-09-11)](https://www.g2.com/products/retell-ai/reviews)
- [CloudTalk: Vapi AI plans and pricing 2026](https://www.cloudtalk.io/blog/vapi-ai-pricing/)
- [Layer3 Labs: Vapi pricing 2026](https://www.layer3labs.io/guides/vapi-pricing)
- [StatusGator: Retell AI status and outage history (2026; egress-blocked, outage count unverified this session)](https://statusgator.com/services/retell-ai)
- [Retell AI: Reliability overview (>99.9% uptime claim)](https://docs.retellai.com/reliability/reliability-overview)
- [Achiya Cohen: AI phone-agent cost analysis, 774 calls, Aug 21-Sep 10 2026](https://github.com/achiya-automation/safari-mcp/blob/29af3b9f87f6cc85e11d35766898ef78aa4abdc1/ai-call-cost-il-2026-09-10.html)
- [Lumentra CallAgent: Vapi gotchas and limitations 2026](https://github.com/Lumentra-AI/CallAgent/blob/4bc844ab50f428e1f5cd5105745394cfde862c85/docs/research/vapi-gotchas-limitations-2026.md)
- [No Code MBA: n8n pricing 2026 (Starter EUR 20/24, Pro EUR 50/60)](https://www.nocode.mba/articles/n8n-pricing)
- [Coworker AI: n8n pricing 2026](https://coworker.ai/blog/n8n-pricing)
- [ExpressTech: Real cost of self-hosting n8n in 2026](https://expresstech.io/the-real-cost-of-self-hosting-n8n-in-2026/)
- [Twilio: A2P 10DLC overview](https://www.twilio.com/en-us/phone-numbers/a2p-10dlc)
- [Twilio Help: Comparison between Sole Proprietor, Low Volume Standard and Standard registration](https://help.twilio.com/articles/4407882914971-Comparison-between-Starter-Low-Volume-Standard-and-Standard-registration-for-A2P-10DLC)
- [Twilio Help: A2P 10DLC campaign vetting FAQ ($15 vetting fee)](https://help.twilio.com/articles/11587910480155-A2P-10DLC-Campaign-Vetting-FAQ)
- [Sociocs: Twilio 10DLC registration and pricing explained](https://www.sociocs.com/post/twilio-10dlc-explained/)
- [Twilio error 30934: Terms and Conditions URL required (from 2026-06-30)](https://www.twilio.com/docs/api/errors/30934)
- [Twilio error 30909: Campaign rejected, message flow or call to action incomplete (2026)](https://www.twilio.com/docs/api/errors/30909)
- [Twilio docs: ISV A2P 10DLC onboarding overview (ISV Reseller/Partner primary profile, secondary customer profiles) (2026)](https://www.twilio.com/docs/messaging/compliance/a2p-10dlc/onboarding-isv)
- [Twilio error 30908: Compliant privacy policy required](https://www.twilio.com/docs/api/errors/30908)
- [Checkout Page: Stripe fees explained 2026 (2.9% + 30c; Billing 0.7%)](https://checkoutpage.com/blog/stripe-processing-fees)
- [Flexprice: Stripe pricing breakdown 2026](https://flexprice.io/blog/stripe-pricing-breakdown-2026)

Beginner attempt
- [ClawOps sales pipeline tracker, 2026-02-24 (0 replies, $0)](https://github.com/rickclaw08/claw-systems/blob/3fa61252f449584a3d3ba7d647700d5531c20f69/claw-agency/sales/pipeline-tracker.md)
- [ClawOps financial reality check, 2026-03-02](https://github.com/rickclaw08/claw-systems/blob/3fa61252f449584a3d3ba7d647700d5531c20f69/claw-agency/finance/financial-reality-check-2026-03-02.md)

Legal and compliance
- [FCC Declaratory Ruling FCC 24-17 (Feb 2024, PDF)](https://docs.fcc.gov/public/attachments/FCC-24-17A1.pdf)
- [JustCall: AI voice agent disclosure laws, federal, state, international 2026 (NPRM 24-84 status)](https://justcall.io/blog/ai-voice-agent-disclosure-laws.html)
- [Zian AI: FCC NPRM 24-84 AI-call disclosure rules](https://www.zian.ai/fcc-nprm-24-84-ai-call-disclosure-rules/)
- [AIemply: Is an AI receptionist legal? 2026 disclosure rules](https://aiemply.com/blog/ai-receptionist-disclosure-laws)
- [Henson Legal: AI voice agent compliance, TCPA, FCC, state laws (2026)](https://www.henson-legal.com/ai-voice-compliance)
- [Thoughtly: AI disclosure requirements for voice agents](https://thoughtly.com/blog/ai-disclosure-requirements-what-to-tell-callers)
- [Agxntsix: New bot disclosure laws for AI voice calls in 2026](https://agxntsix.ai/blog/what-are-the-new-bot-disclosure-laws-for-ai-voice-calls-in-2026)
- [Sembly AI: Call recording in 2026, one-party vs two-party laws](https://www.sembly.ai/blog/call-recording-laws-one-party-vs-two-party-consent/)
- [Viirtue: Call recording consent laws by state, 2026 guide (11 clear all-party states; CT, MI, OR, VT mixed; via reviewer, egress-blocked 2026-09-11)](https://viirtue.com/call-recording-consent-laws-by-state-2026-guide/)
- [Recording Law: Nevada recording laws 2026 (NRS 200.620, all-party for phone calls)](https://www.recordinglaw.com/united-states-recording-laws/one-party-consent-states/nevada-recording-laws/)
- [NextPhone: Call recording laws by state 2026 (11 all-party; CT, MI, OR, VT mixed)](https://www.getnextphone.com/blog/call-recording-laws-by-state)
- [Verrill: Maine law now requires limited disclosures of AI technology, LD 1727 (2025)](https://www.verrill-law.com/news/maine-law-now-requires-limited-disclosures-of-artificial-intelligence-technology/)
- [Hunton: Colorado AI Act amended and effective date delayed to 2027-01-01 (May 2026)](https://www.hunton.com/privacy-and-cybersecurity-law-blog/colorado-ai-act-amended-and-effective-date-delayed)
- [Holland & Knight: Colorado Governor signs SB 189 (2026-05-14)](https://www.hklaw.com/en/insights/publications/2026/05/colorado-governor-signs-sb-189)
- [Wipfli: TCPA informational text messages, rules and requirements (2026)](https://www.wipfli.com/insights/articles/tcpa-informational-text-messages-rules-and-requirements)
- [ActiveProspect: TCPA text messages, rules for 2026 (texts treated as calls)](https://activeprospect.com/blog/tcpa-text-messages/)
- [Infobip: 2026 guide to TCPA compliance for SMS (search snippet; egress-blocked)](https://www.infobip.com/blog/tcpa-compliance-sms)
- [Retell AI: 2026 TCPA compliance playbook for voice AI outbound](https://www.retellai.com/blog/tcpa-compliance-playbook-voice-ai-outbound)

Vault
- [Candidate dossier](../../research/candidates/ai-front-desk-home-services.md) · [Demand skeptic](../../research/candidates/ai-front-desk-home-services-skeptic-demand.md) · [Execution skeptic](../../research/candidates/ai-front-desk-home-services-skeptic-execution.md) · [Final selection](../../decisions/final-selection.md)
