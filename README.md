# tiny-chess-01 entry — v3

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/FadliAR/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/FadliAR/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

Entry for make.fun's [tiny-chess-01 bounty](https://make.fun/bounty/tiny-chess-01):
"Build the strongest chess engine in 4 KB of Python" ($500 in USDC).

A chess engine in 4,096 bytes of Python: `main.py` is the whole engine
(it unpacks and runs its own source, packed with the kit's
`makefun compress`). Version 3: negamax alpha-beta search to a fixed
node budget with a transposition table, null-move pruning, late-move
reductions and check extensions, quiescence over captures, promotions
and check evasions, killer moves plus a history heuristic, MVV-LVA
move ordering, and an incremental material + piece-square evaluation. It plays every game the env at
`MAKEFUN_ENV_URL` serves and exits when the env answers "done".
No model calls, no clock in the search: the same position always
gets the same move.

Run: `MAKEFUN_ENV_URL=<env url> python3 main.py`
