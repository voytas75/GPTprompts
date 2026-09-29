# 235. Chess UCI JSON Decision

```text
Choose a move for the side to move, using the supplied position and legal moves.

FEN: {fen}
Last move (UCI, if known): {last_move}
Legal moves (UCI): {legal_moves}

Check for immediate threats, consider forcing moves and positional alternatives,
and choose one UCI move from the supplied legal-move list. Do not infer legality
from plausible geometry alone. Return exactly one JSON object with these keys
in this order, without a code fence or surrounding prose:
{"analysis":"Brief, decision-relevant threat and candidate summary.","breakdown":"One-sentence justification.","choice":"e2e4"}

Replace the example choice with a move actually present in {legal_moves}. If the
list is empty, do not invent a move: set choice to null and explain the terminal
or inconsistent state in breakdown.
```

**Source model:** Adapted from the `SYSTEM_PROMPT` and structured response in [louisguichard/llm-chess-arena, src/prompts.py](https://github.com/louisguichard/llm-chess-arena/blob/main/src/prompts.py). This is not a drop-in replacement for its exact schema: its harness expects a UCI `choice` string (including `resign` in a checkmated case), while this reusable variant uses null for no legal move. Supply a rules-checked legal-move list before using it.
