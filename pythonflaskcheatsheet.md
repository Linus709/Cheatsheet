- PYTHON FLASK
- from flask import Flask: laster inn flask i koden så den er med og husk pip install flask at du har det lagra på fila.
- if __name__ == "__main__":
    app.run(debug=True)
    denne koden må du ha på bunnen hvis du vil kjøre nettsiden
- app = Flask(__name__): bare must for å få det til å fungere
- @app.route("/skrivhvaduvilherelleringenting")
def index():
    return ("yooo") 
    denne koden er ikke must men egentlig. her skriver du det som skal ende opp på nettsiden og ha flere av disse app routes hvis det skal være flere faner med information.


- templates: dette bruker vi for å kombinere html med python på nettsiden. foran return så kan du da skrive render_template('index.html') dette for å bruke html filen på nettsiden i app routes.
- from flask import Flask, render_template: hvis du skal ha templates med flask gjør det sånn på toppen!

- database: dette er lagringen til nettsiden den gjør så nettsiden husker. henter  også data, oppdaterer og sletter data.
- from flask_sqlalchemy import SQLAlchemy: dette laster ned en database som jeg kan bruke
- app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///kalldethvaduvil.db'
db = SQLAlchemy(app)
putt dette under flask name fordi dette gjør så jeg faktisk har en database på nettsiden.
-   

sql explained
- sql organize data to a tabell where columns contain attributes while each row consists of individual record of data. 
- The rows have there own uniqe id on the clomun that is the primary key. you could also have then a another id that would be the foreign id and example could be team id to represent which team you play for with help from primary key.
this is using sql in the smallets form it could be a much larger database
- important to remember is that sql is not only to read, recreate, update and delete data but also to combine data together
CODE USED FOR SQL
- SELECT and FORM: select can be used to ask for information from the table which the FROM code helps with. this to code have identifiers but you probably dont want every line
- WHERE: this code can be used to filter how many rows you want and this is like looping over every row in the table. 
- LEFT JOIN: this code can connect the data like example a person with a club which would be a primary key and foreign key look under how it could look
LEFT JOIN Teams ON players.team_id = Teams.id;
- this whole code would create a statement in the database
 


    

