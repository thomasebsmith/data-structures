# Graph

## Description
A **graph** is an abstract data type that stores a set of possibly connected
vertices. Each vertex can have an associated value. Sometimes, edges have
associated values as well, but that case is not included in this description.

## Implementations
Graphs are commonly implemented using adjacency lists or adjacency matrices.

## Interface
For a graph containing items of type T with iterators of type I:

| Name      | Type           | Description                                     |
| --------  | -------------- | ----------------------------------------------  |
| vertices  | Size           | The number of vertices contained in the graph   |
| edges     | Size           | The number of edges in the graph                |
| adjacent  | I ➝ I ➝ Bool   | Tests whether two vertices are connected        |
| neighbors | I ➝ [I]        | Get all of the neighbors of a vertex            |
| insert    | T ➝  I         | Adds a vertex to the graph with no edges        |
| remove    | I ➝  ()        | Removes a vertex and its edges from the graph   |
| addEdge   | I ➝ I ➝ ()     | Adds an edge connecting two vertices            |
| eraseEdge | I ➝ I ➝ ()     | Removes an edge connecting two vertices         |

## Performance
Note that v is the number of vertices and e is the number of edges in the graph.

With a adjacency list-based implementation:

| Name            | Average Complexity |
| --------------- | ------------------ |
| \<memory used\> | O(v + e)           |
| vertices        | O(1)               |
| edges           | O(1)               |
| adjacent        | O(v)               |
| neighbors       | O(e)               |
| insert          | O(1)               |
| remove          | O(e)               |
| addEdge         | O(1)               |
| eraseEdge       | O(v)               |

With an adjacency matrix-based implementation:

| Name            | Average Complexity |
| --------------- | ------------------ |
| \<memory used\> | O(v²)              |
| vertices        | O(1)               |
| edges           | O(1)               |
| adjacent        | O(1)               |
| neighbors       | O(e)               |
| insert          | O(v²)              |
| remove          | O(v²)              |
| addEdge         | O(1)               |
| eraseEdge       | O(1)               |

Adjacency lists are generally more efficient for more sparse graphs, while
adjacency matrices are generally more efficient for more dense graphs.

## Examples
- Store the subway stops in a city and the number of passengers at each stop.
- Keep track of how computers are connected to one another in a large network.
