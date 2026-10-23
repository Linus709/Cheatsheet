- pip install flask: for å laste ned flask
- python -m venv .filnavnjegbestemmer: lager et virtuelt miljø husk og gjøre det i mappen din
- pip list: viser hva jeg har lastet ned på pcen min 
- .filnavnpåvirtueltmiljø\Scripts\activate: shortcut for å starte virtuelle miljøet jeg har lagd
- from flask import Flask: alltid på toppen så flask er lasta ned i vscode
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
- loop explained:



    

