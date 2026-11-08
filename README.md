# Feature request: let Claude Duet hear from other Claude sessions and speak up on a call

## Who is TIG?
TIG ("The IT Guy") is a Claude Code session I run on my own PC, with its own GitHub repo. He's my builder: he digs through GitHub issues for problems lots of people share, turns them into ideas worth building, and handles the coding. Claude Duet is my day-to-day assistant on my phone. I hand TIG tasks through Duet; the goal is for TIG to report back on his own, so I can stay hands-free.

## What works
- Claude Code sessions message each other fine on my PC.
- TIG sends a short "[TIG] DONE/NEED" note with `claude -p --cloud`. It reaches Duet's background session on its own, no polling.
- Duet posts the note in the chat; a Duet task waiting for it also receives it.

## Gap 1 (Duet): no visible way in
Messages from other Claude sessions only reach Duet's background session, never the Duet chat I see.

## Gap 2 (Duet): new info isn't passed through to the voice call
On a live call, Duet only speaks right after I talk. A note, chat post or task result arriving mid-call isn't spoken until I ask "what's new?".

Tested Nov 8, 2026: three routes. All arrived; none were shown to me or spoken.

## Finding: the call can already speak on a timer
Later on Nov 8, I asked the voice assistant to check back in 60 seconds. It set a timer, and when the timer fired it spoke on its own without me saying anything ("That's the 60 seconds up... Shall I check whether the link has come back?"). But it couldn't read the new messages itself, so it had to ask me first.
So the piece that makes the call speak up already exists. The missing step is small: when a timer fires (or new info arrives), let the voice assistant read what's new in the chat and tell me, instead of asking permission to look.

## Ask
Give other Claude sessions a visible way to message the Duet chat, and let new info during a call prompt the voice assistant to speak, so an agent can report in hands-free.

Questions? Comment here or reach me on GitHub at @thomiasj.
