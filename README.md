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




A tic-tac-toe AI program that never loses. This program uses the minimax algorithm with alpha-beta pruning to reduce the search space.

Algorithm Details A minimax algorithm is a recursive algorithm for choosing the next move in an n-player game, usually a two-player, back and forth game. A value is associated with each position or state of the game. This value is computed by means of a position evaluation function and it indicates how good it would be for a player to reach that position. The player then makes the move that maximizes the minimum value of the position resulting from the opponent's possible following moves. If it is A's turn to move, A gives a value to each of his legal moves.

A simple version of the minimax algorithm, stated below, deals with games such as tic-tac-toe, where each player can win, lose, or draw. If player A can win in one move, his best move is that winning move. If player B knows that one move will lead to the situation where player A can win in one move, while another move will lead to the situation where player A can, at best, draw, then player B's best move is the one leading to a draw. Late in the game, it's easy to see what the "best" move is. The Minimax algorithm helps find the best move, by working backwards from the end of the game. At each step it assumes that player A is trying to maximize the chances of A winning, while on the next turn player B is trying to minimize the chances of A winning (i.e., to maximize B's own chances of winning).

Alpha–beta pruning is a search algorithm that seeks to decrease the number of nodes that are evaluated by the minimax algorithm in its search tree. This allows us to search much faster and even go into deeper levels in the game tree. It cuts off branches in the game tree which need not be searched because there already exists a better move available. The algorithm maintains two values, alpha and beta, which represent the maximum score that the maximizing player is assured of and the minimum score that the minimizing player is assured of respectively. Initially alpha is negative infinity and beta is positive infinity, i.e. both players start with their lowest possible score. It can happen that when choosing a certain branch of a certain node the minimum score that the minimizing player is assured of becomes less than the maximum score that the maximizing player is assured of (beta <= alpha). If this is the case, the parent node should not choose this node, because it will make the score for the parent node worse. Therefore, the other branches of the node do not have to be explored.

Pseudocode function minimax(node, depth, isMaximizingPlayer, alpha, beta):

if node is a leaf node :
    return value of the node

if isMaximizingPlayer :
    bestVal = -INFINITY 
    for each child node :
        value = minimax(node, depth+1, false, alpha, beta)
        bestVal = max( bestVal, value) 
        alpha = max( alpha, bestVal)
        if beta <= alpha:
            break
    return bestVal

else :
    bestVal = +INFINITY 
    for each child node :
        value = minimax(node, depth+1, true, alpha, beta)
        bestVal = min( bestVal, value) 
        beta = min( beta, bestVal)
        if beta <= alpha:
            break
    return bestVal
// Calling the function for the first time. minimax(0, 0, true, -INFINITY, +INFINITY)

Minimax Algorithm Visualisation

![image](https://github.com/akash16sh/tic-tac-toe/assets/88226545/f8077d78-bb13-47f1-9567-1ce26ce347f4)

