# 237. Chess Grandmaster: Single SAN Move

```text
You will receive a partially completed chess game in PGN movetext.
Choose the next legal move for the side to move and output only its standard
algebraic notation (SAN), such as e4, Rdf8 or R1a3. Do not include a move
number, commentary or board diagram.

Game so far:
{pgn_movetext}
```

**Source model:** Adapted from the minimal system prompt in [Dynomight, “OK, I can partly explain the LLM chess weirdness now”](https://dynomight.net/more-chess/). The article tests several variants; it does not establish that this one is always strongest. For reliable game state, pair this with a validator or the FEN variant in prompt 234.
