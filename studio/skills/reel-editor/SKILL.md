---
name: reel-editor
description: Turn a raw talking-head recording into a tight 9:16 reel with word-by-word captions, using free tools on your own computer. Use when you share a recorded video and ask to "edit this reel", "cut the pauses" or "add captions".
---

# Reel editor (starter)

Works in Claude Code (or any Claude with a terminal on your computer). Free tools only: ffmpeg and Whisper.

## One-time setup
- Install ffmpeg (Mac: `brew install ffmpeg`; Windows: `winget install ffmpeg`).
- Make a Python virtual environment and install `faster-whisper`.
- Make a folder for each reel and put the raw video in it as `raw.mp4`.

## Steps (write small scripts for each and keep them in the folder)
1. **Transcribe** `raw.mp4` with Whisper, with word timestamps. Save `words.json`.
2. **Find the best take.** If a sentence is said twice, keep the last complete one. Show the user the kept lines before cutting.
3. **Cut the dead air.** Remove pauses longer than 0.4 s, keep about 0.1 s between sentences. Never cut inside a word.
4. **Export vertical:** 1080×1920, 30 fps, h264. Don't colour-grade or brighten the footage.
5. **Captions:** re-transcribe the cut so timings match, then make word-by-word captions, max 3 words on screen, bold, lower third, each word appearing as it is spoken. Burn them in with ffmpeg (ASS subtitles).
6. **Loudness:** normalise to −14 LUFS (`loudnorm`), the level Instagram plays at.
7. **Check:** grab one frame per second into a contact sheet and look at it. Captions must not cover the face; no long pauses left.

Save the result as `final.mp4` next to the raw take. Add music inside Instagram when you post.

## Make it yours
Every time you don't like something, tell Claude and ask it to add the fix to this file as a rule. After a few reels, it edits the way you like.
