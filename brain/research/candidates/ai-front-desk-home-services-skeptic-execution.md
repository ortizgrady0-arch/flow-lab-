---
title: "Skeptic (execution lens): Inbound AI front desk for 1-5-truck HVAC, plumbing and electrical shops"
tags: [research, skeptic, execution, ai-front-desk-home-services]
updated: 2026-09-10
lens: execution
verdict: weakened
confidence: 0.6
---

# Execution skeptic: AI front desk for home-service shops

Attacks the automation, tooling, economics and legal claims in [[research/candidates/ai-front-desk-home-services]]. Related: [[research/lenses/local-smb-services]] · [[research/lenses/emerging-2026]] · [[research/saturated-overhyped]] · [[research/shortlist]]

## TL;DR

- **Overall: weakened, not refuted.** Platform per-minute prices in the dossier are correct (Vapi $0.05/min platform, Retell $0.07-0.31/min, verified against the vendors' own pages in dated snapshots from 2026-03-22, 2026-05-14, 2026-07-08 and 2026-09-07), but the "set it and forget it" delivery layer, the revenue ramp and the time-to-first-dollar are all overstated.
- **Automation is closer to 45-55% than 65%.** Real hidden work: Vapi has 63 status-page incidents in 90 days, silent breaking changes ("agent quit working, no changes on our end"), random tool-call failures, a 14-day call-history purge on pay-as-you-go (you must export transcripts before QA), no self-service cancellation and multi-day support; 10DLC campaigns get rejected on the client's website Terms/Privacy pages and the rejection is cached (a documented 2026-06/07 case needed a support ticket). Per client, plan 3-6 h/month of babysitting on top of the dossier's 7 h/wk total.
- **Real call data contradicts the 300-min/shop model and the value story.** An operator running missed-call answering for 10 businesses logged 774 calls in 20 days (Aug 21-Sep 10, 2026): median call 16 s, 63% under 30 s, 37% hung up when a machine answered, 8.7% spam, only 29% (223) left a real message; 60/60 rounding turned 324 real minutes into 752 billable (2.3x). Corrected per-shop platform cost is ~$15-40/mo (margin better than the dossier says), but the owner sees ~2-3 real messages a day, not a flood of recovered jobs.
- **Demand premise is weaker than the missed-call stats imply.** Jobber's 2026 Home Service Trends report: 80% of surveyed service businesses are fully booked or close to it and only 13% name lead volume as a primary growth constraint; Census BTOS (May 2026): fewer than 20% of firms with four or fewer employees use AI at all. "More booked calls" is not the pain for most of the target segment; after-hours emergency triage and not paying a human are.
- **Pricing ceiling is lower and the field is now venture-scale.** Jobber's native receptionist is $29/mo for 30 conversations ($0.79 each after; $99/mo on Grow per the Aug 2025 press release), Goodcall $79/129/249 (verified July 2026), Smith.ai AI $95-800/mo, Dialzara $29-349, Workiz ships "Genius Answering," and Avoca raised $125M at a $1B valuation (Apr 2026, 800+ customers) targeting exactly HVAC/plumbing/roofing. Corrected sellable band: **$149-249/mo + $250-500 setup**; $499 only with two working integrations and a monthly report.
- **Revenue ramp: the one documented beginner attempt made $0.** A Feb-Mar 2026 "AI receptionist for home services" agency repo (ClawOps) shows 85 prospects sourced, 16 contacted, 0 replies, 0 demos, 0 revenue after ~6 weeks at a $2-3k setup + $400-500/mo pitch, burning ~$112/mo. Vendor-side data says voice-AI agencies see 15-25% monthly churn in year one (Trillet, unverified). Corrected: month-3 $0-250 MRR, month-6 base $250-750 MRR (upside ~$1,500), first dollar at 60-90 days, not 40.
- **Legal: inbound-only is directionally right but the dossier's "FCC said TCPA does not reach inbound" claim is unsourced at the primary level.** FCC 24-17 is confined to voice and to *making* calls; the agent's "immediate callback" is an outbound artificial-voice call and needs documented consent. Two-party recording states are 13 (add Michigan and Delaware to the dossier's list); California's B.O.T. Act is scoped to "online" and unsettled for voice; Utah (May 2024) requires disclosure if asked; Colorado's act took effect Feb 2026. Moffatt v. Air Canada: the company owns what its bot says. Payment-processor rules for this service: no data found.
- **Kill-criteria update:** add "any client whose agent breaks twice in a month from a platform update" and "10DLC campaign not approved within 30 days of go-live." Keep the dossier's outreach criterion but count *replies*, not touches; the documented attempt got zero replies from 16 emails.

## Method and evidence quality

- Session constraint (2026-09-10): the WebSearch budget was already exhausted (200/200) and every vendor, government and review domain (retellai.com, vapi.ai, twilio.com, help.getjobber.com, heyrosie.com, n8n.io, g2.com, docs.fcc.gov, ftc.gov, stripe.com, reddit.com, news.ycombinator.com, cekura.ai, cloudtalk.io, oncrew.ai, sociocs.com) was egress-blocked. GitHub was reachable, so this note relies on **dated snapshots of primary pages that third parties committed to public repositories** plus one operator's production call log. That is a step up from the dossier's search-snippet tier but still not a live fetch.
- Evidence tags: **[V]** a dated snapshot that names the vendor page it was verified against; **[O]** operator production data; **[A]** vendor marketing, guru or Reddit-sourced anecdote; **[E]** my arithmetic. "No data found" is written where nothing usable surfaced.
- Not verified this session: Retell/Vapi terms-of-service text; n8n Cloud pricing; Stripe restricted-business list; Rosie's live pricing page; ServiceTitan/CallRail primary stats; Upwork/Fiverr gig counts; any HVAC/plumbing owner Reddit thread in the original.

## Claim-by-claim

### 1. "Delivery is ~100% machine; the stack produces sellable quality today" - **weakened**

- Retell is the strongest quality signal: G2 4.8/5 on 780 reviews, ~780 ms average latency, $36M ARR (Oct 2025) [A: April 2026 competitor research compiled from TechCrunch/Sacra/G2]. If you build on Retell, callers get a usable agent.
- Vapi is the weak link the dossier treats as interchangeable: Trustpilot 2.3/5 with 83% one-star; status page shows **63 incidents in 90 days (39 major, 24 minor), median 20 minutes**; "the most dangerous reliability issue is not outages, it is platform updates that break working agents without warning"; a June 2025 field-type change "broke all customers with strict type validation for ~30 hours"; custom tools "randomly stop working with 'tool response no result returned'"; end-of-call webhooks intermittently never fire and there is no retry; **"There is no 'set and forget.'"** [V: Lumentra CallAgent gotchas research, verified 2026-03-22 against docs.vapi.ai and community reports].
- Transfers, which the dossier relies on for emergency escalation: "Web-to-phone and PSTN-to-SIP transfers are unsupported and will drop"; "there is no built-in failover mechanism" except in the experimental warm-transfer mode; voicemail detection during transfer only with Google/OpenAI providers; the dynamic-routing webhook must answer in 7.5 s or the transfer fails [V: Lumentra transfer research, 2026-03-22].
- Latency: Vapi's default turn-detection setting adds ~1.5 s of delay until you tune it; typical phone-call end-to-end is ~965 ms, acceptable under 1,500 ms; "Voice sounds robotic when concurrency is pushed" [V: Lumentra voice-quality research, 2026].
- Caller acceptance: 37% of real inbound calls ended within seconds "when a machine answered" [O: Achiya Cohen, 774 calls, Aug 21-Sep 10 2026, Hebrew market]; AnswerConnect claims 31% of consumers would hang up on AI and 85% prefer a human, but sells human answering [A, biased]; Slang.ai reported AI-bypass attempts falling from 33% to 22-25% over a year (Forbes, Oct 2025) [A].
- **Corrected:** sellable only on a platform with Retell-class reliability, with the operator on call for breakage. Treat "100% machine" for steps 9-12 as 85-90% with a standing monthly maintenance budget.

### 2. "Automation ~65% by time; 7 h/wk at 5 shops" - **weakened**

Hidden manual work the dossier's table omits or under-weights:

| Hidden task | Evidence | Est. h/mo at 5 shops [E] |
|---|---|---|
| Re-testing agents after platform updates; debugging silent tool failures | 63 incidents/90 days; "agents break when the platform updates" [V, Vapi] | 4-8 |
| Exporting transcripts/recordings before purge | Vapi PAYG call history retained 14 days, chat 30 days; retention added mid-2025 "with minimal announcement" [V] | 1-2 (or build the n8n export and monitor it) |
| 10DLC campaign rejections tied to the client's website | Real case (2026-06/07): campaign FAILED with errors 30882 (Terms & Conditions URL) and 30908 (privacy policy), re-submission returned the cached rejection in under 30 s, needed a support ticket and edits to the client's WordPress footer [O: Odoo-Migration project memory] | 2-6 per client onboarding; can block the SMS feature for weeks |
| Spam and hang-up triage in owner summaries | 67 spam calls of 774 (8.7%); 284 (37%) no-message hang-ups; the owner-notification message "costs five times more than listening to the entire call" [O] | 1-2 |
| Vendor support latency | "Multi-day response times common. No phone support. No SLA" [V, Vapi]; Bland users report 1+ week [A] | unbudgetable; delays client fixes |
| Account admin | Vapi: "No self-service cancellation... Refund processing can take weeks" [V] | small but real |

- **Corrected:** ~45-55% weighted automation; operator time at 5 shops ~10-12 h/wk including outreach, i.e. the entire side-hustle budget. The dossier's steady-state 7 h/wk holds only on a quiet month with no platform changes.

### 3. "Per-minute unit costs: Retell $0.07/min engine, all-in $0.13-0.31; Vapi $0.05 + at-cost" - **holds** (with two corrections)

- Vapi verified 2026-03-22: "Voice calls $0.05/min", "SMS/Chat $0.005/msg", "$10 on signup (no CC required)", concurrency "10 included, +$10/line/mo", Twilio inbound $0.008/min, Vapi telephony $0.00, HIPAA $1,000/mo (a July 2026 snapshot lists HIPAA $2,000/mo and Zero Data Retention $1,000/mo) [V: Lumentra; Seldon Frame 2026-07-08].
- Retell verified 2026-05-14, 2026-07-08 and 2026-09-07: "$0.07-$0.31/min", voice infra $0.055/min, platform TTS $0.015/min, ElevenLabs voices $0.040/min, LLM $0.003-0.32/min, telephony ~$0.015/min, phone numbers $2/mo, 20 concurrent free then $8/line/mo, knowledge base +$0.005/min, PII removal +$0.01/min, guardrails +$0.005/min, $10 free credit (~60 min) [V: Rezo pricingData 2026-05-14; Seldon Frame 2026-07-08; productarena 2026-09-07].
- Correction 1: Vapi's realistic all-in is "3-6x the advertised $0.05/min" and Reddit users report "$0.05/min for silences", "a 5 min call billed me $10.68 ($2.13/min)" on GPT-4o Realtime, and day-to-day LLM cost swings from $0.01 to $0.08/min [A: r/vapiai via March 2026 teardown]. Budget $0.13-0.35/min on Vapi, $0.09-0.15/min on Retell with GPT-4o-mini.
- Correction 2: the dossier's 300 AI-answered min/shop/mo is unsupported. Operator data: 774 calls across 10 businesses in 20 days = ~116 calls/business/month; 324 real minutes = ~49 real min/business/month but ~113 billable minutes after 60/60 rounding [O]. At $0.11-0.15/min that is **$12-17/shop/mo in platform minutes**, not $45-90. Gross margin at $199 is therefore 85-90%, better than the dossier claims; the catch is in section 5, not here.

### 4. "Tool costs and free tiers are correct" - **weakened** (10DLC and n8n)

- A2P 10DLC: the dossier's "$44 brand + $15 campaign" is the Standard-with-secondary-vetting path (one source lists $46; another lists $4.50 + $41.50). The path a 1-5-truck shop actually needs is **Low-Volume Standard: $4.50 brand registration one-time, $15 campaign vetting one-time, $1.50-10/mo campaign fee** [V: three independent 2026 Twilio-console notes; Vyntechs audit 2026-07-10 explicitly corrects a $59 assumption to $4.50 + $15]. TCR brand vetting takes 1-7 business days, campaign approval is "instant (pending carrier approval)" [V: Telnyx knowledge base]; sole-proprietor brands are limited to 1 campaign, 1 number, low throughput [V]. Net: cheaper than the dossier, but the campaign-rejection loop above is the real cost.
- Twilio: local number ~$1.00-1.15/mo, inbound voice $0.0085/min, outbound $0.014/min [V: Seldon Frame July 2026; Lumentra March 2026]. Holds.
- n8n Cloud: no data found this session (n8n.io blocked); keep the dossier's ~$24/mo as unverified.
- White-label wrappers the dossier calls "no data found": Fusion Calling $99-499/mo with Stripe rebilling; My AI Front Desk white-label $419/mo (wholesale $54.99); Synthflow white-label enterprise-only from ~$30,000/yr (one March 2026 source says $2,000/mo) [V/A: Fusion Calling llms.txt Sept 2026; kai-cmo-harness July 2026; Seldon Frame July 2026]. Vapi's pricing page names no reseller program; Retell names Solution/Creator partner programs with no public terms [V: Seldon Frame, July 2026]. ToS text on reselling: still no data found.

### 5. "Retail band $199-299/mo + $300-500 setup" - **weakened**

- Native/bundled: Jobber Receptionist $29/mo for 30 conversations, $0.79 each after, included on Plus; the Aug 2025 GA press release lists $99/mo for Grow; 200K+ conversations handled at GA [V: help.getjobber.com and PRNewswire via two independent 2026 snapshots; the $29-vs-$99 conflict is unresolved]. Housecall Pro CSR AI quote-only, third-party estimates $200-500/mo; ServiceTitan Contact Center Pro quote-only; **Workiz "Genius Answering"** is a fourth native competitor the dossier missed [V: melanatedintech validation, 2026-08-11].
- Standalone: Goodcall $79/$129/$249 monthly ($66/$108/$208 annual), unlimited minutes, $0.50 per extra unique caller [V: July 2026]; Smith.ai AI receptionist $95-800/mo, ~$1.60-1.90/call, custom training ~$2,000 [V: July 2026, third-party]; Dialzara $29-349/mo, $0.35-0.48/min overage, Trustpilot 4.0 on 19 reviews [V/A: July 2026]; Rosie $49/149/299 [A: July 2026 harness citing heyrosie.com/pricing]; Podium AI Employee $99-399 add-on with real spend $500-800/mo and Trustpilot 1.5/5 on billing disputes [A: replifast 2026].
- Venture entrant: Avoca raised $125M at a $1B valuation (Apr 2026), 800+ customers, "on track to book $1 billion in jobs in 2026," targeting HVAC, plumbing, roofing, electrical [A: Fortune 2026-04-27 and PRNewswire via trend snapshot]. It targets larger shops today, but its sales team will call your prospects.
- **Corrected:** $149-249/mo + $250-500 setup. Expect to be anchored against $29-79. The $499 tier exists only as an integration-plus-reporting retainer.

### 6. "Month-3 base $747 MRR, month-6 base ~$1,650; first dollar ~40 days" - **weakened**

- The only documented beginner attempt found (ClawOps, Feb 19-Mar 2, 2026, selling "AI Receptionist" to home services at $2,000-3,000 setup + $400-500/mo): pipeline 85 prospects sourced, 16 contacted, **0 replied, 0 demos, 0 proposals, 0 closed; revenue to date $0; burn ~$112/mo; cash "effectively $0 (Twilio $15.50 credit)"**; the retrospective blames "B2B sales cycles for $2K-$7.5K products are typically 2-6 weeks" [O: repo sales/pipeline-tracker 2026-02-24 and finance/financial-reality-check 2026-03-02]. Their revenue tracker's $7,500 of "revenue" is template rows. One attempt is not a benchmark, but it is the only non-vendor data point and it is zero.
- Churn: "voice-AI agencies see 15-25% monthly churn year one" [A: Trillet retention blog, vendor, unverified] versus the dossier's ~7%/mo assumption. At 20%/mo you need to sign one new shop a month just to hold five.
- Buyer objection data: "contracts never define 'resolved/booked', attribution disputes" [A: Cekura pricing blog]; "customers quickly churn if agents don't consistently deliver" [A: Euclid VC synthesis of a16z/Bessemer]. Both hit the dossier's recovered-jobs report.
- Demand ceiling: Jobber 2026: 80% fully booked or close; only 13% name lead volume as a constraint; 20% respond to leads within an hour [A: vendor survey]. Housecall Pro AI Advantage (June 2026, n=248, "directional"): 48% active AI use; a featured customer went from 15-20% of callers leaving voicemail to 60-70% leaving details with AI [A]. Census BTOS May 2026: <20% of firms with 4 or fewer employees use AI [V: census.gov via snapshot].
- **Corrected:** month-3 $0-250 MRR; month-6 conservative $0-250, base $250-750, upside ~$1,500 (5 shops at $249 plus setups). First invoice realistically 60-90 days: 2-6 week B2B cycle after the first reply, plus a 2-week pilot, plus 10DLC. Cumulative implied hourly over six months: ~$0-8/hr.

### 7. "Legal risk medium and manageable because inbound-only" - **weakened**

- TCPA/FCC: FCC 24-17 (Feb 2024) holds that AI-generated voices are "artificial or prerecorded" and its holding "is confined to voice" [V: CRM open-knowledge wiki citing docs.fcc.gov/FCC-24-17A1.pdf]. No primary source found for the dossier's "FCC has said the TCPA does not reach technologies used to answer inbound calls" (aiemply is a vendor blog). The safer framing: the TCPA restricts *making* calls with an artificial voice; answering is outside it, but the dossier's own "immediate callback the caller just asked for" is an outbound artificial-voice call to a cell and needs prior express consent, so log the caller's request verbatim.
- Bot disclosure: California B.O.T. Act is keyed to "online" (public-facing website, web app, digital app); whether it reaches a voice call is "unsettled, with no case law or Attorney General opinion" [V: CRM wiki]. Utah (enacted May 2024): regulated businesses disclose at start, others "must disclose if asked"; Colorado enacted Feb 2026; California AI Transparency Act (Jan 2026) applies to providers with 1M+ users, not you; pending 2025: Alabama HB 516, Hawaii HB 639, Illinois HB 3021, Maine HP 1154, Massachusetts SB 243 [V: amplifier-voice legal findings, Jan 2026]. The dossier's disclose-everywhere fix still holds.
- Recording consent: **13** two-party states (CA, CT, DE, FL, IL, MD, MA, MI, MT, NV, NH, PA, WA); "when a call crosses state lines, the more restrictive state law applies" [V: Jan 2026]. The dossier lists 11-12 and omits Michigan.
- Liability: "The company owns what its bot says" (Moffatt v. Air Canada) [V: CRM wiki]. Put the hallucinated-quote risk in the client contract and in the agent's guardrails (Retell charges +$0.005/min for guardrails).
- Platform terms: Vapi's retention policy "was added mid-2025 with minimal announcement. Not clearly documented in ToS initially" [V]. Vapi's HIPAA mode "disables call log storage, recording review, and transcript access" [V]. Cancellation "must go through support" [V].
- Payment processors (Stripe restricted categories for telecom/AI services): no data found. Copyright of AI output: not a revenue factor; unchanged. Tax: nothing specific found beyond ordinary self-employment treatment; no data found.

### 8. "Retell/Vapi have no white-label; partner programs have no public terms" - **holds**

Confirmed in the July 2026 Seldon Frame audit of vapi.ai/pricing and retellai.com/pricing. Wrappers priced in section 4.

## Corrected numbers (summary)

| Item | Dossier | Corrected | Basis |
|---|---|---|---|
| Automation share | ~65% | 45-55% | sections 1-2 |
| Operator hours at 5 shops | ~7 h/wk | 10-12 h/wk | section 2 |
| Platform minutes per shop | 300/mo, $45-90 | ~110 billable/mo, $12-17 (Retell) to $15-40 (Vapi) | [O] Cohen 2026-09-10 |
| Gross margin at $199-249 | 60-85% | 85-90% before your time | [E] |
| Real messages per shop | not stated | ~2-3/day; 37% hang-ups, ~9% spam | [O] |
| 10DLC one-time | $44 + $15 | $4.50 + $15 (Low-Volume Standard), $1.50-10/mo | [V] |
| Retail price | $199-299 | $149-249 | section 5 |
| Setup fee | $300-500 | $250-500 | section 5 |
| Monthly churn | ~7% | 15-25% (vendor claim) | [A] Trillet |
| Month-3 MRR (base) | $747 | $0-250 | section 6 |
| Month-6 MRR (base) | ~$1,650 incl. setup | $250-750 | section 6 |
| Time to first dollar | ~40 days | 60-90 days | section 6 |
| Two-party recording states | 11-12 | 13 | [V] |

## What would change the verdict back to "holds"

- A live fetch of retellai.com/pricing and vapi.ai/pricing confirming the snapshot figures (likely; every snapshot agrees).
- Three or more independent operator reports (not vendor case studies) of a solo reseller holding 5+ trade shops for 6+ months with under 10% monthly churn.
- Primary ServiceTitan/CallRail pages showing that the 62%/78% figures apply to 1-5-truck shops rather than to all contractor lines.
- Evidence that Jobber/Housecall Pro/Workiz native receptionists are failing in the field (support complaints, churn), which would reopen the off-platform wedge.

## Sources

Primary-page snapshots and operator data found on GitHub (all fetched 2026-09-10)
- [Achiya Cohen: AI phone-agent cost analysis, 774 calls, Aug 21-Sep 10 2026 (published 2026-09-10)](https://github.com/achiya-automation/safari-mcp/blob/29af3b9f87f6cc85e11d35766898ef78aa4abdc1/ai-call-cost-il-2026-09-10.html)
- [Lumentra CallAgent: Vapi pricing deep dive, verified 2026-03-22 against vapi.ai/pricing and retellai.com/pricing](https://github.com/Lumentra-AI/CallAgent/blob/4bc844ab50f428e1f5cd5105745394cfde862c85/docs/research/vapi-pricing-deep-dive-2026.md)
- [Lumentra CallAgent: Vapi gotchas and limitations 2026 (incidents, breaking changes, retention, support, Trustpilot)](https://github.com/Lumentra-AI/CallAgent/blob/4bc844ab50f428e1f5cd5105745394cfde862c85/docs/research/vapi-gotchas-limitations-2026.md)
- [Lumentra CallAgent: Vapi call-transfer capabilities 2026](https://github.com/Lumentra-AI/CallAgent/blob/4bc844ab50f428e1f5cd5105745394cfde862c85/docs/research/vapi-call-transfer-capabilities-2026.md)
- [Lumentra CallAgent: Vapi human-like voice quality and latency 2026](https://github.com/Lumentra-AI/CallAgent/blob/4bc844ab50f428e1f5cd5105745394cfde862c85/docs/research/vapi-human-like-voice-quality-2026.md)
- [Lumentra CallAgent: Telephony provisioning 2026 (Twilio/Telnyx/SignalWire, 10DLC)](https://github.com/Lumentra-AI/CallAgent/blob/4bc844ab50f428e1f5cd5105745394cfde862c85/docs/research/telephony-provisioning-2026.md)
- [Seldon Frame: competitor pricing facts spec, verified 2026-07-08 (Retell, Vapi, Goodcall, Smith.ai, Synthflow)](https://github.com/seldonframe/seldonframe/blob/3f386a221849843a1a535f442e210bf9d293fff9/docs/superpowers/specs/2026-07-08-competitor-pricing-facts.md)
- [Seldon Frame: competitor-pricing registry, verified July 2026](https://github.com/seldonframe/seldonframe/blob/3f386a221849843a1a535f442e210bf9d293fff9/packages/crm/src/lib/seo/competitor-pricing.ts)
- [Seldon Frame: voice AI reseller programs guide (Vapi, Retell, Synthflow), July 2026](https://github.com/seldonframe/seldonframe/blob/3f386a221849843a1a535f442e210bf9d293fff9/packages/crm/src/lib/seo/guides/voice-ai-reseller-programs.ts)
- [Seldon Frame: how much to charge for an AI agent (Ruby, Twilio, Claude cost floors)](https://github.com/seldonframe/seldonframe/blob/3f386a221849843a1a535f442e210bf9d293fff9/packages/crm/src/lib/seo/guides/how-much-to-charge-for-an-ai-agent.ts)
- [ProductArena voice-agent pricing.json, fetched 2026-09-07 (Retell, Vapi, Bland, ElevenLabs, LiveKit, Pipecat)](https://github.com/ultrametricai/productarena/blob/f5d2ab5c7f318f070d4c5872427a59b921458c52/data/voice-agents/pricing.json)
- [Rezo competitor pricingData.js, last verified 2026-05-14 (Retell, Vapi, Bland)](https://github.com/bhavtoshupadhyay-rezo/Rezo-Competitors-Insights/blob/7923b6cdd88bc8db05031fca72d179e712640d53/src/data/pricingData.js)
- [kai-cmo-harness: voice-agent market evidence, July 5 2026 (Rosie, Goodcall, Smith.ai, Dialzara, Jobber, Podium, churn, objections)](https://github.com/cgallic/kai-cmo-harness/blob/90ef27157baba0c71cfd6d0c376f0a18eeec2c84/workspace/strategy/voice-agent-differentiation/_market-evidence.md)
- [melanatedintech: automation strategy deep validation 2026-08-11 (Jobber/HCP/Census figures, Workiz)](https://github.com/asjames18/melanatedintech/blob/0bcdb2fc10d1648ebbe713c4ef296660d402bd35/docs/MIT-automation-strategy-deep-validation-2026-08-11.md)
- [Voiqur: voice AI competitor research, April 2026 (Retell G2 4.8/780, ARR, Bland price jump, complaints)](https://github.com/ja3ooni/voiqur-platform/blob/8737526f7840638e3e6be4846be40dfd5ed0a401/kiro/voiquyr/docs/Perplexity/voice_ai_competitors_research.md)
- [ClawOps competitor teardown 2026-03-01 (r/vapiai billing complaints)](https://github.com/rickclaw08/claw-systems/blob/3fa61252f449584a3d3ba7d647700d5531c20f69/claw-agency/research/competitor-teardown-2026-03-01.md)
- [ClawOps sales pipeline tracker, 2026-02-24 (0 replies, 0 closed)](https://github.com/rickclaw08/claw-systems/blob/3fa61252f449584a3d3ba7d647700d5531c20f69/claw-agency/sales/pipeline-tracker.md)
- [ClawOps financial reality check, 2026-03-02 ($0 revenue)](https://github.com/rickclaw08/claw-systems/blob/3fa61252f449584a3d3ba7d647700d5531c20f69/claw-agency/finance/financial-reality-check-2026-03-02.md)
- [Vyntechs shop-OS audit 2026-07-10 (Twilio Low-Volume Standard $4.50 + $15)](https://github.com/Vyntechs/VynTechs_Auto/blob/5eda519a114cea4968672e9ecd717a819e99022e/docs/strategy/2026-07-10-shop-os-audit.md)
- [Twilio SMS pricing notes (Low-Volume Standard $4.50 / $15 / $1.50-mo; Standard with vetting $46)](https://github.com/nalotiavaibhav/Automation/blob/a691eeef500e249edb2c54c77c1bdfe7567b6b8e/pricing/sms-twilio-pricing.md)
- [Twilio A2P campaign resubmission notes ($4.50 / $15 / $1.50-10 monthly)](https://github.com/honerlaw/financials/blob/f69460b339f4dd318ee22e1ab8a75aab8db61a55/docs/twilio-a2p-campaign-resubmission.md)
- [Window and Solar Care Odoo migration memory: 10DLC campaign rejected on Terms/Privacy, cached verdict, 2026-06/07](https://github.com/windowandsolarcare-hash/Odoo-Migration/blob/f8fc68e4fbc7ccea1aa8669f8e696c6e8c6b9cc6/memory/project_twilio_a2p_and_entity.md)
- [Telnyx knowledge base: 10DLC messaging part 1 (vetting 1-7 business days, sole-proprietor limits)](https://github.com/team-telnyx/knowledge-base/blob/a9f403558d26ff0c40d7ffaaf1c76a3edeb392e9/wiki/dev-docs/10dlc-messaging--part-1.md)
- [CRM open knowledge wiki: customer-facing AI agents (FCC 24-17 scope, California B.O.T. Act, Moffatt v. Air Canada)](https://github.com/jacquescorbytuech/crm-open-knowledge-wiki/blob/4919c3bbcb8f92a6590cfb6ed34a3e71cd6c5ed7/foundations/customer-facing-ai-agents.md)
- [amplifier-voice: legal considerations, Jan 2026 (state AI-disclosure table, 13 two-party states, TCPA penalties)](https://github.com/bkrabach/amplifier-voice/blob/b7850eb19a5aa7ba1f1d79027885b0013dd20069/ai-context/research/findings/59-legal-considerations.md)
- [Fusion Calling llms-full.txt (white-label $99-499/mo; Synthflow ~$30k/yr, June-Sept 2026 audits)](https://github.com/MrAlaminH/FusionCalling/blob/efd9e8316bcf5989444c0a5a4fa11d6790b38a05/public/llms-full.txt)
- [Anton trend snapshot 2026-05-08 (Avoca $125M at $1B, Fortune 2026-04-27)](https://github.com/denagyantal/anton/blob/19294124f7144c463372403703ea06e3b92fa77a/ideas/raw/trends-2026-05-08.md)
- [gladiusturf competitor intel (Jobber AI Receptionist GA Aug 2025, $99/mo Grow add-on, 200K+ conversations)](https://github.com/wewillwin2026/gladiusturf/blob/b1275df997ad6bcca6cdff5963ef1c717217f5a8/content/competitor-intel-v2.md)

Primary pages named by those snapshots (not fetchable this session)
- [Vapi pricing](https://vapi.ai/pricing)
- [Retell AI pricing](https://www.retellai.com/pricing)
- [Jobber Help: Receptionist powered by Jobber AI](https://help.getjobber.com/hc/en-us/articles/25315927533847-Receptionist-powered-by-Jobber-AI)
- [PRNewswire: Jobber launches AI-powered receptionist (Aug 2025)](https://www.prnewswire.com/news-releases/jobber-launches-ai-powered-receptionist-to-answer-calls-and-texts-for-busy-home-service-businesses-302531125.html)
- [Jobber 2026 Home Service Trends report](https://www.getjobber.com/home-service-trends-report/)
- [Housecall Pro: The AI Advantage report, June 2026 (PDF)](https://www.housecallpro.com/wp-content/uploads/2026/06/062026-HCP-The-AI-Advantage-report.pdf)
- [Census Bureau: AI use by businesses, May 2026](https://www.census.gov/library/stories/2026/05/ai-use-businesses.html)
- [Fortune: Avoca AI agents for missed calls in HVAC, plumbing, roofing (2026-04-27)](https://fortune.com/2026/04/27/avoca-ai-agents-missed-calls-hvac-plumbing-roofing-kleiner-perkins-chen-shrivastava-braswell/)
- [PRNewswire: Avoca raises $125M at $1B valuation](https://www.prnewswire.com/news-releases/avoca-raises-125m-at-1b-valuation-to-power-americas-services-economy-with-ai-302753962.html)
- [Goodcall pricing](https://www.goodcall.com/pricing)
- [Smith.ai AI receptionist pricing](https://smith.ai/pricing/ai-receptionist)
- [Dialzara pricing](https://dialzara.com/pricing)
- [Rosie pricing](https://heyrosie.com/pricing)
- [My AI Front Desk white-label](https://www.myaifrontdesk.com/white-label)
- [Replifast: Podium pricing 2026 (Trustpilot 1.5/5)](https://www.replifast.com/blog/podium-pricing-2026)
- [Trillet: voice-agent client retention strategies (15-25% monthly churn claim)](https://trillet.ai/blogs/voice-agent-client-retention-strategies)
- [Cekura: how to price AI voice agents (attribution disputes)](https://www.cekura.ai/blogs/how-to-price-ai-voice-agents)
- [Euclid VC: what's working in vertical voice AI](https://insights.euclid.vc/p/whats-working-in-vertical-voice-ai)
- [AnswerConnect: consumers turning away from AI customer service (vendor, biased)](https://www.answerconnect.com/blog/news/consumers-turning-away-from-ai-customer-service/)
- [Forbes: AI voice recognition ROI, Slang.ai (2025-10-02)](https://www.forbes.com/sites/quickerbettertech/2025/10/02/ai-voice-recognition-roi/)
- [FCC Declaratory Ruling FCC 24-17 (PDF)](https://docs.fcc.gov/public/attachments/FCC-24-17A1.pdf)
- [Twilio US SMS pricing](https://www.twilio.com/en-us/sms/pricing/us)
- [Twilio A2P 10DLC campaign registration guide](https://help.twilio.com/hc/en-us/articles/1260803965530-A2P-10DLC-Campaign-Registration-Guide)
