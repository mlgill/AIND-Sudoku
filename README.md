# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: The function `naked_twins` iterates through each group in unitlist and looks for two cells that contain exactly the same two possible assignments. These are naked twins. Once found, the two possible assignments are removed from all other cells within the same group. 

The `naked_twins` function has been incorporated into the recursive search function which also reduces the puzzle and attempts to solve it.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: A list of diagonal constraints were created using the following code:

> ```diagonal_units = [[''.join(x) for x in list(zip(rows, cols))],
                  [''.join(x) for x in list(zip(rows, cols[::-1]))]]```

This code creates the following sets of constraints:

> ```[['A1', 'B2', 'C3', 'D4', 'E5', 'F6', 'G7', 'H8', 'I9'],  
      ['A9', 'B8', 'C7', 'D6', 'E5', 'F4', 'G3', 'H2', 'I1']]```
      
These constraints were then added to `unitlist`, which is the master list of constraints. The modular nature of the constraint setup code makes it easy to modify constraints for different situations.

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