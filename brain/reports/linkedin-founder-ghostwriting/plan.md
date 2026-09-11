---
title: "Execution plan: LinkedIn founder ghostwriting from a weekly 30-minute voice interview"
tags: [plan, linkedin-founder-ghostwriting, 90-day]
updated: 2026-09-11
hustle: linkedin-founder-ghostwriting
type: plan
---

# Execution plan: LinkedIn founder ghostwriting

Day-by-day and 90-day plan for the offer analysed in [[reports/linkedin-founder-ghostwriting/report]], delivered with the machine in [[reports/linkedin-founder-ghostwriting/automation-stack]]. Every conversion number is skeptic-corrected ([[research/candidates/linkedin-founder-ghostwriting-skeptic-demand]], [[research/candidates/linkedin-founder-ghostwriting-skeptic-execution]]) or labelled "assumption". Portfolio role and kill criterion come from [[decisions/final-selection]]; dossier at [[research/candidates/linkedin-founder-ghostwriting]].

## TL;DR

- Start date assumed 2026-09-14 (Monday). Week 1 builds the portfolio, list and pitch; outreach starts day 3, not day 30. Budget 10-15 h/wk: ~6 h outreach, ~4 h portfolio/delivery, ~1 h admin in month 1.
- Acquisition math (assumptions, skeptic-corrected): 150 hand-sent messages in 6 weeks -> ~26% connection acceptance (Belkins 2025) -> 5-10% reply on a personalized message with a free rewrite attached (assumption; B2B sales benchmark is 6.5-7.5%) -> ~50% of replies to a call -> ~30-40% of calls to a paid pilot = roughly **1 pilot per 100-200 messages**, first payment in week 4-12 (median ~7).
- Prices: pilot $300-600 for 4 weeks / 8 posts, paid upfront; core retainer $800/mo (band $500-1,200), 3-month minimum, month 1 upfront; growth tier $1,200-1,500 only after two named case studies.
- Decision gates: day 30 = 100+ messages sent and >=5% reply rate or change list/pitch; day 60 = >=1 paid pilot or kill (150 messages, zero pilots); day 90 = >=2 paying clients and first recap showing an inbound conversation, or pivot to the clipping alternate.
- KPIs at day 90 (base): 250 messages, 20 replies, 8 calls, 2-3 pilots, 2 retainers, MRR $1,200-1,600, posts flagged as AI slop = 0, average edit time <= 35 min/post.
- Legal basics before the first call: written recording-consent clause (Otter/Fireflies litigation; 11-12 all-party-consent states), "AI-assisted, human-edited, client-approved" clause, no fabricated testimonials (FTC rule effective 2024-10-21), set aside 25-30% of every payment for tax (15.3% SE tax; quarterly estimates if owing >=$1,000).
- All outreach is hand-sent from the operator's own account; no extensions, no bots, no more than ~20-25 connection requests a day. The client publishes through their own Buffer OAuth; the operator never holds a client password.

## 1. Prerequisites checklist

**Accounts and tools (cost in [[reports/linkedin-founder-ghostwriting/automation-stack]] section 3)**
- [ ] LinkedIn profile rewritten for the offer: headline "LinkedIn ghostwriter for agency owners | One 30-min call a week, hand-edited, never slop"; About section with the anti-slop guarantee; featured section with 3 sample posts.
- [ ] Claude Pro ($20/mo) with one Project named "GW - Template" holding prompts 1-6.
- [ ] Fireflies account (free until the first paid call, then Pro $18/mo or $10/mo annual); speaker-identification/voiceprint features disabled in settings.
- [ ] Google Workspace free: Meet, Docs, Sheets, Drive folder tree `Clients/{ClientCode}/{Drafts, Recaps, Analytics, Contracts}`.
- [ ] Buffer free account for the operator's own posts; a written one-page "how to connect your LinkedIn to Buffer" guide for clients.
- [ ] Canva free (Pro when the first carousel is due); one carousel template at 1080x1350.
- [ ] Wave free invoicing (or Stripe): invoice template with "Due on receipt; work starts on payment"; ACH enabled (1% Wave / $0 Stripe ACH) to cut card fees.
- [ ] Metrics Google Sheet with tabs Outreach, Delivery, Results, Money (spec in the automation note, section 7).

**Assets**
- [ ] Portfolio: 10 posts written for yourself or a friend in the target niche, 3 in the featured section, all 10 in a public Google Doc "Samples".
- [ ] Prospect Sheet with 150 rows (name, company, size, why-them note, last post link, status, dates).
- [ ] Outreach scripts, pitch one-pager, proposal template, onboarding questionnaire, contract (all in section 7 below).
- [ ] Interview question sheet v1 and voice-guide prompt tested on your own past posts.

**Legal and money basics (US sole proprietor)**
- [ ] Operate under your own name at first (no LLC needed for a $300 pilot); register a DBA/LLC when MRR passes ~$2,000 (assumption; check state fees).
- [ ] Contract clauses: scope (calls, post count, 1 revision round per post), payment upfront, 3-month minimum on retainers with 30-day notice, 48-hour silent approval, recording consent (client consents to recording and AI transcription of every call and will inform any guest), AI-assisted drafting disclosure, rights assignment ("all rights the writer holds in the deliverables transfer on payment; writer warrants originality"), no guarantee of reach or leads, client responsible for the accuracy of facts about their business, client will not publish unedited AI drafts.
- [ ] Tax: separate bank account or sub-account; move 25-30% of every payment there; calendar the 2026-2027 estimated dates (Sep 15 2026, Jan 18 2027, Apr 15, Jun 15, Sep 15 2027) ([Found, 2026](https://found.com/resources/tax-deadlines)); note the 1099-K threshold is $600 for 2026 so payment processors will report ([TurboTax, 2026](https://blog.turbotax.intuit.com/self-employed/self-employed-dont-forget-about-the-estimated-tax-deadline-19852/)).
- [ ] If you live in CA, FL, IL, WA, PA, MA, MD, MT, NV, NH, CT or DE: recording consent is not optional; read your state's rule ([Basil AI, 2026-07-07](https://basilai.app/articles/2026-07-07-recording-meetings-two-party-consent-states-ai-notetaker-compliance-guide-2026.html)).

## 2. Week 1, day by day (assumed start Monday 2026-09-14; ~2 h/day)

| Day | Tasks | Expected output |
|---|---|---|
| **Day 1 (Mon)** | 1. Set up Claude Project, Fireflies, Wave, Drive tree, metrics Sheet. 2. Rewrite your LinkedIn headline and About. 3. Pull 20 of your own or a friend's past posts/emails; run Prompt 1 to test the voice-guide process on yourself. | Tools live; profile reads as a ghostwriter for agency owners; you have seen what the voice guide produces and what it gets wrong |
| **Day 2 (Tue)** | 1. Write 5 portfolio posts (use Prompt 3 on a 20-minute self-interview recorded on your phone, then hand-edit each for 30 min). 2. Run Prompt 4 on each until slop score <= 3. 3. Publish 1 on your own profile. | 5 finished samples; first-hand feel for the 20-45 min edit; one live post |
| **Day 3 (Wed)** | 1. Build the first 50 prospect rows: Clutch (marketing/dev/design agencies, 10-49 staff, US), LinkedIn search "founder" + "agency" + city, and "fractional CFO/CMO". Qualify: owner-operator, posts less than weekly or posts generic AI-looking content. 2. Send the first 10 connection requests with the note in section 7.1. | 50-row list; 10 requests sent; funnel tab started |
| **Day 4 (Thu)** | 1. Write 5 more portfolio posts (total 10). 2. Draft the pitch one-pager (Carrd or Notion) with the guarantee, packages, 3 samples. 3. Send 10 more connection requests. 4. For 3 prospects who already accepted or are 2nd-degree, draft a free rewrite of one of their posts with Prompt 3 + hand edit (15 min each) and send the message in 7.2. | 10 samples; one-pager live; 20 requests out; 3 rewrite samples sent |
| **Day 5 (Fri)** | 1. Send 10 connection requests + 5 rewrite-sample messages. 2. Email version: find 10 agency owners' emails from their sites, send the 7.3 email. 3. Record a 25-minute practice interview with a friend using Prompt 2; run the whole pipeline to a finished post in under 90 minutes. | 30 requests, 8 samples, 10 emails out; pipeline timed end to end |
| **Day 6 (Sat)** | 1. Add 50 rows to the prospect list (fractional execs, consultants). 2. Post sample #2 on your profile. 3. Finalize contract, questionnaire and proposal template (section 7). 4. Review the week's funnel numbers. | 100-row list; contract ready; funnel: 30 requests, ~8 accepted (assumption), 0-2 replies |
| **Day 7 (Sun)** | 1. Send follow-ups (7.4) to anyone who accepted but did not reply after 3 days. 2. Plan week 2: 20 requests + 10 samples + 10 emails per week minimum. 3. Update the metrics Sheet. 4. Rest. | Week 2 plan; week 1 totals logged: target 30 requests, 8 samples, 10 emails, 10 portfolio posts, 2 own posts |

## 3. 30 / 60 / 90-day plan

Weekly outreach floor from week 2: 25 connection requests, 10 personalized rewrite-sample messages, 10 emails, 2 own LinkedIn posts, 5 thoughtful comments on prospects' posts (all by hand).

### Days 1-30: prove someone will reply

| Week | Milestones | KPI targets (cumulative) |
|---|---|---|
| 1 | Tools, portfolio, first 30 requests | 30 messages, 100-row list, 10 samples |
| 2 | Outreach at floor; first discovery call booked | 70 messages, 3-5 replies, 1 call |
| 3 | Pitch refined from call feedback; first proposal sent | 110 messages, 6-9 replies, 2-3 calls, 1 proposal |
| 4 | First pilot closed (optimistic edge) or two proposals live | 150 messages, 8-12 replies, 3-4 calls, 0-1 pilots ($300-600 paid) |

Day-30 KPI: >=100 messages sent, reply rate >=5% of accepted connections, >=2 calls, own profile publishing 2x/week.

### Days 31-60: first dollar and first delivery

| Week | Milestones | KPI targets (cumulative) |
|---|---|---|
| 5 | Pilot #1 onboarding: consent, questionnaire, 45-min intake, voice guide approved | 190 messages, 1 pilot, onboarding 4-8 h logged |
| 6 | First weekly interview; first 2-3 posts approved and scheduled via client's Buffer | 230 messages, 3 posts live, revision rounds logged |
| 7 | Pilot #2 closed (median case first payment lands here); pilot #1 week-3 call | 270 messages, 1-2 pilots, 6 posts live |
| 8 | Pilot #1 mini-recap; conversion conversation to $800 retainer with month-2 $100 credit | 300 messages, 8 posts live, 1 retainer offer made |

Day-60 KPI: >=1 paid pilot (kill test: 150 messages with zero pilots = kill); posts flagged as AI slop = 0; average edit time <= 40 min/post; client approval within 48 h on >= 70% of posts.

### Days 61-90: second client and first proof

| Week | Milestones | KPI targets (cumulative) |
|---|---|---|
| 9 | Pilot #1 -> retainer (or documented reason it did not); pilot #2 onboarding | 340 messages, 1 retainer, 2 active clients |
| 10 | First carousel shipped; first monthly recap with the client's analytics export | 380 messages, 12-16 posts live across clients |
| 11 | Referral ask on the first inbound win; case study #1 drafted (with permission) | 1 referral request, 1 case study |
| 12 | Pricing review: new pilots at $500-600; outreach shifts 50% to referrals/warm intros | 400+ messages, 2 retainers, MRR $1,200-1,600 (base), $600 (conservative), $2,000+ (upside) |

Day-90 KPI: >=2 paying clients; >=1 recap showing an inbound DM or call the client attributes to a post; churn 0; hours <= 13 h/wk total; tools <= $66/mo.

## 4. Acquisition playbook: first 10 customers

**Channels, ranked**
1. **LinkedIn connection + personalized DM with a free rewrite of one of their posts** (primary; Dunham's channel; the Substack playbooks' opener). Hand-sent only.
2. **Cold email to agency owners** found via their own websites and Clutch listings (secondary; B2B cold-email replies run 1-5%, [Prospeo, 2026](https://prospeo.io/s/b2b-cold-email-reply-rates)).
3. **Warm intros**: ask every call, paid or not, "who else runs an agency and hates writing?" Practitioners report first clients often arrive "through a chain of four people" (execution skeptic).
4. **Comments on prospects' posts** (5/day, substantive), which makes the later DM a reply not a cold pitch.
5. **Your own profile** posting 2x/week in the client's voice style, so the profile is the portfolio.
6. Not used: Upwork/Fiverr bidding (median $32/h floor; only as a pivot funnel), paid ads, automation tools.

**Daily volume targets (weekdays, ~45-60 min/day)**: 5 connection requests with note, 2 rewrite-sample DMs, 2 emails, 1 comment, plus follow-ups due that day. Weekly: 25 / 10 / 10 / 5. Six-week total: 150 connection requests, 60 sample DMs, 60 emails.

**Conversion assumptions (all assumptions unless cited)**

| Stage | Rate | Basis |
|---|---|---|
| Connection request -> accepted | ~26% | Belkins 2025, 20M+ attempts: 26.42% with note, 26.37% without ([Belkins, 2025](https://belkins.io/blog/linkedin-outreach-study)) |
| Accepted + sample DM -> reply | 5-10% | Assumption. B2B sales campaigns reply 6.4-7.5% by month (Belkins); vendor claims of 18-25% for warm, targeted DMs ([Expandi, 2026](https://expandi.io/blog/linkedin-outreach-benchmarks-2026/)) are treated as an upper bound. The demand skeptic notes no ghostwriting-specific reply data exists |
| Cold email -> reply | 1-5% | ([Prospeo, 2026](https://prospeo.io/s/b2b-cold-email-reply-rates)) |
| Reply -> discovery call | ~50% | Assumption |
| Call -> paid pilot | 30-40% | Assumption; one agency's marketing page claims 15% outreach-to-demo and 30% trial-to-paid (execution skeptic; interested party) |
| Pilot -> retainer | 50-60% | Assumption; no data. Skeptics say assume >=25% churn by month 3 |
| Net | ~1 pilot per 100-200 messages | Both skeptics |

Worked example for 6 weeks: 150 requests -> ~39 accepted -> plus 60 emails -> 5-8 replies -> 3-4 calls -> 1-2 pilots. That is the whole plan for the first 60 days; it is thin by design, which is why the kill criterion is binary.

**First-10 sequencing**: clients 1-2 from cold DMs at $300-600 pilots (weeks 4-10); clients 3-4 from referrals of clients 1-2 plus continued outreach at $500-600 pilots (months 3-5); clients 5-6 replace churn and fill capacity at $800 (months 5-8); clients 7-10 only exist if hours rise above 15/wk or price rises to $1,200+ (assumption; capacity ceiling ~3-4 clients at 10-15 h/wk).

## 5. Delivery calendar template (per client, per month)

| Week | Mon | Tue | Wed | Thu | Fri |
|---|---|---|---|---|---|
| 1 | 30-min call (client's evening slot); Fireflies transcript in | Drafts via Prompt 3; specificity edit posts 1-2 | Edit post 3; Prompt 4 critique; Doc to client (48-h clock) | Client review | Approved posts to client's Buffer: Tue / Thu of next week |
| 2 | Call | Drafts + edit | Critique + Doc | Review | Schedule; carousel seed chosen |
| 3 | Call | Drafts + edit | Critique + Doc | Review | Schedule; carousel copy via Prompt 5, Canva build |
| 4 | Call | Drafts + edit; client exports analytics | Critique + Doc; Prompt 6 recap draft | Review; recap sent; referral ask if inbound win | Schedule; next month's topic bets; invoice for next month (retainers) |

Posting cadence: Tuesday and Thursday mornings in the client's timezone for text posts, one document post per month on a Wednesday (assumption; native documents are the top-engaging format per Socialinsider 2026). Two posts per week satisfies the 8-10/mo core scope; three per week for the growth tier.

## 6. Decision gates

| Gate | Double down if | Adjust if | Kill / pivot if |
|---|---|---|---|
| **Day 30** | >=100 messages sent, reply rate >=8%, >=2 calls booked | Reply rate 3-8%: rewrite the opener, switch from rank-1 niche to rank-2 (fractional execs), add the rewrite sample to every message | <100 messages sent (the problem is you, not the market: fix the schedule before judging the offer); reply rate <3% after 100: change list and pitch, restart the 6-week clock once |
| **Day 60** | >=1 paid pilot and posts shipping with 0 slop flags and <=40 min edits | 1 pilot but edits >60 min/post or >2 revision rounds: fix the interview (longer calls, better questions) before selling more | 150+ hand-sent messages and 0 pilots (the [[decisions/final-selection]] tripwire): stop, run the Fiverr profile-rewrite funnel for 30 days as the last test, then hand the hours to [[research/candidates/podcast-clipping-retainer]] |
| **Day 90** | >=2 paying clients, >=1 attributable inbound conversation, churn 0, MRR >=$1,200 | 2 clients but no attributable inbound: add comment-reply drafting to scope at no charge for one month; if still none, re-examine niche | 1 client and it churned at the end of the pilot, or 2 of 3 clients gone by month 4: the product does not produce results at this price; pivot to the repurposing add-on for the YouTube-manager clients or the clipping alternate |

## 7. Ready-to-use templates

### 7.1 Connection request note (under 300 characters)
> Hi {First}, I write LinkedIn posts for agency owners from a 30-minute call a week, hand-edited so they never read as AI. Saw your post on {specific topic}; would like to follow your work.

### 7.2 DM with free rewrite (send 2-3 days after acceptance)
> {First}, quick one, no pitch deck. I took your post from {date} about {topic} and rewrote it the way I'd write it for you: same story, sharper first line, one concrete number pulled forward. Here it is:
>
> {rewritten post, 600-900 characters}
>
> Why I did that: LinkedIn now cuts views ~40% on posts it flags as AI slop, and most agency owners I talk to are either not posting or posting from a tool that sounds like everyone else. I fix that with one 30-minute call a week and a hand edit on every post.
>
> If the rewrite is useful, keep it, it's yours. If you want 8 of them over the next month, I run a 4-week pilot at ${300-600}, paid upfront, and I'll refund the month if any post I write gets flagged. Worth a 20-minute call?

### 7.3 Cold email (subject: "your {date} post, rewritten")
> Hi {First},
>
> I rewrote one of your LinkedIn posts ({topic}) below. Same story, your words where I could keep them, first line changed so it earns the "see more" click.
>
> {rewrite}
>
> I'm a LinkedIn ghostwriter for agency owners: one 30-minute call a week, 8-10 posts a month, every one hand-edited so it never reads as AI. Four-week pilot is ${price}, upfront, refunded if LinkedIn flags anything I wrote.
>
> If your next client usually comes from someone who already trusts you, this is the cheapest way to make more of those people. Reply "call" and I'll send times.
>
> {Name}
> {one-pager link}

### 7.4 Follow-up (3 days later, once; then 7 days later, once)
> {First}, did the rewrite land? No worries if it's a no; if it's a "not now", tell me when to check back and I will.

> Last note from me: I have {2} pilot slots open for {month}. If you want one, reply and I'll hold it until {date}. Either way, thanks for reading.

### 7.5 Pitch / offer copy (one-pager and discovery call)
**Headline:** One 30-minute call a week. Your LinkedIn, done, never slop.
**Who it's for:** Owners of agencies and fractional executives whose next client comes from being trusted, who have stories to tell and no time to write them.
**How it works:** 1) We talk for 30 minutes on a call you can take from the car. 2) I turn it into 8-10 posts a month, each hand-edited until it sounds like you, plus one document post. 3) You approve in a shared doc (48-hour silent approval), and it publishes from your own account. 4) Monthly one-page recap: inbound conversations first, vanity metrics last.
**Guarantee:** If LinkedIn flags a post I wrote as AI slop, that month is free.
**Pricing:** 4-week pilot ${300-600}, paid upfront. Core retainer $800/month, 3-month minimum. Growth (12 posts, comment drafts, pipeline recap) $1,200-1,500 after month 3.
**What I don't do:** log into your account, automate comments, promise reach, invent customer stories.

### 7.6 Discovery call script (20 minutes)
1. (2 min) "Tell me how your last two clients found you." (listen for referrals/trust)
2. (3 min) "What's your LinkedIn doing today, and who writes it?" (in-house writer = disqualify or profile-rewrite upsell)
3. (5 min) "Tell me about a client project that went sideways this year." (this is a live sample interview; note whether stories come easily)
4. (3 min) Show the rewrite; ask what felt right and wrong; capture banned phrases.
5. (4 min) Scope and price; recording consent; approval rule; who publishes.
6. (3 min) Close: "Pilot is ${price}, upfront; onboarding call next week; first posts live in two weeks. Invoice today?"

### 7.7 Onboarding questionnaire (Google Form, 20 questions)
1. Full name, role, company, URL, LinkedIn URL.
2. In one sentence, who do you sell to and what do they pay you for?
3. How did your last three clients find you?
4. What do you want LinkedIn to do for you in six months (inbound calls, hiring, investors, partners)?
5. Three topics you could talk about for an hour without notes.
6. Three opinions you hold that peers in your industry would argue with.
7. A client story with a number in it (revenue, time saved, percentage) that you are allowed to tell.
8. A failure or expensive mistake you are willing to share.
9. Five phrases you say all the time.
10. Ten words or phrases you hate seeing in LinkedIn posts.
11. Do you use emoji? Hashtags? Swearing? First names of clients?
12. Names, clients, numbers or topics that are off-limits.
13. Any partners, tools or investors you are paid by or have a stake in (for disclosure).
14. Links to 10-20 past posts, emails, talks or podcasts that sound like you.
15. Best weekly 30-minute slot for the call (evenings fine); timezone.
16. Who approves posts, and may I assume approval after 48 hours of silence?
17. Do you consent to recording and AI transcription of our calls? (Yes/No; if No, I will take typed notes.)
18. Will you connect your LinkedIn to Buffer yourself, or post manually?
19. How will you tell me about inbound DMs or calls that come from posts? (monthly reply to my recap is fine)
20. Anything else I should know before I write as you?

### 7.8 Delivery SOP (per client, per week; ~2.5-3 h)
1. Mon, 10 min before the call: run Prompt 2; skim last week's post stats.
2. Call: open with "Quick reminder this call is recorded and transcribed for the posts, all good?"; run the sheet; end with the carousel-seed question.
3. Within 24 h: Fireflies transcript -> Prompt 3 -> Google Doc "Drafts - {code} - {date}".
4. Edit each post 20-45 min: cut every generic line, pull the specific into the hook, restore verbatim phrases, end on a statement.
5. Prompt 4 on each; fix until score <= 3; run the QA checklist in the automation note.
6. Share the Doc with a dated comment "Approve or edit by {date +48h}; silence = approved."
7. On approval: paste into the client's Buffer (their OAuth session, screen-share on onboarding) for Tue/Thu; document posts need a title.
8. Log: posts shipped, edit minutes, revision rounds, days to approval.
9. Week 4: recap via Prompt 6 from the client's export; referral ask if inbound; invoice next month.

### 7.9 Contract clause snippets (edit with a template; not legal advice)
- *Recording:* "Client consents to audio recording and automated transcription of all calls under this agreement, will notify any third party joining a call, and acknowledges recordings are retained for 90 days."
- *AI disclosure:* "Deliverables are drafted with AI assistance, edited by the Writer, and approved by the Client before publication. Client agrees not to publish drafts marked 'not for publication'."
- *Rights:* "On payment, Writer assigns to Client all rights Writer holds in approved deliverables and warrants that they are original and not copied from third parties."
- *Results:* "Writer makes no representation regarding reach, engagement, leads or revenue."
- *Facts:* "Client is responsible for the accuracy of statements about Client's business, customers and results, and confirms permission for any customer named."
- *Approval:* "Drafts not commented on within 48 hours of sharing are deemed approved."
- *Term:* "Retainers require a 3-month minimum and 30 days' written notice; month 1 is payable before work begins."

## 8. KPI dashboard and weekly time budget

**Dashboard (Google Sheet, one row per week; review every Sunday)**

| KPI | Target month 1 | Target month 3 | Source tab |
|---|---|---|---|
| Connection requests sent | 100 | 400 cumulative | Outreach |
| Sample DMs + emails sent | 40 | 160 cumulative | Outreach |
| Reply rate on accepted + sample | >=5% | >=8% | Outreach |
| Discovery calls | 2 | 8 cumulative | Outreach |
| Pilots closed | 0-1 | 2-3 cumulative | Outreach |
| Active retainers | 0 | 2 | Money |
| MRR | $0 | $1,200-1,600 | Money |
| Posts shipped | 0 | 12-16/mo | Delivery |
| Posts flagged as AI slop | 0 | 0 | Delivery |
| Avg edit minutes per post | n/a | <=35 | Delivery |
| Revision rounds per post | n/a | <=1.5 | Delivery |
| Days to approval | n/a | <=2 | Delivery |
| Inbound conversations reported by clients | n/a | >=1 | Results |
| Hours per week (total) | <=12 | <=13 | Money |
| Tool spend | <=$40 | <=$66 | Money |
| Effective $/h pre-tax | $0 | $20-30 | Money |

**Weekly time budget**

| Block | Month 1 (no clients) | Month 3 (2 clients) | Month 6 (2-3 clients) |
|---|---|---|---|
| Outreach and follow-ups | 6 h | 4 h | 2 h |
| Own profile posts and comments | 2 h | 1.5 h | 1 h |
| Client calls (30-45 min each + prep) | 0 | 1.5 h | 2 h |
| Drafting, editing, QA | 3 h (portfolio) | 4 h | 5 h |
| Client review, scheduling, carousel | 0 | 1.5 h | 2 h |
| Admin, invoicing, metrics, tax set-aside | 1 h | 0.5 h | 0.5 h |
| **Total** | **12 h** | **13 h** | **12.5-13 h** |

If the total exceeds 15 h for two consecutive weeks at 3 clients, stop outreach rather than cut the edit; the edit is the product.

## Sources

- [B2B LinkedIn Outreach Benchmarks, 2025 Study (Belkins, 2025)](https://belkins.io/blog/linkedin-outreach-study)
- [LinkedIn Outreach Benchmarks 2026: 13.2M data points (Expandi, 2026; vendor)](https://expandi.io/blog/linkedin-outreach-benchmarks-2026/)
- [B2B Cold Email Reply Rates: 2026 Benchmarks (Prospeo, 2026)](https://prospeo.io/s/b2b-cold-email-reply-rates)
- [My LinkedIn Ghostwriting Side Hustle Makes $9K to $12K a Month (Entrepreneur, 2026-07-30)](https://www.entrepreneur.com/side-hustle/i-turned-a-simple-observation-into-a-linkedin-based-side-hustle-that-makes-9000-to-12000-a-month)
- [How To Land Your First Ghostwriting Client Without Case Studies (Start Ghostwriting, Substack, Feb 2026)](https://startghostwriting.substack.com/p/how-to-land-your-first-ghostwriting)
- [The 5 Moves I'd Make If I Had to Start Ghostwriting From $0 Today (The Human Project, Substack, 2026)](https://thehumanproject.substack.com/p/ai-didnt-kill-ghostwriting-it-killed)
- [LinkedIn says 1M people have reported AI slop, 40% fewer views (Social Media Today, Aug 2026)](https://www.socialmediatoday.com/news/linkedin-says-1m-people-have-reported-ai-slop/828465/)
- [LinkedIn Organic Benchmarks 2026, document posts top format (Socialinsider, 2026)](https://www.socialinsider.io/social-media-benchmarks/linkedin)
- [LinkedIn Automation Rules 2026: Banned vs. Safe Tools (Northlight, 2026)](https://northlight.ai/blog/is-linkedin-automation-against-the-rules)
- [How Much Does LinkedIn Ghostwriting Cost? Real Pricing Tiers for 2026 (Lifast, 2026)](https://www.lifa.st/how-much-does-linkedin-ghostwriting-cost)
- [How Much Does a LinkedIn Ghostwriter Cost? (Mylance, 2026)](https://www.mylance.co/blog/how-much-does-a-linkedin-ghostwriter-cost)
- [Recording Meetings in Two-Party Consent States, 2026 guide (Basil AI, 2026-07-07)](https://basilai.app/articles/2026-07-07-recording-meetings-two-party-consent-states-ai-notetaker-compliance-guide-2026.html)
- [AI Meeting Recorder Lawsuits 2026: Otter.ai, Fireflies (tl;dv, 2026)](https://tldv.io/blog/ai-meeting-recorder-lawsuits/)
- [The Consumer Reviews and Testimonials Rule: Q&A (FTC)](https://www.ftc.gov/business-guidance/resources/consumer-reviews-testimonials-rule-questions-answers)
- [Copyright and AI, Part 2: Copyrightability (US Copyright Office, 2025-01-29)](https://www.copyright.gov/ai/Copyright-and-Artificial-Intelligence-Part-2-Copyrightability-Report.pdf)
- [2026 Tax Deadlines for Small Business Owners (Found, 2026)](https://found.com/resources/tax-deadlines)
- [Estimated Quarterly Tax Dates in 2026 (TurboTax blog, 2026)](https://blog.turbotax.intuit.com/self-employed/self-employed-dont-forget-about-the-estimated-tax-deadline-19852/)
- [Wave Invoicing Pricing and Fees (tech.co, 2026)](https://tech.co/accounting-software/wave-invoicing)
- [Buffer: How to Schedule LinkedIn Posts in 2026 (Buffer resources, 2026)](https://buffer.com/resources/how-to-schedule-linkedin-posts/)
- Vault: [[research/candidates/linkedin-founder-ghostwriting]] · [[research/candidates/linkedin-founder-ghostwriting-skeptic-demand]] · [[research/candidates/linkedin-founder-ghostwriting-skeptic-execution]] · [[decisions/final-selection]] · [[reports/linkedin-founder-ghostwriting/report]] · [[reports/linkedin-founder-ghostwriting/automation-stack]] · [[research/candidates/podcast-clipping-retainer]]
