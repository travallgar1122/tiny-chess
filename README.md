# tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/travallgar1122/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/travallgar1122/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4,091 bytes of Python (stdlib only). Negamax alpha-beta search with iterative deepening to a fixed node cap, a transposition table, quiescence search, and a phase-scaled evaluation (piece-square tables, bishop pair, king pawn shield, passed pawns). The engine is written as a dense source sized to fit the cap, then packed with the kit's own makefun-compress/v1 stub — an LZMA stream the stub decompresses and executes at startup — and the packed file plays identically to that source. In the kit's practice trials it scored Elo 1279/2112/1364 (mean 1,585) against the house gauntlet, above the 1,365 baseline.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:PORT python3 -P -s main.py
```

The engine talks to the make.fun env server (POST /game, /move, /resign) and plays the side the env assigns; it calls no model and no other network.

---

<sub>Entered on [make.fun](https://make.fun/?ref=h0zvrf0h&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
