# fish-game
README.txt

Overview/description of the overall structure of the program:

-The initial board gets printed and the user is prompted to enter input. The player and AI are initially randomly assigned to the board. 
-The player's input is scanned, the direction and step are determined and then the isValid() function is called to check whther the input is valid.
-The board is then updated with the new move.
-The AI plays next, the aiMove() function is called, which computes the max possible score which can be achieved and the direction 
 in which it would do so. This function traverses all 8 directions, keeps track of the maxNum, steps and direction. 
-The updateBoardAI() function is called next which updates the board with the calculated move.
-The game keeps alternating till either one of the player or AI dont have any moves left. At that point, the other one moves till the game ends.
-Track of points is kept using a struct for both the player and the AI. The initPlayer() and initAI() structs are used for this. 
-The checkGameOverForAI() and checkGameOverForPlayer() functions check whether the Player or AI have any moves left and ends the game if 
 both of the dont have any moves left. 
-Then the points are compared and the winner is decided.
Constructed a game board using pointers and a layered score system with movements allowed in 8 possible directions.
Constructed an AI to play against the player at alternate turns. Implemented structs to track scores and some other functions to check validity, update board, track points, possible moves and end game. 
 


Explains how to use pointers to construct the board:

-Every character stores the referance to the memory address of the next character in the different directions using pointers.
-8 direction functions are used namely up, down, left, right, donwLeft, downRight, upLeft and upRight. 
-After the board is initialized using the initBoard() function, the 8 direction functions link every character in the 
fishBoard with their adjacent characters in all the directions. 
-There are conditions to make sure that the elements which are leftmost on the board don't use left pointers and similarly for up,
down and right directions.

Explains how to implement the AI:

-The aiMove() function uses maxNum to store the maximum possible char value, maxDir to store the maximum possible direction and Maxstep 
to store the number of steps. A for loop computes the existing AI position.
-This function traverses the fishBoard in all directions from the existing AI position and keeps track of the maximum char value encountered.
-While traversing the fishBoard, the isValid() method is called to make sure that the move is valid. 
-The best possible move is calculated after traversing all the 8 directions and then the updateBoardAI() function is called. 
-This function updates the calculated best place with the char 'A' and the earlier position of the AI with a '.'
-The updated board is printed.
