# Reel studio starter: 3 Claude skills

Thanks for commenting **studio**! This is a starter version of the setup from the reel: three Claude skills that find the idea, collect the screens and edit the take. You record. Claude does the rest.

## The three skills
1. **reel-idea-scout:** finds what's working in your niche and writes a short, shoot-ready script.
2. **reel-assets:** checks the facts and collects real screenshots and screen recordings into one folder.
3. **reel-editor:** cuts the pauses, keeps your best take and adds word-by-word captions, with free tools on your computer.

## What you need
- Claude with a terminal on your computer: **Claude Code** (desktop app or terminal).
- ffmpeg and Python (the editor skill walks you through it).

## Install the skills (2 minutes)
Copy each folder in `skills/` into `~/.claude/skills/` (for example `~/.claude/skills/reel-editor/SKILL.md`). Restart Claude Code.

## Your first reel
1. "Give me 5 reel ideas for [your niche] and write the best one." → script
2. "Get the assets for this script." → a folder of real screens
3. Record yourself reading it on your phone. Two takes of the first line.
4. "Edit this reel: [path to your video]." → `final.mp4`
5. Tell Claude what you'd change, and ask it to save that as a rule in the skill. Every reel gets better.

Not affiliated with Anthropic. Have fun with it.
