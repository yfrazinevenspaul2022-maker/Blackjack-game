Blackjack Game
A command-line Blackjack game written in Python that simulates the classic card game between a player and the computer dealer.
## Description
This project implements a text-based Blackjack game where the player competes against a computer dealer. The game handles core Blackjack rules including Blackjack detection, Ace value adjustment (11 → 1), busting, and win/loss/draw outcomes.
## Features
- Automatic card dealing via a deal_cards() function
- Smart score calculation that adjusts Aces from 11 to 1 to prevent busting
- Blackjack detection (21 with exactly 2 cards)
- Full win condition logic: Blackjack, bust, higher score, or draw
- Displays the computer's first card while keeping the rest hidden (standard Blackjack rules)
- Continuous gameplay loop until the round ends
## How It Works
1. Both the player and computer are dealt 2 cards to start
2. Scores are calculated each turn using calculate_scores()
3. The player's cards and current score are displayed; only the computer's first card is shown
4. The game ends automatically if:
   - Either player hits Blackjack (21 with 2 cards)
   - The player busts (score > 21)
   - The computer busts
5. compare() determines the final result and prints the outcome
## Game Logic
| Condition | Result |
|---|---|
| User score == Computer score | Draw |
| Computer score == 0 (Blackjack) | Computer wins |
| User score == 0 (Blackjack) | User wins |
| User score > 21 | User busts — Computer wins |
| Computer score > 21 | Computer busts — User wins |
| User score > Computer score | User wins |
| Otherwise | Computer wins |
## How to Run
bash
python blackjack.py

> Requires Python 3. No external libraries needed.
## Project Structure

blackjack.py
├── deal_cards()         # Returns a random card value
├── calculate_scores()   # Calculates hand score, handles Ace adjustment
├── compare()            # Determines winner based on scores
└── Game loop            # Manages game state and player interaction

## Future Improvements
- Add user input to hit or stand
- Support multiple rounds with score tracking
- Add betting system
- Expand to multiplayer support
## Author 
Evens Paul Yfrazin
