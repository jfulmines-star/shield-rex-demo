# REX Demo — Production Guide

## What's Done ✅

### Voiceover
- **File:** `voiceover-adam.mp3` (23.6 seconds, ElevenLabs / Adam voice)
- **Voice:** Deep, authoritative male — matches the Shield exec persona
- **Script:** Timed to the 27-second demo sequence

### Visual Demo
- **URL:** https://shield-demo-eight.vercel.app/shield-demo.html
- **Runtime:** 27 seconds, auto-play, 6 screens

---

## One Thing Needed: Background Music 🎵

All the programmatic download routes are blocked (Pixabay, Mixkit, BenSound CDNs all require browser). Need ~30 seconds of cinematic tension underscore.

### Recommended Track Options (grab any one from browser):

**Option A — Pixabay (free, no attribution)**
1. Go to: https://pixabay.com/music/search/cinematic-tension/?order=popular
2. Search for anything labeled "corporate" or "dark tech" or "tension"
3. Download as MP3

**Option B — Mixkit (free, no attribution)**
1. Go to: https://mixkit.co/free-stock-music/tag/cinematic/
2. Filter by mood: "Dark" or "Tense"
3. Download free license

**Target vibe:** Low pulse, minimal — something that builds slowly. Think Hans Zimmer underscore, not trailer music. Should sit *under* the voiceover, not compete.

---

## Final Assembly (once music is downloaded)

### With ffmpeg (fastest):
```bash
cd ~/Projects/shield-demo

# Mix voiceover + music (music at -18dB under VO)
ffmpeg -i voiceover-adam.mp3 -i music/[TRACK].mp3 \
  -filter_complex "[1:a]aloop=loop=-1:size=500000,volume=0.3[bg];[0:a][bg]amix=inputs=2:duration=first" \
  -y demo-audio-final.mp3

# Trim to 27 seconds
ffmpeg -i demo-audio-final.mp3 -t 27 -y demo-audio-27s.mp3
```

### Without ffmpeg (if not installed):
Use Audacity (free) or GarageBand:
1. Import voiceover-adam.mp3 as track 1
2. Import music as track 2, set volume to ~30%
3. Export mixed MP3

---

## Screen Recording (final step)
1. Open Chrome, go to https://shield-demo-eight.vercel.app/shield-demo.html
2. QuickTime → New Screen Recording → select browser window
3. Play demo audio from demo-audio-27s.mp3 simultaneously
4. Record → export → done

OR use OBS for proper audio sync (recommended):
- OBS → Add Source: Browser (URL) + Audio Output Capture
- Set audio mix in OBS before recording
