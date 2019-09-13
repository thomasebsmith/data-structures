# Queue

## Description
A **queue** is an abstract data type that stores a line of items. Only the item
at the front of the line can be accessed at any given time, and more items can
be added to the back of the line.

## Implementations
Queues are commonly implemented using circular buffers within
[lists](./list.md).

## Interface

For a queue containing items of type T:

| Name     | Type           | Description                                      |
| -------- | -------------- | -----------------------------------------------  |
| size     | Size           | The number of items contained in the queue       |
| push     | T ➝ ()         | Push an item to the back of the queue            |
| front    | T              | The item at the front of the queue               |
| pop      | () ➝ ()        | Remove the item at the front of the queue        |

## Performance
Note that n is the number of items in the queue.
With a list-based implementation:

| Name            | Average Complexity |
| --------------- | ------------------ |
| \<memory used\> | O(n)               |
| size            | O(1)               |
| push            | O(1)               |
| front           | O(1)               |
| pop             | O(1)               |

## Examples
- Perform a breadth-first search on a graph.
- Keep track of a changing list of tasks to perform in order.
