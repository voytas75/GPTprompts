# 239. Chess FEN: Tagged Move Variants

Set `{opening}` to exactly one of the following alternative instructions before
using the prompt. They are **prompt variants**, not claims of playing strength.

- Basic: Choose a strong legal chess move for the position below.
- Grandmaster persona: As a chess grandmaster, select a strong legal move below.
- Engine persona: As a chess-move selector, check the position and pick a strong
  legal move below. Do not claim an engine search or guaranteed optimality.

```text
{opening}

Position (FEN): {fen}
Play the side to move indicated in the FEN. Return only the move in standard
algebraic notation (SAN), enclosed in <move> and </move>, for example
<move>e4</move>. Do not add any other text.
```

**Source model:** Adapted from the `basic`, `grandmaster` and `stockfish` prompt families shown in [Manifest AI, “Post-Training R1 for Chess”](https://manifestai.com/articles/post-training-r1-for-chess/). The source's grandmaster/engine Elo and “quantum” persona assertions are not evidence of actual skill and are deliberately not repeated here. Validate every proposed move in an external chess environment.
