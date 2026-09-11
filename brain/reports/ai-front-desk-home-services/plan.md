---
title: "Execution plan: Inbound AI front desk for 1-5-truck HVAC, plumbing and electrical shops"
tags: [plan, ai-front-desk-home-services, execution, local-sales, 90-day]
updated: 2026-09-11
hustle: ai-front-desk-home-services
type: plan
---

# Execution plan: AI front desk for home-service shops

The 90-day sequence for [[reports/ai-front-desk-home-services/report]], running the machine described in [[reports/ai-front-desk-home-services/automation-stack]]. Conditional pick per [[decisions/final-selection]]; evidence in [[research/candidates/ai-front-desk-home-services]] and its skeptic notes.

## TL;DR

- **Precondition check before day 1:** can you make 30+ local touches a week inside 7-8 am, 12-1 pm and 4-6 pm? If no, do not start; swap to podcast clipping per [[decisions/final-selection]].
- **Week 1** builds the plumbing demo agent on Retell, a demo number, a one-page site with privacy/terms (needed for 10DLC), the prospect list of 100 off-suite plumbing shops within 30 minutes' drive, and makes the first 10 touches by day 7.
- **Day 30 target:** 105+ touches (120 if week 1 hits 30), 10+ replies, 3+ live demos, 2 free pilots running. **Day 60 (kill gate):** 2+ paying shops (setup fee invoiced at go-live, day 15 of each pilot) or stop. **Day 90:** 2 paying is the base case ($398 MRR, the same ramp as the report's month-3 base), 3 paying ($597) is the double-down case; first weekly reports delivered; HVAC template forked for February.
- Acquisition is walk-ins and phone calls to owners, referral asks from every pilot, supply-house and trade-group presence; no cold email blasts, no cold SMS, no AI outbound (the documented beginner attempt, ClawOps, got zero replies from email in six weeks and every vendor already emails these owners).
- Conversion assumptions are labelled: reply rate 10% of touches, demo rate 30% of replies, pilot rate 50% of demos, paid conversion 50% of pilots [all assumption; the skeptics found no data]. That chain needs ~130 touches per paying shop, so 30/wk yields one close per month from week 3, i.e. pilot 1 converting in week 5-6 and pilot 2 in week 7-8: two paying shops by day 60 with no margin, which is the base case and exactly the kill gate.
- Templates included: walk-in script, phone script, voicemail, referral ask, 3-line follow-up text, pitch one-pager copy, onboarding questionnaire (18 fields), go-live SOP, service agreement clauses, 10DLC privacy/terms snippet.
- Weekly time budget 12 h at 0-2 shops: outreach 5, build/onboarding 3, QA/babysitting 1 h + 0.75 h per live shop (1.25 h for a shop in its first month), admin/reporting 1, learning 1. From shop 4 the QA block alone is ~4 h, so outreach drops to 3 h/wk unless you have 15 h; that trade-off is a day-90 gate input. KPI dashboard: touches, replies, demos, pilots, paying shops, MRR, churn, intake accuracy, bookings/shop, hours/shop.

## 1. Prerequisites checklist

**Accounts and tools**
- [ ] Retell account, $10 free credit, API key; one agent named for the plumbing template ([Retell pricing](https://www.retellai.com/pricing), 2026: $0.07/min engine, ~$0.13-0.31 all-in per CloudTalk/Cekura)
- [ ] Twilio account upgraded out of trial ($20 credit; a trial account plays an announcement on every call and only accepts inbound calls from 5 verified numbers, Twilio Help 2026), one local number (~$1.15/mo), voice + SMS enabled; Trust Hub Primary Business Profile created with business type **"ISV Reseller or Partner"** and approved, because every shop's 10DLC registration is a Secondary Customer Profile under that primary (Twilio ISV onboarding docs, 2026); A2P 10DLC Low-Volume Standard brand ($4.50) + campaign vetting ($15) for your own line (Twilio docs / Sociocs, 2026)
- [ ] n8n reachable at a public HTTPS URL (Retell webhooks and Twilio status callbacks need it): either n8n Cloud trial for weeks 1-4 then migrate, or self-hosted with the docker-compose + Caddy + Postgres template on a $5-7 Hetzner/DigitalOcean droplet under a subdomain of your site (Nordbastion 2026 guide; budget 2-3 h, see Day 4); Claude Pro; Claude API key with a $10 cap
- [ ] Google Workspace or free Google account: Calendar, Sheets, Drive, Forms
- [ ] Stripe account with Billing enabled (2.9% + $0.30; Billing 0.7%)
- [ ] Loom free, a Google Voice or cell number you will give owners
- [ ] Apify free tier or a manual Google Maps list

**Assets**
- [ ] One-page website: what it does, the demo number, a 60-second call recording, privacy policy and terms pages with SMS consent language (10DLC requires both; TermsAndConditionsUrl mandatory since 2026-06-30)
- [ ] Demo agent that takes a 2 am "burst pipe" call convincingly (test from a cell, not the browser)
- [ ] Printed one-pager and a business card with the demo number ("Call it now")
- [ ] Service agreement (template clauses in section 7), onboarding questionnaire (Google Form), go-live SOP

**Legal and admin basics (US, general information, not legal advice)**
- [ ] Business name: sole proprietorship under your own name is enough to start; a DBA/LLC in your state is a $50-300 filing [assumption on cost range]; get your own EIN first (IRS online, ~15 min, free) because the Twilio ISV primary profile and Stripe both ask for it and you do not want to hand out your SSN
- [ ] Tax: self-employment income; set aside ~25-30% of net; track platform costs as expenses [assumption on rate; no specific guidance found]
- [ ] Insurance: not required by any platform found; buy general liability only if a client contract asks (cost: no data found)
- [ ] Compliance one-pager for yourself: AI disclosure first sentence (satisfies Utah SB 149, Maine LD 1727 Chatbot Disclosure Act in force since 2025-09-24 and covering voice callbots, and California B.O.T.; Colorado's AI Act is delayed to 2027-01-01 by SB 189); recording consent by state (treat CA, DE, FL, IL, MD, MA, MT, NV, NH, PA, WA as all-party, plus CT, MI, OR, VT as all-party to be safe; Recording Law / NextPhone / Viirtue 2026); inbound-only rule and the text-back rules (one informational SMS to a consumer-initiated contact, inbound call logged as consent, STOP included); 10DLC per shop via the Twilio ISV flow (secondary customer profile under the shop's legal name and EIN)
- [ ] Retell Partner Program application once shop #1 is live (tiers start at 1-8 customers onboarded in 6 months)

## 2. Week 1, day by day (start Thursday 2026-09-17; 2026-09-11 is a Friday, so use the intervening days to read this package, get your EIN and open the accounts)

| Day | Tasks | Expected output |
|---|---|---|
| **Day 1 (Thu)** | 1) Create Retell, Twilio and Stripe accounts; upgrade Twilio out of trial ($20 credit) and buy the number, or use a Retell-provisioned number ($2/mo) for the voice-only demo; in Twilio Trust Hub create the Primary Business Profile as "ISV Reseller or Partner" with your own EIN (approval takes days; needed before any shop's 10DLC). 2) Paste the plumbing system prompt (automation-stack 4.1) into a Retell agent with placeholder shop values; pick a natural voice; set the first-sentence disclosure. 3) Make 5 calls from your cell; fix the worst turn. | A demo line that answers, discloses, triages and takes a message |
| **Day 2 (Fri)** | 1) Add `get_availability`/`book_slot` tools pointing at a stub n8n webhook that returns two fake windows. 2) Generate 40 test scenarios (prompt 4.5); run 15; score in a sheet. 3) Draft the one-page site copy with Claude; publish on Carrd/Framer/Google Sites with privacy + terms pages. | Booking works on the demo line; scoresheet started; site live |
| **Day 3 (Sat)** | 1) Submit your own 10DLC brand + campaign (use the live site URLs). 2) Build the prospect list: Google Maps "plumber" + "drain cleaning" within 30 min drive; 100 rows with name, phone, address, website, review count, whether the site shows Jobber/HCP/ServiceTitan booking widgets, whether recent reviews mention "never called back". 3) Claude scores each 1-5 for fit (1-5 trucks, no suite, review complaints). | 100-shop list ranked; 10DLC submitted |
| **Day 4 (Sun)** | 1) n8n (budget 2-3 h): either (a) start an n8n Cloud free trial for weeks 1-4 and migrate later, or (b) self-host with the official docker-compose + Caddy + Postgres template on a $5-7 Hetzner/DigitalOcean droplet, pointed at a subdomain of your site (A record, WEBHOOK_URL set to the https URL); done when a test webhook URL returns 200 over HTTPS from your phone. 2) Record a 60-second Loom of a demo call. 3) Write the walk-in script, phone script and voicemail (section 5), practise out loud 10 times. 4) Print 20 one-pagers. | n8n live over HTTPS; sales kit ready |
| **Day 5 (Mon)** | 1) 7:30-8:00 am: 4 phone calls to top-ranked shops (owners answer early). 2) 12:00-1:00: 3 walk-ins at shops with a visible office. 3) Log every touch and reply in the outreach sheet. 4) Evening: run 10 more test scenarios; fix address read-back. | 7 touches logged; first reactions noted |
| **Day 6 (Tue)** | 1) 7:30 am: 4 calls. 2) 4:30-6:00 pm: 3 walk-ins (owners back from jobs). 3) Visit one plumbing supply house counter and ask who the good small shops are; leave 3 cards. 4) Evening: n8n A1 skeleton on the Day-4 instance (Retell post-call webhook received over HTTPS, JSON appended to sheet). | 10+ touches cumulative; A1 logging live |
| **Day 7 (Wed)** | 1) 7:30 am: 4 calls including follow-ups to anyone who said "call me back". 2) Lunch: 2 walk-ins. 3) Weekly review: touches, replies, objections heard verbatim; rewrite the opener with Claude using real objections. 4) Evening: draft the onboarding questionnaire as a Google Form (section 7). 5) Book the first demo or pilot start if any reply is warm. | Week 1 close: 15-20 touches, 1-3 replies, opener v2, list of objections, questionnaire ready |

## 3. 30 / 60 / 90-day plan

**Days 1-30: prove the call flow and get two pilots**

| Week | Milestones | KPIs (targets) |
|---|---|---|
| 1 | Demo agent, site, list, first 15-20 touches | touches 15-20; replies 1-3 |
| 2 | 30 touches; 10DLC approved for own line; A1 booking write to Google Calendar working | touches 30; replies 3; demos 1 |
| 3 | 30 touches; first free pilot live (voice only, manual booking entry) | touches 30; demos 2; pilots 1 |
| 4 | 30 touches; second pilot; daily transcript skim; first owner alert SMS delivered | touches 30; pilots 2; intake accuracy measured on >=20 real calls |
| **Day 30 gate** | | cumulative touches 105+ (15-20 in week 1 + 3 x 30; 120 only if week 1 hits 30); replies 10+; demos 3+; pilots 2; intake accuracy >=80% |

**Days 31-60: convert pilots, automate A1/A2, hit the kill gate**

| Week | Milestones | KPIs |
|---|---|---|
| 5 | Pilot 1 go-live (day 15 of its pilot): $250 setup invoice + $199/mo subscription raised together on Stripe; submit the shop's 10DLC (subaccount + secondary customer profile + brand + campaign) | paying 1; MRR $199 |
| 6 | A2 text-back live for shop 1 once campaign approved; A1 owner SMS + daily digest automated; 30 touches with a referral ask to pilot owners | touches 30; referrals asked 2 |
| 7 | Pilot 2 goes live (converts) or is replaced; first weekly recovered-calls report emailed; nightly transcript export | paying 2; reports sent 2 |
| 8 | Third pilot from a referral or supply-house intro; Retell partner application | pilots 1 new; cumulative touches 225+ |
| **Day 60 kill gate** | | **2+ paying shops** with setup fees invoiced, or stop; intake accuracy >=80%; no agent broken twice in a month; 10DLC approved within 30 days of go-live |

**Days 61-90: third shop, template hardening, HVAC fork**

| Week | Milestones | KPIs |
|---|---|---|
| 9 | Pilot 3 live (converts by week 11-12 in the double-down case); onboarding time <=4 h; smoke-test workflow after Retell changelogs | paying 2 (base) to 3; onboarding hours logged |
| 10 | Monthly review call with shop 1; offer annual $149 or integration upgrade $249 | upsell/annual conversions 1 |
| 11 | Fork the HVAC template (no-heat/no-cool rules, thermostat/CO script); build HVAC prospect list for a Feb-Apr push | HVAC template scored >=36/40 on scripted calls |
| 12 | Quarterly numbers: MRR, churn, hours/shop, cost/shop, total hours; decide double-down/adjust/kill (section 6) | MRR $398 base / $597 double-down; cumulative touches 345+; churn events <=1; hours/shop <=6/mo; total hours <=12 or outreach cut to 3 h |

## 4. Acquisition playbook: first 10 paying shops

**Channels, in priority order**
1. **Walk-ins** to shops with a physical office (supply-house strip, industrial parks), 12-1 pm and 4:30-6 pm. Ask for the owner; if absent, leave the one-pager and get the owner's cell from whoever is there.
2. **Phone calls** to the owner's line at 7:30-8 am (before dispatch) and 4-6 pm. Do not use the shop's booking line during the day; that is the phone you are trying to help him answer.
3. **Referral asks** from every pilot and paying owner at go-live and at the first weekly report ("Who else do you know who's answering their own phone from under a sink?").
4. **Supply-house counters and trade groups** (PHCC chapter, local contractor association, ServiceTitan/Jobber user meetups if any): be the person who fixes phones, not the AI guy.
5. **Google review mining**: shops whose recent reviews say "never called me back" get a walk-in with that review printed; it is the only cold pitch that opens with the owner's own pain.
6. Not used: cold email (ClawOps: 0 replies), cold SMS (TCPA/10DLC), AI outbound calls (FCC 24-17), paid ads (every vendor already outspends you), LinkedIn (owners are not there).

**Daily volume targets (12 h/wk budget, 5 h to outreach):** 6 touches/day x 5 days = 30/wk; roughly 12 calls, 12 walk-ins, 6 follow-ups/referral asks. Log every touch with outcome and objection verbatim.

**Conversion assumptions (all "assumption"; the skeptics found no data and the one documented attempt was zero):** reply/conversation rate 10% of touches; live demo 30% of conversations; free pilot 50% of demos; paid conversion 50% of pilots. Chain: 30 touches -> 3 conversations -> 1 demo -> 0.5 pilot -> 0.25 paying per week, i.e. ~1 paying shop per month, 130 touches per close. If after 60 touches replies are under 5%, the opener is wrong; rewrite before continuing. If after 120 touches demos are under 2, the offer is wrong for the list; re-qualify the list.

**Scripts**

*Walk-in (30 seconds):* "Hi, I'm {{name}}, I live over in {{neighbourhood}}. I set up phone answering for small plumbing shops so the calls you miss while you're on a job get answered, booked and texted back. It's not a call centre; it's a system I run for a few local shops. Can I show you in 60 seconds? Call this number from your cell and pretend you've got a burst pipe." (Hand the card. Let the agent do the pitch.) "If it's useful I'll run it free for two weeks on your after-hours line, and you keep it only if it books jobs you'd have missed."

*Phone (owner picks up, 7:30 am):* "Morning, is this {{owner}}? {{name}} here, I'm local, I'll be 40 seconds. I run after-hours and overflow phone answering for a few plumbing shops around {{town}}; it answers, gets the address and the problem, books them into your calendar and texts you. I'm looking for two more shops to run it free for two weeks. Would you be up for hearing it take a call? You can dial it right now." If busy: "When's a bad time to call you back, so I don't do that?"

*Voicemail (10 seconds):* "{{owner}}, {{name}}, local. I run phone answering for small plumbing shops; missed calls get answered and booked. Two-week free trial. Text me at {{cell}} or dial {{demo number}} to hear it. Thanks."

*Follow-up text (only after the owner has given you his cell in person or on a call):* "Hi {{owner}}, {{name}} from {{Tuesday}}. Demo line is {{number}} if you want to hear it grab a call. Free 2-week trial on your after-hours line, nothing to install; I set up the forwarding. Want me to swing by {{day}}?"

*Referral ask (at first weekly report):* "That report shows {{N}} calls you'd have missed. Who's one other owner you'd want this for? If they sign, your next month is on me."

**Objection handling**
- "I don't want a robot talking to my customers." -> "Fair. Right now voicemail is talking to them. Hear it once; if you'd be embarrassed by it, I walk."
- "Jobber/Housecall already does that for $29." -> "If you're on their Plus plan and it books into your calendar, keep it. If you're on the cheap tier or not on them at all, mine books into whatever you use and I set it all up."
- "How much?" -> "$199 a month after the free two weeks, $250 to set it up, cancel any month. One recovered drain call pays for it."
- "Is it legal / does it record?" -> "It says it's an AI assistant and that the call may be recorded in the first sentence, every call, and it never calls anyone. I can turn recording off if you'd rather."

## 5. Delivery calendar template (per shop, steady state)

| When | Task | Owner | Automation |
|---|---|---|---|
| Continuous | Answer, triage, book, text-back, alert | Retell + n8n | full |
| Daily 7 am | Digest email to owner (yesterday's calls, callbacks needed) | n8n | full |
| Daily 9 pm (month 1 only) | Skim transcripts flagged by QA rules | operator | 10 min |
| Weekly Sun 6 pm | Recovered-calls report emailed | n8n + Claude | full; operator skims |
| Weekly Mon | Score 20 transcripts; retune prompt if accuracy <80% | operator | 20-45 min |
| Weekly | Smoke test after any Retell changelog | n8n | full |
| Monthly, 1st | Stripe subscription renews; usage and cost logged | Stripe + n8n | full |
| Monthly | 15-minute review call with owner; upsell annual/integration; referral ask | operator | manual |
| Quarterly | Seasonality check-in: HVAC shops before Oct and Mar shoulder months, offer $49 pause instead of cancel | operator | manual |

## 6. Decision gates

| Gate | Double down if | Adjust if | Kill (or swap) if |
|---|---|---|---|
| **Day 30** | 2 pilots live, intake accuracy >=80%, replies >=10% of touches | pilots 1 or replies 5-10%: rewrite opener, re-rank list, add supply-house channel | 0 pilots after 105 touches AND replies <5%; or intake accuracy <70% on 20+ real calls; or you could not make 30 touches/wk (schedule condition failed) -> swap to podcast clipping |
| **Day 60** | 2+ paying shops, MRR >=$398, 10DLC approved for shop 1, zero double-breaks | 1 paying: extend 30 days only if 2 pilots are live and accuracy >=80% | <2 paying after 60 days of 30+ touches/wk (binding criterion); or agent broken twice in a month by platform updates; or 10DLC not approved within 30 days of go-live |
| **Day 90** | 3+ paying, churn 0-1, hours/shop <=6/mo, total hours <=12 (or outreach consciously cut to 3 h/wk at 4+ shops), one referral-sourced close | 2 paying (base): keep the cadence to day 120; hours/shop >8 or total hours >12 with outreach still at 5 h: template harder, cut integration tier, decide whether you have 15 h/wk | <2 paying or 2+ churned of 3; move to pivot options in the report |

## 7. Ready-to-use templates

**Pitch one-pager copy**

> **Your phone, answered. Every time.**
> Missed calls go to voicemail; voicemail goes to your competitor. {{Brand}} answers the calls you can't, gets the name, address and problem, books the job into your calendar, texts the customer a confirmation, and texts you a one-line summary. Emergencies get pushed to your on-call phone.
> - Says it's an AI assistant up front; never calls anyone; never quotes prices you didn't approve
> - Books into Google Calendar, Jobber or Housecall Pro
> - Weekly one-page report: calls answered, jobs booked, calls to return
> - Set up in one visit; free for two weeks on your after-hours line
> **$199/month after the trial · $250 setup · cancel any month.** Call {{demo number}} and try to book a fake burst pipe.

**Onboarding questionnaire (18 fields, Google Form)**
1. Shop name, owner name, owner cell (for alerts) 2. Trade(s) and services you do NOT do 3. Business hours per day; holidays 4. Service area: ZIPs or radius from address 5. Emergency definition (what gets same-day/after-hours) 6. Urgent definition (next available) 7. After-hours: transfer to on-call (number) or take message with callback promise (minutes) 8. Dispatch/service-call fee and the exact sentence you want said about pricing 9. Calendar or CRM to book into; booking windows (e.g. 8-12, 12-4, 4-7; weekends?) 10. Gas utility name and number for the safety script 11. Existing-customer handling (invoice, warranty questions) 12. Spanish needed? 13. Current phone setup: carrier, main number, who answers, how many rings before voicemail 14. State(s) you serve, including any neighbouring state your service area crosses into; cross-check against the all-party list (CA, DE, FL, IL, MD, MA, MT, NV, NH, PA, WA, plus CT, MI, OR, VT treated as all-party) and record whether recording is OK 15. For SMS registration (Twilio ISV flow): legal business name exactly as registered with the IRS, EIN, business address, website URL, privacy policy and terms page URLs, and an authorized representative (the owner): name, title, email and cell 16. Average job value (optional; used only in your own report) 17. Name you want the assistant to use 18. Anything the assistant must never say.

**Go-live SOP (checklist, ~2 h templated)**
1. Convert form to prompt + config (automation-stack 4.6); owner approves the pricing sentence in writing. 2. Configure Retell agent, tools, voice, disclosure; transfer number tested. 3. Twilio number assigned; A1 config row added; calendar shared to the service account. 4. Owner sets conditional call forwarding (no answer/busy) on his carrier; test from two cells. 5. 10DLC via the ISV flow: create a Twilio subaccount + Secondary Customer Profile from field 15 -> Low-Volume Standard brand ($4.50) -> campaign ($15) with the text-back described in the message-flow field as one informational SMS to a consumer-initiated inbound call; SMS flag off in n8n until the campaign is approved. 6. 40 scripted calls; >=36/40; zero violations. 7. Loom walkthrough sent; first live alert confirmed by owner reply. 8. Stripe: $250 setup invoice + $199/mo subscription both dated go-live (day 15 of the pilot); nothing is invoiced at pilot start. 9. Calendar reminder: day-7 check-in, day-14 conversion call.

**Service agreement clauses (have a lawyer review before signing the third client; general information only)**
- Service: inbound call answering, intake, booking, SMS follow-up and reporting as configured; no outbound marketing calls or texts.
- AI disclosure and recording: the assistant identifies itself as AI and discloses recording; client is responsible for confirming recording is permitted in its state or instructs provider to disable it.
- Accuracy: the assistant may mis-hear or mis-book; provider will correct configuration promptly; client reviews daily digests; provider's liability is capped at fees paid in the prior month.
- Data: transcripts and caller data belong to the client, exported nightly; provider retains configurations and workflows.
- Fees: pilot start (day 1) is free for 14 days; go-live is day 15, when the pilot auto-converts; the $250 setup fee and the first $199 month are invoiced together on go-live; $199/month in advance thereafter; cancel with 30 days' written notice; price changes with 30 days' notice.
- Platform dependency: service relies on third-party providers (Retell, Twilio); outages beyond provider's control are not breaches, but fees are prorated for outages over 24 hours.

**10DLC privacy/terms snippet for the shop's site (paste in footer pages)**
> *Privacy:* Mobile phone numbers and SMS consent collected by {{shop}} are used only to respond to your service request and confirm appointments. We do not share mobile information or SMS opt-in data with third parties or affiliates for marketing or promotional purposes.
> *SMS terms:* By providing your number you agree to receive appointment and service-related text messages from {{shop}}. Message frequency varies. Message and data rates may apply. Reply STOP to opt out, HELP for help.

## 8. KPI dashboard and weekly time budget

**Dashboard (one Google Sheet tab, updated by n8n and a 5-minute Friday manual entry)**

| KPI | Target (day 30 / 60 / 90) | Source |
|---|---|---|
| Local touches (cumulative) | 105 / 225 / 345 (15-20 in week 1, then 30/wk) | manual log |
| Reply rate | >=10% | manual log |
| Demos (live calls to demo line by a prospect) | 3 / 7 / 10 | Retell demo-line log |
| Pilots started | 2 / 3 / 4 | manual |
| Paying shops | 0-1 / 2 / 2 (base) to 3 (double-down) | Stripe |
| MRR | $0-199 / $398 / $398 (base) to $597 | Stripe |
| Setup fees banked | $0-250 / $500 / $500-750 | Stripe |
| Churn events / pause requests | 0 / 0 / <=1 | Stripe + manual |
| Intake accuracy (weekly 20-transcript score) | >=80% | QA sheet |
| Bookings per shop per week | measure; expect 2-3 real messages/day per the operator log, bookings fewer | A1 log |
| Hang-up rate <10 s | <45% | Retell |
| Platform cost per shop (all-in incl. Stripe fees) | <=$45 | Retell + Twilio + Stripe exports |
| Operator hours per shop per month | <=6 | timer |
| Hours per week total | <=12 (at 4+ shops: <=12 only with outreach cut to 3 h, else <=15) | timer |

**Weekly time budget (12 h at 0-2 live shops; scales with shops)**

| Block | Hours | When |
|---|---|---|
| Outreach: calls, walk-ins, follow-ups, referral asks | 5 (drops to 3 at 4+ shops unless you have 15 h) | 7:30-8 am x5, two lunch slots, two 4:30-6 pm slots |
| Build and onboarding (pilots, go-lives, HVAC fork) | 3 | two evenings |
| QA and babysitting (transcripts, smoke tests, owner support) | 1 h + 0.75 h per live shop (1.25 h for a shop in its first month, per automation-stack steps 15 and 18): ~2.5 h at 2 shops, ~3.25 h at 3, ~4.75 h at 5 | daily 10 min + Monday 45 min per shop in month 1, 20 min after |
| Admin, reporting, billing, dashboard | 1 | Friday |
| Learning (trade vocabulary, Retell changelog, n8n) | 1 | weekend |

Worked totals: 2 shops = 12.5 h; 3 shops = 13.25 h; 5 shops = 14.75 h with outreach at 5 h, or 12.75 h with outreach at 3 h. The report's "10-12 h/wk at 5 shops" therefore assumes outreach has been cut to ~3 h; decide that explicitly at the day-90 gate.

## Sources

- [ClawOps sales pipeline tracker, 2026-02-24 (0 replies, $0 revenue; email-led outreach)](https://github.com/rickclaw08/claw-systems/blob/3fa61252f449584a3d3ba7d647700d5531c20f69/claw-agency/sales/pipeline-tracker.md)
- [ClawOps financial reality check, 2026-03-02](https://github.com/rickclaw08/claw-systems/blob/3fa61252f449584a3d3ba7d647700d5531c20f69/claw-agency/finance/financial-reality-check-2026-03-02.md)
- [Jobber Help Center: Receptionist powered by Jobber AI ($29/mo, updated 2026-07-09)](https://help.getjobber.com/hc/en-us/articles/25315927533847-Receptionist-powered-by-Jobber-AI)
- [Jobber: 2026 Home Service Trends Report (referral-led lead generation)](https://www.getjobber.com/home-service-trends-report/)
- [ServiceTitan State of the Trades: HVAC off-hours call spike (Oct 9.8% to Jun 14.1%)](https://www.servicetitan.com/toolbox/state-of-the-trades/trends/hvac-summer-after-hours-call-spike)
- [Valley Marketing Group: Google LSA cost per lead 2026 (plumbing $57, $1,714 ticket)](https://thevalleymarketinggroup.com/blog/google-lsa-cost-per-lead-home-services-2026/)
- [Cekura: Retell AI pricing per minute 2026](https://www.cekura.ai/blogs/retell-ai-pricing-per-minute)
- [CloudTalk: Retell AI pricing 2026](https://www.cloudtalk.io/retell-ai-pricing/)
- [Retell AI: How the certified partner program works (tiers by customers onboarded)](https://www.retellai.com/blog/how-retell-ais-certified-partners-work)
- [Twilio Help: Low Volume Standard vs Standard registration for A2P 10DLC](https://help.twilio.com/articles/4407882914971-Comparison-between-Starter-Low-Volume-Standard-and-Standard-registration-for-A2P-10DLC)
- [Twilio docs: ISV A2P 10DLC onboarding overview, ISV Reseller/Partner primary profile and secondary customer profiles (2026)](https://www.twilio.com/docs/messaging/compliance/a2p-10dlc/onboarding-isv)
- [Twilio docs: A2P 10DLC, gather the required business information (2026)](https://www.twilio.com/docs/messaging/compliance/a2p-10dlc/collect-business-info)
- [Twilio error 30909: Campaign rejected, message flow or call to action incomplete (2026)](https://www.twilio.com/docs/api/errors/30909)
- [Twilio Help: Free trial account restrictions and limitations (2026)](https://support.twilio.com/hc/en-us/articles/360036052753-Twilio-Free-Trial-Limitations)
- [Nordbastion: Self-host n8n on a VPS with Docker, Postgres, Caddy (2026)](https://nordbastion.com/guides/self-host-n8n-on-a-vps/)
- [Twilio Help: A2P 10DLC campaign vetting FAQ ($15)](https://help.twilio.com/articles/11587910480155-A2P-10DLC-Campaign-Vetting-FAQ)
- [Twilio error 30934: Terms and Conditions URL required from 2026-06-30](https://www.twilio.com/docs/api/errors/30934)
- [Twilio error 30908: compliant privacy policy required (third-party sharing statement)](https://www.twilio.com/docs/api/errors/30908)
- [Sociocs: Twilio 10DLC registration and pricing explained](https://www.sociocs.com/post/twilio-10dlc-explained/)
- [Checkout Page: Stripe fees explained 2026](https://checkoutpage.com/blog/stripe-processing-fees)
- [Sembly AI: Call recording laws 2026](https://www.sembly.ai/blog/call-recording-laws-one-party-vs-two-party-consent/)
- [Viirtue: Call recording consent laws by state 2026 (via reviewer; egress-blocked 2026-09-11)](https://viirtue.com/call-recording-consent-laws-by-state-2026-guide/)
- [Recording Law: Nevada recording laws 2026 (NRS 200.620, all-party for phone calls)](https://www.recordinglaw.com/united-states-recording-laws/one-party-consent-states/nevada-recording-laws/)
- [NextPhone: Call recording laws by state 2026](https://www.getnextphone.com/blog/call-recording-laws-by-state)
- [Verrill: Maine LD 1727 chatbot disclosure law, in force 2025-09-24 (2025)](https://www.verrill-law.com/news/maine-law-now-requires-limited-disclosures-of-artificial-intelligence-technology/)
- [Hunton: Colorado AI Act amended and delayed to 2027-01-01 (May 2026)](https://www.hunton.com/privacy-and-cybersecurity-law-blog/colorado-ai-act-amended-and-effective-date-delayed)
- [Wipfli: TCPA informational text messages, rules and requirements (2026)](https://www.wipfli.com/insights/articles/tcpa-informational-text-messages-rules-and-requirements)
- [JustCall: AI voice agent disclosure laws 2026 (FCC NPRM 24-84 still pending Aug 2026)](https://justcall.io/blog/ai-voice-agent-disclosure-laws.html)
- [Henson Legal: AI voice agent compliance 2026](https://www.henson-legal.com/ai-voice-compliance)
- [FCC Declaratory Ruling FCC 24-17 (PDF)](https://docs.fcc.gov/public/attachments/FCC-24-17A1.pdf)
- [Achiya Cohen: AI phone-agent call log, 774 calls, Aug-Sep 2026 (2-3 real messages/day per business)](https://github.com/achiya-automation/safari-mcp/blob/29af3b9f87f6cc85e11d35766898ef78aa4abdc1/ai-call-cost-il-2026-09-10.html)
- [VoiceAI Connect: Client onboarding checklist for AI receptionist agencies 2026 (vendor)](https://www.myvoiceaiconnect.com/blog/client-onboarding-checklist-ai-receptionist-agency)
- [Trillet: Voice agent client retention strategies 2026 (vendor churn claims)](https://trillet.ai/blogs/voice-agent-client-retention-strategies)
- Vault: [Candidate dossier](../../research/candidates/ai-front-desk-home-services.md) · [Demand skeptic](../../research/candidates/ai-front-desk-home-services-skeptic-demand.md) · [Execution skeptic](../../research/candidates/ai-front-desk-home-services-skeptic-execution.md) · [Final selection](../../decisions/final-selection.md)
