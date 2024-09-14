# Maze Generation and Solving Algorithms

This project contains Python implementations of various maze generation and solving algorithms, including 2D and 3D mazes. It explores different data structures and algorithms for creating and solving mazes, comparing their performance and scalability.

## Project Structure

- **Maze Generation:**
  - **Recursive Backtracking (2D & 3D):** Depth-first search (DFS) algorithm for generating perfect mazes.
  - **Prim's Algorithm (3D):** Algorithm that expands the maze by randomly selecting the lowest-cost neighboring cell.
  - **Wilson's Algorithm (3D):** Algorithm that guarantees all mazes are generated with equal probability.

- **Maze Solving:**
  - **Recursive Backtracking:** DFS-based approach to solve mazes.
  - **Wall-Following (2D & 3D):** A right-hand rule to traverse mazes.
  - **Pledge Algorithm (3D):** Extends wall-following by tracking angles to avoid infinite loops.

## Files

- `generation/`: Contains maze generation algorithms.
- `solving/`: Contains maze solving algorithms.
- `maze/`: Implements the data structures for representing 2D and 3D mazes.
- `sampleConfig0XTaskY.json`: JSON configuration files for testing different maze sizes and algorithms.
- `README.txt`: Instructions on how to run the code.

## How to Run

1. **Setup:**
   - Make sure you have Python 3.x installed.
   - Install the required libraries:
     ```
     pip install matplotlib
     pip install numpy
     ```

2. **Running the Maze Generator:**
   To run the maze generation algorithms:
   ```
   python generation/mazeTester.py --config sampleConfig01TaskA.json
   ```

3. **Running the Maze Solver:**
   To run the maze solving algorithms:
   ```
   python solving/solverSelector.py --config sampleConfig01TaskB.json
   ```

## Data Structures

This project implements two data structures for representing mazes:

- **Adjacency List:** Efficient for sparse mazes with fewer walls.
- **Adjacency Matrix:** More suitable for dense mazes but can be slow for large inputs due to its O(n^2) complexity.

## Experimental Results

The report includes a detailed comparison of the performance of these data structures based on execution time, memory usage, and scalability for different maze sizes (small, medium, and large).

## Conclusion

The adjacency list representation significantly outperforms the adjacency matrix for large mazes due to its optimized handling of sparse graphs. Recursive backtracking is efficient for small mazes, while Prim's and Wilson's algorithms offer better scalability for generating larger and more complex mazes.
