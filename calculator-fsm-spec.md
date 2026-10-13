# Formal Specification

## Inputs

- **Digits**: `0, 1, 2, 3, 4, 5, 6, 7, 8, 9`
- **Operators**: `+, -, *, /`
- **Evaluate**: `=`
- **Clear All**: `CA`
- **Delete**: `DEL`

## States

- Initial
- AccumulatingDigits
- OperatorPending
- ResultDisplayed

## State Transition Table

> This Table consists of the cartesian product of the **Inputs** and **States**

| Current State | Input | Next State | Action |
|-|-|-|-|

## State Diagram