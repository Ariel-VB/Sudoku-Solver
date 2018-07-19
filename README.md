# Sudoku Solver

A program to solve sudoku puzzles.

This program takes text files of 9x9 grids of numbers as input, where a 0 represents a blank square. See https://projecteuler.net/problem=96 for sample puzzles.

**Example input:** C:\\Users\\Ariel\\Python Workspace\\Sudoku1.txt

Currently, this solver consists of three functions:

**OnePossible():**

This function checks each section (rows, columns and boxes) to see if there are any squares that only have one possible number they could be. For example, if the row containing the square had the numbers 1 through 5, and the column containing the square had the numbers 6 through 8, this function would find that the only possible choice is 9. It would then make that move and update the puzzle as well as the options for each empty square.

**OnlyPossible():**

This function checks if a number can only be in one square within a section (row, column or box). For example, say there are 3 spaces left within a box. The possibilities for the first are 1, 2 and 3, and the possibilities for
both the second and third squares are 1 and 2. This algorithm would find that 3 is only possible in the first square, and perform that move.

**NakedGroups():**

This function checks if there are any groups of _n_ squares in a section (row, column, or box) that have the same _n_ options available. This is called a naked group. Then it removes these _n_ options from every other square in the section. For example, if the only options of two squares in a row are 1 and 2, we know that 1 and 2 must go in these squares and not any of the other squares in the row.
