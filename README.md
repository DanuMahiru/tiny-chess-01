# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/DanuMahiru/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/DanuMahiru/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

An original 4 KB Python chess engine for the make.fun tiny-chess-01 bounty.

## What it is

`main.py` (4,075 bytes, MIT) is the whole engine: a 0x88 board, negamax
alpha-beta with quiescence, a transposition table, killer moves, MVV-LVA
ordering, null-move pruning (never at ply 1), late-move reductions, check
extensions, and PVS at the root. Evaluation is material + formula
piece-square tables (tapered king), bishop pair, pawn shield, and a tempo
bonus. It searches to a fixed budget of 100,000 nodes per move — never to
a clock — so it is fully deterministic for a given position.

Practice trials vs the house gauntlet: mean Elo 1422 (trials 1364, 1451,
1451), above the 1154 floor, about 2.9 s per move, no move over 10 s.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

## Licence

MIT, see `LICENSE`. Written from general chess-programming knowledge; no
code was copied from any other engine.

<sub>Entered on [make.fun](https://make.fun/?ref=qs7ay7nf&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
