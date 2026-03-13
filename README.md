# ♠️ War Card Game – Python Implementation

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Algorithm](https://img.shields.io/badge/Algorithm-Fisher--Yates%20Shuffle-9cf)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 🎯 Project Overview

Card games are a classic foundation for understanding **data structures, randomization, and object-oriented design**.

This project implements a **two-player War-style card game** in Python, built around the Fisher-Yates Shuffle Algorithm. It covers deck generation, draw and discard pile management, turn-based comparison logic, and a robust tie-breaking system — all simulated and logged via console output.

---

## 🃏 Game Rules

- The deck contains **40 cards** — numbers 1 through 10, each appearing **4 times**
- The deck is shuffled and split evenly: each player receives **20 cards** as their draw pile
- Each turn, both players draw the top card from their draw pile
- The **higher card wins** and the winner takes both cards into their discard pile
- **Ties:** If both players draw equal cards, those cards are held — the winner of the **next round** claims all tied cards
- **Consecutive ties:** If multiple ties occur in a row, the eventual round winner claims all accumulated tied cards
- If a player's draw pile is empty, their discard pile is **recycled** and becomes the new draw pile
- A player **loses** when they have no cards left in either pile

---

## 🔬 Implementation Breakdown

### 🔀 Task 1 — Deck Creation & Shuffle
- `gen_deck()` generates a 40-card deck (values 1–10, four copies each)
- `FYS(deck)` implements the **Fisher-Yates Shuffle Algorithm** for unbiased random shuffling — iterates from the last index down, swapping each card with a randomly chosen card at or before its position

### 🃏 Task 2 — Drawing Cards
- `draw_card(player)` draws from the top of the player's draw pile
- If the draw pile is empty, `shuffle_discard_into_draw(player)` recycles the discard pile back into a new draw pile
- Returns `None` if both piles are empty, triggering game over

### ⚔️ Task 3 — Playing a Turn
- `player_turn()` handles card comparison, winner determination, and tie tracking
- Tied cards are accumulated in `tied_cards` and awarded to the next round winner
- Consecutive tie detection prevents infinite stalemates

### 🖥️ Task 4 — Console Output
- Each round prints both players' current card counts and drawn cards
- Round winner (or tie) is announced after every turn
- Final game winner is declared once a player runs out of cards

---

## 🧪 Tests

| Task   | Test Case |
|--------|-----------|
| Task 1 | A new deck contains exactly **40 cards** |
| Task 1 | The shuffle function randomizes the deck *(mock `random.randint`)* |
| Task 2 | Drawing from an empty draw pile correctly shuffles the discard pile into the draw pile |
| Task 3 | The higher card always wins the round |
| Task 3 | A tie followed by a win awards **4 cards** to the winner |

---

## 📁 Project Structure

```
war-card-game/
│
├── card_game.ipynb      # Main Jupyter Notebook with full implementation & output
└── README.md            # Project documentation
```

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/your-username/war-card-game.git
cd war-card-game
```

### 2. Install dependencies
```bash
pip install notebook
```

### 3. Run the notebook
```bash
jupyter notebook card_game.ipynb
```

Run all cells sequentially — the game will simulate automatically and print a full round-by-round log to the output cell.

---

## 🛠️ Tech Stack

| Tool              | Purpose                                      |
|-------------------|----------------------------------------------|
| Python 3.x        | Core language                                |
| Jupyter Notebook  | Interactive development & output display     |
| `random`          | Random index generation for Fisher-Yates     |
| OOP               | `CardGame` class encapsulates all game logic |

---

## 💡 Key Highlights

- Faithful implementation of the **Fisher-Yates Shuffle** for statistically unbiased deck randomization
- Clean separation of draw and discard piles per player, with automatic recycling
- Robust **consecutive tie handling** to prevent stalemates — a common edge case in War-style games
- Round-by-round console output gives full visibility into game state at every step
- Player 1 won the sample run in **200+ rounds**, demonstrating game completion and correct win detection

---

## 📌 Learning Outcomes

This project demonstrates proficiency in:
- Implementing classic **computer science algorithms** (Fisher-Yates) from scratch
- Designing **stateful, turn-based game logic** using OOP
- Managing **multiple data structures** (draw piles, discard piles, tied card buffers) simultaneously
- Writing clean, readable Python with meaningful variable naming and comments

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

## 👤 Author

**Abdurrahman Tahir** — Junior Data Scientist / ML Engineer

🌍 Islamabad, Pakistan | Berlin, Germany 🇩🇪

[![GitHub](https://img.shields.io/badge/GitHub-artimistic--afk-black?logo=github)](https://github.com/artimistic-afk)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-abdurrahmantahir79-blue?logo=linkedin)](https://www.linkedin.com/in/abdurrahmantahir79/)
