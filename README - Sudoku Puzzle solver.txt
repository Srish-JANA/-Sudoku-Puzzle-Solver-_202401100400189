README - Sudoku Puzzle solver 
-----------------------------------------------------------------------------------

## Introduction
This is a Python-based Sudoku solver that utilizes the BACKTRACKING ALGORITHM to find a solution for a given 9x9 Sudoku puzzle. The solver efficiently places numbers in empty cells while ensuring they follow Sudoku rules.

## Features
- Automatically finds the solution to a Sudoku puzzle (if solvable)
- Uses backtracking for efficient solving
- Validates each number placement based on Sudoku constraints
- Outputs the solved grid in a readable format

## How It Works
1. Find an Empty Cell: The program scans the grid for the first available empty space (denoted by `0`).
2. Check Validity: It tries numbers `1-9` in that position and checks whether they satisfy Sudoku rules:
   - The number must not exist in the same row.
   - The number must not exist in the same column.
   - The number must not exist in the 3x3 sub-grid.
3.RECURSIVE BACKTRACKING: If a valid number is placed, the program recursively attempts to solve the remaining empty cells. If an incorrect placement is detected later, it BACKTRACKS and tries the next possible number.
4. Solution Found: Once all empty cells are filled correctly, the solved Sudoku grid is displayed.

## Code Structure
- find_empty_location(grid): Finds the next empty position (cell containing `0`).
- is_valid_placement(grid, row, col, num): Checks if placing num at (row, col) is valid.
- solve_sudoku(grid): Main function that implements BACKTRACKING to solve the Sudoku puzzle.

## Usage
1. Install Python (if not installed).
2. Copy and paste the code into a Python file, e.g., `sudoku_solver.py`.
3. Replace the grid variable with your unsolved Sudoku puzzle.
4. Run the script: python sudoku_solver.py
5. If the puzzle is solvable, the program will print the completed Sudoku grid.

## Example Input
grid = [
    [0, 0, 0, 6, 0, 0, 0, 0, 3],
    [0, 6, 0, 0, 3, 0, 0, 8, 0],
    [0, 0, 9, 0, 0, 0, 5, 0, 0],
    [5, 0, 0, 0, 8, 0, 0, 0, 6],
    [0, 0, 3, 0, 0, 0, 7, 0, 0],
    [8, 0, 0, 0, 4, 0, 0, 0, 1],
    [0, 0, 6, 0, 0, 0, 9, 0, 0],
    [0, 3, 0, 0, 6, 0, 0, 1, 0],
    [9, 0, 0, 0, 0, 4, 0, 0, 0]
]
## Example Output
[4, 5, 8, 6, 9, 7, 1, 2, 3]
[7, 6, 1, 5, 3, 2, 4, 8, 9]
[2, 3, 9, 1, 8, 4, 5, 6, 7]
[5, 7, 4, 9, 8, 1, 2, 3, 6]
[6, 1, 3, 2, 5, 9, 7, 4, 8]
[8, 9, 2, 7, 4, 3, 6, 5, 1]
[1, 4, 6, 3, 7, 5, 9, 8, 2]
[3, 8, 5, 4, 6, 9, 1, 7, 9]
[9, 2, 7, 8, 1, 4, 3, 5, 6]

## Limitations
- Only solves standard 9x9 Sudoku grids.
- Does not handle multiple solutions (it finds the first valid one).
- Performance may degrade for highly complex puzzles.

## Possible Enhancements
- Improve efficiency using constraint propagation.
- Support for multiple solutions.
- GUI-based Sudoku solver.

## License
This project is open-source and free to use. Feel free to modify and improve it!

Author
Srish Jana

