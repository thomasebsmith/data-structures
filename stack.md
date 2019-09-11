# Stack

## Description
A **stack** is an abstract data type that stores a pile of items. Only the top
item can be accessed at any given time, and more items can be added to the top
of the stack.

## Implementations
Stacks are commonly implemented using [lists](./list.md).

## Interface
For a stack containing items of type T:

| Name     | Type           | Description                                      |
| -------- | -------------- | -----------------------------------------------  |
| size     | Size           | The number of items contained in the stack       |
| push     | T ➝ ()         | Push an item onto the top of the stack           |
| top      | T              | The item at the top of the stack                 |
| pop      | () ➝ ()        | Remove the item at the top of the stack          |

## Performance
Note that n is the number of items in the list.
With an array implementation:

| Name            | Average Complexity |
| --------------- | ------------------ |
| \<memory used\> | O(n)               |
| size            | O(1)               |
| push            | O(1)               |
| top             | O(1)               |
| pop             | O(1)               |

## Examples
- Perform a depth-first search on a graph.
- Keep track of the actions a user can undo and/or redo in an program.
