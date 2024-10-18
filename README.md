# Rock Paper Scissors Duel Game on Arduino


## Introduction
This project is an Arduino implementation of the classic "Rock, Paper, Scissors" (RPS) game. RPS is a hand game played between two players where each player forms one of three shapes (rock, paper, or scissors) simultaneously. The outcome of each round is determined by a set of rules:
- Rock beats Scissors
- Scissors beats Paper
- Paper beats Rock

Players can make their choices via buttons, and the outcome is visually indicated using LEDs. The game features a simple interface with four buttons for player inputs and five LEDs to represent different game states.

The project involves programming two Arduinos, which will play RPS against each other. A tournament will be held to evaluate the strategies developed by each team, with the goal of determining the winning team based on their strategy implementation.

## Features

- **Interactive Gameplay**: Players select Rock, Paper, or Scissors using physical buttons.
- **LED Feedback**: The results of each round are displayed through the state of five LEDs.
- **Visual Indications**: LEDs blink and light up based on the game state, indicating waiting for player input, showing results, and more.
- **Round Tracking**: The game can remember a maximum of 50 rounds.

## Components Required

- Arduino Board (e.g., Arduino Uno)
- 4 Push Buttons
- 5 LEDs
- Resistors (for buttons and LEDs)
- Breadboard and jumper wires

## Pin Configuration

The following pins are used for buttons and LEDs:

| Component | Pin Number | Description                        |
|-----------|------------|------------------------------------|
| Button 1  | 3          | Opponent selects Rock              |
| Button 2  | 4          | Opponent selects Paper             |
| Button 3  | 5          | Opponent selects Scissors          |
| Button 4  | 2          | Start the current turn             |
| LED 1     | 12         | Leftmost LED                       |
| LED 2     | 11         |                                    |
| LED 3     | 10         |                                    |
| LED 4     | 9          |                                    |
| LED 5     | 8          | Rightmost LED                      |

## Installation

1. Clone this repository or download the code files.
2. Open the Arduino IDE and load the main `.ino` file.
3. Connect the Arduino board to your computer via USB.
4. Select the appropriate board and port from the Arduino IDE.
5. Upload the code to the Arduino.

## Usage

1. Press the button corresponding to your choice (Rock, Paper, or Scissors).
2. The game will display the result using the LEDs:
   - **LED1 (Arduino)**: Lights up for a win.
   - **LED5 (Opponent)**: Lights up for a loss.
   - Both LEDs light up for a draw.
   - Blinking LEDs indicate waiting for a player's turn.
3. The game can continue for multiple rounds, tracking the results.

## Code Overview

The code consists of several key components:

- **Pin Configuration**: Defines the pins used for buttons and LEDs.
- **LED Patterns**: Enumerates different LED states (off, blinking, on) using a double-bit pattern.
- **Button Handling**: Functions for waiting for button presses and blinking LEDs while waiting.
- **Game Logic**: Determines round results based on player choices and updates LED states accordingly.
- **Utility Functions**: Includes helper functions for time tracking, LED manipulation, and bitwise operations.
