[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/chuachua3225-pixel/tiny-chess-20261122/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/chuachua3225-pixel/tiny-chess-20261122/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

# tiny-chess-01 entry

A chess engine in at most 4,096 bytes of Python for make.fun's
[tiny-chess-01](https://make.fun/bounty/tiny-chess-01) bounty.

`main.py` is the whole engine (packed with the kit's `compress` from the
readable source, which is written and tested in the build sessions).
It plays the house gauntlet through the env at MAKEFUN_ENV_URL:
negamax alpha-beta with a transposition table, quiescence search,
null-move pruning and late-move reductions, over a compact mailbox
board with incremental Zobrist hashing, at a fixed node budget so
every replay plays the same moves.
