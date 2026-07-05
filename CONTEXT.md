# CONTEXT - portable brain for the Year of the ZAO Festivals campaign

This file exists so a fresh Claude on any machine (a new PC with none of the local memory, skills, or
config) can pick up the work with full context. It is committed to the repo, so `git clone` carries it.
Read this first, then HANDOFF.md, LOOP.md, partners-tracker.md, intake-artizen-festivals.md.

Last synced from the Mac's Claude memory + global rules on 2026-07-05.

## Style rules (non-negotiable, these are global and NOT otherwise in this repo)

- NO emojis anywhere. Not in chat, code, commits, docs, pages, or posts. Use text labels instead
  (`[LIVE]`, `DONE`, `OVERDUE`).
- NO em dashes. Use hyphens.
- NO spaced-hyphen dash connector (" - " as a sentence dash). Use commas, periods, parentheses, or
  rephrase. Compound-word hyphens (open-source, community-owned) and bullet markers are fine.
- Outbound messages: short, ONE ask, max about 7 lines. Do not wall people.

## Brand glossary (exact spellings, never autocorrect)

| Correct | Never |
|---|---|
| WaveWarZ | Wave Wars, Wavewarz |
| The ZAO | the Zao, ZAO alone (when standalone use "The ZAO") |
| BetterCallZaal | Better Call Zaal, bettercallzaal as a name |
| ZAO-PALOOZA / ZAO-CHELLA | run-together or spaced forms; both hyphenated all-caps |
| COC Concertz | COC Concerts, z not s |
| Thy Revolution | The Revolution (it is "Thy") |
| ZOE | Zoe (all caps, the ZAO orchestrator agent) |
| ZABAL Games | Zabal games |
| ZAOstock | Zao Stock (one word) |

## Canonical proof numbers (reconciled 2026-07-03, do not drift)

- WaveWarZ: 950 live battles, 459+ SOL traded (about $60k), payouts straight to artists (1% of volume).
- The ZAO: 188 members onchain (Base) + 1,000+ ecosystem participants; 250+ artists in 3 years; 90+
  consecutive weeks of Respect-game governance; 80+ open-source repos; 400+ newsletters.
- Zaal: FarHack 2026 Snap category winner; earlier led a $1.5M robotics project (7x throughput).
- Use "188 members onchain + 1,000+ ecosystem participants" as the verifiable community line. "250+
  artists" is a broader network claim.

## ZAO Festivals: the event history (proof this is real)

- ZAO-PALOOZA: NYC, NFT NYC 2024, 12 artists, broke even, first ZAO IRL meetup.
- ZAO-CHELLA: Wynwood Miami, Dec 6 2024, during Art Basel. 10 Web3 musicians, AR art, trading cards,
  WaveWarZ LIVE rematch. Organized by AttaBotty + DaNici. Gold sponsor: Student $LOANZ Token. IG reel
  DDa-oPBJ7G7 (engagement is login-walled, screenshot from Zaal's account before quoting).
- ZAO-PROS: ETH Denver 2025, conference activation.
- COC Concertz: ongoing metaverse concerts (Stilo World / Spatial.io, Twitch). 50/50 JV, Thy Revolution
  leads, COC owns it, The ZAO does not own it.
- ZAOstock: the flagship IRL festival, Oct 3 2026, Ellsworth Maine (gateway to Acadia, Art of Ellsworth
  weekend). Steve Peer (430 house concerts since 1989) co-curates.

## The campaign rule (repeat it in every plan)

The ZAO organizes ONLY ZAOstock. Every other event on the circuit is a PARTNERSHIP: we bring
entertainment (a music stage, a live WaveWarZ battle, a showcase) to their event. We never say we run it.

## Event-circuit people (the "events I can go to" network)

India leg (DevCon India Nov 2026 is the anchor):
- Arun Phillips: longtime friend, founder of DreamStarter (Hyderabad; DAO tooling + agentic marketing
  automation, a music-video auto-clipper). WaveWarZ India lead. Attending DevCon India; may be NYC Aug
  2026. First call for anything India + AI creator tooling.
- Kshitij Garg + Rishabh: Delhi founders of DDAN, a pop-up community-stay business for Web3 conferences
  (did ETHGlobal Delhi, India Blockchain Week, Solana Breakpoint). For DevCon India they have 3 houses
  (dev house, rooftop founders house with podcast studio, newcomer house) 15-20 min from the venue.
  Open to a "music house" for ZAO + traveling artists, and ZAO community discount coupons.
- Shriyash Soni: founder of Apna Coding (India + UK, 50k+ developer database, stake-to-list board).
  DevCon volunteer. The door to an Indian-musician side-event slot. Telegram only, not Discord/email.
- Zaal is ON the team helping run the DevCon India MUSIC STAGE (with EF organizers). Wants to crowdfund
  to bring Thy Revolution (UK) + Iman (Zambia) so the three go together. Scholarships are time-sensitive,
  apply as soon as they open. Contacts Candy/Candyloo + Carlota (Telegram).

US / crypto / culture:
- Telamon Ardavanis: runs Edge City / Edge Esmeralda (pop-up village, Healdsburg CA) and Goa gatherings.
  Direct-invite relationship. The door to Edge City IRL houses. Also curates two Artizen funds.
- Aaron Rafferty: founder of Wide (Wyoming DEX), cause-coins (trading fees fund nonprofits) + a debit
  card. Live Wide x WaveWarZ x ZAO partnership thread (benefit battles as a cause-coin expression).
- Bayo: founder of MPC (creator tools + supply-chain auth). JV with Tim Parker (Spacium, AR/XR). Has a
  musician brother (ZAOstock / WaveWarZ candidate). The Atrium content-studio intro is a revenue thread.
- Tom Fellenz: veteran event producer (20+ events), ZAOstock advisor. Runs Fellenz Tourz North America.

Full detail on all of these lives in the ZAOOS research library (research/events/ docs) and the Mac's
Claude memory. This is the working summary.

## How the work ships (workflow rules)

- This repo is zaotravelz (GitHub: bettercallzaal/zaotravelz). Push to main = GitHub Pages redeploys
  at https://bettercallzaal.github.io/zaotravelz/.
- NO artifacts. Build real pages into docs/. Status board = docs/index.html, sponsor pitch =
  docs/devcon8.html. Every iteration: edit docs/, update partners-tracker.md, commit, push.
- The loop pattern (LOOP.md): CHECK live signals, BUILD one real thing, UPDATE the board.

## Where everything lives (the ZAO repo map)

- zaotravelz (THIS repo): the Year of the ZAO Festivals event-circuit campaign.
- ZAOartizen (GitHub: ZADEVZ/ZAOartizen): the Artizen fundraising work. Three plans (PLAN-1 meet
  projects, PLAN-2 the two live projects, PLAN-3 the ZAO Fund), fund targets, the BCZ deck. The Artizen
  watch-loop is paused; resume by cloning that repo and re-running its LOOP.md. ZAO Festivals is live on
  Artizen Season 6 as the funding rail for this circuit.
- ZAOOS (GitHub: bettercallzaal/ZAOOS): the monorepo lab + the full research library (research/ has
  800+ numbered docs, the permanent institutional memory).

## If you need the deeper memory

The Mac holds ~80 project/feedback memory files and the full research library. The events-relevant
subset is summarized above. If a decision needs detail not here, ask Zaal, or (if the ZAOOS repo is
cloned) grep research/events/ and research/business/ for the topic. Do not invent facts to fill a gap.
