# matrix_path
## [Matrix Navigation System](https://pypi.org/project/matrix-path/)

This Python package contains a `Matrix` class that models a grid of cells, some of which are accessible (represented by "0") and some are walls (represented by "|"). A start point ("*") and an end point ("#") are also part of the matrix. The class provides functionality for navigating this matrix with movement methods: up, down, left, and right.

## Installation 
```shell
pip install matrix_path
```

## How to use?
```python
from matrix import Matrix

start_point = [0, 0]
end_point = [0, 4]
walls = [[0, 1], [1, 2]]
maze = Matrix(5, start_point, end_point, walls)
maze.print_matrix()
```

**Movement**

The `Matrix` class has four methods for moving around the matrix: `up()`, `down()`, `left()`, and `right()`. Each of these methods moves the current position in the respective direction by one step, if possible.

```python
from matrix import Matrix

# Initialize a 5x5 matrix with start point at (0,0), end point at (4,4), and walls at (2,2) and (3,3)
m = Matrix(5, (0,0), (4,4), [(2,2), (3,3)])

# Move up
m.up()

# Move down
m.down()

# Move left
m.left()

# Move right
m.right()
```

**Clearing Paths**

The clear_paths() method resets the matrix, removing all recorded paths ("1") and returning to the start point.
```python
m.clear_paths()  # Clear all paths and return to start
```


**Getting Matrix Elements and Matrix**

You can get individual elements of the matrix or the entire matrix by using the get_element(row, column) and get_matrix() methods, respectively.

```python
element = m.get_element(0, 0)  # Get the element at row 0, column 0
matrix = m.get_matrix()       # Get the entire matrix
```

## License
© 2020 Arush Sharma

This repository is licensed under the MIT license. See LICENSE for details.


