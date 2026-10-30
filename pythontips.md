- pip install flask: for å laste ned flask
- python -m venv .filnavnjegbestemmer: lager et virtuelt miljø husk og gjøre det i mappen din
- pip list: viser hva jeg har lastet ned på pcen min 
- .filnavnpåvirtueltmiljø\Scripts\activate: shortcut for å starte virtuelle miljøet jeg har lagd
- from flask import Flask: alltid på toppen så flask er lasta ned i vscode

- PYTHON ENKELT FORKLART
- datatypes i python er
- integer = 2211     interger er bare hvilket som helst tall
- word = 'text'      strings er bare tekst
- decimal = -10.123 dette er en float brukes når tall har komma   
- cordinates = (2.5, 3.0, 1.0) kan inneholde 2 3 4 kordinater
- isHappy = false    dette kalles en boolean bare true or false
- example_list = ['luigi', 'mario', 'bowser']  dette er bare en list komando så når denne printes blir det navnene som printes ut i en liste
- uniqe{1,2,3,4,4,5} denne er unik altså den vil ikke printe samme tall altså duplicates i kode
- users = {"bob": 1, "james": 2} dette er dictonary og de er samlet sammen altså bob 1 og james 2



- eksempel av integer og strings sammen
integer = 2000
name = 'Mario'   
string_number = '11'  dette faktisk string også pga tegnene 
print(name + integer)   dette funker ikke
print(10 + int(string_number))  dette funker og konverter tallet til integer med plus 10 i starten.

- math in python
a = 10
b = 5

addition = a + b
difference = a - b
multiply = a * b
divide = a/b
power = a**b
if you print this it will do math
print(addition)   = 15 i terminalen

- if code and else/elif code function in python
age = 17
isHappy = false

if age > 21:                      
    print("you are old!")
elif age == 18:
    print("you are getting old!")
else:
    print("you are young!")

- samme med 
if isHappy:
    print("you are happy!)         true 
else:
    print("you are not happy!")    false

- loops forklart
for i in range(10):
    print("hello", i + 1)    i starter på 0 så hvis du vil at den skal starte på 1 gjør som koden
print(range(10))  denne vil printe ut   range(0, 10)    

- men du kan også gjøre dette med list

name_list = ['luigi', 'mario', 'bowser']
for name in name_list:
    print(name)      printer ut alle navn

- while loop forklart
  i er jo 0 og < det tegnet sier hvis i er mindre enn 5 så da er det false og den vil exite loopen og vise 1 2 3 4 5 i terminalen
i = 0

while i <5:
    i = i + 1 
    print(i)

- denne vil vise spørsmål så kan du skrive og hvis mindre enn 0 we are done here også stopper loopen

while True:
    user.input = input(("enter something))   
    if user_input == "0":
        print("we are done here.")
        break    stopper loopen denne koden vis ikke fortsetter den evig

- hvordan lage en function?
def say_hello(name):     mest brukt til å bare bruke koden din igjen
    print("hey there", name)       

say_hello("luigi") nå vil den vise hey there luigi
say_hello("mario") nå vil den vise hey there mario

- def kode i python

def get_internett():    hvis u kjører denne linjen vil du få en error fordi det er ikke noe inne i def 
    

def run_game():
pass 
denne linjen vil funke fordi den har pass og pass gjør at den aksepterer at det ikke er noe der

- def kode 2 i python
def greet(name: str, greeting: str) --> None:
    print(f"{greeting}, {name}!")

greet(name:"bob", greeting:"ciao")    når vi kjører denne koden vil vi få greeting og name til ¨å funke som funksjon og få ciao bob i terminalen


- def kode 3 
def greet(name: str, greeting: str = "hi") --> None:
print(f"{greeting}, {name}!")

greet(name:"bob", greeting:"ciao") 
greet("james" )
greet("bob")
denne koden vil istendfor det andre vise hi james og hi bob hvis du ønsker og definere stringen på funksjonen

- number
number = input("please provide your number >> ") lar deg skrive

try:
    print(10 + int(number))   når du har skrevet og det er nummer så plusser den på 10 hvis ikke går den ned
except:
    print("that is not a valid number")  du skrev tekst så ikke valid

- sjekke verdier bolean egentlig

a: int = 1
b: int = 2

print(1 > 2)   false    > more  < less == equal  <= less and more
print(1 >= 2)  false

- exeption code
a, b = 10 "fifteen"

try:
    print(a + b)
except exepction as e:
    print("please enter a valid number")   

print("continuing with the program...")
denne koden vil vise begge setningene på print også vi

- importing
import math
import math as m   gjør så du slipper å skrive math
from math impoty sqrt, tan     hvis man vil være spesefik og du kan adde flere

print(math.etterpunktummassegreier) under eksempel
print(math.sqrt(3)) vis man kjører denne får man squere root
print(m.sqrt(3)) her trenger du nå bare og skrive m
print(sqrt(3)) nå trenger jeg bare og skrive squere root pga spesefik import kode
print(tan(2)) flere fra spesefik import







koder

- render_template: templates gjør så jeg kan redigere nettsider med html og ikke bare ha hello world
- class skrivhvaduvilher(skrivhvilkenimporther):: dette er koden for og lage en class som er på måte sjefen over hele koden hva det du har under skal være er det class burde hete. også huske og spesifisere hvilke import jeg bruker i classen jeg skriver kode i.
- def _eksempel_det_her(self): dette legges på under en def for og videre utvikle noe du lager som et spill, nettside, funksjon osv. men må ikke være en kode fra class kan stå hva som helst foran def så lenge det er under classen.
- if __name__ == "__main__":
    main()    :Denne koden må du alltid ha i slutten av en python kode så jeg kan kjøre den i terminalen så den får med alt jeg har skrev se videre under hvordan
- def main(): her kan du få med classene under så main matcher med greia nederst så du får kjørt koden eksempel spill så vil du gjøre dette så ikke spillet stopper eksempel under
def main()
    board = dettekanværeclass()
    board = blablabla()
    board = kanværemange()
    #denneunderhererikkemustbarehvisjegønskeratdenikkeskalstoppeførjegvilsometspill
    board.mainloop()
- import flask: imports skal ALLTID være på toppen så koden under får imported greiene!
- integer: tall i python
- string: bokstaver i python
- index: et tall som viser plasseringen til et element i en liste, string, integers osv.
- brackets: det er parantesene/klammene i eksempel en liste eller kode linjer generelt

arrays

- herskriverduarray.append(detduvilappende): append legger til noe i slutten av din kode så ser sånn ut under her
frukter = ["eple", "banan"]
frukter.append("appelsin")
print(frukter)  # ['eple', 'banan', 'appelsin']
- return hvasomhelsther: dette vil sende det du skriver foran return i verdi tilbake så ender opp i output/returnvalue. eksempel hvis linus=16 så vil return linus gi 16. denne koden sender verdien også videre i koden så du kan skrive mer
- for i in range(bestemmtallellerverdi): denne får en loop/løkke til å skje så her kan du putte apend under for og få en ordetnlig løkke. i bokstaven i koden er index for liksom talla du henter fra som den skal starte på eksempel under.
class Solution:
    def shuffle(self, nums: List[int], n: int) -> List[int]:
        answer = []
        for i in range(n):
            answer.append(nums[i])
            answer.append(nums[i + n])
        return answer
- if funksjonsnavn >= endaetfunksjonsnavn: if funksjoen fungerer sånn at hvis det skjer en økning eksempel så vil pengene gå opp sånn kan if funksjonen funke. så det du skriver i midten av tegn definerer om det er høyere lavere eller =.
- elif: denne funksjonen er akkurat som if bare den neste dørvakten kan man si. den sjekker en ny betingelse bare hvis den forrige betingelsen var usann
- else: denne komandoen er vanligst og putte på slutten så hvis ingen av if eller elif betingelsene stemte vil else brukes eksempel under
if temperatur > 25:
    print("Det er kjempevarmt!")
elif temperatur > 10:
    print("Det er mildt ute.")
elif temperatur > 0:
    print("Det er kaldt, husk jakke.")
else:
    print("Det er minusgrader!") 
- n = len(navneher): dette er en funksjon som finner ut hvor mange tall som skal være der liste.
- counter = counter(navnher): denne koden lager en oversikt over tallene

METHOD POST AND GET
GET: The get method requests for data and retrives data from a server/database/templates. 
POST: Post is used to send data to a server/website/database/osv. it also is used to delete, update, create and like submitting a login form. 








