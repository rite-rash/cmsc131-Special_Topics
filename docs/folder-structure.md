# Project Folder Structure Guide

This document's purpose is to explain each directory and file type used in this project.


## Main Directories
**include/**
Contains shared C header files (.h). These files declare functions, structures, constants, and data types that can be accessed by different C modules.

**src/c/**
Contains c source code (.c), including the application entry point, input handling, rendering, screens, and leaderboard.

**src/asm/**
Contains NASM assembly source files (.asm) responsible for the core game logic which includes movement, collision detection, fruit spawning, scoring, and game status

**src/asm/include/**
Contains reusable NASM include files (.inc)

- platform.inc - defines platform-specific macros and symbol naming conventions
- game_state_offsets.inc - define memory offsets corresponding to shared C GameState structure

**assets/**
Contains resources such as sprites, fomts, and audio (to be decided)

**docs/**
Contains project documentation, architecture explanations, and other technical references

**tests/**
Contains test files for verifying C modules and NASM routines.

**build/**
stores compilation outputs such as object files

**bin/**
Stores compiled game executables

## FIle Extensions
| Extension | Purpose |
| :--- | :--- |
| `.c` | C source code and function implementations |
| `.h` | C header files and declarations |
| `.asm` | NASM assembly source code |
| `.inc` | Reusable NASM definitions, macros, and constants |
| `.md` | Markdown documentation |
| `Makefile` | Build and compilation instructions |



