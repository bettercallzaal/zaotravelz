# YoZF Build Loop - Playbook

Every wake runs three phases. No iteration ships drafts only - each one must CHECK something live, BUILD something real, and UPDATE the board.

## Phase 1 - CHECK (live signals, every wake)

| Signal | How | Trigger |
|---|---|---|
| Builder Discount opened? | WebFetch tickets.devcon.org | OPEN -> alert Zaal, top of board, this beats everything |
| Ecosystem Program R2 opened? | WebFetch devcon.org/en/ecosystem-program | OPEN -> finalize application from outreach/ecosystem-program-email.md |
| RFP-13 forum activity | WebFetch forum.devcon.org RFP-13 thread | New accepted hubs / template changes -> adjust proposal |
| bettercallzaal.com | curl -I | UP -> unblock links in all pitch materials |
| Outreach replies | ask Zaal in report | reply -> tracker status bump + next step |

## Phase 2 - BUILD (one artifact per wake, priority order)

1. Anything unblocked by a CHECK trigger (applications > all)
2. Deck build (season deck HTML) once photo archive exists
3. ZAOstock <-> circuit tie-ins (run-of-show as case study template, post-event metrics report template)
4. Remaining collateral (insurance research, testimonial request drafts)
5. ETH lessons (folded in: 03 account abstraction, 04 Foundry testing, 05 splits) - lower priority than campaign artifacts, higher during Build Camp week when they feed the buildathon

## Phase 3 - UPDATE

- NO MORE ARTIFACTS (Zaal, 2026-07-03). All pages ship to docs/ in the zaotravelz repo and deploy via GitHub Pages: https://bettercallzaal.github.io/zaotravelz/
- Status board = docs/index.html (single source of truth); sponsor pitch = docs/devcon8.html
- Every iteration: edit docs/, update partners-tracker.md, then git commit + push (Pages redeploys automatically)
- Report to Zaal: what changed, what is blocked on him (keep the blocked list SHORT and explicit)

## Cadence rules

- Active build phase: 30 min wakes
- Blocked on Zaal sends/replies: 60 min wakes, CHECK-only iterations
- Build Camp week (Jul 4-11): bias BUILD toward camp support (lesson files, project scaffolding) in the morning, campaign in the afternoon
- Any CHECK trigger fires: immediate full iteration regardless of cadence

## Standing blocked-on-Zaal queue (as of 2026-07-03)

1. Send 5 outreach messages (ecosystem email, Shriyash, Coop, cast, rail asks x2)
2. Approve rate card numbers
3. AttaBotty: photo/video archive ask (critical path to deck + reel)
4. Token2049 SG vs ADE decision (Jul 15)
5. Fix bettercallzaal.com AWS host (DNS fine, server dead)
6. Confirm hub co-organizers (AttaBotty, Ike)
