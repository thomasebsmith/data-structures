# Priority Queue

## Description
A **priority queue** is an abstract data type that stores a collection of items,
each with an associated priority. It allows addition of items and removal of the
item with the highest priority.

## Implementations
Priority queues are commonly implemented using binary heaps (e.g. with
the `std::..._heap` family of functions in C++).

## Interface
For a priority queue with items of type T and priorities of type P:

| Name     | Type           | Description                                      |
| -------- | -------------- | -----------------------------------------------  |
| size     | Size           | The number of items contained in the queue       |
| insert   | T ➝ P ➝ ()     | Insert an item and its associated priority       |
| increase | T ➝ P ➝ ()     | Increase the priority of an item                 |
| front    | T              | The item with the highest priority               |
| pop      | () ➝ ()        | Removes the item with the highest priority       |

## Performance
Note that n is the number of items in the priority queue.
With a binary heap-based implementation:

| Name            | Average Complexity |
| --------------- | ------------------ |
| \<memory used\> | O(n)               |
| size            | O(1)               |
| insert          | O(log n)           |
| increase        | O(log n)           |
| front           | O(1)               |
| pop             | O(log n)           |

Note that other heap-based implementations (e.g. Fibonacci heaps) can allow for
O(1) insertions and increases.

## Examples
- Prioritize network bandwidth to give certain kinds of traffic low latency.
- Implement Dijkstra's algorithm for finding the shortest distance between two
  nodes on a graph.
