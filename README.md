# Hexapawn
This is a Python implementation of [Martin Gardner's game
Hexapawn](http://www.cs.williams.edu/~freund/cs136-073/GardnerHexapawn.pdf),
which was designed to be solved by a very simple type of AI implemented with
matchboxes.

https://www.instructables.com/id/Matchbox-Mini-Chess-Learning-Machine/

## Game overview
There are three pawns of two colours on a 3x3 board. 

There are two legal moves: 
- move a pawn straight forward, or 
- move a pawn diagonally left or right to capture an enemy pawn, which is
  removed from the board.

Players alternate taking turns until one of three end conditions is achieved: 
- a pawn advances to the third row, 
- all enemy pawns are captured, or
- a position is achieved in which the enemy has no legal moves.

In the PDF, the game is simplified somewhat by requiring that the robot go
second and that the player's first move be only the left or centre pawn, since
the right pawn would produce a mirrored sequences of moves to the left pawn.

For each move the robot can make, there is a match box depicting the current
state of the board, with coloured arrows showing the possible transitions to the
next state. There is a coloured bead in the box for each of the coloured arrows
on the box. Choosing the next move is done by randomly selecting a bead from the
box.

If the machine loses the game, it is punished by having the bead for the last
move it made taken away, so that it cannot play that move again.

A variation is to add a bead of the proper colour to each box when the machine
wins.

A similar type of machine can be built to play
[nim](https://en.wikipedia.org/wiki/Nim).


