# System Architecture

## Architectural Overview
 The project follows a modular, layered architecture inspired by the Model-View-Controller (MVC) pattern.

The system is dividied into two primary implementation layers:
- **C Layer:** Responsible for application initialization, user input, graphical rendering, game screens, and leaderboard persistence.
- **NASM Layer** Responsible for core game logic, including movement, collision detection, fruit spawning, scoring, and game-state updates.

Moreover, the two layers communicate through a shared GameState structure.

## System Components
### C Application Layer
| Component | Responsibility |
| :--- | :--- |
| Main | Application entry point |
| App | Initializes Raylib and manages the main game loop |
| Input | Captures and processes keyboard input |
| Screens | Manages the start, gameplay, and end screens |
| Renderer | Draws the game grid, dachshund, fruit, and HUD |
| Game Bridge | Coordinates calls between C and NASM |
| Leaderboard | Handles player-name input and local score persistence |


### NASM Game Logic Layer

| Module | Responsibility |
| :--- | :--- |
| Game Initialization | initializes game state |
| Snake | Manages snake-related data and growth |
| Movement | Updates the snake's position |
| Collision | Detects wall and self-collisions |
| Fruit | Handles fruit spawning and consumption |
| Scoring | Updates the player's score |
| Game Status | Checks win and lose conditions |


## Game Loop and Component Interaction
Following sequences takes place during gameplay:
1. Application takes keyboard input through Raylib
2. C translates input to a game component
3. C passes appropriate data to NASM
4. NASM processes movement and updates game state
5. NASM checks collisions, fruit consumption, scoring, and win condition
6. C reads updated game state
7. Raylib renders updated game
8. Repeat until game reaches win/lose state

## Shared Game State
C and NASM communicates through a shared GameState structure.

C structure is defined in include/shared/game_state.h, while the corresponding NASM memory offsets are defined in src/asm/include/game_state_offsets.inc.

Both definitions must remain synchronized.

Structure information stores the following:
- Game status
- Player score
- Snake length
- Snake segment coordinates
- Current direction
- Fruit coordinates




