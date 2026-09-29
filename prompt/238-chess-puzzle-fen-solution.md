# 238. Chess Puzzle: FEN Solution

```text
Solve this chess puzzle for the side to move shown by the FEN (w = White,
b = Black).

FEN: {fen}

Find a strong legal move for that side. Reply with a single move in standard
algebraic notation (SAN), with no commentary. Do not assume the puzzle is
always for White. If a legal-move list is supplied by the test harness, select
from it; the harness must validate the solution independently.
```

**Source model:** Adapted from the FEN-based puzzle example in [kagisearch/llm-chess-puzzles](https://github.com/kagisearch/llm-chess-puzzles). Its published example has `b` (Black to move) in the FEN but asks for White's best move; this version uses the FEN turn to avoid that contradiction.
