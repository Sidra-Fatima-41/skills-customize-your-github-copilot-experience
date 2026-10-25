
# 📘 Assignment: Hangman Game

## 🎯 Objective

Build a Hangman game in Python that lets a player guess a hidden word before running out of attempts. Practice string manipulation, loops, conditionals, user input, and random selection.

## 📝 Tasks

### 🛠️ Set Up the Game

#### Description
Use the provided list of words and starter code to randomly select a secret word and initialize the game state.

#### Requirements
Completed program should:

- Randomly select a word from the predefined `words` list.
- Track the letters guessed by the player.
- Set a maximum number of incorrect guesses.


### 🛠️ Implement the Guessing Game

#### Description
Create the main game loop so the player can guess letters, reveal the matching letters in the hidden word, and receive feedback about the game result.

#### Requirements
Completed program should:

- Accept letter guesses from the player and display the current progress, such as `_ _ _`.
- Track and display the number of incorrect guesses remaining.
- End when the player guesses the word or uses all available attempts.
- Display a clear win or lose message.
