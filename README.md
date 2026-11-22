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
