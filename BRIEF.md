# Shield Rex Agentic Team — Animated Demo

Build a single self-contained HTML file: `shield-demo.html`

## Design Standard
- Background: #0a0f1e (deep navy)
- Font: Inter (Google Fonts)
- Accent: #2563eb (blue)
- Success: #22c55e (green)
- Text: white / #e2e8f0
- Style: Clean, dark, enterprise — NOT sci-fi, NOT gradient-heavy. Confident and precise.

## Sequence (auto-plays, ~24 seconds total)

### Screen 1 — The Problem (0–4s)
Full screen. Black bg. White text types in letter by letter:
"Every morning. Same problem."
Then three intel items tick in one by one with a small bullet and slight delay:
• 34 defense contracts awarded overnight
• 2 new procurement officers at Lockheed Martin
• Leadership change: Southwest Airlines MRO Division

### Screen 2 — Rex Opens (4–9s)
Smooth slide transition. Rex interface appears. Header bar: "REX // DAILY BRIEF — March 25, 2026"
Three intel cards animate in from right with 0.3s stagger:
Card 1 (blue left border): 🛡️ DoD Contract Award | Lockheed F-35 Block 4 Upgrade | $340M | MATCH: Envelop Covers
Card 2 (blue left border): 🔄 Leadership Change | Southwest Airlines MRO | Karen Hill → Director of Procurement
Card 3 (green left border): ✦ New Contact Identified | Karen Hill | Southwest Airlines | Priority: HIGH

### Screen 3 — Draft Email (9–15s)
Email draft slides up from bottom. Clean email UI:
From: andy@shieldtechnologies.com
To: karen.hill@southwest.com
Subject: Envelop Cover Solutions — Southwest MRO Fleet
Body: 3 lines of realistic cold outreach copy specific to Southwest's Boeing fleet and Lockheed supply chain
Two buttons below: [APPROVE] (blue, full) and [HOLD] (grey, outline)

### Screen 4 — One Click (15–19s)
APPROVE button glows and pulses. Then three confirmation rows fire with slight stagger + green checkmarks:
✅ Email sent → karen.hill@southwest.com
✅ HubSpot: Contact logged — Karen Hill, Southwest Airlines
✅ Deal stage: Prospect → First Contact

### Screen 5 — Follow-up (19–23s)
Clean time-skip: "Day 5" fades in top-right corner.
Notification card slides in: 
"⚡ Karen Hill — No reply detected. Follow-up draft ready."
Same APPROVE / HOLD buttons.

### Screen 6 — Closer (23–27s)
Everything fades. Center-aligned:
REX (large, weight 700, letter-spacing 0.3em)
"Built for the ones who don't miss."
Small footer: "Powered by AxiomStream Group"
Replay button appears after 1s.

## Technical Notes
- All transitions: cubic-bezier easing, smooth and intentional
- Typewriter effect on Screen 1
- No external dependencies except Google Fonts (Inter)
- Replay button resets and replays from Screen 1
- Must look great at 1280×720 (screen record target)
- Single file — no external JS or CSS files

Save as: shield-demo.html
