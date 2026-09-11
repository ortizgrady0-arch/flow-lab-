---
title: "Inbound AI front desk for 1-5-truck HVAC, plumbing and electrical shops"
tags: [research, candidate, ai-front-desk-home-services]
updated: 2026-09-11
status: dossier
slug: ai-front-desk-home-services
---

# Inbound AI front desk for 1-5-truck HVAC, plumbing and electrical shops

Voice receptionist (Retell/Vapi) for after-hours and overflow calls + missed-call text-back + n8n intake-to-booking pipeline, sold flat at $199-499/mo per shop plus a $250-1,000 setup fee. Inbound only. Related: [[research/shortlist]] · [[research/saturated-overhyped]] · [[research/lenses/local-smb-services]] · [[research/lenses/emerging-2026]] · [[decisions/comparison-matrix]]

## TL;DR

- **Pain is the best-evidenced in the whole portfolio, but every figure is second-hand.** ServiceTitan's 50k-line analysis (62% of home-service calls missed; 47% of calls arrive outside business hours; HVAC after-hours calls +45% Oct->Jun) and CallRail's Sept 2025 consumer survey (n=1,000: 78% abandoned a business after an unanswered call, 82% would call a competitor) are cited consistently across a dozen 2026 vendor blogs, and a Feb 2026 LSA dataset ($6.72M spend, 888 contractors) puts a replacement lead at $51-57. No primary page could be fetched this session (all vendor domains egress-blocked, search budget exhausted), so treat numbers as [S] snippet-level until re-verified.
- **The retail price you can charge is already capped by SaaS at $29-299/mo** (Dialzara $29 unlimited; Rosie $49/149/299 for 250/1,000/2,000 min; Goodcall $79/129/249; Jobber's native Receptionist $29/mo for 30 conversations or free on the $389 Plus plan; Housecall Pro CSR AI quote-only). A solo reseller wins only on setup, trade-specific call flow, CRM/calendar integration, and being the local human who fixes it, so the realistic band is **$199-299/mo + $300-500 setup**, with $499 reserved for shops with 2+ integrations.
- **Unit economics hold:** Retell $0.07/min engine, all-in $0.13-0.31/min; Vapi $0.05/min platform + at-cost components, all-in $0.10-0.30/min. A shop consuming 300 AI-answered min/mo costs $40-95 in platform fees against $249 retail = **60-85% gross margin**, before your time. Fixed overhead before clients is ~$50/mo.
- **Automation ~65% by time (my weighting), not 85%.** Delivery (answering, booking, SMS, owner alert, reporting, billing) is ~100% machine; the operator's hours are almost entirely sales, onboarding (6-10 h per shop the first time, ~4 h once templated), transcript QA and support. At 5 shops the steady state is ~7 h/wk of operations, leaving the rest of the 10-15 h for outreach, which is the binding constraint.
- **Economics for the profile:** startup ~$150 (test minutes, Twilio number, 10DLC registration, domain, n8n VPS); first dollar in ~40 days (setup fee from shop #1 after a 2-week free pilot); month-6 revenue conservative $500 / base ~$1,650 / upside ~$3,200 per month; implied hourly at base ~$25-30 by month 6, near zero for the first 8 weeks.
- **Legal risk is medium and manageable because it is inbound-only:** the FCC's Feb 2024 ruling (AI voice = "artificial or prerecorded" under TCPA) governs outbound calls and, per compliance counsel, the TCPA does not reach technology used to answer inbound calls. What still applies: all-party recording consent in 11-12 states, bot-disclosure laws (California, Utah, Colorado, more coming), and never letting the agent place marketing callbacks. Fix: disclose "AI assistant, call may be recorded" in the greeting, everywhere.
- **Biggest structural threat is bundling, not competitors like you:** Jobber ($29 add-on), Housecall Pro (CSR AI), ServiceTitan (Virtual Agent, quote-only, enterprise-priced) now ship native AI receptionists. Your defensible customer is the 1-5-truck shop that is not on those suites or is on their cheap tier, which is most of the ~118k HVAC contractors (IBISWorld 2025) plus plumbing and electrical.
- **Verdict: go, as a services play with a sales-first plan.** Scores: demand 8, automation 6, economics 6, low-risk 6, solo-fit 7. Kill criteria: fewer than 2 paying shops after 60 days of 30+ local touches/week, or first-pilot transcripts showing under ~80% correct intake on real calls.

## Method and evidence quality

- Web work this session (2026-09-10): 21 WebSearch queries returned before the session-wide search cap (200/200) was hit; all ~45 WebFetch attempts to primary pages (Retell, Vapi, Rosie, Goodcall, Dialzara, Smith.ai, Twilio, CallRail, ServiceTitan, Jobber, Housecall Pro, n8n, IBISWorld, Henson Legal, Trillet, and others) were blocked by the egress proxy, and curl was blocked too.
- Evidence tags used below: **[S]** figure quoted in a search snippet from the named source (page not opened); **[A]** anecdotal, vendor marketing, or guru claim; **[E]** my estimate or arithmetic. Nothing here is a verified platform report in the strict sense; the pricing figures are corroborated by 2-4 independent 2026 comparison sites each, which is the strongest tier available this session.
- Items not researched or not found this session: Upwork/Fiverr listing counts and rates for Retell/Vapi builds; Synthflow and Vapify white-label price sheets; Retell/Vapi terms of service text; published churn benchmarks for AI receptionists; IBISWorld counts for plumbing and electrical contractors; average job-ticket values from a primary source; named YouTube "voice AI agency" case studies. Each is marked "no data found" where it matters.

## 1. Demand evidence

**Who pays:** owner-operators of residential HVAC, plumbing and electrical companies with 1-5 trucks, where the owner or a spouse answers the phone and cannot while on a job. The buyer's alternative is voicemail, a human answering service ($255-1,275/mo human-hybrid [S: getaira, getnextphone 2026] or Smith.ai human from $292.50/mo for 30 calls [S: marblism 2026]), or a SaaS receptionist ($29-299/mo, see section 3).

**Missed-call pain (the core claim)**
- 62% missed-call rate across home services, from ServiceTitan's analysis of 50,000+ contractor phone lines [S: contractorincharge.com, dialfyne.com, calljolt.com, agentzap.ai, all 2026, each citing ServiceTitan]. This is the most-repeated number in the category; the underlying ServiceTitan page was not fetched.
- 47% of home-service calls arrive outside standard business hours [S: ServiceTitan via agentzap.ai 2026]. ServiceTitan State of the Trades: HVAC residential after-hours calls jump 45% from October to June [S: servicetitan.com/toolbox, 2026 snippet].
- Even during open hours, 25-30% of inbound calls go unanswered in high-volume windows (lunch, evenings, surge days) [S: calljolt/ainora 2026, attributing to ServiceTitan]; HVAC and plumbing companies lose 40-55% of after-hours and overflow calls to voicemail [S: cloudtalk.io best-AI-voice-agent-for-plumbers, 2026, unattributed vendor figure].
- CallRail Sept 2025 survey of 1,000 US consumers: 78% have abandoned a business after an unanswered call; 82% would call a competitor [S: quo.com, oncrew.ai, ainora.lt, pcnanswers.com 2026, all citing CallRail]. oncrew.ai explicitly notes this is one of the few missed-call stats with a verifiable source.
- Booking benchmarks: ServiceTitan average residential CSR book rate 65-75%, top call centers >85%, weak ones <50% [S: agentzap 2026]; average booking rate near 38% when calls are answered "and handled properly" appears in the same snippet set with unclear provenance [S].
- Two 2026 "studies" are worth pulling when fetch works again: Higrovi "2026 Contractor Missed Call Report, 4.2M calls analyzed" and PCN "2026 Small Business Missed Call Revenue Study" [S: titles only; methodology not seen].

**What a missed call is worth (replacement cost)**
- Google Local Services Ads, Feb 2026 analysis of $6.72M spend across 888 home-service contractors: $53 average CPL; HVAC $51 (range $25-80), plumbing $57 with a 44.5% book rate; most contractors pay $20-80/lead; water-damage restoration up to $150 [S: skillmammoth.com, searchlightdigital.io, thevalleymarketinggroup.com, 2026]. Google Search Ads CPL for plumbing ran $55-183 in the earlier lens work [S: webtonic.io 2026].
- Vendor arithmetic: emergency service calls average $400-1,500 in revenue, so an agent pays for itself in 4-6 weeks for shops doing $30k+/mo [A: cloudtalk.io 2026]. Job-value figures from a primary source: no data found.

**Market size proxies**
- 118,433 US heating and air-conditioning contractor businesses in 2025, +2.3% YoY [S: IBISWorld]. Plumbing and electrical counts: no data found this session (an older 2020 figure of ~990k combined plumbing+HVAC establishments appears in ConsumerAffairs; treat as stale).
- AI receptionist market $2.7B (2025) forecast to $31.4B by 2035 at 27.8% CAGR [S: market.us, 2026]; the "virtual receptionist" market $4.64B in 2026 [S: brilo.ai/sci-tech-today, 2026]. Analyst-report numbers; directional only.

**Trend direction 2024 -> 2026**
- Plumbing AI adoption 7% (2024) -> 19% (2026); 38% of commercial HVAC contractors report measurable AI impact, up from 17% in 2025 [S: pipelineon.com 2026, survey source not named].
- US small-business AI adoption 39% (2024) -> 55% (2025) [S: brilo.ai citing an SMB survey]; US Chamber 2026 says 89% use AI in some form but paid operational use is only 17-20% (Census BTOS May 2026, JPMC Institute Dec 2025) [S: carried from [[research/lenses/local-smb-services]]]. Read: awareness high, wallets mostly closed, pitch "recovered jobs" not "AI".
- Supply-side signal: Y Combinator funded Acrely, "the AI customer service representative for home services" [S: ycombinator.com launch page, 2026], and Jobber/Housecall Pro/ServiceTitan all shipped native AI answering between 2025 and 2026 (section 4). The category is being validated and commoditized at the same time.

**Seasonality (strong, and it is your sales calendar)**
- HVAC peak-week call volume runs 2-4x the annual daily average in first heat waves (June/July); a 5-truck shop that handles 20-30 calls/day can see 60-100+ on the first extreme-heat day; HVAC companies miss 30%+ of calls in summer and winter peaks [S: kaicalls.com, callexperts.com, titanprotechnologies.com 2026]. Some vendors claim +340% peak vs. spring [A].
- Implication [E]: sell HVAC in March-May and September-October (before the June and December spikes), plumbing year-round with a winter freeze angle, electrical steadily. Expect churn attempts in the shoulder months when the owner "can answer the phone myself again"; the text-back and booking pipeline are what keep the subscription through the trough.

## 2. Who pays and how much (observed pricing benchmarks)

All prices are 2026 list prices as reported by independent comparison sites; the vendors' own pages were not fetched.

| Product / benchmark | Price | Notes | Source |
|---|---|---|---|
| Dialzara | from $29/mo, unlimited calls | cheapest flat rate seen | [S: marblism.com 2026] |
| Rosie (heyrosie.com) | $49/mo 250 min; $149/mo 1,000 min; $299/mo 2,000 min | $49 tier does not book in-call; $149 adds booking, warm transfer, mid-call SMS; $299 adds document training, white-glove onboarding; 7-day trial; calls round up to full minute | [S: cloudtalk.io, oncrew.ai, serviceagent.ai 2026] |
| Goodcall | $79 / $129 / $249 per mo | 100/250/500 unique callers, unlimited minutes, $0.50 per extra caller, ~17% off annual | [S: cloudtalk.io, serviceagent.ai, xpay.sh 2026] |
| OnCrew | $49/mo, 100 calls, $0.99/call overage | contractor-targeted | [S: nextiva/oncrew 2026] |
| Jobber Receptionist (native) | $29/mo add-on, 30 conversations, $0.79 each after; unlimited on Plus ($389/mo) | spam/no-conversation calls do not count | [S: help.getjobber.com, myquoteiq 2026] |
| Housecall Pro CSR AI (native) | quote-only; third parties estimate $349-689/mo incl. Essentials plan | HCP Assist live answering priced by coverage | [S: projul.com, nextiva 2026] |
| ServiceTitan Virtual Agent | quote-only, requires Phones/Contact Center Pro; $4,500-10,000+/mo all-in for 20+ employee shops | not your customer | [S: nextiva 2026] |
| Smith.ai | AI receptionist from $95/mo; human from $292.50/mo for 30 calls | 2-5 business days script setup | [S: marblism 2026] |
| Human-hybrid answering services | $255-1,275/mo, $7-11 per-call overage | | [S: getaira, getnextphone 2026] |
| Agency resale to HVAC/plumbing/roofing | $297-797/mo at 60-80% margins | agency-platform marketing | [A: trillet.ai 2026] |
| Direct-to-business AI receptionists vs human | $200-700/mo vs $1,500-3,000/mo human receptionist | | [A: mostailabs 2026] |
| White-label platform for agencies | VoiceAI Connect $199/mo flat | | [S: myvoiceaiconnect pricing, from lens note] |
| "Most small businesses pay" | $99-499/mo | vendor pricing guides | [S: getaira, agentzap, callbirdai 2026] |

**Pricing conclusion [E]:** a 1-5-truck shop will benchmark you against Rosie $149 and Goodcall $129-249. Charge $199-299/mo for "voice + text-back + booking into your calendar/CRM + a human who answers when it breaks," and $300-500 setup (an owner will pay a setup fee for a working phone tree; SaaS trials do not give them that). The $499 tier only clears when you integrate Jobber/Housecall Pro/ServiceTitan APIs and deliver a weekly recovered-jobs report. Setup fees are the fastest cash; recurring is the asset.

**Marketplace rate cards for the build work itself:** no data found this session (Upwork/Fiverr searches were not executed before the cap). The earlier lens note recorded n8n/Make builders at $40-100/hr on Upwork, senior $125-250+ [S: ciela.ai 2026]; use that for the setup-fee floor.

## 3. Competition and saturation

- **Direct SaaS competitors visible to the buyer (10+ named in 2026 roundups):** Rosie, Goodcall, Dialzara, OnCrew, Smith.ai, My AI Front Desk, AIRA ($24.95), Avoca, Newo.ai, RingReady, CallBird, Voksha, NextPhone, ServiceAgent, plus the suite-native ones (Jobber, Housecall Pro, ServiceTitan). Every one of them publishes an "AI receptionist for HVAC/plumbers" blog, so the SEO lane is fully saturated; the 2026 roundups are mostly vendors ranking themselves [S: cloudtalk, voksha, serviceagent, revved.digital, pipelineon, marblism 2026].
- **Price compression is real and dated:** entry tiers fell to $29-49/mo in 2026 (Dialzara $29, Jobber $29, Rosie $49, OnCrew $49) versus the $149-299 flat tier that defined 2025 [S: same sources; earlier lens note recorded $149-299 as the flat band in 2025-early 2026]. Goodcall's plans were $59 in the earlier lens note and $79 in this session's 2026 snippets, so not every vendor is cutting.
- **Reseller/agency side:** Retell and Vapi are infrastructure with no native white-label; Retell names a "Solution Partner Program" and "Creator Partner Program" with no public terms; Vapi's pricing page names no reseller program at all; agency-oriented wrappers (Trillet, Synthflow, Convocore, Vapify, VoiceAI Connect) exist and pitch "flat pricing, compliance bundled" as of June 2026 [S: trillet.ai, seldonframe.com, famulor.io, buildwithhermes.com 2026]. The number of agencies doing this: no data found; the volume of "best voice AI platform for agencies" content implies many entrants.
- **Guru saturation:** the generic "AI automation / AI voice agency" pitch is flagged saturated in [[research/saturated-overhyped]] (buyer skepticism, churn when no metric moves). This dossier's offer is the skeptic's prescribed form: one vertical, one measurable outcome (booked jobs from previously missed calls), one template.
- **What differentiates winners (from the comparison content and case studies, [S]/[A]):** (1) in-call booking that writes to the shop's actual calendar/CRM rather than an SMS link (Rosie only does it at $149+; Jobber's native one does it only inside Jobber); (2) trade-specific triage (no-heat/no-cool/burst-pipe escalation, service-area rules, pricing guidance); (3) integration depth with ServiceTitan/Housecall Pro/Jobber (oncrew.ai 2026 guide treats this as the buying criterion); (4) recovered-revenue reporting; (5) a human who picks up when the owner calls angry. None of these are things a $29 SaaS tier does for a shop that has never configured software.
- **Platform flooding of your acquisition channel:** contractors receive AI-receptionist cold pitches constantly (every vendor above runs outbound). Local, in-person, referral-based acquisition is the only uncrowded channel a solo operator has, which is also the slowest.

## 4. Automation map

Assumes steady state of 5 paying shops plus 1 new shop per month, ~300 AI-answered minutes per shop per month. Hours are manual-equivalent per month; automation share is my estimate of how much of that time the machine absorbs [E].

| # | Step | Level | Tools (monthly cost) | Manual-equiv h/mo | Auto % | Quality risk |
|---|---|---|---|---|---|---|
| 1 | Build prospect list (shops with no CSR, 1-5 trucks, poor Google-review response times) | assisted | Google Maps + Apify/n8n scrape, Claude to score ($0-20) | 4 | 75% | stale numbers, wrong contact |
| 2 | Outreach: walk-ins, phone calls, referral asks, short personalized emails | manual | Claude drafts scripts/emails ($20 Claude Pro shared) | 16 | 30% | inbound-only pitch; no cold SMS, no cold AI calls (TCPA) |
| 3 | Demo: prospect calls your demo line; the agent demos itself | assisted | Retell/Vapi demo agent (~$5 test minutes) | 3 | 50% | latency or a bad turn kills the sale |
| 4 | Discovery: hours, service area, emergency rules, calendar, CRM | manual | call + Claude-generated intake form | 1.5 | 0% | wrong scoping leads to churn |
| 5 | Build agent: system prompt, knowledge base, booking tool, transfer rules | assisted | Claude drafts from template; Retell/Vapi builder | 4 | 50% | hallucinated pricing/promises |
| 6 | Telephony: Twilio number, conditional call forwarding on the shop's carrier, 10DLC campaign for the shop's SMS | manual | Twilio number ~$1.15/mo, 10DLC $44 brand + $15 campaign + $1.50-10/mo per shop [S: sociocs, ghlscaleup 2026] | 2 | 10% | carrier forwarding quirks; 10DLC approval delay |
| 7 | Test calls and tuning (20-50 scripted scenarios) | assisted | Retell simulation/test features, Claude to generate scenarios | 3 | 40% | edge cases: rentals, commercial, angry callers |
| 8 | Owner training and go-live | manual | Loom walkthrough | 1 | 0% | owner ignores SMS summaries |
| 9 | Answer calls 24/7, capture name/address/problem/urgency, offer windows | full | Retell $0.07/min + LLM + telephony = $0.13-0.31/min; Vapi $0.05 + components = $0.10-0.30/min [S: cekura, cloudtalk, layer3labs, zeeg 2026] | 25 | 100% | mis-transcribed addresses; interruption handling; accents |
| 10 | Book to calendar / CRM (Google Calendar, Jobber, HCP API) | full | n8n self-host $4-7/mo or cloud ~$23-24/mo Starter [S: nocode.mba, openhosst, expresstech 2026] | 5 | 100% | double-booking, timezone bugs |
| 11 | Missed-call text-back and two-way SMS follow-up | full | Twilio SMS + Claude API (pennies/conversation) | 5 | 100% | 10DLC blocks unregistered traffic; opt-out handling |
| 12 | Owner alert (SMS/email) and emergency warm transfer | full | Twilio, Retell transfer | 2 | 100% | transfer fails after hours; define fallback |
| 13 | Transcript QA: review flagged/failed calls, retune | assisted | Retell post-call analysis + n8n auto-flag + Claude summaries | 7.5 | 40% | this is where quality is made or lost |
| 14 | Weekly/monthly recovered-jobs report | full | n8n + Claude -> email/PDF | 2.5 | 90% | over-claiming attribution |
| 15 | Billing: Stripe subscription + setup invoice | full | Stripe (2.9% + $0.30) | 1 | 95% | failed cards |
| 16 | Support and escalations | manual | phone/SMS | 2.5 | 20% | owner expects instant human response |
| | **Total** | | | **85 h** | **~66% weighted** | |

Weighted automation ~ **65%** (56 of 85 manual-equivalent hours absorbed by the machine). Operator hours remaining ~29 h/mo (~7 h/wk) at 5 shops including outreach; more outreach time is the only way to grow. Earlier lens notes estimated 55% (emerging-2026) and 70% (local-smb-services); this table sits between them.

## 5. Economics

**Startup (one-time) [E, priced from [S] sources]**
- Retell/Vapi test minutes beyond the $10 free credit (about 67-90 min at production rates [S: cekura 2026]): $30
- Twilio number ($1.15/mo) + $20 SMS/voice credit: $22
- A2P 10DLC brand registration $44 + one campaign vetting $15 (for your own text-back demo; each client shop registers its own brand, billed into the setup fee): $59 [S: sociocs.com, ghlscaleup 2026]
- n8n: self-host on a $5-7/mo VPS (or n8n Cloud Starter ~$23-24/mo): $7 first month
- Domain + one-page site with the demo number: $15
- Claude Pro or ChatGPT (already paying, per profile): $0-20
- **Total: ~$135-155.** Cash reserve for the first month's per-minute fees on a free pilot: ~$40. Well under the $500 cap.

**Monthly tool cost**
- Fixed overhead before clients: Claude $20 + n8n VPS $7 + Twilio number $1.15 + demo minutes ~$10 + Stripe $0 = **~$40-50/mo**.
- Variable per shop [E]: 300 min x $0.15-0.30 = $45-90 platform minutes; Twilio number $1.15; 10DLC campaign $1.50-10; SMS ~$5; n8n executions negligible. **~$55-105 per shop per month**, i.e. 60-85% gross margin at $249.

**Time to first dollar [E]:** build the demo agent in week 1-2; 30+ local touches/week from week 2; offer a 2-week free pilot to the first 3 shops; invoice the setup fee ($300-500) on go-live. Realistic first invoice at **~40 days**; 10DLC approval (reported 1-4 weeks, [S: earlier lens note]) can delay the SMS component but not the voice go-live.

**Revenue scenarios (gross, before platform fees)**

| | Month 3 | Month 6 | Assumptions |
|---|---|---|---|
| Conservative | 1 shop x $199 + 1 setup already banked = $199 MRR | 2 shops x $249 = $498 MRR | ~1 close per 60-80 touches; 30 touches/wk |
| Base | 3 shops x $249 = $747 MRR (+$400 setup that month) | 5 shops x $249 = $1,245 MRR + 1 setup $400 = **~$1,650** | ~1 close per 40 touches; one churn replaced |
| Upside | 5 shops x $299 = $1,495 MRR + 2 setups | 8 shops x $299 = $2,392 + 2 setups $800 = ~$3,200 | referral flywheel from first HVAC client; 2 integrations sold at $499 |

Net at base month 6: $1,650 - (5 x $75 variable) - $50 fixed = **~$1,225/mo**.

**Hours and implied hourly [E]:** 10-12 h/wk throughout (weeks 1-8 are almost all build and outreach, unpaid). Month-6 base: ~48 h/mo for ~$1,225 net = **~$25/hr** that month; cumulative over six months roughly $12-15/hr. Upside case at 8 shops nears $50/hr but is at the ceiling of a side-hustle time budget (earlier note put the ceiling at 10-15 recurring shops).

**Churn:** no published benchmark for AI-receptionist resellers found. The earlier note recorded "20% first-month churn" as commonly described for prosumer/SMB subscriptions [A: SaaStr commentary via lens]. Assume 1 of 5 shops leaves every quarter and plan replacement outreach accordingly.

## 6. Platform, policy, and legal risks

- **TCPA / FCC (federal).** FCC Declaratory Ruling FCC-24-17 (Feb 8, 2024): AI-generated voices, including real-time conversational AI, are "artificial or prerecorded voice" under the TCPA, so outbound AI calls to cell phones need prior express consent (informational) or prior express written consent (marketing); statutory damages $500-1,500 per call, class settlements in 2025-26 ran $5-20M [S: henson-legal.com, retellai.com TCPA playbook, agxntsix.ai 2026]. **Inbound is different:** no US law bans an AI receptionist and the FCC has said the TCPA does not reach technologies used to answer inbound calls [S: aiemply.com 2026]. The Aug 2024 FCC NPRM on AI-call disclosure was still not final as of April 2026, and the current FCC signals a lighter posture [S: henson-legal 2026]. Rule for this business: the agent never dials out except an immediate callback the caller just asked for; no reactivation campaigns unless the shop has documented consent (see [[research/lenses/local-smb-services]] candidate 6).
- **State bot-disclosure laws.** California (bot disclosure; AB 2905 effective Jan 1, 2025 requires upfront AI disclosure and all-party recording consent for calls involving California residents), Utah AI Policy Act, Colorado already on the books; if a caller asks whether they are speaking to a bot and the agent does not disclose, liability attaches regardless of call direction [S: aiemply, thoughtly, henson-legal 2026]. Mitigation: greeting says "Hi, this is Sam, the AI assistant for X Plumbing; this call may be recorded," in every state.
- **Call-recording consent.** 38 one-party states, 12 all-party; the AI agent generally satisfies the federal one-party rule as a party controlled by the business, but all-party states (CA, CT, FL, IL, MD, MA, MT, NV, NH, PA, WA, plus DE/OR nuances in some lists) require the caller's consent before recording [S: thoughtly, dialzara, pyai, getnextphone 2026]. Retell/Vapi record by default for transcripts; keep the disclosure in the greeting or disable recording for all-party-state shops.
- **SMS: A2P 10DLC.** Standard brand registration $44 one-time, $15 per campaign vetting, $1.50-10 per campaign per month, plus carrier surcharges per message; inbound replies incur small fees on AT&T/T-Mobile/US Cellular [S: sociocs, ghlscaleup, twilio.com 2026]. Unregistered traffic is fully blocked (since Feb 2025, per earlier lens note). Each client shop must be registered under its own brand (its EIN), which means collecting the owner's EIN and opt-in language during onboarding.
- **Platform terms.** Retell and Vapi ToS text: no data found this session. Known constraints from comparison content: neither offers native white-label; Retell's partner programs have no public terms; Vapi pricing page names no reseller program [S: seldonframe, famulor 2026]. Risk: a platform price change or acquisition changes your margin overnight; keep the agent design portable (prompt + tools in n8n, not vendor-locked features).
- **Suite bundling.** Jobber $29 add-on (unlimited on Plus), Housecall Pro CSR AI, ServiceTitan Virtual Agent [S: help.getjobber.com, projul, nextiva 2026]. If a client upgrades to those suites they may drop you; position as the integrator that connects the AI to whatever they use.
- **FTC / advertising.** Do not publish fabricated "recovered $X" testimonials; recovered-revenue reports should attribute only jobs the agent actually booked (FTC fake-review/endorsement rule, effective Oct 21, 2024, up to $53,088 per violation, per [[research/saturated-overhyped]]). Disclose that the receptionist is AI in the shop's own marketing if the shop advertises "24/7 live answering."
- **Copyright of AI output:** irrelevant to revenue here; prompts and workflows are your trade secret, and transcripts belong to the client shop (put that in the contract).
- **YouTube/social AI-content rules:** only relevant if you build a companion channel (see [[research/candidates/workflow-tutorial-channel]] if it exists); the July 2025 inauthentic-content policy does not touch a B2B phone service.
- **Liability edge cases:** the agent must never give safety advice beyond "if you smell gas, leave and call 911/the utility"; put a limitation-of-liability clause and an "AI may err" clause in the service agreement; carry general liability only if a client requires it (cost: no data found).

## 7. Skills needed and learning curve (for the stated profile)

- **Voice-agent building (Retell or Vapi builder, prompts, tools/functions, transfer rules):** 1-2 weekends for a first working agent given ChatGPT/Claude fluency; the hard part is call-flow design for edge cases, which takes ~50 real transcripts per shop to learn.
- **n8n:** already in the profile; needed for calendar/CRM writes, text-back, alerting, reports. Light JS for date handling is the one "light scripting" requirement.
- **Telephony basics:** Twilio numbers, conditional call forwarding codes on the shop's carrier (varies by carrier), 10DLC forms. Tedious, not hard; 2-4 hours to learn.
- **Trade vocabulary:** enough HVAC/plumbing/electrical to triage (no-heat vs. maintenance, water heater vs. slab leak, breaker vs. panel). One evening with a trade glossary plus the first client's input.
- **Local B2B sales:** the actual learning curve and the profile's gap (no audience, no network). Walk-in and phone outreach to owner-operators, a 90-second demo (call the number), a 2-week pilot offer. Expect 40-80 touches per close early; this skill is the difference between the conservative and base scenarios.
- **Compliance hygiene:** disclosure greeting, recording rules by state, 10DLC; a checklist, not a credential.
- **Time budget fit:** the build and monitoring fit 10-15 h/wk comfortably; outreach must be scheduled in owner-available windows (7-8 am, lunch, 4-6 pm), which is compatible with a side hustle only if the operator's day job allows short calls.

## 8. Real examples (2025-2026)

- **Acrely (YC-backed), "AI customer service representative for home services"** - verified that a funded startup targets exactly this buyer; pricing not seen [S: ycombinator.com launch OH3, 2026].
- **Jobber AI Receptionist customer:** one owner reported $4,800 in first-month bookings from calls that had been going to voicemail [A: vendor testimonial via pipelineon/newo 2026].
- **Bonney Plumbing** cut missed calls by 60% with an AI receptionist [A: vendor case study, ring-ready.com/newo.ai 2026].
- **HVAC client booking rate 55% -> 90% after replacing an answering service; another books 85% on ~400 calls/week** [A: vendor case study, 2026 roundup].
- **Kaizen AI Consulting (UK): Nottingham plumbing company** - custom AI receptionist, ~34 extra jobs/month, ~GBP 7,480/month added revenue on a system costing ~GBP 250/month to run [A: consultancy's own case study, 2026]. Closest analogue to this dossier's offer (solo consultancy, one plumber, build-and-run), but self-reported.
- **Newo.ai** claims a 99.6% "Lead Success Score" for plumbing/HVAC clients vs ~80% for human staff [A: vendor metric, undefined].
- **Image Orthodontics recovered $401,500 in Q1 2025** from booked calls that would have been missed [A: vendor case study; different vertical].
- **Trillet / VoiceAI Connect / Seldon Frame agency blogs** describe agencies reselling to HVAC/plumbing/roofing at $297-797/mo at 60-80% margins [A: platforms selling to those agencies].
- **YouTube "AI voice agency" creators (Vapi/Retell HVAC walkthroughs):** not searched before the cap; no data found this session. The earlier skeptic note treats guru income claims as unverified.
- **Reddit operator sentiment:** no HVAC-specific threads retrieved this session; the earlier lens synthesis (ciela.ai, 2026) records buyer skepticism toward template sellers and churn when no client metric moves [A].

Verified-vs-anecdotal summary: the only "verified" items are that the products, prices, and funded competitors exist as listed by multiple independent 2026 comparison sites; every revenue outcome above is a vendor or consultancy self-report.

## Open questions for the next session (when fetch works)

- Pull the primary ServiceTitan pages (62% missed, 47% after-hours, +45% Oct->Jun) and the CallRail Sept 2025 report to confirm sample and wording.
- Fetch Retell and Vapi pricing and ToS pages; confirm concurrency limits, number pricing, partner-program terms, and any reseller restrictions.
- Upwork/Fiverr: count live "Retell/Vapi agent" gigs and typical fixed prices to sanity-check the $300-500 setup fee.
- Toll-free verification as a faster alternative to 10DLC for the text-back component (not verified this session).
- Any published churn or retention data for AI receptionist SaaS in trades.

## Sources

Voice platform pricing (2026)
- [Cekura: Retell AI pricing per minute (2026)](https://www.cekura.ai/blogs/retell-ai-pricing-per-minute)
- [CloudTalk: Retell AI pricing 2026](https://www.cloudtalk.io/retell-ai-pricing/)
- [Layer3 Labs: Retell AI pricing 2026](https://www.layer3labs.io/guides/retell-ai-pricing)
- [Dialora: Retell AI pricing 2026](https://www.dialora.ai/blog/retell-ai-pricing)
- [G2: Retell AI pricing 2026](https://www.g2.com/products/retell-ai/pricing)
- [CloudTalk: Vapi AI plans and pricing 2026](https://www.cloudtalk.io/blog/vapi-ai-pricing/)
- [Cekura: Vapi AI pricing 2026](https://www.cekura.ai/blogs/vapi-ai-pricing)
- [Zeeg: Vapi AI pricing true cost 2026](https://zeeg.me/en/blog/post/vapi-ai-pricing)
- [Layer3 Labs: Vapi pricing 2026](https://www.layer3labs.io/guides/vapi-pricing)
- [AI Agent Square: Vapi pricing 2026](https://aiagentsquare.com/blog/vapi-pricing-2026)
- [Famulor: Retell AI vs Vapi 2026](https://www.famulor.io/blog/retell-ai-vs-vapi-2026-which-platform-is-actually-better)
- [Trillet: Vapi alternatives for agencies, white-label (June 2026)](https://trillet.ai/blogs/vapi-alternative-for-agencies)
- [Seldon Frame: Voice AI reseller programs (Vapi, Synthflow, Retell)](https://www.seldonframe.com/guides/voice-ai-reseller-programs)
- [Hermes: Best voice AI platforms for agencies 2026](https://www.buildwithhermes.com/blog/best-voice-ai-platforms-agencies-2026-hermes-synthflow-retell-vapi)
- [VoiceAI Connect: value-based pricing for AI receptionist agencies (2026)](https://www.myvoiceaiconnect.com/blog/value-based-pricing-ai-receptionist-agency)
- [Trillet: Voice AI for home-services agencies (2026)](https://trillet.ai/blogs/voice-ai-for-home-services-agencies)

Missed-call and demand statistics
- [Contractor In Charge: Missed call statistics for home service companies (62%)](https://contractorincharge.com/blog/missed-call-statistics-for-home-service-companies)
- [Dialfyne: Missed call statistics 2026](https://dialfyne.com/missed-call-statistics)
- [CallJolt: Home service business missed call statistics 2026](https://calljolt.com/blog/guides/home-service-business-missed-call-statistics)
- [CallJolt: Home service phone statistics 2026](https://calljolt.com/blog/hvac/home-service-industry-phone-statistics)
- [AgentZap: How to stop missing service calls in ServiceTitan (2026)](https://agentzap.ai/blog/how-to-stop-missing-service-calls-in-servicetitan-a-contractors-guide-2026)
- [AgentZap: HVAC industry phone statistics 2026](https://agentzap.ai/blog/hvac-phone-statistics)
- [Ainora: HVAC, plumbing and electrical service call statistics 2026](https://ainora.lt/blog/hvac-service-call-statistics-2026)
- [Ainora: Missed call statistics small business 2026](https://ainora.lt/blog/missed-call-statistics-small-business-2026)
- [Quo (OpenPhone): Small business callback statistics 2026](https://www.quo.com/blog/small-business-callback-statistics/)
- [OnCrew: Missed call statistics, verified sources (2026)](https://oncrew.ai/resources/missed-call-statistics)
- [PCN: 2026 small business missed call revenue study](https://pcnanswers.com/missed-call-revenue-study/)
- [Higrovi: 2026 contractor missed call report (4.2M calls)](https://www.higrovi.com/blog/contractor-missed-call-report-2026)
- [ServiceTitan State of the Trades: HVAC summer after-hours call spike](https://www.servicetitan.com/toolbox/state-of-the-trades/trends/hvac-summer-after-hours-call-spike)
- [KaiCalls: How many calls do HVAC companies miss (seasonal)](https://www.kaicalls.com/blog/how-many-calls-do-hvac-companies-miss)
- [Call Experts: HVAC summer surge answering guide](https://callexperts.com/blog/hvac-summer-surge/)
- [Titan Pro Technologies: Why HVAC and roofing miss calls in peak season](https://titanprotechnologies.com/blog/servicetitan-missed-calls-peak-season/)
- [PipelineOn: Missed lead statistics in home services](https://pipelineon.com/blog/missed-lead-statistics-home-services/)
- [PipelineOn: AI tools for HVAC and plumbing scheduling (adoption stats)](https://pipelineon.com/blog/ai-tools-for-hvac-plumbing-scheduling/)
- [IBISWorld: Heating and air-conditioning contractors in the US, number of businesses](https://www.ibisworld.com/united-states/number-of-businesses/heating-air-conditioning-contractors/1945/)
- [Market.us: AI receptionist market size and CAGR](https://market.us/report/ai-receptionist-market/)
- [Brilo AI: AI receptionist statistics and trends 2026](https://www.brilo.ai/resources/ai-receptionist-trends-2026)

Lead-cost benchmarks
- [Skill Mammoth: Local Services Ads cost 2026, CPL by trade](https://skillmammoth.com/blog/local-service-ads-cost)
- [Searchlight Digital: Google LSA cost per lead by trade (2026)](https://searchlightdigital.io/google-local-service-ads-cost-per-lead/)
- [Valley Marketing Group: HVAC and plumbing Google Ads CPL 2026](https://thevalleymarketinggroup.com/blog/hvac-plumbing-google-ads-cost-2026/)
- [Web Tonic: Plumbing Google Ads statistics 2026](https://www.webtonic.io/blog/plumbing-google-ads-statistics)

Retail AI receptionist pricing (2026)
- [CloudTalk: Rosie AI answering service pricing 2026](https://www.cloudtalk.io/blog/rosie-ai-answering-service-pricing/)
- [OnCrew: Rosie AI pricing 2026](https://oncrew.ai/blog/rosie-ai-pricing-2026)
- [ServiceAgent: Rosie AI review 2026](https://serviceagent.ai/blogs/rosie-ai-pricing/)
- [Rosie (heyrosie.com) home page](https://heyrosie.com/)
- [CloudTalk: Goodcall pricing 2026](https://www.cloudtalk.io/blog/goodcall-pricing/)
- [ServiceAgent: Goodcall pricing 2026](https://serviceagent.ai/blogs/goodcall-pricing/)
- [Contractor ToolStack: Goodcall review 2026](https://contractortoolstack.com/software/goodcall/)
- [xpay: Goodcall pricing 2026](https://www.xpay.sh/saas-pricing/goodcall/)
- [Marblism: 9 best AI receptionists for small business 2026](https://www.marblism.com/blog/best-ai-receptionist)
- [CloudTalk: Best HVAC AI virtual receptionists](https://www.cloudtalk.io/blog/best-hvac-ai-virtual-receptionist/)
- [CloudTalk: Best AI voice agents for plumbers and HVAC 2026](https://www.cloudtalk.io/blog/best-ai-voice-agent-for-plumbers/)
- [Voksha: Best AI receptionist for HVAC companies 2026](https://voksha.com/blog/best-ai-receptionist-for-hvac-companies)
- [ServiceAgent: AI phone answering service for HVAC by budget](https://serviceagent.ai/blogs/ai-phone-answering-service-for-hvac/)
- [PipelineOn: AI receptionist for contractors 2026](https://pipelineon.com/blog/ai-receptionist-contractor/)
- [Growth100x: Best AI voice agents for HVAC and plumbing 2026](https://growth100x.com/insights/best-ai-voice-agents-hvac-plumbing-2026/)
- [Revved Digital: Best AI receptionist platforms for home services 2026](https://revved.digital/best-ai-receptionist-home-services/)
- [Nextiva: AI receptionist for home services 2026 buying guide](https://www.nextiva.com/blog/ai-receptionists-for-home-service-businesses.html)
- [OnCrew: How AI phone answering integrates with ServiceTitan, Housecall Pro, Jobber (2026)](https://oncrew.ai/blog/servicetitan-ai-integration-phone-answering)
- [Jobber Help: Receptionist powered by Jobber AI](https://help.getjobber.com/hc/en-us/articles/25315927533847-Receptionist-powered-by-Jobber-AI)
- [MyQuoteIQ: Jobber pricing breakdown 2026](https://myquoteiq.com/jobber-pricing-breakdown-2026/)
- [Projul: Housecall Pro pricing 2026](https://projul.com/blog/housecall-pro-pricing-analysis-2026/)
- [Housecall Pro: How much does an answering service cost (2026)](https://www.housecallpro.com/resources/how-much-does-an-answering-service-cost/)
- [AIRA: AI receptionist cost 2026](https://www.getaira.io/blog/ai-receptionist-cost)
- [NextPhone: AI receptionist pricing guide 2026](https://www.getnextphone.com/blog/ai-receptionist-pricing-guide)
- [AgentZap: AI receptionist pricing guide 2026](https://agentzap.ai/blog/ai-receptionist-pricing-complete-guide-2026)
- [CallBird: AI receptionist pricing 2026](https://www.callbirdai.com/blog-ai-receptionist-cost-pricing-guide)
- [Most AI Labs: AI receptionists for plumbers/HVAC, missed-call math 2026](https://mostailabs.com/ai-for/home-services)
- [Augmented Trades: AI receptionist software for plumbers 2026](https://augmentedtrades.com/ai-receptionist-software-plumbers-2026/)

Case studies and examples
- [Y Combinator: Acrely, AI customer service representative for home services](https://www.ycombinator.com/launches/OH3-acrely-the-ai-customer-service-representative-for-home-services)
- [Newo.ai: AI receptionist for plumbing service scheduling](https://newo.ai/ai-receptionist-for-plumbing-service-scheduling/)
- [Kaizen AI Consulting: Nottingham plumbing company AI receptionist case study](https://kaizenaiconsulting.com/nottingham-plumbing-company-ai-receptionist-books-jobs-24-7/)
- [RingReady: AI receptionist case studies by industry](https://www.ring-ready.com/case-studies)
- [CallBird: Best AI receptionist for contractors (2025)](https://www.callbirdai.com/blog-best-ai-receptionist-contractors)

Compliance and legal
- [Retell AI: 2026 TCPA compliance playbook for voice AI](https://www.retellai.com/blog/tcpa-compliance-playbook-voice-ai-outbound)
- [Henson Legal: AI voice agent compliance, TCPA, FCC, state laws (2026)](https://www.henson-legal.com/ai-voice-compliance)
- [AIemply: Is an AI receptionist legal? 2026 disclosure rules](https://aiemply.com/blog/ai-receptionist-disclosure-laws)
- [Thoughtly: AI disclosure requirements for voice agents](https://thoughtly.com/blog/ai-disclosure-requirements-what-to-tell-callers)
- [Thoughtly: Call recording consent for AI voice agents, state guide](https://thoughtly.com/blog/call-recording-consent-ai-voice-agents-state-guide)
- [Dialzara: Call recording laws for AI agents by state](https://dialzara.com/blog/call-recording-laws-ai-agents-by-state)
- [PyAI: Call recording consent by state](https://pyai.com/voice-ai-compliance/call-recording-consent-by-state)
- [NextPhone: Call recording laws by state 2026](https://www.getnextphone.com/blog/call-recording-laws-by-state)
- [Trillet: Voice AI call recording compliance for agencies (2026)](https://trillet.ai/blogs/voice-ai-call-recording-compliance)
- [Agxntsix: How TCPA rules apply to AI voice calls in 2026](https://agxntsix.ai/blog/tcpa-rules-ai-voice-calls-2026)
- [Twilio: A2P 10DLC overview](https://www.twilio.com/en-us/phone-numbers/a2p-10dlc)
- [Sociocs: Twilio 10DLC registration and pricing explained](https://www.sociocs.com/post/twilio-10dlc-explained/)
- [GHL Scale Up: A2P 10DLC fees explained (2026)](https://www.ghlscaleup.com/blog/a2p-10dlc-fees-explained)
- [TextBolt: 10DLC compliance](https://textbolt.com/blog/10dlc-compliance/)

Tooling costs
- [No Code MBA: n8n pricing 2026](https://www.nocode.mba/articles/n8n-pricing)
- [OpenHosst: n8n Cloud pricing 2026](https://openhosst.com/blog/n8n-cloud-pricing)
- [ExpressTech: Real cost of self-hosting n8n in 2026](https://expresstech.io/the-real-cost-of-self-hosting-n8n-in-2026/)

Saturation and operator sentiment
- [Ciela: Freelance AI automation rates 2026 (Reddit synthesis)](https://ciela.ai/blogs/freelance-ai-automation-rates-2026)
- [Layer3 Labs: Is an AI automation agency worth it](https://www.layer3labs.io/guides/is-an-ai-automation-agency-worth-it)
