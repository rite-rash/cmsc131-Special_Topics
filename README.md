# SSSSecret

SSSSecret is a dachshund-themed snake game developed using C, Raylib and x86-32 NASM Assembly for CMSC 131 Special Topics.

Players control a growing dachshund as it moves around the game area, collects fruit, and avoids collisions. The project combines C programming and Assembly language through a shared game-state structure.

## 🛠️ Built With

| Layer | What we used |
| :--- | :--- |
| 💻 Application | C |
| 🎮 Graphics and Input | Raylib |
| ⚙️ Game Logic | x86-32 NASM Assembly |
| 🔗 Integration | C and NASM through a shared `GameState` structure |
| 🖥️ Target Platforms | Windows (Win32) and Linux (ELF32) |

The C layer handles application initialization, keyboard input, graphical rendering, game screens, and leaderboard persistence. The NASM Assembly layer handles the core game logic, including snake movement, collision detection, fruit spawning, scoring, and game-state updates.

Both layers communicate through a shared `GameState` structure.

## Target Platforms
- Windows(Win32)
- Linux (ELF32)

## Project Structure
```
./
├── assets/
│   ├── audion/
│   ├── fonts/
│   └── sprites/
├── bin/
├── build/
├── docs/
│   ├── architecture.md
│   └── folder-structure.md
├── include/
│   ├── app/
│   │   └── app.h
│   ├── game/
│   │   └── game.h
│   ├── input/
│   │   └── input.h
│   ├── leaderboard/
│   │   └── leaderboard.h
│   ├── rendering/
│   │   └── renderer.h
│   └── shared/
│       └── game_state.h
├── Makefile
├── README.md
├── src/
│   ├── asm/
│   │   ├── collision.asm
│   │   ├── fruit.asm
│   │   ├── game_init.asm
│   │   ├── game_status.asm
│   │   ├── include/
│   │   │   ├── game_state_offsets.inc
│   │   │   └── platform.inc
│   │   ├── movement.asm
│   │   ├── scoring.asm
│   │   └── snake.asm
│   └── c/
│       ├── app/
│       │   └── app.c
│       ├── game/
│       │   └── game.c
│       ├── input/
│       │   └── input.c
│       ├── leaderboard/
│       │   └── leaderboard.c
│       ├── main.c
│       ├── rendering/
│       │   └── renderer.c
│       └── screens/
│           ├── end_screen.c
│           ├── game_play_screen.c
│           └── start_screen.c
└── tests/
    ├── asm/
    └── c/




```

For a more detailed explanation of the folders and files, see Folder Structure in docs/folder-structure.md.

## Architecture
 The project follows a modular, layered architecture inspired by the Model-View-Controller (MVC) pattern.

The system is dividied into two primary implementation layers:
- **C Layer:** Responsible for application initialization, user input, graphical rendering, game screens, and leaderboard persistence.
- **NASM Layer** Responsible for core game logic, including movement, collision detection, fruit spawning, scoring, and game-state updates.

For more information, see System Architecture in docs/architecture.md.

## Current Development Status
This project is currently ongoing

## Building and Running
TODO: 


## About this Project
This project fulfills the Special Topics requirement for **CMSC 131: Introduction to Computer Organization & Machine Level Programming**, taken during the first semester of our third year at the **University of the Philippines Visayas** under **Ma'am Nicole Beatriz F. Pascasio**.



