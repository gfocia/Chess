#  Chess AI Agents: Minimax vs Alpha-Beta

This repository contains two Java-based chess-playing agents implemented using classic search algorithms: **Minimax** and **Alpha-Beta Pruning**. These agents are designed to run in a custom chess environment using the BU/SEPIA framework.

---

##  Agent Descriptions

###  `MinimaxAgent.java`

Implements the basic **Minimax algorithm**:
- Recursively explores the game tree up to a fixed depth.
- Alternates between MAX and MIN nodes (agent vs opponent).
- Uses a heuristic function to evaluate non-terminal board states.
- Selects the best move assuming optimal play from both players.

###  `AlphaBetaAgent.java`

Extends Minimax with **Alpha-Beta pruning**:
- Adds `alpha` and `beta` thresholds to eliminate unnecessary branches.
- Prunes the search tree to reduce the number of nodes evaluated.
- Incorporates **move ordering** with `CustomMoveOrderer` to improve efficiency.
- Achieves deeper searches within the same time budget.

---

##  Features

- Configurable search depth and time limit
- Executes in a separate thread with timeout enforcement
- Custom heuristic evaluation via `CustomHeuristics`
- Move selection logged via `Streamer`
- Compatible with SEPIA chess simulation framework

---

##  Usage

Compile and run the agents in your BU/SEPIA-compatible environment:

```bash
# Run Alpha-Beta Agent
java AlphaBetaAgent <playerID> <PlayerType> <timeLimitInSeconds> [maxDepth] [filePath]

# Run Minimax Agent
java MinimaxAgent <playerID> <PlayerType> <timeLimitInSeconds> [maxDepth] [filePath]
