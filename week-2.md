## Nim Game

Github Repo: [https://github.com/marsian83/nim-game-activity](https://github.com/marsian83/nim-game-activity)

## Completed Tasks

1. **Basic Gameplay**: The core gameplay mechanics are implemented, allowing turns for both the player and the AI.
   
2. **AI Implementation**: The AI is designed using the Nim-sum concept, ensuring optimal moves.

3. **Difficulty settings**: The user can switch between easy, medium and hard.

4. **Turn-Based Messaging**: The robot responds with different text messages during the game.

### Difficulty Levels
1. **Easy Mode**: The robot picks items randomly, without following a specific strategy.

2. **Medium Mode**: The robot makes strategic moves 75% of the time and random moves 25% of the time.
   
3. **Hard Mode**: The robot makes purely strategic moves using the Nim-sum logic.

### AI Logic
### Nim-Sum Logic
The key to winning at Nim-like games is understanding the Nim-sum, which is the binary digital sum (exclusive or, XOR) of the number of items in each row.

#### Nim-Sum Calculation
1. **Binary Representation**: Convert the number of items in each row to binary.
2. **XOR Operation**: Perform the XOR operation on all the binary numbers.
   - Example: For rows with 1, 3, 5, and 7 items:
     ```
     1 ⊕ 3 ⊕ 5 ⊕ 7 = 0
     ```
#### Strategic Move
- If the Nim-sum is zero, the player is in a losing position if the opponent plays optimally.
- If the Nim-sum is non-zero, the player can force a win by making the Nim-sum zero after their move.

### AI Move Determination
1. **Calculate Nim-Sum**: The robot calculates the Nim-sum of the current state.
2. **Determine Optimal Move**:
   - For each row, calculate the result of removing a certain number of items to make the Nim-sum zero.
   - Choose the move that results in a zero Nim-sum.
3. **Random Move** (for Easy and Medium modes):
   - In Easy mode, the robot chooses a random valid move.
   - In Medium mode, the robot has a 25% chance of making a random move instead of the optimal move.

### Example Move
- Suppose the current rows have 4, 5, and 7 items.
  - Binary: 4 (100), 5 (101), 7 (111)
  - Nim-sum: 100 ⊕ 101 ⊕ 111 = 010 (2 in decimal)
- The robot will choose a move to make the Nim-sum zero.
  - For instance, removing 2 items from the row with 5 items (101 - 010 = 011, which is 3) results in rows 4, 3, and 7 with a Nim-sum of 000.

https://github.com/marsian83/GSoC-24-report/assets/114365550/c928201a-4f6e-4ae7-94e9-c2a09353119e

## Pending Tasks
1. Visual Customization: Options for selecting enemy character and item visuals (e.g., coins, matchsticks).

2. Configuration Customization: Options for setting the number of rows, items per row, and the maximum number of items a player can remove per turn.

3. Sound Effects: Add sound effects for actions like item removal and winning/losing to make the game more immersive.

5. Testing: Conduct thorough testing to ensure all features work as expected and the game is enjoyable.
