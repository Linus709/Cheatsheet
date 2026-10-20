codes explantion
Step1
- import tkniter: imports/downloads tkniter in to my libary so i can use it in my library
- class hvaduvilher(tk.TK): lager en class som kalles det jeg vil for et spill, nettside eller noe annet
- self.title("dubestemmerhvasomstårher"): koden er for og gi tittel til spill, nettside, funksjon osv ofte i en class.
- self.cells = {}: oppretter en tom ordbok som brukes for og videre kode spillets knapper eller rutenett
- super().__init__():denne koden brukes for og intialisere klassen og betyr ofte at den arver fra noe eksempel tk.TK fra tictactoe spillet.

Step2
- display_frame = tk.Frame(master=self): lager en ramme inne i hovedvinduet(self)
- display_frame.pack(fill=tk.Y)plasserer rammen min i vinduet
- self.display = tkLabel(masse greier inne her): dette oppretter en widget og i mitt spill er det tk.Label og inne i self.display viser den ready? justerer litt skrift størrelse osv.
- self.display.pack(): denne sørger for at faktisk tekstvisningen blir visst på skjermen

step3
- grid_frame = tk.Frame(master=self): this code creates a frame to hold the grid of cells and it is set to master argument to self som betyr at den er main window.
- grid_frame.pack(): this code adds so the window like the code i am writing is visible

step4
- for row in range(3): this code is the outer loop like the outer code. So it decides the size like(weight and minisize) thats what i writed inside
- for col in range: this is the inner loop it has the inner code. in my code i have the font, color, width, height and a background and grid frame.
- button = tk.button(): this code makes the button and inside the parentheses there is code that customize the button like size, color, height, width and more.
- this outer and inner code run through numbers 0, 1 and 2 this creates a 9 by 9 suqare with positions like a tictactoe board.

step5
- self._cells[button] = (row, col): the code makes button as a key in a dictionary self._cells and locats it to a specific (row, col) cordinates. helps the program to track which button was clicked later on
- button.grid(): grid places the button on the screen in like a table layout and inside it the code sticky nsew means (north, south, east and west) makes the button expand fully in the grid.

step6
- self._create_board_display()
- self._create_board_grid()
- both these codes adds the to block with code that i have and makes them work when i run program i terminal

step7
- if __name__ == "__main__":this code is a must in every code so i can run it in the terminal 
    main()
and is always in the end of code.
- def main() in here i write the class and write mainloop so it doesnt stop when it runs. now i can run the program and see the tictactoe board.

step8 
- from typing import NamedTuple: This code is at the top and it imports something called NamedTuple that makes the game work
- class player(NamedTuple): this code player class contains a code to the text symbol representing the player which would be x or 0 since this is tictactoe. and color str makes the x red and 0 black since tictactoe
- class Move(NamedTuple): this class code contains cordinates to where the clicks can move like row cordinate grid (0, 1, 2) and column the same diagonal. and label marks the cell where i click

step9
- class TicTacToeGame: this class is like the brain of the game
- def __init__(self, players=DEFAULT_PLAYERS, board_size=BOARD-SIZE):this is the setup like sets deafult values in the start for who is x and o and how big the board is 
- self._players = cycle(players): this code uses the new tool i imported which is itertools and i makes so it loops with player x and o when turns change
- self.current_player = next(self._players): this code chooses who goes first from my cycled list
- self.winner_combo = []: this code keeps track on who wins gets three x or 0 in a row
- self.current_moves = []: this code makes the game remember the moves made so far
- self.has_winner = False: this code is a boolean which checks if the game has been won yet
- self.winning_combos = []: this predefines al combiantions of winning lines 
- self._setup_board(): this code calls for a method to intialize grid structure and tracking moves

step10
- board_size 3
  default_players=(): this code is setting x and o as red and blue because they were not defined yet so this code is used to define the player it could be something more complicated.

step11
- def _setup_board(self): we use this def to figure out the winning combos and how under her you under stand
- self._current_moves = []: track current moves in the game this is from the class tictactoegame
- inside self._current_moves: inside we use the older code with row and col so it knows how big the game is and the range and in the end self.board_size to be 100% sure it knows hoe big the map is.
- self._winning_combos = self._get_winning_combos(): this will confirm if you have won or not but i need to define this know so thats what i am going to do.

step12
- _get_winning_combos(self): in this code def it has the code under her and that is calculating every row with some code divs earlier made. 
rows = [
    [(move.row, move.col) for move in ror]
    for row in self._current_moves
]
- columns = [list(col) for col in zip(*rows)]: this unpacks all the rows and zip * is a trick to unzip all rows
- first_diagonal = [row[i] for i, row in enumerate(rows)]
  second_diagonal = [col[j] for j, col in enumerate(reversed(columns))]: this code is a little compicalted because it is calculating everything first diagonal grabs top left to bottom right (0,0) (1,1) (2,2) and the second is grabbing topright to bottom left 0,2 1,1 2,0 
- return rows + columns + [first_diagonal, second_diagonal]: this last combines everything i have coded to get all the winning combinations when a player makes a move know the game can easily check the winning combinations.

step13 
- def is_valid_move(Self,move): this code def checks if your move is legal in the game 
- row, col = move.row, move.col: 



#link til Virtual Environments toturial
#https://docs.python.org/3/tutorial/venv.html#tut-venv
#https://www.youtube.com/watch?v=QWjiHDJz10Q


#nettside til hvordan jeg kodet dette brukte nettsiden under.
#https://realpython.com/tic-tac-toe-python/#project-overview
#den forklarer hvordan alt funker og hvordan man lager tictactoe i python
"""tic-tac-toe game built with python and tkinter"""

