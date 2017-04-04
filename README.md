# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver
1. Implemented the "naked twins" function to solve the Sudoku
2. Modify the solution code from class to solve a diagonal Sudoku

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: naked twins are used to exclude possibilities in other squares(or boxes which are defined in the code), in the same group(or called peers which are defined in the  code). The constraint which is implemented in naked twins technique is there are no other alternatives for these two squares or boxes, because these two digit values in the squares or boxes have no other possibilities we can deduce. By eliminating these values from their peers, we can make one more step close to the solution. The main benefit of applying the constraint propagation using naked twins stragety is to reduce the search space.

The corresponding code is divided into two parts and implemented in the function called "naked-twins" in solution.py
1. find all the naked twins
2. eliminate the naked twins as possibilies for their peers

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: The main project framwork, or structure is built upon the materials from the class. I added one more list for diagonal into the unit list for the constraint to solve the diagonal suduko. I named it and defined it in code as diag-units as below: 
`diag_units = [[rows[i] + cols[i] for i in range(9)], [rows[::-1][i] + cols[i] for i in range(9)]]`

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.