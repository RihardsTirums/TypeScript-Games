# Number-Guessing-Game

## Task: Create a Number Guessing Game in TypeScript

Your task is to create a simple console-based number-guessing game in TypeScript. The game will generate a random secret number between 1 and 100, and the user has to guess this number. After each guess, the game should tell the user if their guess was too high, too low, or correct.

![Game Picture](<Screenshot 2023-07-08 at 14.51.44.png>)

## Basic Functionality

1. **Generate a random secret number between 1 and 100** - The game should be able to generate a random number that the user will aim to guess. Use [Math.random()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random) to achieve this.
2. **Create a function to get user's guess** - Use the readline interface to prompt the user for their guess. [Node.js Readline](https://nodejs.org/api/readline.html).
3. **Validate the user's guess** - Ensure the user's guess is a valid number between 1 and 100. If it's not, prompt them to enter a new guess.
4. **Store the user's guess** - Once a valid guess has been made, store this guess for comparison to the secret number.
5. **Compare the user's guess to the secret number** - Create a function that takes the user's guess and the secret number, and determines if the guess is too low, too high, or correct. [TypeScript Comparison Operators](https://www.w3schools.blog/typescript-operators)
6. **Provide feedback to the user** - Depending on the comparison, return a message informing the user if their guess was too low, too high, or correct. Use [TypeScript console.log()](https://developer.mozilla.org/en-US/docs/Web/API/console/log) to output these messages.
7. **Create a function to end the game** - If the user's guess is correct, the game should end. Create a function to close the game session. [Node.js Readline close()](https://nodejs.org/api/readline.html#rlclose)
8. **Repeat guessing process** - If the user's guess was incorrect, allow them to guess again until they get it right or choose to quit the game. Implement this using [Loops in TypeScript](https://www.tutorialspoint.com/typescript/typescript_loops.htm#).
9. **Handle invalid inputs gracefully** - The game should not crash or behave unexpectedly if the user provides an invalid input. It should instead inform the user of the invalid input and request a new input. [TypeScript - If Statement](https://www.tutorialspoint.com/typescript/typescript_if_statement.htm)
   ![Not valid input](<Screenshot 2023-07-08 at 14.52.29.png>)
10. **Create a main game function** - Combine all the previous functions into a main game function that runs the game from start to finish.
11. **Store all past guesses** - Keep track of all the guesses the user has made for reference. [TypeScript - Arrays](https://www.w3schools.com/typescript/typescript_arrays.php)
12. **Limit the number of guesses** - Add a limit to the number of guesses a user can make to increase the challenge.
13. **Display the number of remaining guesses** - After each guess, let the user know how many guesses they have left.
14. **Offer the ability to quit** - At any point, the user should have the option to quit the game.
15. **Create a restart function** - If the user guesses correctly or reaches the guess limit, ask them if they want to play again and restart the game if they do. [TypeScript console.log()](https://developer.mozilla.org/en-US/docs/Web/API/console/log), [TypeScript Functions](https://www.typescriptlang.org/docs/handbook/functions.html)

## Extra Features

To make the game more interesting, you can add the following features:

1. If the user's guess is close to the secret number (within a range of 5), print a special message, "YOU ARE VERY CLOSE!". [Math.abs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/abs)
2. Implement difficulty levels. For instance, 'Easy' could allow more guesses and hints, while 'Hard' could provide no hints and fewer guesses. [Node.js Readline](https://nodejs.org/api/readline.html)
3. Add a scoring system. The fewer guesses the user makes, the higher their score. Display the user's score when they guess correctly. [TypeScript Variables](https://www.typescriptlang.org/docs/handbook/variable-declarations.html)
4. Allow the user to play again without needing to run the program again. After a game ends, ask if they would like to play again. If so, generate a new secret number and start a new game. [Loops in TypeScript](https://www.tutorialspoint.com/typescript/typescript_loops.htm#)
5. Improve user experience by providing clear instructions and feedback after each guess. Remind the user of the rules and state of the game. [TypeScript console.log()](https://developer.mozilla.org/en-US/docs/Web/API/console/log), [String Interpolation in TypeScript](https://upmostly.com/typescript/string-interpolation-in-typescript)
---
# Hangman

## Task: Create a Hangman Game in TypeScript

In this task, you are to create a console-based version of the classic word guessing game - Hangman. The computer will select a secret word from a list and the player will try to guess the word one letter at a time. The player will have a limited number of incorrect guesses before the game ends.

![Hangman](<Screenshot 2023-07-08 at 15.49.51.png>)

Here's a simple ASCII representation of the hangman you might want to use:
![Hangman](<Screenshot 2023-07-08 at 15.26.26.png>)

After each incorrect guess, a part of the hangman is drawn. You can add these in the order you prefer:

![Hangman](<Screenshot 2023-07-08 at 15.27.07.png>)


If the hangman is completed (i.e., all the parts are drawn), the game is over and the player loses. If the player guesses all the letters in the word before the hangman is completed, they win.

## Core Functionality

1. Define a list of words that the game will use as potential secret words. [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
2. Generate a random secret word from the list you defined. [Math.random](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random)
3. Initialize a variable to represent the hangman's current state. This variable should change as the user makes incorrect guesses. [TypeScript Variables](https://www.typescriptlang.org/docs/handbook/variable-declarations.html)
4. Use the readline interface to get the user's letter guess from the console. [Node.js Readline](https://nodejs.org/api/readline.html)
5. Implement logic to validate the user's input. The game should handle invalid inputs (e.g., numbers, special characters, or previously guessed letters) gracefully. [TypeScript - If Statement](https://www.tutorialspoint.com/typescript/typescript_if_statement.htm)
6. Check if the guessed letter is in the secret word. [Array.indexOf](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf)
7. If the letter is in the word, reveal the position(s) of the letter in the word. [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
8. If the letter is not in the word, add a part to the hangman's figure and display it to the user. [TypeScript - If Statement](https://www.tutorialspoint.com/typescript/typescript_if_statement.htm)
9. Keep track of letters the user has already guessed and do not count repeated guesses against them. [Array.includes()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/includes)
10. Display the current state of the secret word and the hangman after each guess. [TypeScript console.log()](https://developer.mozilla.org/en-US/docs/Web/API/console/log)
11. If the user correctly guesses all the letters in the word, congratulate them and end the game. [Array.every](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every)
12. If the user makes a certain number of incorrect guesses and the hangman is complete, tell them they've lost and end the game. [TypeScript Variables](https://www.typescriptlang.org/docs/handbook/variable-declarations.html)

## Extra Features

To make the game more interesting, you can add the following features:

1. Allow the user to guess the entire word, not just a single letter. [TypeScript Variables](https://www.typescriptlang.org/docs/handbook/variable-declarations.html)
2. Implement difficulty levels. For instance, 'Easy' could have longer guess limits and shorter words, while 'Hard' could provide shorter guess limits and longer words. [Node.js Readline](https://nodejs.org/api/readline.html)
3. Display a hint or definition related to the secret word. [TypeScript console.log()](https://developer.mozilla.org/en-US/docs/Web/API/console/log)
4. Implement a scoring system. The fewer guesses the user makes, the higher their score. Display the user's score when they guess correctly. [TypeScript Variables](https://www.typescriptlang.org/docs/handbook/variable-declarations.html)
5. Allow the user to play again without needing to run the program again. After a game ends, ask if they would like to play again. If so, select a new secret word and start a new game. [Loops in TypeScript](https://www.tutorialspoint.com/typescript/typescript_loops.htm#)
6. Improve user experience by providing clear instructions and feedback after each guess. Remind the user of the rules and state of the game. [TypeScript console.log()](https://developer.mozilla.org/en-US/docs/Web/API/console/log), [String Interpolation in TypeScript](https://upmostly.com/typescript/string-interpolation-in-typescript)

## Additional Resources

Here are some extra resources that might come in handy as you are working on this task:

- [TypeScript For Loop](https://www.tutorialspoint.com/typescript/typescript_loops.htm#): You will likely need to use a loop to keep the game going until the word is guessed or the hangman is completed.
- [String.prototype.split()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split): This method can be used to split the secret word into an array of letters, making it easier to check if the guessed letter is in the word and reveal it.
- [Array.prototype.join()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join): This method can be used to join the array of letters back into a string for display to the user.
---

# Casion Blackjack Game

## Task: Create a Blackjack Game in TypeScript

In this task, you will create a console-based version of the classic casino card game, Blackjack. The game will be played against the computer, who acts as the dealer. 

The player will be dealt two cards, and will then decide whether to ask for more cards in an attempt to get their card total as close to 21 as possible, without going over. The dealer will also draw cards, and the player wins if they get closer to 21 than the dealer, or if the dealer goes over 21.
[Blackjack](https://en.wikipedia.org/wiki/Blackjack)
## Example of Console Output

Here's a visual example of what the console output could look like:
![Alt text](<Screenshot 2023-07-08 at 18.06.58.png>)

## Core Functionality

1. **Define the suits and ranks that a card can have.** Each card should have a suit (hearts, diamonds, clubs, spades) and a rank (2-10, J, Q, K, A).[TypeScript Object Type](https://www.typescriptlang.org/docs/handbook/2/objects.html)
2. **Create a Card class.** This class should have properties for the suit and rank, and might have methods to get the value of a card and to display it as a string. [TypeScript Classes](https://www.typescriptlang.org/docs/handbook/classes.html)
3. **Create a deck of cards** as an array of Card objects. [TypeScript - Arrays](https://www.w3schools.com/typescript/typescript_arrays.php)
4. **Shuffle the deck of cards.** This could be done by swapping each card with another random card. [Math.random()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random) and [TypeScript - Array.prototype.sort](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)
5. **Initialize the player's and dealer's hands** as empty arrays. [TypeScript - Arrays](https://www.w3schools.com/typescript/typescript_arrays.php)
6. **Deal two cards** to the player and the dealer.[Array.pop](https://www.tutorialspoint.com/typescript/typescript_array_pop.htm)
7. **Display the player's hand** and one of the dealer's cards.[TypeScript console.log()](https://developer.mozilla.org/en-US/docs/Web/API/console/log)
8. **Calculate the total value of a hand.** Aces can be worth 1 or 11, face cards (J, Q, K) are worth 10, and other cards are worth their rank. [TypeScript Variables](https://www.typescriptlang.org/docs/handbook/variable-declarations.html)
9. **Ask the player if they want to "hit"** or "stand". [Node.js Readline](https://nodejs.org/api/readline.html)
10. **If the player hits,** add another card to their hand, calculate their new total, and display their hand again. [Array.push()](https://www.tutorialspoint.com/typescript/typescript_array_push.htm)
11. **If the player's total exceeds 21,** they lose. Display a message indicating this and end the game. [TypeScript - If Statement](https://www.tutorialspoint.com/typescript/typescript_if_statement.htm)
12. **If the player stands,** reveal the dealer's full hand and calculate the total value. [TypeScript console.log()](https://developer.mozilla.org/en-US/docs/Web/API/console/log)
13. **If the dealer's total is less than 17,** have them draw cards until their total is 17 or higher.[TypeScript While Statement](https://www.tutorialsteacher.com/typescript/while-loop)
14. **If the dealer's total exceeds 21,** the player wins. Display a message indicating this. [TypeScript - If Statement](https://www.tutorialspoint.com/typescript/typescript_if_statement.htm)
15. **If the dealer's total is greater than the player's,** the dealer wins. Otherwise, the player wins. Display a message indicating the result. [TypeScript - If Statement](https://www.tutorialspoint.com/typescript/typescript_if_statement.htm)
16. **Ask the player if they want to play again.** If they do, start a new game with a fresh deck of cards. If not, end the game. [Node.js Readline](https://nodejs.org/api/readline.html)

## Extra Features
1. **Splitting Hands** If the player is dealt two cards of the same rank, they should be allowed to split the hand into two separate hands and play them independently. This adds a new layer of strategy and decision-making to the game. [TypeScript - If Statement](https://www.tutorialspoint.com/typescript/typescript_if_statement.htm), [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
2. **Double Down** Implement a "double down" feature. If a player chooses to double down, they can double their initial bet, but must commit to stand after receiving exactly one more card. This feature can make the game more exciting and closely simulate real-world blackjack. [TypeScript Variables](https://www.typescriptlang.org/docs/handbook/variable-declarations.html), [Node.js Readline](https://nodejs.org/api/readline.html)
3. **Insurance** When the dealer's up-card is an Ace, offer the player "insurance" against the possibility that the dealer has a blackjack. The player can wager up to half of their initial bet as insurance. [TypeScript - If Statement](https://www.tutorialspoint.com/typescript/typescript_if_statement.htm), [Node.js Readline](https://nodejs.org/api/readline.html)
---

# Battleship Game

## Task: Create a Battleship Game in TypeScript

In this task, you will create a console-based version of the classic board game, Battleship. The game will be a single-player, where the computer will randomly place ships on a grid, and the player will attempt to guess the locations of these ships.

The game board is a two-dimensional grid (usually 10x10 in the standard game, but you can adjust this for difficulty levels). The player and the computer each have a fleet of ships of varying lengths that are placed on the grid. The locations of the computer's ships are hidden from the player. The player takes turns guessing grid coordinates (for example, 'B5'), and the goal is to sink all of the computer's ships by guessing their locations on the grid.

Here's a visual example of what the console output could look like:

![BattleShip](<Screenshot 2023-07-08 at 18.28.51.png>)

## Core Functionality
1. **Create a 10x10 grid for the player and the computer** - This will be used to place the ships and track the guessed coordinates. [TypeScript - Multi-Dimensional Arrays](https://www.tutorialspoint.com/typescript/typescript_multi_dimensional_arrays.htm)
2. **Allow the player to place their ships on the grid** - You can decide how many ships the player will have and their sizes. [Node.js Readline](https://nodejs.org/api/readline.html)
3. **Place ships on the grid for the computer** - This should be done automatically at the start of the game. [Math.random()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random)
4. **Allow the player to guess a coordinate** - The player should be able to enter a coordinate where they think one of the computer's ships is located. [Node.js Readline](https://nodejs.org/api/readline.html)
5. **Check if the guessed coordinate is a hit or a miss** - If a ship is located at the guessed coordinate, mark it as a hit. Otherwise, mark it as a miss. [TypeScript - If Statement](https://www.tutorialspoint.com/typescript/typescript_if_statement.htm)
6. **The computer guesses a coordinate** - After the player has guessed a coordinate, it's the computer's turn to guess. [Math.random()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random)
7. **Determine the winner of the game** - The game ends when all the ships of a player have been sunk. [TypeScript - If Statement](https://www.tutorialspoint.com/typescript/typescript_if_statement.htm), [TypeScript Array.every](https://www.tutorialspoint.com/typescript/typescript_array_every.htm)
8. **Display the game boards** - Show the current state of the game after each turn. [TypeScript console.log()](https://developer.mozilla.org/en-US/docs/Web/API/console/log)

## Extra Features
To make the game more interesting, you can add the following features:

1. **Implement different types of ships**, each with their own size and number of hits required to sink.
2. **Add special weapons** that can target multiple grid squares or reveal parts of the grid.
3. **Implement a radar system** that gives a hint about the location of the ships.
4. **Provide the player with the ability to choose the level of difficulty**, adjusting the number of ships and their sizes based on the selected level.
---

# Tic-Tac-Toe

## Task: Create a Tic-Tac-Toe Game in TypeScript

Your task is to create a console-based version of Tic-Tac-Toe. The game is played on a grid of 3x3, where two players take turns marking the spaces in a grid with their symbol (X or O). The player who succeeds in placing three of their marks in a horizontal, vertical, or diagonal row wins the game.

## Core Functionality
1. **Board Creation**: Generate a 3x3 game board. This could be represented as a 2D array. [TypeScript - Multi-Dimensional Arrays](https://www.tutorialspoint.com/typescript/typescript_multi_dimensional_arrays.htm)
2. **User Input**: Allow players to specify their move as a coordinate on the grid (e.g., top middle, bottom left). Validate that the selected move is both within the bounds of the board and not already occupied. [Node.js Readline](https://nodejs.org/api/readline.html), [TypeScript - If Statement](https://www.tutorialspoint.com/typescript/typescript_if_statement.htm)
3. **Turn System**: Players take turns to make their move. After each move, check if there's a winner. [TypeScript - If Statement](https://www.tutorialspoint.com/typescript/typescript_if_statement.htm)
4. **Win Condition**: Implement a function to check if a player has won. The function should check all rows, columns, and the two diagonals to see if any of them consist of the same player's symbol. [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
5. **Draw Condition**: If the entire board gets filled up and there is no winner, declare the game as a draw. [TypeScript - If Statement](https://www.tutorialspoint.com/typescript/typescript_if_statement.htm)
6. **Game Loop**: After a game ends (either with a winner or a draw), ask the players if they want to play again. If they do, reset the board and start a new game. [Loops in TypeScript](https://www.tutorialspoint.com/typescript/typescript_loops.htm#)

## Extra Features

To make the game more interesting, you can add the following features:
1. **Player Names**: At the start of the game, ask the players for their names and use these when announcing whose turn it is or who has won the game. [Node.js Readline](https://nodejs.org/api/readline.html)
2. **Score Keeping**: Keep track of how many games each player has won. After each game, display the scores before asking if they want to play again. [TypeScript Variables](https://www.typescriptlang.org/docs/handbook/variable-declarations.html)
---