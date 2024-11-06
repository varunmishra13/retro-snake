# Retro Snake Game

## Overview:

This project is a simple implementation of the classic **Snake** game using the **Raylib** graphics library in **C++**. The game follows the traditional mechanics where the player controls a snake that grows in length as it eats food while avoiding collisions with the walls and its own body.

## Features:

- **Snake Movement:** The snake is controlled using the arrow keys (Up, Down, Left, Right). The snake’s direction can be changed, but it cannot turn 180 degrees (e.g., moving from left to right directly).
- **Snake Growth:** The snake grows longer every time it eats food. This is achieved by adding a new segment to the front of the snake’s body whenever it eats food.
- **Food Mechanics:** The food is represented as a texture (image of a food item), which is randomly placed within the grid. When the snake collides with the food, its size increases, and the score is updated.
- **Game Over Conditions:** The game ends when the snake collides with the boundaries of the window or runs into its own tail.
- **Graphics & Visuals:** The game uses custom textures for the snake and food, with simple colors for the background and grid. The game board is drawn using rectangles to represent the individual cells, providing a retro-style look.

## Gameplay:

- The game begins with the snake positioned in the middle of the screen.
- The snake moves in the current direction and consumes food when it reaches the food’s position.
- When food is consumed, the snake grows by one unit, and the score increases by 1.
- The game continues until the snake collides with a wall or its own body. At that point, the game restarts, resetting the snake’s position and the score to zero.

## Code Structure:

### Classes:
- **Snake:** Manages the snake’s body, movement, and growth logic.
- **Food:** Handles the food generation and drawing, ensuring it does not overlap with the snake’s body.
- **Game:** The main game logic, which includes checking for collisions, updating the game state, and drawing the game objects.

### Key Functions:
- **ElementInDeque:** Checks if a given element (in this case, a position) exists in the snake’s body to detect collisions with its tail.
- **eventTriggered:** Ensures that game updates occur at fixed intervals, avoiding overly fast updates and ensuring smoother gameplay.

### Graphics:
Uses Raylib’s built-in functions like `DrawRectangle`, `DrawRectangleRounded`, and `DrawTexture` to render the snake, food, and game environment.

## Technologies Used:

- **C++:** The core programming language used for game logic and object management.
- **Raylib:** A simple and easy-to-use library for creating graphical applications, ideal for small-scale games like this one.
- **Image Assets:** Used for food representation to enhance the visual aspect of the game.

## Setup Instructions:

1. **Install Raylib** using your preferred package manager (e.g., Homebrew for macOS).
2. **Clone/Download the Project** repository and open it in your favorite C++ IDE.
3. **Compile and Run:** Build the project and run the executable to start the game.

## Future Improvements:
- **High Score Saving:** Implement a system to track and display the highest score across multiple game sessions.
- **Difficulty Levels:** Introduce varying difficulty levels, where the snake moves faster or the grid becomes smaller as the game progresses.
- **Multi-Player:** Add support for two-player mode with both players controlling different snakes.
- **Sound Effects and Music:** Add sound effects for eating food, colliding with walls, and other game events to make the game more immersive.
- **Enhanced Graphics:** Use more detailed textures or animations for the snake and food to make the game look more polished.

## Conclusion:

This project demonstrates how to create a basic game using **C++** and **Raylib**. The simple gameplay mechanics provide a fun and engaging experience, while the clean and minimalistic code structure allows for easy customization and future expansion.
