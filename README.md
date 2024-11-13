# Hangman
This project involves creating a fully functional *Guess the Word* game in Python. In this game, the player tries to guess a hidden word, one letter at a time, within a limited number of incorrect guesses. The program randomly selects a word from a file containing various words, providing an interactive experience as the user attempts to reveal the word letter by letter. Key features include two difficulty levels, a display that updates after each guess, and session statistics that provide feedback on wins and losses across multiple games.

### How It Works - Big Picture
The game begins by prompting the user to select a difficulty level, where "easy" provides 12 guesses and "hard" offers 8. The program then selects a random word, chosen based on a randomly selected length between 5 and 10 letters, which remains hidden from the player. The player guesses letters one at a time, and the display updates to reveal correctly guessed letters and show remaining letters as underscores. Incorrect guesses reduce the player’s remaining attempts. The game continues until the player either guesses the word or uses up all allowed guesses. After each game, the player can choose to play again, with session statistics showing total wins and losses.

### Key Demonstrated:
1. **Modular Function Design**: The game is divided into distinct, well-defined functions that each serve a specific purpose, such as getting user input, updating the game display, and processing guesses. This modular approach enhances readability, enables easier debugging, and allows functions to be reused or modified without impacting other parts of the program.

2. **String Manipulation and Display Updates**: The game updates the displayed word with correctly guessed letters, showing guessed letters in sorted order and using underscores for letters yet to be guessed. This is achieved through string and list manipulation. 

3. **User Input Handling and Error Checking**: The program handles user input carefully, ensuring no repeated guesses reduce the remaining attempts, and provides feedback if the player guesses the same letter again. This creates a smooth and intuitive user experience.

4. **File Handling and Random Selection**: Words are selected from a predefined file (`lowerwords.txt`), adding variety to each game session. The program uses random selection to pick words of different lengths, enhancing replayability and challenge.

5. **Game Flow and Logic Using Loops**: A series of `while` loops manage the main game logic, from guessing each letter to replaying the game. This structure allows for flexible game sessions and ensures that game conditions, such as winning or losing, are correctly handled and displayed.

**Key Functions:**

**handleUserInputDifficulty():** Selects the game mode (easy or hard) based on user choice.

**getWord():**  Randomly picks a word of specified length from a file.

**createDisplayString():**  Generates the display showing guessed letters and the secret word's current state.

**handleUserInputLetterGuess():**  Manages user letter input, ensuring no repeats.

**updateGuessedWordAsList():**  Updates guessed letters in the word’s display list.

**processUserGuess():**  Processes each guess, adjusting game state based on correctness.

**runGame():**  Orchestrates the entire game, tracking progress and prompting replay.
