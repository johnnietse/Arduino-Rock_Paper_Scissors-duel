# Rock Paper Scissors Duel Game on Arduino


## Introduction
This project is an Arduino implementation of the classic "Rock, Paper, Scissors" (RPS) game. RPS is a hand game played between two players where each player forms one of three shapes (rock, paper, or scissors) simultaneously. The outcome of each round is determined by a set of rules:
- Rock beats Scissors
- Scissors beats Paper
- Paper beats Rock

Players can make their choices via buttons, and the outcome is visually indicated through an LED bar. The game features a simple interface with four buttons for player inputs and five LEDs to represent different game states.

The project involves programming two Arduinos, which will play RPS against each other. A tournament will be held to evaluate the strategies developed by each team, with the goal of determining the winning team based on their strategy implementation.


## Features

- **Interactive Gameplay**: Players select Rock, Paper, or Scissors using physical buttons.
- **LED Bar Feedback**: The results of each round are displayed using a series of five LEDs, creating a dynamic visual representation of the game state.
- **Visual Indications**: LEDs blink and light up based on the game state, indicating waiting for player input, showing results, and more.
- **Round Tracking**: The game can remember a maximum of 50 rounds.

## Components Required

- Arduino Board (e.g., Arduino Uno)
- 4 Push Buttons
- 5 LEDs
- Resistors (for buttons and LEDs)
- Breadboard and jumper wires

## Pin Configuration

The following pins are used for buttons and the LED bar:

| Component | Pin Number | Description                        |
|-----------|------------|------------------------------------|
| Button 1  | 3          | Opponent selects Rock              |
| Button 2  | 4          | Opponent selects Paper             |
| Button 3  | 5          | Opponent selects Scissors          |
| Button 4  | 2          | Start the current turn             |
| LED 1     | 12         | First LED (Arduino wins)          |
| LED 2     | 11         |                                    |
| LED 3     | 10         |                                    |
| LED 4     | 9          |                                    |
| LED 5     | 8          | Last LED (Opponent wins)          |



## Game Controls
- The turn button in Figure 1 below is used to start and end a given RPS round.
- The rock, paper and scissors buttons in Figure 1 below are used to tell the Arduino what RPS choice the opponent selected
for the current round.

![Buttons](https://github.com/user-attachments/assets/695451e0-6a7b-402c-8869-d8ba3beac484) 

Figure 1: Arduino RPS Game Controls




## Installation of the Arduino Code 

1. Clone this repository or download the code files.
2. Open the Arduino IDE and load the main `.ino` file.
3. Connect the Arduino board to your computer via USB.
4. Select the appropriate board and port from the Arduino IDE.
5. Upload the code to the Arduino.



## Usage

1. Press the button corresponding to your choice (Rock, Paper, or Scissors).

When a new round is begun, the Arduino shows its RPS choice through the LEDs. Figure 2 below shows
the different LED states for each RPS Choice:

![Screenshot (110)](https://github.com/user-attachments/assets/58dbae4d-3c97-42ed-a1c8-7377f4d4a193) 

Figure 2: LED States for RPS Choices




2. The LED bar will display the result using the LEDs:
   - **LED1 (First LED)**: Lights up for a win (Arduino wins).
   - **LED5 (Last LED)**: Lights up for a loss (Opponent wins).
   - Both LEDs light up for a draw.
   - All LEDs blink to indicate waiting for a player's turn.


The Arduino will then determine the winner of the round based on the RPS choices and display it
through the LEDs, as shown in Figure 3 below:

![Screenshot (111)](https://github.com/user-attachments/assets/bd7f7f30-d70f-4d67-9a79-fc6205682515) 

Figure 3: LED States for Round Results



3. The game can continue for multiple rounds, tracking the results.

## Code Overview

The code consists of several key components:

- **Pin Configuration**: Defines the pins used for buttons and the LED bar.
- **LED States**: Enumerates different LED states (off, blinking, on) using a double-bit pattern.
- **Button Handling**: Functions for waiting for button presses and blinking the LED bar while waiting.
- **Game Logic**: Determines round results based on player choices and updates the LED states accordingly.
- **Utility Functions**: Includes helper functions for time tracking, LED manipulation, and bitwise operations.
