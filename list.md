# List

## Description
A **list** is an abstract data type that stores an ordered collection of items.
Any item can be accessed at any time, and the list can grow if more items need
to be added.

## Implementations
Lists are commonly implemented using arrays (e.g. `std::vector` in C++) or
linked lists (e.g. `std::list` in C++). In almost all use cases, arrays are much
more efficient.

## Interface
For a list containing items of type T with iterators of type I:

| Name     | Type           | Description                                      |
| -------- | -------------- | -----------------------------------------------  |
| size     | Size           | The number of items contained in the list        |
| append   | T ➝ ()         | Insert an item at the end of the list            |
| insert   | I ➝ T ➝ ()     | Insert an item before a given index in the list  |
| erase    | I ➝ ()         | Erase the item pointed to by an iterator         |
| get      | Size ➝ I       | Get an iterator to the value at a given index    |

## Performance
Note that n is the number of items in the list.
With an array implementation:

| Name            | Average Complexity |
| --------------- | ------------------ |
| \<memory used\> | O(n)               |
| size            | O(1)               |
| append          | O(1)               |
| insert          | O(n)               |
| erase           | O(n)               |
| get             | O(1)               |

With a doubly-linked list implementation:

| Name            | Average Complexity |
| --------------- | ------------------ |
| \<memory used\> | O(n)               |
| size            | O(1)               |
| append          | O(1)               |
| insert          | O(1)               |
| erase           | O(1)               |
| get             | O(n)               |

Note that because of caching and memory overhead, the linked list implementation
is almost always slower in practice (except when performing enormous numbers of
arbitrarily-located insertions and erases).

## Examples
- Store all the pixels in an image in memory.
- Keep track of all the people who have finished a race in order.
