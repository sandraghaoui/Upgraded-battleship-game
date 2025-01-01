This Project contains:
-Overall.c which is the file that should be ran, other files except weapons are here for reading purposes
-A main method (Main)
-A twoPlayer method
-easy, Medium and Hard which are the 3 difficulties of the single player fucntion
-Methods file, which contain every helper method that is not a weapon
-weapons file, containing weapon methods

Game details:

Ships: Each player has a fleet of ships that vary in size and number. This fleet includes:
(a) 1 Carrier (5 cells)
(b) 1 Battleship (4 cells)
(c) 1 Destroyer (3 cells)
(d) 1 Submarine (2 cells)
- Objective: To sink all of the opponent's ships.

Gameplay:
Players take turns performing a single move per turn. At the beginning of each turn, the program
should display the updated game grid of the current player's opponent, followed by the list of
available moves. The program then asks the current player (using the player's name) for
their choice and receive the player's move as an input. The list of possible moves are:

1. Fire: The basic action where a player tries to hit an opponent's ship by guessing a coordinate.
Command structure: Fire [coordinate]. Example: Fire B3
Command output: Either hit or miss

2. Radar Sweep: Reveals whether there are any opponent ships in a specified 2x2 area of the
grid without showing exact locations of ships.
Command structure: Radar [top-left coordinate]. Example: Radar B3 reveals whether there
are any opponent ships in cells B3, C3, B4, C4
Command output: Either Enemy ships found or No enemy ships found.
Note that every player is allowed 3 radar sweeps per the entire game. If a player attempts to
perform more than 3 sweeps, they lose their turn.

3. Smoke Screen: Obscures a 2x2 area of the grid by hiding it from radar sweeps.
Command structure: Smoke [top-left coordinate]. Example: Smoke B3 obscures whether there
are ships in cells B3, C3, B4, C4, such that if the opponent later on performs a radar sweep
that touches any of these cells, it would count them as misses regardless of whether or not
ships resided in them.
Note that players are allowed one smoke screen per ship they have sunk. If a player attempts
to perform more than their allowed limit, they lose their turn. (For example, a player who
has sunk three ships so far and has only performed one smoke screen, can still be allowed to
perform two more smoke screens).
Also note that if the player performs a smoke screen move, the program clears the
current screen to preserve the secrecy of the move.

4. Artillery: An attack move that works similarly to Fire but targets a 2x2 area.
Command structure: Artillery [top-left coordinate]. Example: Artillery B3 will hit any ships
in cells B3, C3, B4, C4
Command output: Either hit or miss.
Condition: this move is unlocked only once during the next turn of the player who sinks the
other player's ship in the current turn.
5. Torpedo: A powerful attack that targets an entire row or column.
Command structure: Torpedo [row/column]. Example: Torpedo B will hit any ships in column
B
Command output: Either hit or miss
Condition: this move is unlocked only once during the next turn of the player who sinks the
other player's third ship in the current turn.
