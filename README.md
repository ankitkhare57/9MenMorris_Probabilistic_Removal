**`Code Dependencies Required:`**
`Import copy`
`Import sys`
`Import random`

**`Steps to run the Project:`**
1. `Download repository`
2. `Make sure the required dependencies are installed.`
3. `Run human_vs_human.py`
4. `Follow on-screen prompts.`

**`Procedure Descriptions:`**

***`def printBoard(board):`***
**`Input: Board list`**
**`Output: Prints the current state of the board `**

***`def adjacentLocations(position):`***
**`Input: Position of the player `**
**`Output: Returns an array of the adjacent positions for the input position `**
**`Description: It has an array which has precalculated adjacent positions for each position, the index of the array is the position.`**

***`def isPlayer(player, board, p1, p2):`***
**`Input: Current Player, Current board, two positions`**
**`Output: Boolean value`**
**`Description: This is a helper function for checkNextMill(), this function takes the current board and player and checks if both the positions have that same player on them.`**
`    `
***`def checkNextMill(position, board, player):`***
**`Input: Position to be placed, Current board, Current Player `**
**`Output: Boolean Value`**
**`Description: The function checks if the player can make a mill (3 pieces in a row) in with the move `**

***`def isMill(position, board):`***
**`Input: Current position, Current board`**
**`Output: Boolean Value`**
`This function checks if the current position is a part of a mill or not `

***`def numOfPieces(board, value):`***
**`Input: Current board, player`**
**`Output: Integer value `**
**`Description: This function counts the number of pieces of a player on the board. `**

***`def allIsMill(board, player):`***
**`Input: Current board, player`**
**`Output: Boolean Value`**
**`Description: This function checks if all the pieces for a certain player are only mills so that it can be removed by the opponent if the opponent forms a mill.`**
`    `
***`def removePiece(board_copy, board_list, player):`***
**`Input: Copy of the board, Current board, Current player `**
**`Output: Updated board (board_list)`**
**`Description: This function updates the board by removing the piece, checks that if the opponent piece is a part of a mill or not if it is removed fails or else it passes and then the board is updated.                `**

***`def possibleMoves_stage2(board, player):`***
**`Input: Current Board, Current Player`**
**`Output: board_list`**
**`Description: This function takes the current board and the current player; it checks what are the adjacent positions and the valid positions. After which it puts an x in place of the current position and then updates the new position and then checks if it forms a mill. If it does it goes for the removal of the opponent's piece. `**

***`def possibleMoves_stage3(board, player):`***
**`Input: Current Board, Current Player`**
**`Output: board_list `**
**`Description: This function puts an x to all the empty positions other than the opponent’s pieces as possible positions for the current player. It also checks if the current piece is forming a mill. If it forms a mill then it asks which of the opponent’s pieces has to be removed and removes it. If a mill is not formed then just updates the board.`**
`This function handles a special stage called the flying stage. In this when one of the players has only 3 pieces remaining they can not only move their pieces to adjacent positions but also to any position available on the board.`

***`def possibleMoves_stage2or3(board, player='1'):`***
**`Input: Current board and Current player`**
**`Output: Which stage to go ahead with depending on the number of players`**
**`Description: Checks if the number of pieces of a player is 3 then go for stage 3 else go for stage 2. This is done by calling that function for the possible moves respectively (possibleMoves_stage3() or possibleMoves_stage2())`**

***`def human_vs_human():`***
**`Description: This is the main function that uses all the above functions to implement the game. Here the probability of failing to remove an opponent's piece after forming a mill is 25% of the time. This is decided by the variable “ans” in the code.`**