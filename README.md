# 🏴‍☠️ Minesweeper Game

A simple Minesweeper game implemented using **React.js**.

## 🌟 Features

- Supports only single-click operations to reveal squares; manual flagging of mines is not supported (in most cases, mines will be automatically flagged without manual intervention).
- Game records are stored using **LocalStorage**, with options to export data in:
  - **JSON format**
  - **DBF format** (DBF format does not include the specific distribution of mines or the exact click positions for each step).

## 📜 Square Revealing Rules

1. When a square with **0 adjacent mines** is revealed, all of its **8 neighboring squares** will also be revealed.
2. If a square has a **non-zero mine count** and the number of adjacent unrevealed squares equals its mine count, those adjacent unrevealed squares will be flagged as containing mines.
3. If a square has a **non-zero mine count** and the number of flagged squares around it equals its mine count, the surrounding unflagged squares will be revealed.
4. Repeat steps 1, 2, and 3 for each square in the minefield until no more squares can be revealed.
