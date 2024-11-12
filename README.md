# Command-Line Wordle Game

This project is a command-line Wordle-style game, based on the popular game created by Josh Wardle and made popular by The New York Times. It is implemented in Python and the rules for the game are the same as the original. Players attempt to guess a hidden word within a limited number of attempts. The game provides feedback for each guess by using ANSI color codes to highlight letter accuracy.

## Key Features

- **Random Word Generation**: The game randomly selects a hidden word from the NLTK corpus based on a specified word length.
- **Color-Coded Feedback**: Each guess is evaluated, and letters are color-coded to indicate their correctness.
- **Turn-Based Gameplay**: Players enter guesses in sequential rounds, with visual feedback displayed after each attempt.
- **Win/Loss Detection**: The game tracks win/loss conditions, ending the game when a player guesses correctly or exhausts the maximum attempts.

## Installation

1. **Clone the repository**:
   ```bash
   git clone <repo_url>
   cd <repo_name>
    ```
   
2. **Install NLTK** (if not already installed):
    ```bash
    pip install nltk
    ```
3 **Download NLTK Word Corpus** (for generating the word list):
    ```bash
    import nltk
    nltk.download('words')
    ```

## Usage

Run the game from the command line by executing:
    ```bash
    python wordle.py
    ```

### Game Instructions
1. Input your guesses based on the word length specified.
2. After each guess, feedback is provided with color-coded hints:
   - <span style="color: limegreen;">**Green**</span>: Letter is in the correct position.
   - <span style="color: gold;">**Yellow**</span>: Letter is in the word but in the wrong position.
   - <span style="color: silver;">**Gray**</span>: Letter is not in the word.

3. Continue guessing until you find the correct word or run out of attempts.

## Code Structure

- **Board Class**: Manages game states, guess recording, and feedback rendering.
  - `add_row`: Adds a guess to the board, applies color-coding, and checks for win/loss conditions.
  - `decorate_letters`: Determines color feedback for each letter in a guess.
  - `check_win`: Checks if the last guess matches the hidden word.
  
- **Utility Functions**:
  - `set_secret`: Selects a hidden word of specified length from the NLTK word list.
  - `get_word`: Prompts players for guesses and validates word length.
  - `check_word`: Ensures each guess is a valid word in the NLTK word list.

## Project Skills

This project showcases skills in:
- Console-based game design and development.
- ANSI color customization for a dynamic CLI experience.
- Word list filtering using the NLTK corpus.
- Interactive game logic with user feedback.

## License

This project is licensed under the MIT License.
