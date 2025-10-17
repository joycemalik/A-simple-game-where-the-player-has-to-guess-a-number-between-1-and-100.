# Guess the Number Game

A simple, single-page web game where the player has to guess a randomly generated number between 1 and 100. The game provides immediate feedback on guesses, tracks the number of attempts, and allows players to reset the game to start a new round.

## How to Use

1.  **Save the file:** Save the provided `index.html` content to a file named `index.html` on your local computer.
2.  **Open in Browser:** Double-click the `index.html` file, or drag and drop it into any modern web browser (e.g., Chrome, Firefox, Edge, Safari).
3.  **Start Guessing:** A new game will start automatically. Enter a number between 1 and 100 in the input field.
4.  **Submit Guess:** Click the "Guess" button or press the Enter key to submit your guess.
5.  **Get Feedback:** The game will tell you if your guess was "Too high!", "Too low!", or if you guessed correctly.
6.  **Track Attempts:** The number of attempts will be displayed and updated with each guess.
7.  **Reset Game:** Click the "Reset Game" button at any time to start a new game with a new random number.

## Code Explanation

This project is built using only HTML and vanilla JavaScript, contained within a single `index.html` file for simplicity and portability.

*   **HTML Structure (`index.html`):**
    *   Sets up the basic layout with a main heading, instructions, an input field (`<input type="number">`) for the player's guess, and two buttons ("Guess" and "Reset Game").
    *   Includes dedicated paragraphs (`<p id="feedback">` and `<p id="attempts">`) to display game feedback and the current attempt count.
    *   Basic inline CSS (`<style>`) is used to provide a clean, readable, and centered layout, along with specific color feedback for "too high", "too low", and "correct" guesses.

*   **JavaScript (Vanilla):**
    *   **Variables:** `targetNumber` stores the randomly generated number, and `attempts` keeps track of the player's guesses. DOM elements are cached for efficient access.
    *   **`startGame()` function:**
        *   Initializes a new game round.
        *   Generates a new random `targetNumber` between 1 and 100.
        *   Resets `attempts` to `0`.
        *   Clears previous feedback, input value, and re-enables the guess input and button.
        *   Sets focus on the input field for immediate play.
    *   **`checkGuess()` function:**
        *   Reads the user's input from the `guessInput` field.
        *   Validates the input to ensure it's a number within the 1-100 range, providing an error if invalid.
        *   Increments the `attempts` counter.
        *   Compares the `userGuess` to the `targetNumber` and updates the `feedbackDisplay` with appropriate messages ("Too high!", "Too low!", or "Congratulations!").
        *   If the guess is correct, it disables the input and guess button, congratulating the player.
        *   Clears the input field after each guess and re-focuses it for convenience.
    *   **Event Listeners:**
        *   An event listener is attached to the "Guess" button to call `checkGuess()` when clicked.
        *   Another listener is on the "Reset Game" button to call `startGame()` when clicked.
        *   A `keypress` listener on the input field allows the player to submit a guess by pressing the 'Enter' key.
    *   **Initialization:** `document.addEventListener('DOMContentLoaded', startGame);` ensures that a new game begins as soon as the HTML content is fully loaded in the browser.

## License

This project is licensed under the MIT License.