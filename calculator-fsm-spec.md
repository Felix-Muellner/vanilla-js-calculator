# Formal Specification

## Inputs

- **Digits**: `0, 1, 2, 3, 4, 5, 6, 7, 8, 9`
- **Operators**: `+, -, *, /`
- **Evaluate**: `=`
- **Clear All**: `CA`
- **Delete**: `DEL`

## States

- Initial
- AccumulatingFirstNumberDigits
- AccumulatingSecondNumberDigits
- OperatorPending
- ResultDisplayed

## State Transition Table

> This Table consists of the cartesian product of the **Inputs** and **States**

| Current State | Input | Next State | Action |
|-|-|-|-|
| Initial | Digits | AccumulatingDigits | Store Digit |
| Initial | Operators | OperatorPending | Store Operator |
| Initial | Evaluate | Initial | Ignore |
| Initial | Clear All | Initial | Ignore |
| Initial | Delete | Initial | Ignore |
| AccumulatingFirstNumberDigits | Digits | | |
| AccumulatingFirstNumberDigits | Operators | | |
| AccumulatingFirstNumberDigits | Evaluate | | |
| AccumulatingFirstNumberDigits | Clear All | | |
| AccumulatingFirstNumberDigits | Delete | | |
| AccumulatingSecondNumberDigits | Digits | | |
| AccumulatingSecondNumberDigits | Operators | | |
| AccumulatingSecondNumberDigits | Evaluate | | |
| AccumulatingSecondNumberDigits | Clear All | | |
| AccumulatingSecondNumberDigits | Delete | | |
| OperatorPending | Digits | | |
| OperatorPending | Operators | | |
| OperatorPending | Evaluate | | |
| OperatorPending | Clear All | | |
| OperatorPending | Delete | | |
| ResultDisplayed | Digits | | |
| ResultDisplayed | Operators | | |
| ResultDisplayed | Evaluate | | |
| ResultDisplayed | Clear All | | |
| ResultDisplayed | Delete | | |

## State Diagram