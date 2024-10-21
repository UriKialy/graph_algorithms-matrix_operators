---

# Graph Algorithms & Operators in C++

This project focuses on graph algorithms and the manipulation of graphs using matrix (Mat) operators, where the graph is represented by an adjacency matrix. It also follows the requirement of using the `ariel` namespace as part of an assignment from my university.

## Algorithms

The following graph algorithms are implemented in the `Algorithms` class:

- **`isConnected(Graph& g)`**: Determines if the graph is connected. It returns 1 if connected, 0 otherwise.
  
- **`shortestPath(Graph& g, int start, int end)`**: Finds the shortest path between two vertices. If no path exists, it returns "-1"; otherwise, it returns the path as a string.

- **`isContainsCycle(Graph& g)`**: Checks if the graph contains a cycle. If a cycle is found, the cycle is returned as a string; if not, it returns "0".

- **`isBipartite(Graph& g)`**: Verifies if the graph is bipartite. If it is, it returns the bipartition; otherwise, it returns an empty string.

- **`negativeCycle(Graph& g)`**: Detects the presence of a negative cycle in the graph. If no negative cycle exists, it returns "no negative cycle".

## Operators (Mat Operators)

Since the graph is represented by an adjacency matrix, the following Mat operators manipulate the matrix directly to reflect changes in the graph structure:

- **Addition (`+`) and Subtraction (`-`) Operators**: These operators perform element-wise addition or subtraction on the adjacency matrices of two graphs. They are useful for combining two graphs or removing connections. Both graphs must have the same number of vertices, or an exception is thrown.

- **Multiplication (`*`) and Division (`/`) Operators**: These operators apply scalar multiplication or division to the adjacency matrix. For multiplication, each element in the matrix is scaled by a given factor, which can represent amplifying the weight of edges. For division, the elements of the matrix are divided by a scalar, which can reduce edge weights. Division by zero is not allowed and will raise an error.

- **Unary Minus (`-`) Operator**: This negates the weights of all edges in the adjacency matrix. It is useful for inverting the graph’s edge directions or weights.

- **Matrix Multiplication (`*`) Operator**: Multiplies the adjacency matrix of two graphs, which results in a matrix representing the paths of length 2 between nodes.

## Additional Operators

- **Transpose**: Creates a new graph with its adjacency matrix transposed, effectively reversing the direction of all edges.

- **Equality/Inequality (`==`, `!=`) Operators**: These compare two graphs based on their adjacency matrices, ensuring both have the same structure and edges.

- **Increment/Decrement (`++`, `--`) Operators**: These increase or decrease all the edge weights in the adjacency matrix by 1.

## Namespace

The project encapsulates its functionalities within the `ariel` namespace, which was part of a university assignment. The name `ariel` refers to the name of my university, ensuring all graph-related classes and functions are properly scoped.

## Compiling and Running

To compile the project, use the provided `Makefile`:

```bash
make
```

This will generate the executable `demo`. You can run the program using:

```bash
./demo
```

Alternatively, for testing, use:

```bash
./test
```

---
