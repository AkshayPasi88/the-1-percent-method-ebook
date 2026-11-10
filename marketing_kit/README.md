# Batch 01 v2 — The 1% Method · Voiced Reels + Slides

Produced: 10 Nov 2026 · Brand: @self_efficient_daily · Niche: Tiny Habits / Self-Improvement

## What's in this batch

| Asset | Files | Spec |
| --- | --- | --- |
| Voiced hype reels ×10 | `../reels/hype_01..10.mp4` | 1080×1920 · 30fps · H.264 + AAC (male TTS voice, karaoke captions, hooks + ebook CTA, 10 distinct color themes + animated SVG elements) |
| Motivational slides ×6 | `../slides/slide_01..06.png` | 1080×1350 (4:5) single-image quote cards, 6 color themes |
| Classic reels ×3 (v1) | `../reels/classic/*.mp4` | silent text-design reels from batch 01 v1 |
| Ebook | `../The_1_Percent_Method_Ebook_4x5.pptx` + `.pdf` | 18 pages · 8×10 in · 4:5 |
| Instagram captions | `captions_instagram.txt` | 10 reel captions + 6 slide captions |
| Pinterest copy | `captions_pinterest.txt` | video pin + idea pin copy |
| Hashtag sets | `hashtags.txt` | broad / niche / branded tiers |
| Zernio guide | `zernio_posting_guide.md` | VERIFIED API posting (presign → upload → post) |

## The 10 reels

| # | File | Theme | Hook | Length |
| --- | --- | --- | --- | --- |
| 01 | hype_01 | gold / bars | 1% EVERY DAY = ×37.78 | 12.8s |
| 02 | hype_02 | cream mono / chain | MOTIVATION IS WEATHER. | 8.9s |
| 03 | hype_03 | lime / streaks | THE 2-MINUTE RULE | 10.6s |
| 04 | hype_04 | crimson / bolt | NEVER MISS TWICE. | 9.5s |
| 05 | hype_05 | ocean / waves | EVERY ACTION IS A VOTE. | 11.9s |
| 06 | hype_06 | steel / checks | WILLPOWER IS OVERRATED. | 13.1s |
| 07 | hype_07 | forest / rings | DON'T BREAK THE CHAIN. | 11.2s |
| 08 | hype_08 | coral / clock | INVISIBLE TODAY. UNDENIABLE IN A DECADE. | 10.3s |
| 09 | hype_09 | violet / dots | STOP WAITING FOR MONDAY. | 10.9s |
| 10 | hype_10 | sunset / arc | YOU DON'T NEED MORE MOTIVATION. | 9.9s |

Every reel: emotional male voice-over (Fish Audio s2.1-pro-free, voice "Adrian"),
word-synced karaoke captions, hook overlay → value → ebook CTA card, progress bar,
grain + vignette finish. Audio verified against captions via ASR transcription.

## Posting schedule (IST)

| Day | Time | Asset | Platforms |
| --- | --- | --- | --- |
| Mon | 09:30 | hype_01 (launch reel) | IG Reels + Pinterest |
| Tue | 12:00 | slide_03 (the math) | IG feed + Pinterest |
| Wed | 12:00 | hype_03 | IG Reels + Pinterest |
| Thu | 18:00 | slide_02 | IG feed + Pinterest |
| Fri | 18:00 | hype_07 | IG Reels + Pinterest |
| Sat | 11:00 | slide_06 | IG feed + Pinterest |
| Sun | 20:00 | hype_08 | IG Reels + Pinterest |

Remaining reels (02, 04, 05, 06, 09, 10) + slides (01, 04, 05): drip into the
following weeks via the weekly automation.

## Publishing

One command per post (see `zernio_posting_guide.md`):

```bash
node /home/z/my-project/scripts/zernio_post.mjs <file> "<caption>" --type video|image --platforms ig,pin
```

Or let the weekly scheduled task handle it (random reel/slide each week).
