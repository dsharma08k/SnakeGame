# Snake Game

This is a classic Snake Game built in Python using the `turtle` graphics library. The player controls a snake that moves around the screen, eating food to grow and trying to avoid collisions with the walls or its own tail. The game tracks and saves high scores between sessions.

## Game Features

- **Control**: Use the arrow keys to direct the snake's movement.
- **Food**: Randomly appears on the screen; each piece eaten makes the snake grow.
- **Score**: Tracks the player's current score and saves the high score to a file.
- **Game Over**: Occurs if the snake collides with the wall or itself.

## Project Structure

The project contains the following files:

### Python Files

1. **`food.py`**: 
   - Defines the `Food` class, responsible for creating and placing the food on the screen.
   - Key features:
     - Inherits from `Turtle` to represent food as a small blue circle.
     - Randomly places food on the screen using the `refresh()` method.

2. **`main.py`**: 
   - The main game file, setting up the game screen, managing game logic, and handling collisions.
   - Key features:
     - Initializes the screen and creates instances of `Snake`, `Food`, and `Scoreboard`.
     - Contains the main game loop, updating the game and handling:
       - Collision with food (increases score and grows the snake).
       - Collision with walls or the snake's tail (triggers a game reset).

3. **`scoreboard.py`**: 
   - Manages score display and high score tracking.
   - Key features:
     - Displays current and high scores on the screen.
     - Reads and writes high score data to `high_score.txt`.
     - Resets score on game-over and updates high score if beaten.

4. **`snake.py`**: 
   - Implements the snake's behavior, including movement, growth, and collision detection.
   - Key features:
     - Moves the snake in segments, with controls to change direction.
     - Grows the snake by adding segments after eating food.
     - Resets snake position and length if it collides with walls or itself.

### Text File

- **`high_score.txt`**: 
  - Stores the high score achieved in the game, which persists between sessions.
    
## How to Play

**Run the Game**: Start the game by running the `main.py` file.
   ```bash
   python main.py
