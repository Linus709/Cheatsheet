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






#link til Virtual Environments toturial
#https://docs.python.org/3/tutorial/venv.html#tut-venv
#https://www.youtube.com/watch?v=QWjiHDJz10Q


#nettside til hvordan jeg kodet dette brukte nettsiden under.
#https://realpython.com/tic-tac-toe-python/#project-overview
#den forklarer hvordan alt funker og hvordan man lager tictactoe i python
"""tic-tac-toe game built with python and tkinter"""

