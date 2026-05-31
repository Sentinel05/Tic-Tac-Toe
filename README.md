# Tic-Tac-Toe

A terminal-based Tic-Tac-Toe game where the player competes against an unbeatable CPU opponent. Written in C++.

## Overview

The CPU uses the **Minimax algorithm** to calculate the optimal move at every turn, making it impossible for the CPU to lose. The best outcome a human player can achieve is a **draw**.

## Files

| File | Description |
|---|---|
| `TicTacToe.cpp` | Full game source code |

## How to Compile & Run

```bash
g++ TicTacToe.cpp -o TicTacToe
./TicTacToe
```

On Windows:

```bash
g++ TicTacToe.cpp -o TicTacToe.exe
TicTacToe.exe
```

## How to Play

1. On launch, choose whether you want to go first (`y`) or let the CPU go first (`n`).
2. The board cells are numbered 1–9 as follows:

```
 1 | 2 | 3
-----------
 4 | 5 | 6
-----------
 7 | 8 | 9
```

3. On your turn, enter the number of the cell where you want to place your mark (`X`).
4. The CPU plays `O` and responds with the best possible move.
5. The game ends when someone wins or all 9 cells are filled (draw).
6. After each game, you are prompted to play again or quit.

## Symbols

| Symbol | Player |
|---|---|
| `X` | Human |
| `O` | Computer |
| `*` | Empty cell |

## Algorithm

The CPU uses the **Minimax** algorithm with recursive backtracking to evaluate every possible future game state and choose the move with the highest guaranteed score:

- A CPU win scores **+10**.
- A Human win scores **-10**.
- A draw scores **0**.

The CPU always maximises its score; the human always minimises it. Because all game states are explored, the CPU never makes a suboptimal move.

## Key Functions

| Function | Purpose |
|---|---|
| `initialise()` | Sets up an empty board filled with `*` |
| `showBoard()` | Prints the current board state |
| `showInstructions()` | Displays the cell-numbering guide |
| `gameOver()` | Checks rows, columns, and diagonals for a win |
| `minimax()` | Recursively scores all possible moves |
| `bestMove()` | Finds the optimal cell for the CPU to play |
| `playTicTacToe()` | Main game loop |
| `declareWinner()` | Announces the result |

## Game Features

- Choose who goes first each round.
- Input validation: occupied cells and out-of-range inputs are rejected with a message.
- Replay support: play multiple rounds in one session without restarting the program.

