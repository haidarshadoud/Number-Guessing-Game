## Number Guessing Game in Python

A simple interactive game: the program picks a secret number from 1 to 100, and the player keeps guessing until they find it. After each guess the program says whether the value was too high, too low, or correct. When the player wins, it prints guess statistics and asks whether to play again.

### Project Objectives

This project aims to:

* Implement a classic number guessing game in Python.
* Practice fundamental programming concepts like random number generation, user input, conditional statements, and loops.
* Create a user-friendly and interactive experience.

### Features

* Random secret number between 1 and 100
* Feedback for high / low / correct guesses
* Invalid (non-numeric) input is rejected without crashing
* Guess counters (too high, too low, total)
* Optional extra round after a win

### Requirements

* Python 3 (verified with Python 3.12.0)
* Standard library only (`random`) — no extra packages

### Installation

No package install is required.

Optional virtual environment (Windows):

```bat
python -m venv .venv
.venv\Scripts\activate
```

### How to run

From the folder that contains `Number Guessing Game.py`:

```bat
python "Number Guessing Game.py"
```

Quote the filename because it contains spaces.

### Project structure

```text
Number-Guessing-Game---Python-main/
├── Number Guessing Game.py    # main program
├── README.md
├── RUN_GUIDE.md               # Arabic run instructions
├── LICENSE
└── step-by- step - explanation.pdf
```

### Example usage

```text
Please guess a number between 1 and 100: 10

Too low, try again.
Please guess a number between 1 and 100: 90

Too high, try again.
Please guess a number between 1 and 100: 42

You got it correct! Congratulations!

Number of times too high: 1
Number of times too low: 1
Total number of guesses: 3

Do you want to play again? (y/n): n

Thanks for playing! 👋
```

### How it Works

1. The program imports the `random` module.
2. `play_game()` generates a secret number and loops until the player guesses it.
3. Each guess is compared with the secret number; counters and messages are updated.
4. `main()` starts a round, then asks whether to play again (`y` continues; anything else exits).

### What I Learned

Developing this game helped solidify understanding of:

* The `random` module for generating random numbers.
* Working with user input and converting it to an integer.
* Conditional statements (`if`, `elif`, `else`) for decision making.
* Loops (`while`) for repetitive tasks.
* Displaying formatted output using `print` statements.

### Project Purpose

This number guessing game serves as a:

* **Learning tool:** It reinforces core Python programming concepts in a practical and engaging way.
* **Simple entertainment:** It provides a casual game experience for users to test their luck and intuition.

### Further Development

* Difficulty levels with adjustable number ranges.
* Limited number of attempts to add an element of challenge.
* Score tracking based on the number of guesses.

For Arabic setup and troubleshooting, see [RUN_GUIDE.md](RUN_GUIDE.md).
