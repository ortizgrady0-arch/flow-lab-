---
title: "Skeptic (demand): Inbound AI front desk for 1-5-truck HVAC, plumbing and electrical shops"
tags: [research, skeptic, demand, ai-front-desk-home-services]
updated: 2026-09-10
lens: demand
verdict: weakened
confidence: 0.45
---

# Skeptic (demand lens): AI front desk for 1-5-truck trade shops

Adversarial review of the demand and pricing case in [[research/candidates/ai-front-desk-home-services]]. Related: [[research/lenses/local-smb-services]] · [[research/lenses/emerging-2026]] · [[research/saturated-overhyped]] · [[research/shortlist]]

## TL;DR

- **Overall: weakened, not refuted.** The pain (missed calls in trades) is plausibly real, but every demand number in the dossier is a vendor-blog citation of an unfetched primary page, and the vault's own notes carry a contradicting primary-adjacent figure: CallRail's Jan 2025 dataset of 1.1M leads puts the home-services missed-call rate at **14%**, not the **62%** headline (ServiceTitan via vendor blogs). The true rate for a 1-5-truck shop is **no data found**; plan on the pilot shop's own call log, not either number.
- **The $199-499/mo band is refuted at the top and weakened in the middle.** The dossier's own price table shows the buyer's benchmark is Rosie $149 (with in-call booking), Goodcall $129-249, OnCrew $49 contractor-targeted, and Jobber's native receptionist at $29. Entry prices fell from $149-299 (2025) to $29-49 (2026) inside one year per the vault's own notes; the corrected sellable band is **$149-249/mo + $250-500 setup**, with the $499 tier and the $1,000 setup ceiling treated as unsupported.
- **"Who pays" is smaller than the 118k-HVAC-contractor proxy implies.** That IBISWorld count includes commercial, multi-truck and suite-using firms; the share that is 1-5 trucks, not on Jobber/HCP/ServiceTitan, misses enough calls to feel it, and will pay ~$200/mo rather than $29 for a bundled add-on is **no data found**. Plumbing and electrical counts were never sourced.
- **The revenue-per-missed-call logic is weakened:** the $51-57 LSA cost-per-lead is a replacement cost only if the missed caller never calls back; the CallRail 78% figure is "have ever abandoned a business," an attitude statistic, not a per-call loss rate. No source gives the share of missed trade calls that are actually lost.
- **Every outcome claim (recovered revenue, book rates, 60-80% agency margins, $297-797 resale) is vendor or agency-platform marketing** [A]; no independent case study, churn benchmark, Reddit post-mortem, or Google Trends series could be retrieved (search budget 200/200 exhausted before this session; all 30 fetch attempts egress-blocked). Default verdict on those claims: weakened.
- **Commoditization is the strongest refuting evidence and it comes from the dossier itself:** field-service suites (Jobber, Housecall Pro, ServiceTitan) and VoIP incumbents (Nextiva, OpenPhone/Quo appear in the dossier's own source list publishing "AI receptionist for home services" guides) are shipping the feature; 15+ SaaS vendors already sell to this exact buyer with free trials and no setup fee.
- **Corrected planning numbers [E]:** missed-call rate 14-62% (use pilot data); price $149-249/mo; setup $250-500; month-6 base **3 shops x $199 = ~$600 MRR** (dossier: $1,245 MRR at 5 x $249), conservative unchanged at $400-500; sales conversion **no data found** (dossier's 1 close per 40-80 touches is an unsourced estimate).
- **What would flip this to "holds":** the primary ServiceTitan page confirming 62% with its population definition; one non-vendor case of a 1-5-truck shop paying $200+/mo for 6+ months; a live count of Upwork/Fiverr "Retell/Vapi receptionist" gigs and their prices.

## Method and limitations

- Date: 2026-09-10. Task: attack each demand and pricing claim in the dossier with web evidence.
- **Web access this session: none.** The session-wide WebSearch budget was already exhausted (200/200) before the first query; all 10 planned searches were refused. Thirty WebFetch attempts were made to primary and secondary pages (oncrew.ai, callrail.com, help.getjobber.com, heyrosie.com, goodcall.com, housecallpro.com, servicetitan.com, ibisworld.com, retellai.com, vapi.ai, calljolt.com, cloudtalk.io, reddit.com x3, hn.algolia.com, news.ycombinator.com, web.archive.org, bing.com, duckduckgo.com, census.gov, fcc.gov, trends.google.com, wikipedia.org, ycombinator.com, github.com); every one was blocked by the egress proxy, refused, or rate-limited.
- Consequently this note is an **adversarial audit of the dossier's own evidence chain** plus cross-checks against the vault's other notes. Evidence tags: **[S]** figure as quoted in a search snippet of the named source in a prior session (primary page never opened); **[A]** vendor, agency-platform or guru claim; **[E]** estimate/arithmetic; **[V-internal]** contradiction found between two notes in this vault.
- Per the brief, claims with no support either way default to **weakened**. Nothing below is a newly verified number.

## Claim-by-claim verdicts

### D1. "62% of home-service calls are missed" (ServiceTitan, 50k+ lines) - WEAKENED

- Dossier status: the most-repeated number in the category, cited via contractorincharge.com, dialfyne.com, calljolt.com, agentzap.ai; ServiceTitan page never fetched [S].
- Attack: [[research/lenses/local-smb-services]] records, from the same prior session, a CallRail Jan 2025 analysis of **1.1M leads** giving missed-call rates of 32% healthcare, 28% legal, **14% home services**, 9% real estate [S: cited there via getaira.io/phone2.io]. That is a 4x gap on the headline stat **[V-internal]**. The lens explains it away as "call-tracking users are already optimized," which is plausible but unproven; the opposite reading is that 62% describes a specific population (e.g. after-hours lines, or "calls not answered live by a person including voicemail pickup") and is being generalized by vendors. The population definition, date and method of the 62% figure are **no data found**.
- Also note the 411 Locals 2024 figure (37.8% of inbound calls answered live, 85 businesses, 58 industries) in the same lens note is tiny-sample and cross-industry.
- Corrected: **no single planning number is defensible.** Use a range of 14-62% and make the pilot shop's carrier call log the real evidence. If the real rate for a target shop is nearer 14%, a shop taking 15 calls/day misses ~2/day, and the value case shrinks proportionally.
- Sources: [Contractor In Charge (62%)](https://contractorincharge.com/blog/missed-call-statistics-for-home-service-companies), [Dialfyne](https://dialfyne.com/missed-call-statistics), [AIRA (62%, 411 Locals, CallRail 14%)](https://www.getaira.io/blog/missed-business-calls-statistics), [Phone2 (CallRail 14%)](https://www.phone2.io/post/true-cost-of-missed-calls) - all vendor blogs, 2026, not fetched.

### D2. "47% of calls arrive after hours; HVAC after-hours calls +45% Oct->Jun" - WEAKENED

- Single vendor (agentzap.ai) attributes 47% to ServiceTitan; the +45% Oct->Jun figure is from a ServiceTitan "State of the Trades" snippet [S]. Neither page fetched; sample and definition **no data found**. The two figures are also not the same population (all home services vs. HVAC residential).
- Skeptic reading: after-hours share is exactly the metric a vendor selling after-hours coverage would foreground. Even if true, an after-hours caller with no heat calls the next shop; the question is whether an AI answering at 11pm books the job or merely takes a message the owner reads at 7am, by which time the caller may have booked elsewhere anyway. Booking-in-call is therefore the whole product, which pushes the buyer to the tiers that do it (Rosie $149+, Jobber native).
- Sources: [AgentZap HVAC phone statistics](https://agentzap.ai/blog/hvac-phone-statistics), [ServiceTitan State of the Trades snippet](https://www.servicetitan.com/toolbox/state-of-the-trades/trends/hvac-summer-after-hours-call-spike) - not fetched.

### D3. "78% of consumers have abandoned a business after an unanswered call; 82% would call a competitor" (CallRail, Sept 2025, n=1,000) - WEAKENED as a demand driver

- The dossier and oncrew.ai treat this as one of the few verifiable stats. Grant that the survey exists as described [S]. The attack is on relevance: "have abandoned a business after an unanswered call" is a lifetime-ever attitude statistic across all business types; it does not measure the share of *trade-service* calls lost per missed call, nor the owner's willingness to pay. A 78% lifetime figure is compatible with a low per-call loss rate.
- Per-call loss rate for HVAC/plumbing missed calls: **no data found** in any source in the vault.
- Sources: [OnCrew missed-call statistics](https://oncrew.ai/resources/missed-call-statistics), [Quo/OpenPhone callback statistics](https://www.quo.com/blog/small-business-callback-statistics/) - vendor pages citing CallRail, 2026, not fetched; [CallRail](https://www.callrail.com/) blocked.

### D4. "Replacement cost of a missed lead is $51-57 (LSA, $6.72M spend, 888 contractors, Feb 2026)" - WEAKENED

- The LSA CPL figures are the best-sourced numbers in the dossier (three independent agency blogs, same dataset) [S]. The attack is the inference: CPL equals the value of a missed call only if (a) the missed caller is lost, and (b) the shop would otherwise buy that lead. Small shops that rely on referrals and never buy LSAs do not price a missed call at $55; they price it at zero until a bad month. The share of 1-5-truck shops buying paid leads: **no data found**.
- Emergency-job values of $400-1,500 and "pays for itself in 4-6 weeks" are cloudtalk.io vendor arithmetic [A]; primary job-ticket data **no data found**.
- Sources: [Skill Mammoth LSA cost](https://skillmammoth.com/blog/local-service-ads-cost), [Searchlight Digital LSA CPL](https://searchlightdigital.io/google-local-service-ads-cost-per-lead/), [Valley Marketing Group](https://thevalleymarketinggroup.com/blog/hvac-plumbing-google-ads-cost-2026/), [CloudTalk plumbers guide (vendor)](https://www.cloudtalk.io/blog/best-ai-voice-agent-for-plumbers/) - not fetched.

### D5. "Who pays: most of ~118k HVAC contractors plus plumbing and electrical" - WEAKENED (size overstated)

- 118,433 HVAC businesses (IBISWorld 2025) [S] is a count of all establishments, including commercial/mechanical contractors, multi-branch firms, and suite users. The dossier's own segmentation says the defensible buyer is the shop that (1) is 1-5 trucks, (2) is not on Jobber/HCP/ServiceTitan or is on a cheap tier, (3) has no CSR, and (4) misses enough calls to feel it. The share meeting all four: **no data found**. Plumbing and electrical business counts: **no data found** (the ConsumerAffairs ~990k combined figure is 2020 and includes establishments, not firms).
- Adoption trend cited (plumbing AI adoption 7% -> 19%, 2024 -> 2026) is from pipelineon.com with the survey unnamed [A]; the Census BTOS May 2026 paid-operational AI use of 17-20% (via [[research/lenses/local-smb-services]]) is the better anchor and says roughly four in five small firms have not opened a wallet for operational AI.
- Skeptic reading: the buyer's real alternative is not Smith.ai at $292; it is voicemail plus the spouse's cell, which costs $0. The sale is against "do nothing," which is the hardest sale in SMB services.
- Sources: [IBISWorld HVAC contractors](https://www.ibisworld.com/united-states/number-of-businesses/heating-air-conditioning-contractors/1945/) (blocked), [PipelineOn adoption stats](https://pipelineon.com/blog/ai-tools-for-hvac-plumbing-scheduling/), [Capsule CRM SMB AI adoption 2026 (BTOS)](https://capsulecrm.com/blog/small-business-ai-adoption-statistics/) - not fetched.

### D6. "Market: AI receptionist $2.7B (2025) -> $31.4B (2035), 27.8% CAGR" - WEAKENED

- market.us analyst-report figure [S]; methodology not seen; such reports routinely define the category to include enterprise contact-center AI. Irrelevant to a solo operator's addressable market. Directional only, as the dossier itself concedes.
- Source: [Market.us AI receptionist market](https://market.us/report/ai-receptionist-market/) - not fetched.

### P1. "Charge $199-499/mo per shop" - REFUTED at $499 for the target segment; WEAKENED at $299

- The dossier's own price table (all [S], 2-4 comparison sites each): Dialzara $29 unlimited; Jobber Receptionist $29 add-on (unlimited on Plus); Rosie $49/149/299 with in-call booking from $149; Goodcall $79/129/249; OnCrew $49 contractor-targeted; AIRA $24.95; Smith.ai AI from $95. The vault's earlier lens note recorded the "flat" band at $149-299 in 2025-early 2026 and this dossier recorded entry tiers at $29-49 by mid-2026 **[V-internal price compression within ~12 months]**.
- A 1-5-truck owner comparing $499/mo against Rosie $149 (booking, transfer, SMS) or Jobber $29 needs a reason worth $350/mo every month; "a local human who fixes it" is a real reason for the first quarter and a weak one once the agent works. The $499 tier is also gated in the dossier itself on integrations with suites that already sell their own receptionist.
- "Agencies resell at $297-797/mo at 60-80% margins" is from trillet.ai, a platform selling to those agencies [A]; "most small businesses pay $99-499" is from vendor pricing guides whose upper bound is their own top tier [A].
- Corrected: **$149-249/mo**, with $199 the likely closing price for a shop with no integrations; $299 only with a suite/calendar integration and a recovered-jobs report; $499 unsupported.
- Sources: [Marblism best AI receptionists 2026](https://www.marblism.com/blog/best-ai-receptionist), [CloudTalk Rosie pricing](https://www.cloudtalk.io/blog/rosie-ai-answering-service-pricing/), [OnCrew Rosie pricing 2026](https://oncrew.ai/blog/rosie-ai-pricing-2026), [CloudTalk Goodcall pricing](https://www.cloudtalk.io/blog/goodcall-pricing/), [Jobber Help: Receptionist](https://help.getjobber.com/hc/en-us/articles/25315927533847-Receptionist-powered-by-Jobber-AI), [Trillet agency blog (A)](https://trillet.ai/blogs/voice-ai-for-home-services-agencies), [AgentZap pricing guide (A)](https://agentzap.ai/blog/ai-receptionist-pricing-complete-guide-2026) - not fetched.

### P2. "Setup fee $250-1,000" - WEAKENED; $1,000 unsupported

- Every SaaS competitor in the table onboards for free with a 7-day trial (Rosie) or self-serve setup; Smith.ai's script setup is 2-5 business days, included. A setup fee is sellable only as "I make call forwarding, the calendar and the SMS work for you," which the dossier prices at 6-10 hours the first time and ~4 hours templated. At Upwork n8n rates of $40-100/hr [S: ciela.ai] that is $160-400 of labor; $1,000 needs a suite integration that the suite is now bundling.
- Upwork/Fiverr live gig counts and fixed prices for Retell/Vapi receptionist builds: **no data found** (never searched in any session).
- Corrected: **$250-500**, invoiced on go-live; treat $1,000 as a rare integration project, not a list price.
- Source: [Ciela freelance AI automation rates 2026](https://ciela.ai/blogs/freelance-ai-automation-rates-2026) - not fetched.

### P3. "Unit economics: 300 min/shop/mo, 60-85% gross margin" - HOLDS on platform cost, WEAKENED on volume

- Platform per-minute prices ($0.13-0.31 Retell all-in, $0.10-0.30 Vapi) are corroborated by 4+ independent 2026 breakdowns [S] and are not the problem. The 300 min/shop/mo figure is the operator's estimate [E]; if a small shop's after-hours/overflow line really carries 300 minutes (roughly 75-100 calls) a month, the missed-call rate is high and the shop is bigger than 1-2 trucks; if it carries 60 minutes, the owner sees a $199 bill for ~15 calls and churns in the shoulder season. Actual after-hours call volumes for 1-5-truck shops: **no data found**.
- Sources: [Cekura Retell pricing](https://www.cekura.ai/blogs/retell-ai-pricing-per-minute), [Zeeg Vapi pricing](https://zeeg.me/en/blog/post/vapi-ai-pricing), [Layer3 Labs Vapi pricing](https://www.layer3labs.io/guides/vapi-pricing) - not fetched.

### P4. "Month-6 base: 5 shops x $249 = $1,245 MRR (+setup); 1 close per 40 touches" - WEAKENED

- Both the conversion rate and the price are unsourced estimates [E]. Nothing in the vault evidences a solo operator with no local network closing 1 in 40 cold walk-ins/calls for a $249/mo AI subscription; the vault's own skeptic note ([[research/saturated-overhyped]] #14) says the generic AI-agency pitch meets buyer skepticism and that "two or three clients is the realistic ceiling at this time budget."
- Contractors are cold-pitched by every vendor in the table (the dossier concedes "platform flooding of your acquisition channel"), so the walk-in is arriving after several emails and calls from Rosie/Goodcall/OnCrew.
- Corrected [E]: base month-6 **3 shops x $199 = ~$600 MRR** plus one $300-500 setup; conservative 1-2 shops ($200-400 MRR); upside 5-6 shops at $199-249 (~$1,200-1,500 MRR). Implied hourly at base falls to roughly $10-15 by month 6, below the dossier's $25-30.

### C1. "Suite bundling is the biggest structural threat" - HOLDS (and strengthens the skeptic case)

- Jobber $29 add-on (unlimited on Plus), Housecall Pro CSR AI, ServiceTitan Virtual Agent are all in the dossier [S]. Add: the dossier's own source list includes buying guides from Nextiva and Quo (OpenPhone), i.e. business-phone providers are publishing "AI receptionist for home services" content, which signals the feature is arriving in the phone system the shop already pays for. Once the shop's phone plan or job-management app answers calls, the reseller is selling a third login.
- Sources: [Nextiva AI receptionist buying guide](https://www.nextiva.com/blog/ai-receptionists-for-home-service-businesses.html), [Quo callback statistics](https://www.quo.com/blog/small-business-callback-statistics/), [Jobber Help](https://help.getjobber.com/hc/en-us/articles/25315927533847-Receptionist-powered-by-Jobber-AI), [Projul HCP pricing](https://projul.com/blog/housecall-pro-pricing-analysis-2026/) - not fetched.

### C2. "Saturation: 10+ SaaS vendors, every one with an HVAC/plumber blog" - HOLDS

- The dossier lists 15+ named vendors selling directly to this buyer, plus YC-funded Acrely, plus agency wrappers (Trillet, Synthflow, Convocore, Vapify, VoiceAI Connect) whose existence implies many resellers. Count of resellers/agencies: **no data found**, but a category with five white-label platforms marketing to agencies is not an uncrowded category.
- Search-interest trend for "AI receptionist" 2024-2026: **no data found** (Google Trends blocked).

### C3. "Case studies: $4,800 first month (Jobber), Bonney Plumbing -60% missed calls, Nottingham plumber +34 jobs/mo, 55% -> 90% book rate" - WEAKENED

- All are vendor testimonials or a consultancy's own case study [A]; none has an independent audit, a denominator, or a retention period. The Nottingham (Kaizen) case is the only solo-consultancy analogue and is self-reported. Negative post-mortems (Reddit r/HVAC, r/Plumbing, r/smallbusiness, r/Entrepreneur): **no data found** (Reddit and HN blocked; not searched in any session). Consumer-side pushback against AI phone answering: **no data found**.
- Sources: [Newo.ai plumbing](https://newo.ai/ai-receptionist-for-plumbing-service-scheduling/), [Kaizen AI Consulting case](https://kaizenaiconsulting.com/nottingham-plumbing-company-ai-receptionist-books-jobs-24-7/), [RingReady case studies](https://www.ring-ready.com/case-studies) - vendor/consultancy, not fetched.

### C4. "Churn: assume 1 of 5 shops per quarter" - WEAKENED (could be worse)

- No published churn benchmark for AI-receptionist SaaS or resellers exists in the vault (**no data found**); the "20% first-month churn" figure is SaaStr commentary about prosumer subscriptions generally [A]. The dossier's own seasonality section predicts churn attempts in shoulder months when the owner "can answer the phone myself again." For a shop paying $199-249 for a service whose value is concentrated in 2-3 peak months, seasonal pausing is the rational buyer behavior; the dossier's steady-state 5 shops may require closing 8-10 over the year.

### C5. "Quality: >=80% correct intake on real calls" (kill criterion) - WEAKENED

- No source in the vault gives real-world intake accuracy (address capture, urgency triage, accent handling) for Retell/Vapi agents on trade calls; **no data found**. If the first pilot shows 60-70%, the owner hears about the misses from customers, which is the fastest churn path and a reputational one for a local operator.

## Corrected numbers (summary)

| Item | Dossier | Skeptic correction | Basis |
|---|---|---|---|
| Missed-call rate, home services | 62% | 14-62%; use pilot call log | CallRail 1.1M-lead 14% vs ServiceTitan 62%, both [S] [V-internal] |
| After-hours share | 47% | no data found (single vendor attribution) | [S] |
| Per-call loss rate | implied ~78-82% | no data found | CallRail figure is lifetime attitude |
| Monthly price | $199-499 | $149-249 ($299 with integration; $499 unsupported) | dossier price table [S] |
| Setup fee | $250-1,000 | $250-500 | Upwork n8n rates [S], SaaS onboarding free |
| Addressable shops | "most of 118k HVAC" + plumbing/electrical | no data found for the 1-5-truck, no-suite, no-CSR subset | IBISWorld count is all establishments |
| Sales conversion | 1 close / 40-80 touches | no data found | [E] only |
| Month-6 base MRR | $1,245 (5 x $249) | ~$600 (3 x $199) [E] | corrected price and close rate |
| Month-6 implied hourly (base) | ~$25-30 | ~$10-15 [E] | same hours, lower MRR |
| Churn | 1 of 5 per quarter | no data found; seasonal pausing likely higher | dossier seasonality section |
| Agency resale price/margin | $297-797, 60-80% | treat as marketing [A] | trillet.ai sells to agencies |

## What would change the verdict

1. Fetch the ServiceTitan primary page and confirm the 62% population; if it is "calls not answered live, including voicemail pickup, across all sizes," the number is not a 1-5-truck number.
2. One independently verifiable 1-5-truck shop paying $200+/mo to a solo reseller for six months or more (an invoice, not a testimonial).
3. Live Upwork/Fiverr counts and prices for "Retell/Vapi receptionist" builds (setup-fee floor).
4. Google Trends for "ai receptionist" and "missed call text back," 2024-2026, to test whether buyer interest is still rising or has plateaued as the feature gets bundled.
5. Reddit r/HVAC and r/Plumbing threads on AI answering (owner and customer sentiment), which no session has yet retrieved.

## Sources

All URLs below were cited by the dossier or the vault's lens notes from search snippets in a prior session; none could be opened in this session (egress-blocked). Dates are as reported by those snippets (2025-2026).

Missed-call statistics (vendor blogs citing ServiceTitan, CallRail, 411 Locals)
- [Contractor In Charge: missed call statistics for home service companies (62%)](https://contractorincharge.com/blog/missed-call-statistics-for-home-service-companies)
- [Dialfyne: missed call statistics 2026](https://dialfyne.com/missed-call-statistics)
- [AIRA: 62% of business calls go unanswered (also cites CallRail Jan 2025, 14% home services)](https://www.getaira.io/blog/missed-business-calls-statistics)
- [Phone2: true cost of missed calls (CallRail 14% home services)](https://www.phone2.io/post/true-cost-of-missed-calls)
- [OnCrew: missed call statistics, verified sources (CallRail Sept 2025)](https://oncrew.ai/resources/missed-call-statistics)
- [Quo (OpenPhone): small business callback statistics 2026](https://www.quo.com/blog/small-business-callback-statistics/)
- [AgentZap: HVAC industry phone statistics 2026 (47% after hours)](https://agentzap.ai/blog/hvac-phone-statistics)
- [ServiceTitan State of the Trades: HVAC summer after-hours call spike](https://www.servicetitan.com/toolbox/state-of-the-trades/trends/hvac-summer-after-hours-call-spike)
- [CallRail (blocked this session)](https://www.callrail.com/)

Lead cost and job value
- [Skill Mammoth: Local Services Ads cost 2026](https://skillmammoth.com/blog/local-service-ads-cost)
- [Searchlight Digital: Google LSA cost per lead by trade](https://searchlightdigital.io/google-local-service-ads-cost-per-lead/)
- [Valley Marketing Group: HVAC and plumbing Google Ads CPL 2026](https://thevalleymarketinggroup.com/blog/hvac-plumbing-google-ads-cost-2026/)
- [CloudTalk: best AI voice agents for plumbers and HVAC (vendor ROI arithmetic)](https://www.cloudtalk.io/blog/best-ai-voice-agent-for-plumbers/)

Market size and adoption
- [IBISWorld: HVAC contractors, number of businesses (blocked)](https://www.ibisworld.com/united-states/number-of-businesses/heating-air-conditioning-contractors/1945/)
- [Market.us: AI receptionist market](https://market.us/report/ai-receptionist-market/)
- [PipelineOn: AI tools for HVAC and plumbing scheduling (adoption stats, unnamed survey)](https://pipelineon.com/blog/ai-tools-for-hvac-plumbing-scheduling/)
- [Capsule CRM: small business AI adoption statistics 2026 (Census BTOS)](https://capsulecrm.com/blog/small-business-ai-adoption-statistics/)

Retail pricing benchmarks
- [Marblism: 9 best AI receptionists for small business 2026 (Dialzara $29, Smith.ai)](https://www.marblism.com/blog/best-ai-receptionist)
- [CloudTalk: Rosie AI answering service pricing 2026](https://www.cloudtalk.io/blog/rosie-ai-answering-service-pricing/)
- [OnCrew: Rosie AI pricing 2026](https://oncrew.ai/blog/rosie-ai-pricing-2026)
- [CloudTalk: Goodcall pricing 2026](https://www.cloudtalk.io/blog/goodcall-pricing/)
- [Jobber Help: Receptionist powered by Jobber AI](https://help.getjobber.com/hc/en-us/articles/25315927533847-Receptionist-powered-by-Jobber-AI)
- [Projul: Housecall Pro pricing 2026](https://projul.com/blog/housecall-pro-pricing-analysis-2026/)
- [Nextiva: AI receptionists for home service businesses (buying guide)](https://www.nextiva.com/blog/ai-receptionists-for-home-service-businesses.html)
- [AgentZap: AI receptionist pricing guide 2026 (vendor)](https://agentzap.ai/blog/ai-receptionist-pricing-complete-guide-2026)
- [Trillet: voice AI for home-services agencies (agency-platform marketing)](https://trillet.ai/blogs/voice-ai-for-home-services-agencies)
- [Ciela: freelance AI automation rates 2026 (Upwork n8n rates)](https://ciela.ai/blogs/freelance-ai-automation-rates-2026)

Platform per-minute cost
- [Cekura: Retell AI pricing per minute](https://www.cekura.ai/blogs/retell-ai-pricing-per-minute)
- [Zeeg: Vapi AI pricing true cost 2026](https://zeeg.me/en/blog/post/vapi-ai-pricing)
- [Layer3 Labs: Vapi pricing 2026](https://www.layer3labs.io/guides/vapi-pricing)

Case studies (vendor/consultancy self-reports)
- [Newo.ai: AI receptionist for plumbing](https://newo.ai/ai-receptionist-for-plumbing-service-scheduling/)
- [Kaizen AI Consulting: Nottingham plumbing case study](https://kaizenaiconsulting.com/nottingham-plumbing-company-ai-receptionist-books-jobs-24-7/)
- [RingReady: case studies](https://www.ring-ready.com/case-studies)
- [Y Combinator: Acrely launch](https://www.ycombinator.com/launches/OH3-acrely-the-ai-customer-service-representative-for-home-services)

Saturation and operator sentiment
- [Layer3 Labs: is an AI automation agency worth it](https://www.layer3labs.io/guides/is-an-ai-automation-agency-worth-it)
- [Ciela: is starting an AI automation agency worth it (Reddit synthesis)](https://ciela.ai/blogs/is-starting-an-ai-automation-agency-worth-it-reddit)
- [SaaStr: 2026 AI predictions (churn commentary)](https://cloud.substack.com/p/top-10-saastr-ai-predictions-for)
