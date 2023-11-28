#Project Overview:

The Island Perimeter coding challenge is a problem where you're given a 2D grid representing an island, and you need to calculate the perimeter of the island. The island is represented by '1's, and the water is represented by '0's. The goal is to find the total perimeter of the island, where each cell contributes to the perimeter based on its surroundings.

Here's a brief overview of the problem and the typical approach to solving it:

### Problem Description:

Given a 2D grid of 0's and 1's, where 1 represents land and 0 represents water, calculate the total perimeter of the island. The island is surrounded by water on all sides, and the perimeter is determined by how many sides of a land cell are exposed to water.

### Example:

```plaintext
Input:
[
  [0, 1, 0, 0],
  [1, 1, 1, 0],
  [0, 1, 0, 0],
  [1, 1, 0, 0]
]

Output: 16
```

### Approach:

1. **Iterate Through the Grid:**
   Traverse each cell in the grid.

2. **Calculate Perimeter for Each Land Cell:**
   For each land cell ('1'), check its surroundings (top, bottom, left, and right). If there is water ('0') in any direction or if the cell is at the boundary of the grid, increment the perimeter by 1.

3. **Calculate Total Perimeter:**
   Accumulate the perimeter for all land cells to find the total perimeter of the island.

### Example Walkthrough:

Consider the example grid:

```plaintext
[
  [0, 1, 0, 0],
  [1, 1, 1, 0],
  [0, 1, 0, 0],
  [1, 1, 0, 0]
]
```

1. For the first land cell at `(1, 1)`, there are water cells in the top and left directions, so the perimeter is 3.

2. For the second land cell at `(1, 2)`, there is water on the top and right, so the perimeter is 3.

3. Proceed similarly for all land cells, and accumulate the perimeters to get the total perimeter of the island.

### Implementation:

The problem can be solved using a simple nested loop to iterate through the grid and a conditional statement to calculate the perimeter for each land cell.

### Summary:

The Island Perimeter coding challenge tests your ability to navigate a 2D grid and calculate the perimeter based on the conditions specified in the problem. It's a good exercise in understanding array manipulation, conditional logic, and problem-solving. The key is to identify the rules for calculating the perimeter and implement a solution that efficiently covers all land cells in the given grid.

# Island Perimeter

This project contains interview coding challenges.

## Tasks To Complete

+ [x] 0. **Island Perimeter**<br/>[0-island_perimeter.py](0-island_perimeter.py) contains a module with a function having the prototype `function def island_perimeter(grid):`, which returns the perimeter of the island described in `grid`, with the following requirements:
  + `grid` is a list of list of integers:
    + 0 represents water.
    + 1 represents land.
    + Each cell is square, with a side length of 1.
    + Cells are connected horizontally/vertically (not diagonally).
    + `grid` is rectangular, with its width and height not exceeding 100.
  + The grid is completely surrounded by water.
  + There is only one island (or nothing).
  + The island doesn't have "lakes' (water inside that isn't connected to the water surrounding the island).
