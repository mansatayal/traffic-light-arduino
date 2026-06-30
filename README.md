# Traffic Light Controller with Countdown Display

An Arduino-based traffic signal simulator with a synced 8x8 LED matrix countdown timer for each light state.

## How It Works

Three LEDs (red, yellow, green) cycle through a traffic signal sequence, while an 8x8 LED dot-matrix display (driven via `LedControl` / MAX7219) shows a live countdown of seconds remaining for the current light. Digits 0-9 are rendered using a custom bitmap font on the matrix.

**Cycle:**
- Yellow — 3s
- Red — 7s
- Yellow — 3s
- Green — 5s

(loops indefinitely)

## Hardware

- Arduino board
- 3x LEDs (red, yellow, green) — connected to pins 5, 6, 7
- 8x8 LED dot-matrix display with MAX7219 driver
  - DIN → D4
  - CLK → D3
  - CS → D2

## Tech Stack

- Arduino (C++)
- `LedControl` library (MAX7219 matrix driver)

## Setup

1. Install the `LedControl` library via Arduino Library Manager
2. Wire components per the pin mapping above
3. Flash `traffic_light.ino` to the board

## Notes

Early embedded systems project — first hands-on work with LED matrix driving and digit bitmap rendering, alongside basic timed state-machine logic for the signal cycle.
