# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: Naked twins is a state where 2 grid boxes amongst peers contain the same digits. In this state we know that one of those two numbers must be the solution for each of the 2 grid boxes, and can't be the solutuion for any other peer of those grid boxes. We apply this contrain in the following manner:
- Loop through units to find unsolved boxes and their corresponding values
- Identify twins amongst unsolved boxes 
- Identify members of each unit which contain digits in common with identified twins and retrieve their values
- Eliminate those twin digits from the unit values.

This routine is then addded to the search function which executes a depth first search and propogates constraints defined by eliminate, only_choice, and naked_twins.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: The key to solve diagonal Sudoku wiht constraint propogation is to define the diagonal units and add those units to the unitlist.  Since our contraint propogation functions (eliminate, only_choice, naked_twins) and search function operate on or below the unit list level, this makes these units part of the contraint propogation and search operations.

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
