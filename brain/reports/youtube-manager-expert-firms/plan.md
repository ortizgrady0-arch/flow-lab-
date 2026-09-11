---
title: "Execution plan: Fractional YouTube channel manager for expert firms"
tags: [plan, youtube-manager-expert-firms, outreach, 90-day, youtube]
updated: 2026-09-11
hustle: youtube-manager-expert-firms
type: plan
---

## TL;DR

- 90-day objective (skeptic-corrected): 3+ A/B packs sold by day 56, first Core retainer ($800) signed by day 90-120 (day 90 is an adjust gate; kill/demote at day 120, matching kill trigger 2 in [[reports/youtube-manager-expert-firms/report]]), hours per client-month measured at or below 22. Start date assumed Monday 14 Sep 2026, so the CPA test window (Oct-Nov) and Q4 advisor planning season are in reach.
- Week 1 builds the portfolio (two public-domain federal recordings re-cut in Descript Hobbyist), the one-page site, the sending setup (aged personal address for weeks 1-3 while the business domain warms up), the prospect sheet (60 RIAs, 30 law firms, 0 CPAs until October) and the compliance checklist; first outbound goes out day 5.
- Acquisition math: 20-30 personalized touches per week; expect 2-4% replies (financial services 1.5-3.5%, average 3.43%), 1-3 meetings per 100 emails, 20-30% close on calls (assumption). That is ~1 A/B pack per 50-75 touches and 150-300 touches per retainer; budget 4 h/wk for outreach until two clients are signed.
- Decision gates: day 30 = 100+ touches, 1+ pack sold or 3+ calls booked; day 60 = 3 packs sold to channels clearing ~1,000 views per video on recent uploads, or kill/pivot; day 90 = 1 Core retainer at $800+ or a signed start date and per-client hours logged, else adjust (keep going only with 2+ live proposals or a verbal yes); day 120 = no retainer after 300+ touches, demote to a ghostwriting upsell and hand the hours to podcast clipping.
- Delivery calendar per client: recording by the 5th, package to compliance by the 15th, approval SLA 5 business days (expect 2-4 weeks in months 1-2 for RIAs), publish weekly Tuesdays, Shorts Thu/Sat, memo on the 1st.
- Weekly time budget at two clients: 8-11 h production (2 x 16-22 h/month), 2 h client loop, 1-2 h outreach/admin = 11-15 h/wk, touching the top of the 10-15 h budget; three clients breaks it.
- Templates included: cold email, LinkedIn note, follow-ups, A/B pack pitch, Core proposal copy, onboarding questionnaire, delivery SOP, memo skeleton. Companion notes: [[reports/youtube-manager-expert-firms/report]], [[reports/youtube-manager-expert-firms/automation-stack]].

## 1. Prerequisites checklist

Accounts and tools (month 0 spend ~$150, see [[reports/youtube-manager-expert-firms/report]] section 7)
- [ ] Google account dedicated to the business (Drive, Sheets, Forms, Meet, YouTube Studio access as Manager on client channels). Buy the domain on day 1 and put Google Workspace (or a Zoho/Fastmail mailbox) on it, but do not cold-email from it until it is warmed up (see "Sending setup" below)
- [ ] Descript **Hobbyist $24 from day 1** (10 media hours/mo, 400 AI credits, no watermark; Free is capped at 60 media minutes/mo with 720p watermarked exports, so it cannot hold two 45-60 min portfolio webinars: [Sonix, 2026](https://sonix.ai/resources/descript-pricing/), [Castmagic, 2026](https://www.castmagic.io/blog/descript-pricing), [fluxnote, 2026](https://fluxnote.io/guides/descript-pricing-2026)); Creator $35 once the first client signs. OpusClip Free (60 credits, watermarked; trim sample Shorts in CapCut desktop instead) or Starter $15 (150 credits, no watermark), Pro $29 at first client. Canva Free, Pro $18 at first client. Claude Pro $20 from day 1 (all six prompts live in it). Month-0 cash $59-124 inside the $150 budget; the remainder funds the +$43/mo step-up to Creator/Pro/Pro in the first client month (report section 7.1 uses the same figures)
- [ ] n8n self-hosted or Cloud Starter deferred to month 2
- [ ] Stripe account with ACH enabled; Wave as free fallback; Dropbox Sign or similar free e-sign
- [ ] Loom free (proposal videos), Calendly/Google appointment schedule for calls
- [ ] Domain and a one-page site (Carrd/Framer free tier): who it is for, the A/B pack, the Core retainer, two portfolio samples, one paragraph on compliance handling, plus a privacy-policy page and a support email (both required to publish the Google OAuth consent screen used by Automation 1 in [[reports/youtube-manager-expert-firms/automation-stack]])

Sending setup (deliverability; a four-day-old mailbox lands in spam and would fail the day-30 gate for reasons unrelated to the message)
- [ ] Weeks 1-3: send from an aged personal address you have used for years, 15 per day maximum, personalized, plain text, no tracking pixels
- [ ] Day 1: buy the domain, create the business mailbox, set SPF, DKIM and DMARC (p=quarantine or stricter), point the domain at the live one-page site, and start a 2-3 week warm-up (a warm-up tool, or manual daily sends and replies with friends). Guides put a new mailbox at roughly three weeks to warm and a brand-new domain at four to six, with 5-15 cold sends per day for the first 30 days ([UnifyGTM, 2026](https://www.unifygtm.com/explore/cold-email-2026-domain-setup-deliverability-sequences); [Ozigi, 2026](https://blog.ozigi.app/blog/how-to-warm-up-sending-domain-2026); [Litemail on Google sender requirements, 2026](https://litemail.ai/blog/google-sender-requirements-2026-cold-email)). Instantly has no permanent free warm-up tier (warm-up is bundled with its $37-47/mo Growth plan; [Litemail, 2026](https://litemail.ai/blog/free-email-warmup-tools-2026-good-enough)), so budget it only if the manual route fails
- [ ] Week 4 onward: move outreach to the business domain once domain age is 3+ weeks and SPF/DKIM/DMARC pass (check with a free mail-tester); keep the personal address for replies already in flight

Assets
- [ ] Portfolio: two public-domain recordings re-cut into one 10-minute episode and three Shorts each, with sample thumbnails and a mock memo. Works of the US federal government are public domain ([17 U.S.C. 105](https://www.law.cornell.edu/uscode/text/17/105); [USAGov](https://www.usa.gov/government-copyright)), so: financial sample = an IRS Video Portal webinar on retirement plans or tax tips ([irsvideos.gov](https://www.irsvideos.gov/)) or an SSA retirement video (the SSA channel states its videos are "produced at U.S. taxpayer expense"; [SSA blog, 18 Aug 2026](https://www.ssa.gov/blog/en/posts/2026-08-18.html)); legal sample = a federal legal-education recording (e.g. Department of Labor EBSA retirement-plan rights videos, [dol.gov](https://www.dol.gov/agencies/ebsa/about-ebsa/our-activities/resource-center/videos), or a CFPB elder-financial-protection video), or a state-bar/law-school consumer video only if its page states an explicit reuse licence (no CC-licensed legal source was found on 2026-09-11; verify before use). Caveats: strip any third-party copyrighted material embedded in a government video, never imply agency endorsement, and label both samples "sample re-edit, not a client". Alternative: record a 30-minute mock interview with any acquaintance who is a professional and edit that
- [ ] One-page compliance checklist per vertical (RIA: SEC Marketing Rule; law: ABA 7.1/7.2 plus the client's state; CPA: state board ad rules) built from the QA list in [[reports/youtube-manager-expert-firms/automation-stack]]
- [ ] Jargon glossary template (30 lines) and onboarding questionnaire (section 7)
- [ ] Contract template with: scope, 2 revision rounds, $200-250 per extra round, approval clause (client responsible for regulatory approval; nothing publishes without written sign-off), assignment of deliverables, raw-file deletion at 90 days, 30-day cancel, billed in advance

Legal and tax basics (US)
- [ ] Operate as a sole proprietor under your own name until the first retainer clears; then decide on an LLC (state fees vary, $50-300, assumption) and a DBA if you want a brand name
- [ ] EIN (free, IRS) so clients do not need your SSN for 1099-NEC
- [ ] Set aside ~25-30% of net for federal income and self-employment tax (assumption; confirm with a tax preparer); quarterly estimated payments once income is steady
- [ ] Check your state's sales-tax treatment of digital/editing services before the first invoice (no data found; the execution skeptic flags 30+ states taxing some digital products)
- [ ] 1099-K from Stripe only above $20,000 and 200 transactions (restored threshold); irrelevant at this scale but income is taxable regardless
- [ ] CAN-SPAM basics for outreach: real name, physical address line, honor opt-outs; domain age 3+ weeks and SPF/DKIM/DMARC pass before the business domain sends; never exceed 15/day from any one mailbox in the first 30 days

## 2. Week 1, day by day (Mon 14 Sep to Sun 20 Sep 2026)

| Day | Tasks | Expected output |
|---|---|---|
| **Day 1 (Mon)** | (1) Buy the domain, create the business Google account and mailbox, set SPF/DKIM/DMARC, start the warm-up (send from the aged personal address until week 4); Claude Pro project with the six prompts and both compliance checklists; Descript Hobbyist subscribed; (2) build the prospect Sheet columns: firm, vertical, state, registration (SEC/state RIA, BD-affiliated Y/N), channel URL, last upload date, average views on last three uploads, Advanced Features Y/N (ask on the call if not visible), recording source (webinar/podcast), contact, email, LinkedIn, touch 1-4 dates, reply, meeting, outcome; (3) read the SEC Marketing Rule FAQ summary and one state bar ad rule end to end | Empty but structured pipeline; checklists loaded |
| **Day 2 (Tue)** | (1) Find 30 fee-only RIAs with a webinar/podcast and <1 YouTube upload a month (search YouTube for "retirement planning webinar" + firm names, then check SEC IAPD for registration and no BD affiliation); (2) find 15 estate-planning firms in non-filing states with a channel; (3) log views on the last video for each | 45 qualified rows |
| **Day 3 (Wed)** | (1) Re-cut portfolio recording #1 (IRS or SSA public-domain video, financial sample) in Descript Hobbyist (no watermark, 10 media hours): one 10-min episode, three Shorts via OpusClip Free (trim in CapCut desktop to avoid the watermark) or Starter; (2) three thumbnails in Canva Free; (3) log hours per step | Sample set #1 labeled "sample re-edit, not a client"; first real time log |
| **Day 4 (Thu)** | (1) Re-cut portfolio recording #2 (federal legal-education video, legal sample) in Descript Hobbyist; (2) write the mock memo from Prompt 5 on real public analytics if available, otherwise clearly labeled sample data; (3) publish the one-page site with both samples, a privacy-policy page and a support email | Sample set #2; site live |
| **Day 5 (Fri)** | (1) Draft 15 first-touch emails with Prompt 6, personalize each with one observation, send 15 from the aged personal address (not the four-day-old business mailbox, which is still warming); (2) send 10 LinkedIn connection notes; (3) record a 90-second Loom walking through what an A/B pack changes on one prospect's actual video (generic, reusable) | 25 touches out; Loom link |
| **Day 6 (Sat)** | (1) Finish prospect rows to 60 RIAs + 30 law firms; (2) build the approval form (Google Form: video, version, approver name, approved Y/N, notes) and Drive folder template (01_raw, 02_transcripts, 03_shorts_captions, 04_package_draft, 05_approved, 06_published); (3) set up Stripe ACH and the e-sign contract | 90 rows; delivery infrastructure ready |
| **Day 7 (Sun)** | (1) Review: hours logged for both samples versus the 16-22 h target (samples are half a client-month, so expect 8-11 h); (2) write next week's send list (25 touches, still from the personal address); (3) check warm-up progress on the business mailbox; (4) rest | Week 1 report in the KPI sheet |

## 3. 30 / 60 / 90-day plan

| Week | Milestone | KPI target (numeric) |
|---|---|---|
| 1 | Portfolio, site, pipeline, 25 touches | 90 qualified prospects; 25 touches; hours per sample logged |
| 2 | 25-30 touches; day-5 follow-ups; first calls | 55 cumulative touches; 1-2 replies; 1 call booked |
| 3 | 25-30 touches; refine message on reply data | 85 touches; 2-3 replies; first A/B pack proposal sent |
| 4 | 25-30 touches; first pack delivered if sold; switch sending to the warmed business domain (domain age 3+ weeks, SPF/DKIM/DMARC pass) | **Day 30: 100+ touches, 3+ replies, 1 pack sold or 3 calls booked** |
| 5 | Test & Compare running on pack #1; keep sending | 130 touches; 2 packs sold cumulative |
| 6 | Readout for pack #1 delivered with a Core proposal attached | 160 touches; 1 Core proposal out |
| 7 | Second readout; CPA test list built (20 firms) for October | 190 touches; 3 packs sold cumulative |
| 8 | Decision gate | **Day 60: 3 packs sold to channels clearing ~1,000 views per video on recent uploads; 200+ touches; 2+ Core proposals out** |
| 9-10 | Core close pursuit; onboarding kit final; October CPA outreach (20 touches) | 250 touches; 1 verbal yes |
| 11-12 | First Core month runs: recording, package, compliance submission | 300 touches; contract signed; first ACH invoice paid |
| 13 | Decision gate (adjust) | **Day 90: 1 Core retainer at $800+ signed (or signed start date within 30 days); hours per client-month logged at or below 22; approval cycle time recorded.** Short of that, continue only with 2+ live proposals or a verbal yes |
| 17 | Decision gate (kill) | **Day 120: no retainer at $800+ after 300+ personalized touches = demote** (report kill trigger 2) |

Realism note: the demand and execution skeptics put the first retainer at 2-4 months, so a day-90 outcome of "signed, first month in progress" is the base case, not "two retainers running". Two retainers is the month-5-6 base.

## 4. Acquisition playbook: first 10 customers

Targets: 10 customers = ~7 A/B packs + 2-3 Core retainers over months 1-6 (assumption consistent with the base scenario in [[reports/youtube-manager-expert-firms/report]]).

**Channels, in priority order**
1. **Cold email to RIA principals** (primary). Financial-services reply rates are the lowest of any vertical (1.5-3.5%, [Reachoutly 2026](https://reachoutly.com/cold-email/response-rate/); cross-industry average 3.43%, [Instantly 2026](https://instantly.ai/cold-email-benchmark-report-2026)), so the observation in line one must be about their actual video.
2. **LinkedIn connection note + comment-first** on advisors and attorneys who post their videos on LinkedIn (they are already video-motivated).
3. **Warm intros** via any CPA/attorney/advisor you personally know; ask for one introduction each, not a referral program.
4. **Communities where advisors talk about marketing** (XYPN, Kitces-adjacent groups, r/CFP for reading only, state bar solo-practice sections): answer questions about Test & Compare and compliance-safe packaging; never pitch in-thread.
5. **Upwork/Contra** only for posts that name a monthly budget of $800+ for channel management; ignore $100 fixed-price posts. Beginner win rates 3-8% (execution skeptic) make this a side channel.

**Daily volume:** 5-6 personalized touches per working day (25-30/wk), plus day-5 and day-12 follow-ups. Personalization takes 6-8 minutes each with Prompt 6 (assumption).

**Conversion assumptions (skeptic-corrected):** 100 touches -> 2-4 replies -> 1-3 meetings -> 0.3-0.9 closes. A/B packs close easier than retainers because the ask is $150-300 and two weeks; assume 1 pack per 50-75 touches and 1 retainer per 150-300 touches. Packs convert to Core at roughly 1 in 3 after a readable Test & Compare result (assumption); an "Inconclusive" result still converts if the memo shows what to test next.

**Qualification rule (do not waste a touch):** SEC- or state-registered RIA with no broker-dealer affiliation (IAPD check), or a law firm in a state without ad pre-filing fees; an existing recording habit; a channel with fewer than one upload a month. For A/B pack targets, qualify on recency and velocity, not lifetime views: the channel averages 1,000+ views per video on its last three uploads AND has uploaded in the last 90 days (Test & Compare needs roughly 1,000-5,000 fresh impressions per variant inside the two-week window, [Gyre, 2026](https://gyre.pro/blog/youtubes-new-title-ab-testing-tool-everything-creators-need-to-know); a months-old video with 1,000 lifetime views gets a few hundred impressions in two weeks and reads "Inconclusive"). If no recent video qualifies, offer the test on the client's next upload. Also confirm Advanced Features are enabled on the channel (Test & Compare requires them; phone verification plus ID/video verification or channel history; check in Studio > Settings > Channel > Feature eligibility, [YouTube Help](https://support.google.com/youtube/answer/9891124?hl=en)).

## 5. Delivery calendar template (per client, per month)

| Date | Action | Owner |
|---|---|---|
| 1st | Memo for last month sent; invoice for this month issued (ACH, due on receipt) | Operator |
| By 5th | Client records 45-60 min (camera + screen tracks); uploads to 01_raw | Client |
| 6th-8th | Transcript, segment proposal, rough cuts | Operator |
| 9th-12th | Retention polish, Shorts fix pass, thumbnails, metadata, compliance pre-check | Operator |
| 13th-15th | Package to compliance owner via approval form | Operator -> Client |
| SLA | 5 business days after month 2; expect 2-4 weeks in months 1-2 for RIAs (execution skeptic) | Client |
| Approval + 2 days | Schedule: Episode 1 Tue week 1, Episode 2 Tue week 2, Episode 3 Tue week 3; Shorts Thu and Sat each week; Test & Compare on each episode | Operator |
| Weekly Mon | Analytics pull to Sheet (manual month 1, n8n from month 2) | Automation |
| 25th | Next-recording brief: one question from the memo's "ask" plus two search-intent topics | Operator |

Content pillars for an RIA (rotate): (1) a rule or threshold explained (Social Security at 62 vs 70, RMD ages, Roth conversion brackets); (2) a mistake-to-avoid story with no client identifiers; (3) a "what changed this year" update. For an estate firm: (1) document basics (will vs trust); (2) a scenario ("what happens if..."); (3) state-specific rules.

## 6. Decision gates

| Gate | Double down if | Adjust if | Kill / pivot if |
|---|---|---|---|
| **Day 30** | 100+ touches, 3+ replies, 1 pack sold or 3 calls booked | Under 3 replies: rewrite line one (observation), switch 50% of volume to LinkedIn, test law firms harder | Zero replies after 100 touches and 2 message rewrites: pause, get 3 warm intros before spending more hours |
| **Day 60** | 3+ packs sold to channels with ~1,000+ views per video on recent uploads; 2+ Core proposals out; hours per pack under 4 | 1-2 packs sold: extend 3 weeks, cut price to $150, add Loom teardown to every touch | 0 packs after 200+ touches: kill per [[decisions/final-selection]]; move hours to podcast clipping or ghostwriting upsell |
| **Day 90** (adjust gate) | 1 Core retainer at $800+ signed; per-client hours at or below 22; approval cycle under 3 weeks | Retainer verbal but unsigned, or 2+ live proposals, or hours 22-26: keep going to day 120, template steps 8-10, raise price to $1,000 for the next client | Not a kill gate; if fewer than 2 live proposals and no verbal yes, spend the next 30 days on warm intros only |
| **Day 120** | 1 Core retainer signed and first month in progress | Verbal yes with a start date inside 30 days: hold | No retainer at $800+ after 300+ personalized touches: demote to a year-two upsell for ghostwriting clients (report kill trigger 2) |
| **Month 6** | 2 clients, hours per client trending to 16, one attributable booking per client | 2 clients but hours over 20: stop selling, template, then resume | 1 client and churn: run the compliance-and-packaging micro-offer ($300-500) instead |

## 7. Ready-to-use templates

### 7.1 Cold email (first touch)

```
Subject: Your Roth conversion video

[First name],

Your "[video title]" from [month] has [N] views and the title is the only thing on the page that does not say what it is about: it reads "[current title]". The moment at [mm:ss] where you explain [specific point] is the hook, and it is not on the thumbnail.

I run YouTube packaging and channel operations for fee-only RIAs. For $[200] I would set up a title-and-thumbnail test on that one video using YouTube's built-in Test & Compare (3 variants, two weeks), send you a one-page readout, and route everything through your compliance review first. Nothing goes live without your sign-off.

Worth a two-week test on that video?

[Name]
[Site] | [City, State] | Reply "no" and I will not follow up.
```

### 7.2 LinkedIn connection note (under 300 characters)

```
[First name], watched your "[video title]" episode; the [mm:ss] point about [topic] should be its own Short. I package YouTube for fee-only RIAs with compliance review built in. Happy to send one specific suggestion, no pitch.
```

### 7.3 Follow-ups

Day 5: "One more thing on [video title]: your description has no chapters, so the [topic] section at [mm:ss] is invisible to search. Two-week test still on the table if useful."
Day 12: "Last note from me. If YouTube is not a 2026 priority, no reply needed. If it is, here is a 90-second walkthrough of what the test changes: [Loom]."
Day 30 (packs only): "Test & Compare results on a similar channel came back this week: [one number]. Happy to share the readout format."

### 7.4 A/B pack pitch (call or proposal copy)

```
What you get: 3 titles and 3 thumbnails for one existing video, built from your face and your words; Test & Compare configured in your Studio (you keep full control); a one-page readout after two weeks (winner, CTR change, what to test next); a compliance note listing every word on every variant for your reviewer.
What I need: Manager access to the channel (never your password), Advanced Features enabled on the channel (Studio > Settings > Channel > Feature eligibility; a 5-minute phone plus ID or video verification if not), a video from the last 90 days on a channel averaging about 1,000+ views per upload (or we run the test on your next upload), your head-shot or a frame from the video, your disclaimer text, your compliance contact.
Price: $[200], paid on delivery of the variants; readout included. If the test comes back inconclusive, the readout tells you why and what to run next at no charge.
```

### 7.5 Core retainer proposal copy

```
Monthly: one 45-60 minute recording from you becomes 3 episodes, 8 Shorts, tested titles and thumbnails, descriptions with chapters and a tracked booking link, a compliance package for your reviewer, and a one-page memo with three numbers and one recommendation.
Your time: about 2-3 hours a month (recording plus one approval batch).
Price: $800/month, billed in advance by ACH, 30-day cancellation. Two consolidated revision rounds included; additional rounds $200.
Compliance: you or your CCO approve every item before it is scheduled; approved versions are archived with date and approver. I never use AI avatars, AI voices or synthetic likenesses; the only person on your channel is you.
First month: expect the review cycle to take 2-4 weeks while your reviewer sets a template; from month two the target is five business days.
```

### 7.6 Onboarding questionnaire (Google Form)

1. Firm legal name, registration type (SEC RIA / state RIA / BD-affiliated / law firm state / CPA state) and the name and email of the person who approves marketing.
2. Required disclaimer text, exactly as it must appear. Any required labels ("Attorney Advertising")?
3. Words or claims your reviewer has rejected before.
4. Three client problems you most want to be found for (phrased as the client would search them).
5. Who is your ideal client (age, situation, asset range or matter type)? Who is not?
6. Existing recordings: webinars, podcasts, past videos (links). Recording setup: camera, mic, screen-share tool. Can you record camera and screen as separate tracks?
7. Booking link and website; do you have a CRM or booking tool that can export UTM data?
8. Brand assets: logo, colors, fonts, head-shots; any existing thumbnail style.
9. Glossary: 20-30 terms, statutes, forms, product names and how you spell them.
10. Preferred recording day each month and approval turnaround you can commit to.
11. Channel access: will you add my account as Manager; is Advanced Features enabled on the channel (Studio > Settings > Channel > Feature eligibility); and will the channel owner authorize the read-only analytics connection once (it shows a Google "unverified app" screen because the app has under 100 users; details in the onboarding note)?
12. Anything off limits (topics, competitors, personal details).

### 7.7 Delivery SOP (one recording to published)

1. Confirm the raw upload has separate camera and screen tracks; if not, note it and proceed with the composite (Shorts will need square layout).
2. Descript: import once; transcript; correct glossary terms; remove long silences; filler removal at "moderate", never "all"; Studio Sound on camera track only; export the cleaned transcript with timestamps.
3. Claude Prompt 1 on the transcript; choose three segments; note the cold open for each.
4. Descript text-based cut per episode; add disclaimer card at 0:00-0:03 and at the end; lower thirds on first appearance; chapter cards at segment changes; 3-5 stat callouts; export 1080p.
5. OpusClip on the cleaned master: request 15-20 candidates; select 8; fix cuts to sentence boundaries; reframe; export caption text; run Prompt 3; correct captions; re-export.
6. Canva: 2-3 thumbnails per episode from a real frame or head-shot; check at 120 px width.
7. Claude Prompt 2 for metadata; edit; Claude Prompt 4 for the compliance pre-check; complete the human checklist.
8. Assemble the package in 04_package_draft: episodes, Shorts, thumbnails, metadata Doc, checklist, verification list of every number spoken; send the approval form link.
9. On written approval: move to 05_approved; upload as Private; set title, description, chapters, tags, playlist, end screen, pinned comment; set Test & Compare variants; schedule; confirm AI-disclosure toggle is No; log the approval and schedule in the Sheet.
10. Weekly analytics; monthly memo via Prompt 5; send by the 1st with the next-recording brief.

### 7.8 Monthly memo skeleton

```
[Firm] YouTube memo, [Month YYYY]
1. Booked consultations from YouTube links: [n] (last month [n]). Watch time: [h] (+/-%). Best CTR: [video] at [x]% after Test & Compare picked "[winning title]".
2. What worked: ...
3. What did not: ...
4. Next month: ...
5. Please answer on camera next recording: "[question phrased as a search]"
```

## 8. KPI dashboard and weekly time budget

**Dashboard (one Google Sheet, tabs: pipeline, delivery, finance, time)**

| KPI | Target | Source |
|---|---|---|
| Touches per week | 25-30 until 2 clients | Pipeline tab |
| Reply rate | 2-4% (floor 1.5%) | Pipeline tab |
| Meetings per 100 touches | 1-3 | Pipeline tab |
| A/B packs sold (cumulative), to channels meeting the recent-velocity rule | 1 by day 30, 3 by day 60, 7 by month 6 | Pipeline tab |
| Core retainers active | 1 by day 90-120 (kill gate day 120), 2 by month 6 | Finance tab |
| Hours per client-month | 16-22, trending to 16 | Time tab |
| Hours per A/B pack | under 4 | Time tab |
| Approval cycle time | under 3 weeks month 1-2, 5 business days after | Delivery tab |
| Revision rounds per batch | 2 or fewer | Delivery tab |
| Test & Compare readable results | 2 of 3 tests conclusive | Delivery tab |
| Attributable bookings per client per month | 1+ by month 4 of a retainer | Delivery tab (UTM) |
| Gross revenue, tool cost, net, effective hourly | Month 6 base $1,600 gross, $26-34/h; step to $1,000 price | Finance tab |

**Weekly time budget**

| Phase | Outreach | Production | Client loop / admin | Total |
|---|---|---|---|---|
| Weeks 1-8 (no retainer) | 4-5 h | 2-4 h (samples, packs) | 1 h | 7-10 h |
| 1 Core client | 3-4 h | 4-6 h | 1-2 h | 8-12 h |
| 2 Core clients | 1-2 h | 8-11 h | 2 h | 11-15 h |
| 3 Core clients (not recommended) | 1 h | 12-16 h | 2-3 h | 15-20 h |

## Sources

- [Instantly: Cold email benchmark report 2026 (3.43% average reply)](https://instantly.ai/cold-email-benchmark-report-2026)
- [Reachoutly: Cold email response rate 2026 (financial services 1.5-3.5%)](https://reachoutly.com/cold-email/response-rate/)
- [Cleverly: Cold email benchmarks by industry](https://www.cleverly.co/blog/cold-email-benchmarks-by-industry)
- [Gyre: YouTube title A/B testing in 2026 (impressions per variant, two-week window)](https://gyre.pro/blog/youtubes-new-title-ab-testing-tool-everything-creators-need-to-know)
- [YouTube Help: A/B test titles and thumbnails](https://support.google.com/youtube/answer/16391400?hl=en-GB)
- [YouTube Help: Channel permissions and API access](https://support.google.com/youtube/answer/9367690?hl=en)
- [YouTube Help: Get access to intermediate and advanced features (Test & Compare prerequisite)](https://support.google.com/youtube/answer/9891124?hl=en)
- [Google Cloud Help: Manage app audience (Testing vs In production, 7-day token expiry)](https://support.google.com/cloud/answer/15549945?hl=en)
- [Sonix: Descript pricing 2026](https://sonix.ai/resources/descript-pricing/)
- [Castmagic: Descript pricing 2026, free plan limits (60 media minutes, watermarked)](https://www.castmagic.io/blog/descript-pricing)
- [fluxnote: Descript pricing 2026 (Hobbyist $24, 10 media hours)](https://fluxnote.io/guides/descript-pricing-2026)
- [eesel: OpusClip pricing 2026 (Free 60 credits, Starter 150)](https://www.eesel.ai/blog/opusclip-pricing)
- [UnifyGTM: Cold email in 2026, domains, deliverability, replies](https://www.unifygtm.com/explore/cold-email-2026-domain-setup-deliverability-sequences)
- [Ozigi: How to warm up a sending domain in 2026](https://blog.ozigi.app/blog/how-to-warm-up-sending-domain-2026)
- [Litemail: Google sender requirements 2026 for cold email teams](https://litemail.ai/blog/google-sender-requirements-2026-cold-email)
- [Litemail: Free email warm-up tools 2026 (Instantly warm-up bundled with paid plans)](https://litemail.ai/blog/free-email-warmup-tools-2026-good-enough)
- [17 U.S.C. 105: US Government works (Cornell LII)](https://www.law.cornell.edu/uscode/text/17/105)
- [USAGov: Copyright and federal government materials](https://www.usa.gov/government-copyright)
- [IRS Video Portal](https://www.irsvideos.gov/)
- [SSA blog: 5 Social Security YouTube videos everyone should see (18 Aug 2026)](https://www.ssa.gov/blog/en/posts/2026-08-18.html)
- [DOL EBSA videos](https://www.dol.gov/agencies/ebsa/about-ebsa/our-activities/resource-center/videos)
- [IAA: Investment Adviser Industry Snapshot 2026](https://www.investmentadviser.org/wp-content/uploads/2026/06/Snapshot-2026.pdf)
- [The Florida Bar: Advertising regulation and fees from 1 Jul 2026](https://www.floridabar.org/ethics/etad/)
- [FINRA: Regulatory Notice 26-14](https://www.finra.org/rules-guidance/notices/26-14)
- [Smarsh: SEC Marketing Rule FAQs 2026](https://www.smarsh.com/blog/thought-leadership/sec-marketing-rule-faqs-2026-compliance-guidance/)
- [FeeCalcPro: Stripe ACH fees 2026](https://www.feecalcpro.com/blog/stripe-ach-guide/)
- [OneSuite: Video editing contract template 2026 (revision rounds)](https://onesuite.io/blog/video-editing-contract/)
- [Focus Digital: Marketing agency churn benchmarks 2026](https://focus-digital.co/average-marketing-agency-churn/)
- Vault: [[research/candidates/youtube-manager-expert-firms]], [[research/candidates/youtube-manager-expert-firms-skeptic-demand]], [[research/candidates/youtube-manager-expert-firms-skeptic-execution]], [[decisions/final-selection]], [[reports/youtube-manager-expert-firms/report]], [[reports/youtube-manager-expert-firms/automation-stack]]
