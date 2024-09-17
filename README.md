# Stopwatch Circuit Assignment Readme

## Overview

This assignment involves implementing a stopwatch interface using Logisim Evolution 3.8.0. The interface is provided as a Logisim file named `main.circ`. You are required to build your solution using this file and adhere to the constraints and stages outlined below.

## Logisim Version

- **Required Version**: Logisim Evolution 3.8.0
- **Download Link**: [Logisim Evolution 3.8.0](https://github.com/logisim-evolution/logisim-evolution/releases)

Ensure compatibility with this version to avoid issues with testing.

## Allowed Components

You are permitted to use the following Logisim components:

- **Logic Gates**: Any
- **Flip Flops**: JK, D, S-R, T
- **LEDs**
- **Clock**: Only one
- **Hex Digit Display**: Provided in the interface
- **Buttons**: Provided in the interface
- **Pins**: For connecting circuits
- **Constants**: For setting inputs that will not change
- **Splitter**: For using HEX Digit Display

> **Note**: The use of any other components, such as pre-built circuits like registers or shift registers, will result in penalties.

## Assignment Stages

The assignment is divided into stages, each contributing to the overall grade. Complete each stage in order and save your files with the naming convention `stageX.circ`.

### Stage 1: Implement the Start/Stop Button (10%)

- Wire a circuit that toggles between Start and Stop states using the provided Start/Stop button.
- Use a Flip Flop to track the current state.
- Ensure the "Clock Started" LED is ON when in the Start state and OFF when in the Stop state.

### Stage 2: Implement a Single Digit “Seconds” Display (15%)

- Replace the flashing LED with a counter that increments the seconds display by 1s (0-9) every clock tick.
- The display should start at “00” when the Start/Stop button is first pressed.
- The display should stop when the Start/Stop button is pressed in the Start state and resume counting when pressed in the Stop state.

### Stage 3: Implement the Full Two-Digit “Seconds” Display (20%)

- Expand the display to show seconds in both units and tens columns (00-59).
- Reset the display to “00” when the Reset button is clicked and ensure the stopwatch enters the Stop state.
- Prevent illegal values (e.g., hex values or digits above “5” in the tens column).

### Stage 4: Implement the “Minutes” Display (15%)

- Implement a two-digit minutes display (00-99).
- The minutes display should increment when the seconds display wraps back to “00”.
- Ensure the Start/Stop and Reset buttons function correctly for the minutes display.

### Stage 5: Implement the “Split” Button (15%)

- Implement a “Split” display to show the time when the Split button is pressed.
- The Split Time display should remain unchanged until the Split button is pressed again or the Reset button is clicked.
- Reset the Split Time display to “00:00” when the Reset button is pressed.

### Stage 6: Implement “Split” Time Recording and Multi-“Split” Display (15%)

#### Part 6A

- Record up to 5 split times when the Split button is pressed, using Flip Flops for storage.
- Display the most recent split time and reset all split times to 0 when the Reset button is pressed.

#### Part 6B

- When in the Stop state, display each split time in turn on the Split Time display when the Split button is pressed, wrapping back to the earliest split time after showing the most recent one.

### Stage 7: One Display for Everything (10%)

- Combine all split times and elapsed time into the single “Elapsed Time” display.
- Display split times and elapsed time on the same display when the stopwatch is in the Stop state.
- Indicate when a Split time is being displayed using an additional LED.

## Submission

Submit the following via Canvas (Assignment 1):

- **Logisim File**: `main.circ` implementing the most complete version of your assignment.
- **Stage Files**: Separate Logisim files for each stage, named `stageX.circ`.
- **Report**: A document (Word or PDF) of up to 5 pages including:
  - Your name, student number, unit code, and lab session
  - Description of the circuit
  - Design outline for each stage completed
  - Assumptions made
  - Any unresolved problems
  - Screenshots of your working circuit for each stage

> **Late Submission**: A 10% deduction per day applies for late submissions.
