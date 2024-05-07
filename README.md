# Combination Lock State Machine in Verilog

## Overview
This project implements a Moore finite state machine in Verilog, designed to simulate a combination lock on an Altera Board. The state machine uses a 4-input combination to lock or unlock, mimicking the functionality of a physical combination lock.

## File Description
- **combolock.v**: Main Verilog file containing the state machine design.

## Functionality
1. **Setting and Entering Combination**:
   - The lock is set with a predefined 4-input combination.
   - Users enter the combination on the Altera Board and then activate the Enter switch (set Enter input high).
   - If the input matches the stored combination, the door opens (Open output goes high).
   - The door remains open until the Enter is activated again, which closes the door.

2. **Alarm System**:
   - If two incorrect combinations are entered consecutively, an alarm is triggered (Alarm output goes high).
   - The alarm can be reset by pushing the Reset switch high.

3. **Changing the Combination**:
   - To change the combination, enter the current combination and activate the Change switch (set Change input high).
   - If authorization is successful, the New output will go high, allowing a new combination to be set.
   - Confirm the new combination by pressing either the Enter or Change switch high.

## Output Display
- **Hex Display Outputs**:
  - All outputs LOW: Displays '-'
  - Alarm HIGH: Displays 'A'
  - New output HIGH: Displays 'n'
  - Open output HIGH: Displays 'O'

## Usage
- Ensure the Altera Board is properly configured to use this Verilog design.
- Load the `combolock.v` file onto the board.
- Follow the operational guidelines above to interact with the combination lock.

## Additional Information
This project is intended for educational purposes and simulates basic security system functionalities using digital logic and state machines.
