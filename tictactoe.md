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
- row, col = move.row, move.col: thid code reveals/unpacks the the numbers for row and column so i can click were i want to
- move_was_not_played = self._current_moves[row][col].label == "": this code just checks were you clicked that there is not a x or o there so the game doesnt bug
- no_winner = not self.has_winner: this is the last code and it is just cheking if the game is over og still going on also so the game doesnt bug.
return no_winner and move_was_not_played: just confirming so code understands and game moves on or ends.

step14
- def process_move(self, move): this code def code is to check if anyone have won the game when there is no more places to click.
- row, col = move.row, move.col: this code is just to get the cordinates from input move 
- self._current_moves[row][col] = move: this code just checks makes sure so the game remebers the clicks that have been made
- for combo in self._winning_combos:this code just takes a loop to check all wining combinations from last step.
-  self._current_moves[n][m].label
|   for n, m in combo: this code just loops through every avaible click also the code under
- is_win = (len(results) == 1) and ("" not in results): this code and under just checks if you have won if true loop breaks or not 

step15
- def has_winner(self):
    retuen self._has_winner: this just code just checks if anyone have won drawn or lost 

step16
- def is_tied(self): before this def it checked that there was no winner yet so then it moves to this so its a draw.
- no_winner = not self._has_winner: this code just makes it true if there is no winner. 
- played_moves(): this code goes through every row and checks 100% that its a draw
- move.label for row in self._current_moves for move in row: this is the code that does it over
- return no_winner and all(played_moves): this code only returnts true if no one have won and it is checked all rows that everything has been clicked and it is a draw. 

step17
def toggle_player(self)
    self.current_player = next(self._players): this code toggles player and allows the next to click when one has clicked  

step18
- def play(self, event): this code is the def and play the event the game basically 
- clicked_btn = event.widget: this code makes it possible to click from other codes
- row, col = self._cells[clicked_btn]: goes over the whole 3 by 3 board for clicks then goes to next code
-  move = move(row, col, self._game.current_player.label): sjekker hvem sin tur det
- if self._game.is_valid_move(move): denne sjekker om move som ble gjort er valid
- self._update_button(clicked_btn): hvis move var valid så oppdaterer den og lar neste klikke
- self._game_process_move(move): denne får alt dette til å kjøre på nytt så når alle ruter er klikket går den videre 
- if self._game.is_tied():: så skriver jeg hvis game er tied skjer det under i koden ganske simpelt
    self._update_display(msg="TIED GAME!", color="red")
- elif self._game.has_winner(): and if it is not tied then there is a winner so then it says the code under current player WON! står det på skjerm altså WON!
self._highlight_cells()
msg = f'Player "{self._game.current_player.label}" WON!'
color = self._game.current_player.color
self._update_display(msg, color)
- else: self._game.toggle_player(): hvis ingen har vunnet enda eller uavgjort begynner denne koden og fortsetter spillet videre og denne koden bytter turen mellom x og o
msg = f"{self._game.current_player.label}'s "
self._update_display(msg)
og denne over her oppdaterer displayet til hvem sin tur det er

step19
button.bind("<ButtonPress-1", self.play): denne koden fungerer sånn at alle rutene reagerer/følger med hvis man museklikker på de og sender også spillet videre til playfunksjoen.

step20
- def _update_button(self, clicked_btn):this def is making so when you click in a box it actually is a x with the color red 
- clicked_btn.config(text=self._game.current_player.label): dette er koden som setter x eller o for hvilken player du er
- clicked_btn.config(fg=self._game_current_player.color):dette er koden som setter fargen for x eller o når du trykker i en rute

step21 
- def _update_display(self, msg, color="black"):: this def is just the code to tweak the color and style for the display with boxes.
- self.disply["text"] = msg: denne kode linjen endrer teksten som vises på skjermen
- self.display["fg"] = color: denne kode linjen endrer bare tekst fargen på displayet. fg st¨år for foreground betyr i programering tekstfarge.

step22
- def _highlight_cells(self): denne def koden gjør så når du får winner combo vinner du og får highlight bakgrunn i rød
- for button, coordinates in self._cells.items():
if coordinates in self._game.winner_combo:: denne koden bare sjekker hvis du har vunnet så skjer dette under
- button.config(highlightbackground="red"): highlighter det rødt og blir rødt


#link til Virtual Environments toturial
#https://docs.python.org/3/tutorial/venv.html#tut-venv
#https://www.youtube.com/watch?v=QWjiHDJz10Q


#nettside til hvordan jeg kodet dette brukte nettsiden under.
#https://realpython.com/tic-tac-toe-python/#project-overview
#den forklarer hvordan alt funker og hvordan man lager tictactoe i python
"""tic-tac-toe game built with python and tkinter"""

