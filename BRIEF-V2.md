# Shield Rex Demo — V2 Brief (90 seconds)
_Nick + Kit, 2026-03-25_

## Concept
90-second animated demo. Split-screen layout: LEFT = polished Rex UI that Andy sees. RIGHT = narrow terminal log panel showing the engine running in real time. Left side tells the story. Right side proves it's real.

---

## Voiceover Script (90 seconds — measured military cadence, deep male voice)

[SCREEN 1 — Problem, 0–10s]
*"Every morning. Same problem."*
*"Contracts awarded. Leadership changes. New contacts. And your competitors already called."*

[SCREEN 2 — Rex Opens with log panel, 10–22s]
*"Rex sees it first."*
*"Every contract. Every command change. Every new name — already read, sorted, and matched to your pipeline. While you slept."*

[SCREEN 3 — Draft approved, 22–35s]
*"New contact identified. Draft ready. One decision."*
*"Send. CRM updated. Nothing falls through."*

[SCREEN 4 — Competitive alert, 35–46s]
*"Northrop just won a F-35 sustainment modification. $180 million. Rex flagged it. Your draft is queued."*
*"Your competitors will find out by Friday. You already know."*

[SCREEN 5 — Meeting prep, 46–60s]
*"Two hours before your call. Rex pulls everything — what she cares about, what Southwest flies, and the angle most likely to land."*
*"You walk in ready."*

[SCREEN 6 — Weekly summary, 60–72s]
*"End of week. Pipeline summary drafted. Queued for your review. One approval — it goes to Collins."*
*"You didn't write a single report."*

[SCREEN 7 — Closer, 72–90s]
*"This is the full sales week. Intel. Outreach. Prep. Reporting."*
*"You don't manage the pipeline."*
*[beat]*
*"You just run it."*
*"Rex. Built for the ones who don't miss."*

---

## Layout

### Split Screen
- LEFT (70% width): Polished Rex UI — dark navy `#0a0f1e`, Inter font, blue `#2563eb` accent
- RIGHT (30% width): Terminal log panel — slightly darker background `#060c18`, monospace font, green `#22c55e` text, timestamps, scrolling auto

### Terminal Log Entries (scroll continuously through demo)
```
[06:14] intel.agent: scanning DoD FPDS feed...
[06:14] 34 contract awards parsed
[06:15] match: Lockheed Martin — F-35 Block 4 ($340M)
[06:15] match: Southwest Airlines MRO — leadership change
[06:15] contact.search: Karen Hill, Southwest Airlines
[06:15] confidence: 94% — queueing draft
[06:16] draft.ready → andy.parks@shieldtechnologies.com
[06:16] awaiting approval...
[06:31] approved — sent ✓
[06:31] hubspot.log: Karen Hill → First Contact
[06:31] deal.update: Prospect → Active
[07:02] intel.agent: competitive scan running...
[07:03] Northrop Grumman — F-35 sustainment mod ($180M)
[07:03] territory.flag: overlaps Shield coverage area
[07:03] draft.queued → competitive response
[09:58] meeting.prep: Karen Hill — 11:00 AM
[09:58] pulling: Southwest fleet data, MRO priorities
[09:59] brief.ready → andy.parks@shieldtechnologies.com
[17:45] week.summary: 12 contacts, 4 drafts sent, 2 replies
[17:45] pipeline.report: queueing for Collins review
[17:46] awaiting approval...
```

---

## Screen Sequence (7 screens, 90 seconds total)

### Screen 1 — The Problem (0–10s)
- Full black. White typewriter text: *"Every morning. Same problem."*
- Three items tick in:
  • 34 defense contracts awarded overnight
  • Leadership change: Southwest Airlines MRO
  • Your competitors already called

### Screen 2 — Rex Opens (10–22s)
- LEFT: Rex Daily Brief slides in. Header: "REX // DAILY BRIEF — March 25, 2026"
- Three intel cards animate in (staggered 0.3s):
  - 🛡️ DoD Contract Award | Lockheed F-35 Block 4 | $340M | MATCH: Envelop Covers
  - 🔄 Leadership Change | Southwest Airlines MRO | Karen Hill → Director of Procurement  
  - ✦ New Contact | Karen Hill | Priority: HIGH
- RIGHT: Terminal panel fades in, log starts scrolling from top

### Screen 3 — Draft + Approve (22–35s)
- LEFT: Email draft slides up. From: andy.parks@shieldtechnologies.com / To: karen.hill@southwest.com
- APPROVE button glows → clicked
- Three confirmations fire: ✅ Email sent / ✅ HubSpot logged / ✅ Deal stage updated
- RIGHT: Log entries scroll: `approved — sent ✓` / `hubspot.log: Karen Hill → First Contact`

### Screen 4 — Competitive Alert (35–46s)
- LEFT: Alert card slides in with orange left border:
  ⚡ COMPETITIVE ALERT
  Northrop Grumman — F-35 sustainment modification — $180M
  Territory: overlaps Shield coverage | Draft ready
  [APPROVE] [HOLD]
- RIGHT: `intel.agent: competitive scan running...` / `territory.flag: overlaps Shield coverage area`

### Screen 5 — Meeting Prep (46–60s)
- LEFT: Meeting brief card:
  📅 MEETING IN 2 HOURS
  Karen Hill — Director of Procurement, Southwest Airlines
  What she cares about: [3 bullet points]
  Southwest fleet: Boeing 737 MAX fleet — active MRO contracts
  Best angle: Envelop Covers — weight savings on high-cycle aircraft
- RIGHT: `meeting.prep: Karen Hill — 11:00 AM` / `pulling: Southwest fleet data, MRO priorities`

### Screen 6 — Weekly Summary (60–72s)
- LEFT: Weekly summary card:
  📊 WEEK IN REVIEW — March 21–25
  12 contacts touched | 4 outreach emails sent | 2 replies received
  Pipeline summary drafted → queued for Collins review
  [APPROVE TO SEND] button
- RIGHT: `week.summary: 12 contacts, 4 drafts sent, 2 replies` / `pipeline.report: queueing for Collins review`

### Screen 7 — Closer (72–90s)
- Both panels fade
- Center: REX (large, 700 weight, wide letter-spacing)
- Tagline fades in: *"Built for the ones who don't miss."*
- Footer: *"Powered by AxiomStream Group"*
- Replay button appears at 88s

---

## Technical Specs

- Single HTML file: `shield-demo-v2.html`
- No external dependencies except Google Fonts (Inter + JetBrains Mono for terminal)
- Terminal panel: auto-scrolls continuously, entries fade in one by one
- All transitions: cubic-bezier easing, confident and precise
- Target viewport: 1280×720 (screen record) + mobile responsive (min() for widths)
- Viewport meta tag required
- Replay button resets and replays from Screen 1

---

## Replit Agent 4 Brief (copy-paste ready)

```
Build shield-demo-v2.html — an animated 90-second product demo for a defense sales AI called Rex.

LAYOUT: Split screen throughout (except Screen 1 which is full-screen). LEFT 70%: polished Rex UI. RIGHT 30%: terminal log panel showing the engine running.

LEFT PANEL design:
- Background: #0a0f1e (deep navy)
- Font: Inter (Google Fonts)
- Accent: #2563eb (blue)
- Success: #22c55e (green)
- Alert: #f97316 (orange, for competitive alert)
- Text: white / #e2e8f0
- Style: clean, dark, enterprise. NOT sci-fi.

RIGHT PANEL design:
- Background: #060c18 (slightly darker)
- Font: JetBrains Mono (Google Fonts), 11px
- Text: #22c55e (green)
- Timestamps in grey #6b7280
- Entries scroll upward automatically, new entries fade in at bottom
- Thin left border: 1px solid #1a2a1a

SCREEN SEQUENCE (auto-plays, ~90 seconds total):

SCREEN 1 (0–10s, full screen): Black bg. "Every morning. Same problem." types in. Three items tick in.

SCREEN 2 (10–22s): Split layout appears. Left: Rex Daily Brief header + 3 intel cards animate in (staggered). Right: terminal panel fades in, log entries start scrolling.

SCREEN 3 (22–35s): Left: email draft slides up (From: andy.parks@shieldtechnologies.com, To: karen.hill@southwest.com). APPROVE button glows/pulses → clicked → 3 confirmations fire. Right: log shows approval + HubSpot update.

SCREEN 4 (35–46s): Left: competitive alert card with orange left border — Northrop Grumman F-35 sustainment mod $180M, territory flag, APPROVE/HOLD buttons. Right: log shows competitive scan + territory flag.

SCREEN 5 (46–60s): Left: meeting prep card — Karen Hill in 2 hours, Southwest fleet data, best pitch angle. Right: log shows meeting prep pulling.

SCREEN 6 (60–72s): Left: weekly summary card — 12 contacts, 4 emails, 2 replies, pipeline report queued for Collins, APPROVE TO SEND button. Right: log shows week summary compiling.

SCREEN 7 (72–90s): Both panels fade. Center: REX (large, Inter 700, letter-spacing 0.3em). Tagline: "Built for the ones who don't miss." Footer: "Powered by AxiomStream Group". Replay button appears at 88s.

TECHNICAL:
- Single self-contained HTML file
- Google Fonts: Inter + JetBrains Mono
- Viewport meta tag: width=device-width, initial-scale=1.0
- Mobile responsive: use min(Xpx, 95vw) for fixed-width containers
- All fixed px widths on body/containers must use min() or % for mobile
- Replay resets all state and restarts from Screen 1
- Screen-record ready at 1280×720
```
