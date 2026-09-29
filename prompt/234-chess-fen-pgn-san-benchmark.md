# 234. Chess FEN + PGN Move Selection (SAN)

```text
Play the side to move in this chess position.

Current position (FEN): {fen}
Move history (PGN movetext): {pgn_movetext}
Assigned color: {color}

Use the FEN as the authoritative position and check that the history and color
agree with it. Consider the strongest legal move; your choice must not leave
your king in check. If the inputs conflict, report the inconsistency instead
of guessing a move. Otherwise give your final move in standard algebraic
notation (SAN) on one line: Final Answer: <SAN move>
```

**Source model:** Adapted from [Game Arena, Appendix B.1 Chess](https://arxiv.org/html/2609.31473) (FEN + PGN context, color, legal SAN move and `Final Answer` delimiter). This version uses a concise final response instead of demanding a printed reasoning trace; a chess engine or rules library must validate legality externally.
