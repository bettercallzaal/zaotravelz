# zaotravelz - Year of the ZAO Festivals Campaign HQ

**One line:** Central coordination repo for The ZAO's event-circuit strategy, anchored on Devcon 8 Mumbai (Nov 2026) as the 2026 "proof leg" toward a 2027 full conference circuit.

**Who it's for:** Zaal (founder), anyone building the ZAO festivals operation, or a fresh Claude reading this to pick up where the last session left off.

## Status

Working repo, mid-campaign (updated 2026-07-13). The core deliverables (sponsor pitch, crowdfund copy, Scholars essay) are drafted. Campaign is live on GitHub Pages. Awaiting external signals (Builder Discount applications, Ecosystem Program R2, photo archive from AttaBotty) to unlock the next phase.

| Workstream | State |
|---|---|
| Campaign HQ (docs/index.html) | LIVE. Live signals dashboard updated daily. |
| Devcon 8 sponsor pitch (docs/devcon8.html) | LIVE. Numbers reconciled Jul 3. |
| Build Camp (Jul 4-11 ETH curriculum) | IN PROGRESS. Lessons 01-02 written, 03-05 queued. Demo day Jul 11. |
| Outreach kit (7 messages) | DRAFTED. Zero sent - awaiting Zaal's send signal. |
| Collateral (reel, tech rider, rate card, testimonials, insurance) | IN PROGRESS. Rate card + tech rider drafted. Photo archive = critical blocker. |
| Scholars essay + crowdfund copy | DRAFTED. Sequencing: lock Build Camp result + Ecosystem outcome, THEN launch. |
| Community Hub proposal (RFP-13) | DRAFTED. Co-organizer confirmation = blocker (deadline Aug 12). |
| Trip logistics | LOCKED. $969-2,294 per person; Diwali surge warning Nov 6-10; Indian artist lever available. |
| 2027 circuit research | PAUSED. Zaal: "wait and align after". Revisit trigger = after Devcon 8 wraps (mid-Nov). |

## Stack

- **No code.** Static markdown docs + HTML pages (GitHub Pages).
- **Source of truth:** This repo.
- **Live:** https://bettercallzaal.github.io/zaotravelz/ (push main = Pages redeploy).
- **Research backref:** ZAOOS research/events/ (doc 945 logistics/funding, 946 history/Mumbai, 947 circuit/landscape) - UNMERGED in ZAOOS, Zaal reviews.
- **Fundraising:** Separate repo + loop (ZAOartizen + Artizen Season 6 live now).

## Quick Start

No build step. Clone, read, edit in markdown, push to main.

```bash
git clone https://github.com/bettercallzaal/zaotravelz
cd zaotravelz
# Read the files below to understand current state
cat HANDOFF.md LOOP.md CONTEXT.md
# Edit .md or .html files, push to main
git add .
git commit -m "..."
git push origin main
# GitHub Pages redeploys automatically; live at bettercallzaal.github.io/zaotravelz
```

**Env vars:** None. No secrets to set.

**Dependencies:** None. Markdown + static HTML.

## Project Map

Read these in order to pick up the work:

1. **HANDOFF.md** (session close from Jul 3) - what's live, what's blocked on Zaal, top 5 next actions.
2. **LOOP.md** (build playbook) - every wake runs CHECK (live signals) -> BUILD (one artifact) -> UPDATE (board + tracker). Cadence rules + standing blocked queue.
3. **CONTEXT.md** (portable brain) - brand rules, proof numbers, event-circuit people, workflow rules, repo map. Read if you're new.
4. **partners-tracker.md** - full outreach + partnership tracking table (15 pages). Status, next step, owner for every person/event/application.

**Campaign core files:**

- **docs/index.html** - live campaign HQ (status signals, upcoming actions, crew roster).
- **docs/devcon8.html** - sponsor pitch (offerings, WaveWarZ proof, community numbers, testimonials).
- **2027-year-of-zao-festivals.md** - THE MASTER STRATEGY. 2026 proof leg (Mumbai Oct, Marfa, ZAOstock Oct 3), 2027 circuit targets (10-15 events, quarterly breakdown).
- **devcon-guide.md** - Devcon 8 sponsorship intel (available tiers, deadlines, community hub path, ecosystem program).
- **devcon-america.md** - US builder community track (ESP mini-grant angle, parallel to Mumbai).

**Pitch kit (ready to send):**

- **pitch/sponsor-onepager.md** - 1-page tier table + deliverables.
- **pitch/crowdfund-copy.md** - Seed Club campaign copy + Farcaster cast sequence (PARKED until Build Camp + Ecosystem outcome).
- **pitch/scholars-essay.md** - Devcon Scholars application (PARKED same reason).
- **pitch/season-sponsor-deck-outline.md** - outline only; build blocked on photo archive.

**Collateral drafts:**

- **collateral/rate-card.md** - artist booking rate card (awaiting Zaal approval).
- **collateral/tech-rider.md** - AV/setup requirements for an event.
- **outreach/\*.md** - 7 drafted messages (ecosystem email, Shriyash, Coop DM, Farcaster cast, 2 rail partner asks).

**Trip facts & logistics:**

- **trip-facts.md** - Devcon ticket tiers, group rules, per-person cost breakdown (LOW/MID scenarios), artist eligibility checklist, Diwali surge warning, Indian artist leverage math.
- **budget.md** - trip budget summary (visa paid, BOS confirmed).
- **docs/travel.html** - circuit travel ops (days-away load, entry requirements, multi-stop budget, crew roster - LIVE).
- **docs/events.html** - 2026-2027 event calendar (all known upcoming stops).

**Build Camp (Jul 4-11):**

- **buildcamp/notes.md** - project ideas, prep checklist, demo day schedule.
- **eth-learning/01-*.md, 02-*.md** - Ethereum fundamentals + rollups/Base curriculum. 03-05 queued.

**Research & intake:**

- **research-conference-landscape-full.md** - full conference landscape research (2,000+ lines).
- **intake-artizen-festivals.md** - Artizen fundraising intake and proof pack.

## How to Continue

**Next 5 actions (priority order, from HANDOFF.md):**

1. **TONIGHT (if Build Camp is active, else by Jul 14):** Finalize Build Camp prep checklist (buildcamp/notes.md) + day-1 cast.
2. **Send drafted outreach** - Shriyash/Arun (India co-organizer) + ecosystem@devcon.org emails (both in outreach/). These unlock the Aug 12 hub proposal critical path.
3. **CHECK loop on wake** - webfetch tickets.devcon.org (Builder Discount) and devcon.org/en/ecosystem-program (R2). If either opens, apply same day.
4. **Reconcile numbers with Zaal** - confirm WaveWarZ battles (950), community size (188 onchain + 1k+ ecosystem), then update docs/devcon8.html + pitch surfaces, push.
5. **Aug 1 gate:** Hub proposal must have confirmed co-organizers (AttaBotty, Ike, India lead via Shriyash/Arun). Finalize collateral kit (insurance research, testimonial requests).

**Cadence rules (from LOOP.md):**

- Active build: 30-min wakes (CHECK -> BUILD -> UPDATE).
- Blocked on Zaal replies: 60-min wakes, CHECK-only.
- Build Camp week (Jul 4-11): morning = lesson files + camp support, afternoon = campaign.
- Any CHECK trigger fires: full iteration regardless of cadence.

**Standing blocked-on-Zaal queue (keep these short and explicit):**

1. Send 5 outreach messages (ecosystem email, Shriyash, Coop, Farcaster cast, 2 rail asks).
2. Approve rate card numbers.
3. Ask AttaBotty for photo/video archive (critical blocker for reel, deck, testimonials).
4. Token2049 Singapore vs ADE Amsterdam decision (Jul 15 deadline).
5. Fix bettercallzaal.com (DNS OK, AWS host dead - check 18.204.152.241).
6. Confirm hub co-organizers with AttaBotty + Ike + India lead.

**Pause signals (do NOT build these until Zaal confirms):**

- 2027 circuit research is PAUSED (Zaal: "let's wait and align after Devcon 8 wraps, Nov 2026"). Do not spec Edge India, apply to Sonar+D, research Bitcoin 2027, etc. SXSW Dec 18 2026 deadline is the one exception.
- Crowdfund + Scholars essays are PARKED until Build Camp result + Ecosystem Program outcome are locked (early Aug).

## Key Gotchas

**1. The campaign rule (repeat it in every plan):**
The ZAO organizes ONLY ZAOstock (Oct 3 2026, Ellsworth Maine). Every other event on the circuit (Devcon, Marfa, 2027 events) is a PARTNERSHIP: we bring a music stage / live battle / showcase to THEIR event. Never say we "run" Devcon or any other partner event.

**2. Devcon group rules (no workaround):**
- No group/team discount tier. Each discounted seat is an individual application.
- Max 2 tickets per order.
- Discounted tickets are non-transferable; each artist must apply and claim themselves.
- Implication: Zaal cannot buy cheap seats for the crew. He CAN buy GA seats 2-per-order at $699 each.

**3. Ecosystem Program unlock (found Jul 3, unlocked path):**
Devcon 8 Ecosystem Program R2 (opens July) offers up to 5 free/discounted tickets + $500 grant for hosting a community event tied to Devcon. A ZAO music x onchain event qualifies. This can cover the artist crew's tickets - apply ASAP when R2 opens.

**4. Diwali surge (Nov 6-10):**
Mumbai lodging surges 40-60% that week. Book by early Sept or per-person cost rises from ~$200 toward $300+.

**5. Indian artist lever (lowest-cost crew):**
An India-based WaveWarZ/ZAO artist attends for ~$149 (resident ticket) + domestic travel vs $1,200-1,800 per US artist. Recruiting Indian artists before Nov multiplies presence at ~20% of cost. This is a force multiplier; prioritize India scouting.

**6. Photo archive = critical blocker:**
The reel, deck, testimonials, and collateral all hinge on a photo/video archive from ZAO-PALOOZA + ZAO-CHELLA. AttaBotty holds this; requesting it is a top-priority Zaal action.

**7. GitHub Pages workflow:**
- Edit markdown + HTML in place.
- Commit and push to main.
- Pages redeploys automatically (may take 30-60 seconds).
- Live at https://bettercallzaal.github.io/zaotravelz/.

**8. No build step, no dependencies, no .env:**
Everything is static. No npm install, no secrets to rotate, no database. Read and edit.

## Secrets & Security

**No secrets in this repo.** All config lives in HANDOFF.md, LOOP.md, and partners-tracker.md as plain text. Outreach messages contain real email addresses and Telegram handles of ZAO team members (Zaal, AttaBotty, Iman, etc.) - these are public.

Verify before committing:
- No API keys, private wallet addresses, or credentials.
- No real email addresses of third-party individuals (Arun, Shriyash, etc.) - use first-name-only or redact as needed.
- No passwords or account tokens.

Use `git diff` before push to double-check.

## Related Repos

- **ZAOOS** (bettercallzaal/ZAOOS) - the monorepo lab + 800+ research docs. Research backref for this campaign (docs 945-947 on logistics, Mumbai, circuit landscape).
- **ZAOartizen** (ZADEVZ/ZAOartizen) - separate fundraising loop. ZAO Festivals is live on Artizen Season 6 as the funding rail.

## Questions?

- **Quick clarification:** Read CONTEXT.md, HANDOFF.md, partners-tracker.md (in that order).
- **Deep context:** Grep ZAOOS research/events/ for numbered topics or ask Zaal.
- **Do not invent facts to fill gaps.** If something is unclear, ask Zaal or check ZAOOS research.

---

**Last updated:** 2026-07-13. Session note: repo is active, awaiting CHECK triggers + photo archive + Zaal outreach sends to unlock next phase. Build loop cadence = 30-60 min wakes per LOOP.md.
