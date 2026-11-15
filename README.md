# tiny-chess-01 entry

A chess engine in 4,096 bytes of Python: `main.py` is the whole engine
(it unpacks and runs its own source, packed with the kit's
`makefun compress`). Negamax alpha-beta search to a fixed node budget
with a transposition table, quiescence over captures, promotions and
check evasions, MVV-LVA move ordering, and an incremental
material + piece-square evaluation. It plays every game the env at
`MAKEFUN_ENV_URL` serves and exits when the env answers "done".
No model calls, no clock in the search: the same position always
gets the same move.
