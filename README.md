# The 1% Method — Ebook, Reels & Slides

**Free lead-magnet content pack** in the self-improvement niche (tiny habits /
compound growth). Produced by [the-1-percent-press](https://github.com/Padlock-Games/the-1-percent-press) engine · 10 Nov 2026.

## Contents

```
├── ebook/
│   ├── The_1_Percent_Method_Ebook_4x5.pptx   ← editable master (18 pages, 8×10 in, 4:5)
│   └── The_1_Percent_Method_Ebook.pdf        ← distribution copy
├── reels/                                    ← 9:16 · 1080×1920 · 30fps · H.264 + AAC
│   ├── hype_01..14.mp4                       ← voiced reels (male TTS, karaoke captions)
│   └── classic/                              ← 3 silent text-design reels (batch v1)
├── slides/                                   ← 4:5 · 1080×1350 PNG quote cards (photo posts)
├── marketing_kit/
│   ├── captions_instagram.txt                ← captions for all 14 reels + 6 slides
│   ├── captions_pinterest.txt                ← video pin + idea pin copy
│   ├── hashtags.txt                          ← tiered hashtag sets
│   ├── README.md                             ← batch overview + posting schedule (IST)
│   └── zernio_posting_guide.md               ← verified Zernio API posting guide
└── sources/                                  ← rebuild inputs (slide HTML, TTS scripts, audio, timings)
```

## The reels

Fourteen reels in twelve distinct color themes, each with an emotional male
voice-over (Fish Audio `s2.1-pro-free`, reference voice "Adrian"), word-synced
karaoke captions, a scroll-stopping hook, and an ebook CTA card at the end.

**Dynamic Centre Visual Engine** (drives every reel):
- **Centre stage never empty** — every narration beat gets contextual visuals:
  real photos (auto-discovered via image search, watermark-scanned, cached,
  attributed in `sources/CREDITS.md`), kinetic main text with word-by-word
  reveal + expressive scale on key words, and animated stat counters (×37.78,
  1%, 300 votes).
- **Background morphs with the narration** — each scene carries a subject
  palette (workout → crimson, reading → gold, math → lime…); tints crossfade
  over 0.7 s with an ambient glow that follows the beat.
- **Beat-synchronized effects** — audio onset detection + spoken-word starts
  produce beat markers; image cards kick, text words pulse, glow breathes on
  every hit.
- **Motion-graphics grammar** (from `karanmrn/karanagentskills`,
  `dxny-aep/remotion-skills`, `0xzgbot/hermes-media-skill-pack`
  `motion_graphics_kinetic_type`, and the catalog at
  `clonn/awesome-agent-video-skills`): Lissajous ambient drift (kills the
  slideshow feel), parallax depth layers (bg 0.85 / content 1.14),
  ScalePunch/BlurDissolve/TrackingReveal entrances, OUT_EXPO/CUBIC broadcast
  easing, crossfaded scene switches (no empty frames at cuts).
- **30s long-form reels (11–12)** rotate ~6 scenes each: photo card → giant
  kinetic text → counter, roughly one visual change every 4–5 s.
- **Viral cinematic reels (13–14)** — the full short-form engine: word-SLAM
  hooks over rapid hard-cut footage, one 1–3 s scene per narration sentence
  (energy-driven cuts: shout/angry = hard cut + punch zoom, calm/sad = slow
  push + crossfade), EMOTIONAL voice performance (per-sentence TTS with
  real atempo speed + loudness + pause variation — shout/fast/angry/sad/
  whisper/dramatic), synthesized sound design (sub-bass impacts, whooshes on
  every scene switch, riser into the CTA, ducked heartbeat music bed), word-
  level kinetic captions with keyword accents, beat-synced punch-zooms, and
  an ending that points at the ebook (card + tapping arrow + LINK IN BIO).
  QC: automated black-frame/silence scans + vision QA on every render.

| # | Hook | Theme |
| --- | --- | --- |
| 01 | 1% EVERY DAY = ×37.78 | gold · rising bars |
| 02 | MOTIVATION IS WEATHER. | cream mono · chain links |
| 03 | THE 2-MINUTE RULE | lime · speed streaks |
| 04 | NEVER MISS TWICE. | crimson · lightning bolt |
| 05 | EVERY ACTION IS A VOTE. | ocean · flowing waves |
| 06 | WILLPOWER IS OVERRATED. | steel · drawing checkmarks |
| 07 | DON'T BREAK THE CHAIN. | forest · concentric rings |
| 08 | INVISIBLE TODAY. UNDENIABLE IN A DECADE. | coral · ticking clock |
| 09 | STOP WAITING FOR MONDAY. | violet · pulse dot grid |
| 10 | YOU DON'T NEED MORE MOTIVATION. | sunset · rising arc |
| 11 | DAY 20. STILL NOTHING. | gold · rising bars · **30s long-form** |
| 12 | YOU BECOME WHAT YOU REPEAT. | ocean · flowing waves · **30s long-form** |
| 13 | NOBODY IS COMING TO SAVE YOU. | onyx cinematic · full-bleed footage |
| 14 | PAIN OF DISCIPLINE, OR PAIN OF REGRET. | iron cinematic · full-bleed footage |

## The slides

Six single-image motivational quote cards (4:5, 1080×1350) for Instagram feed
and Pinterest photo posts — dopamine-hitting, hard-work content that points to
the ebook.

## Publishing

All assets are ready-to-post through the **Zernio API** (Instagram
@self_efficient_daily + Pinterest self_efficient). See
`marketing_kit/zernio_posting_guide.md` — the pipeline is verified end-to-end:

```bash
node /home/z/my-project/scripts/zernio_post.mjs reels/hype_01.mp4 "<caption>" --type video --platforms ig,pin
node /home/z/my-project/scripts/zernio_post.mjs slides/slide_01.png "<caption>" --type image --platforms ig,pin
```

## License / brand

Placeholder brand "@self_efficient_daily" — swap in your handle before posting
if different. Content generated for the Padlock-Games content engine.
