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
| Initial | Digits | AccumulatingFirstNumberDigits | Store Digit |
| Initial | Operators | OperatorPending | Store Operator |
| Initial | Evaluate | Initial | Ignore |
| Initial | Clear All | Initial | Ignore |
| Initial | Delete | Initial | Ignore |
| AccumulatingFirstNumberDigits | Digits | AccumulatingFirstNumberDigits | Store Digit |
| AccumulatingFirstNumberDigits | Operators | OperatorPending | Store Operator |
| AccumulatingFirstNumberDigits | Evaluate | AccumulatingFirstNumberDigits | Ignore |
| AccumulatingFirstNumberDigits | Clear All | Initial | Clear All |
| AccumulatingFirstNumberDigits | Delete | !!!AccumulatingFirstNumberDigits!!! | Delete last Digit |
| OperatorPending | Digits | AccumulatingSecondNumberDigits | Store Digit |
| OperatorPending | Operators | OperatorPending | Ignore |
| OperatorPending | Evaluate | OperatorPending | Ignore |
| OperatorPending | Clear All | Initial | Clear All |
| OperatorPending | Delete | AccumulatingFirstNumberDigits | Delete Operator |
| AccumulatingSecondNumberDigits | Digits | AccumulatingSecondNumberDigits | Store Digits |
| AccumulatingSecondNumberDigits | Operators | AccumulatingSecondNumberDigits | Ignore |
| AccumulatingSecondNumberDigits | Evaluate | | |
| AccumulatingSecondNumberDigits | Clear All | | |
| AccumulatingSecondNumberDigits | Delete | | |
| ResultDisplayed | Digits | | |
| ResultDisplayed | Operators | | |
| ResultDisplayed | Evaluate | | |
| ResultDisplayed | Clear All | | |
| ResultDisplayed | Delete | | |

## State Diagram