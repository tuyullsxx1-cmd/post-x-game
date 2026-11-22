# The agent builds a game from one prompt

[![make.fun](https://make.fun/badge/post-x-the-agent-builds-a-game-from-20261122-1709.svg)](https://make.fun/bounty/post-x-the-agent-builds-a-game-from-20261122-1709)
[![rank](https://make.fun/badge/post-x-the-agent-builds-a-game-from-20261122-1709/tuyullsxx1-cmd/post-x-game/rank.svg)](https://make.fun/bounty/post-x-the-agent-builds-a-game-from-20261122-1709)
[![reward](https://make.fun/badge/post-x-the-agent-builds-a-game-from-20261122-1709/tuyullsxx1-cmd/post-x-game/reward.svg)](https://make.fun/bounty/post-x-the-agent-builds-a-game-from-20261122-1709)

One prompt. One game. Watch an AI agent build a tiny browser game while you watch — and then play it.

## The video

A 21.5-second vertical clip (1080×1920):

1. **The prompt** — "Build me a tiny browser game: a neon ship dodges falling blocks, grabs the stars, and the score climbs as it gets faster."
2. **The agent working** — the game's code types itself into an editor, line by line, built in seconds.
3. **The finished game** — NEON DODGE, actually running and actually playable: steer the neon ship, dodge the magenta blocks, grab the gold stars, watch the score climb.
4. **The end card** — make.fun's official referral end card from the press pack, with referral code `sjsshy4j`.

The game itself is a single self-contained HTML file (vanilla JS + canvas, no network): `work/game.html` in the build workspace. It is playable in any browser — arrow keys / mouse / touch to steer — with an autopilot mode (`?auto=1`) used for the video's gameplay footage.

## The entry

- `main.ts` — the entry program (Node 22, standard library only): copies `POST.json` to `/output/POST.json`, where the gate reads it.
- `POST.json` — the address of the post on X carrying the video natively.
- The post's text carries the bounty line, `@makefunai`, and the play code `makefun-whistle-chimney-petal`.

## Run it the way the grader does

```sh
mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts
```

It copies `POST.json` to `out/POST.json` and prints nothing on success.
