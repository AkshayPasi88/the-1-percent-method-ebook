# Publishing via Zernio — VERIFIED & WORKING

Status: **pipeline tested end-to-end on 10 Nov 2026** (dummy test posts published
to both accounts, then this guide was finalized). The automation posts directly
through the API — no dashboard needed.

Connected accounts:
- Instagram: **@self_efficient_daily** (reels + feed posts) — account id in `.secrets/instagram_account_id`
- Pinterest: **self_efficient** (pins incl. video pins) — account id in `.secrets/pinterest_account_id`

## How posting works (the automated path)

The script `scripts/zernio_post.mjs` does three things:

1. `POST /v1/media/presign` — asks Zernio for an upload URL
2. `PUT` the file to that URL — Zernio hosts it at a public URL
3. `POST /v1/posts` — publishes to both platforms in one call

```bash
# Post a reel (video → Instagram Reel + Pinterest video pin):
node /home/z/my-project/scripts/zernio_post.mjs \
  /home/z/my-project/download/reels/hype_01.mp4 \
  "Caption text + hashtags from captions_instagram.txt" \
  --type video --platforms ig,pin

# Post a slide (image → Instagram feed + Pinterest pin):
node /home/z/my-project/scripts/zernio_post.mjs \
  /home/z/my-project/download/slides/slide_01.png \
  "Caption text #hashtags" \
  --type image --platforms ig,pin

# Schedule instead of posting now:
  --at "2026-11-16T09:30:00+05:30"

# Optional extras:
  --first-comment "Link in bio"     # IG first comment
  --board <boardId>                 # Pinterest board
  --pin-title "Pin title <100 chars"
```

The API key lives in `/home/z/my-project/.secrets/zernio_key` (chmod 600) and is
never printed or committed.

## Verified behavior (from the live test)

- 9:16 MP4 videos publish as **Instagram Reels** automatically (no extra flags).
- The same video becomes a **Pinterest video pin** in the same call.
- 4:5 PNGs publish as **Instagram feed posts** and **Pinterest pins**.
- Instagram takes ~20–30s extra to process (status `processing` → `published`).
- Response includes the live URLs: `instagram.com/reel/...` and `pinterest.com/pin/...`.

## Weekly automation

The scheduled task (Mon 09:00 IST) now posts automatically:
- randomly picks a **reel** or a **slide** as that week's content
- creates it fresh (TTS voice + new theme, or a new quote slide)
- publishes to Instagram + Pinterest via the script above
- archives everything to GitHub

## Manual posting via dashboard (fallback)

1. Log in to zernio.com → composer → select both accounts.
2. Upload the MP4/PNG, paste the caption from `captions_instagram.txt` /
   `captions_pinterest.txt`, schedule at the IST slots in README.md.
3. Use Queue to spread posts automatically.

## Cadence guide (IST)

| Slot | Content |
| --- | --- |
| Mon 09:30 | reel of the week |
| Wed 12:00 | second reel or slide |
| Fri 18:00 | reel or slide |
| Daily 20:00 | Pinterest pin (rotating) |
