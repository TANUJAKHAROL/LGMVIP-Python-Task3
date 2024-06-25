# Rock-Paper-Scissors Game

This is a simple command-line based Rock-Paper-Scissors game where you play against the computer. 

## Features

- Play the classic Rock-Paper-Scissors game.
- Random computer choices ensure a fair game.
- Option to play multiple rounds.

## How to Play

1. Run the script.
2. Enter your choice when prompted (rock, paper, or scissors).
3. The computer will randomly choose its move.
4. The result of the game will be displayed.
5. You will be asked if you want to play again. Enter `y` to play another round, or any other key to quit.

## Code

The main functionality is provided by a simple loop and conditionals to determine the game outcome.

```python
import random

options = ("rock", "paper", "scissors")
running = True

while running:

    player = None
    computer = random.choice(options)

    while player not in options:
        player = input("Enter a choice (rock, paper, scissors): ")

    print(f"Player: {player}")
    print(f"Computer: {computer}")

    if player == computer:
        print("It's a tie!")
    elif player == "rock" and computer == "scissors":
        print("You win!")
    elif player == "paper" and computer == "rock":
        print("You win!")
    elif player == "scissors" and computer == "paper":
        print("You win!")
    else:
        print("You lose!")

    if not input("Play again? (y/n): ").lower() == "y":
        running = False

print("Thanks for playing!")
