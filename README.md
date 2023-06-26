# tic-tac-toe
C++ mini project (A tic-tac-toe AI program that never loses. This program uses the minimax algorithm with alpha-beta pruning to reduce the search space.)


Tic Tac Toe, also known as noughts and crosses, is a classic two-player game played on a grid consisting of 3 rows and 3 columns. It is commonly implemented in C++ as a console-based application. Here's a description of a typical implementation of Tic Tac Toe in C++:

The game starts by displaying an empty 3x3 grid on the console. Each cell of the grid is initially empty and represented by a symbol, such as a space or a dot. The players take turns to make their moves. One player is assigned the symbol "X" and the other player is assigned the symbol "O".

To make a move, the players enter the coordinates of the cell they want to mark. The row and column indices are typically numbered from 0 to 2. For example, the top-left cell is (0, 0), the middle cell is (1, 1), and the bottom-right cell is (2, 2). The program prompts the current player for their move and validates it to ensure it is a valid and unoccupied cell.

Once a player makes a move, their symbol is placed in the corresponding cell on the grid. The updated grid is then displayed on the console. The program checks if the current move results in a winning condition. A player wins if they have three of their symbols consecutively in a row, column, or diagonal. If a winning condition is detected, the game ends, and the program declares the winner.

If all the cells on the grid are filled and no winning condition is met, the game ends in a draw. The program detects a draw by checking if all cells are occupied.

After the game ends, the program gives the players the option to play again or exit the game. If they choose to play again, the grid is cleared, and a new game starts. If they choose to exit, the program terminates.

The implementation of Tic Tac Toe in C++ typically involves defining functions or classes to handle various aspects of the game, such as displaying the grid, validating moves, checking for a winning condition, and managing the game flow.

Overall, Tic Tac Toe in C++ is a simple yet enjoyable game that showcases basic programming concepts like input handling, data structures, conditional statements, and loops.
