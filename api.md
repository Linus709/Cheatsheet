- API greier første gang 
- response = requests.post(url, formatet.skriv.hereksjson={'query': query}, headers=headers): dette sender forespørsel til en server jeg henter api fra og endre den til det som passer til min api
- if response.status_code == 200:

- eks data =  repsonse.her.skriver.du.formatet.fra.kode.api(): sørger for så formatet vil funke 

- eks print("svar fra nettsidejeghentaapifra):
 svar når du kjører koden ekstra 

- så  print(data):
 printer ut teksten over og data

- import requests: dette henter vi inni python bibloteket brukes for å sende forespørseler til nettsider/apier. husk dette må være instalert pip install blabla

- url = blabla: hit skal python sende melding og få informasjon

- headers = {....}: nettsider/apier krever ofte hvem jeg er så skriv inn regel og veriden kan jeg kalle hva jeg vil eksempel her under
headers = {
    "ET-Client-Name": "mitt-skoleprosjekt-app"
}

- query """ """: de tre hermetegnene skal være på slutten og starten og brukes i python for å lage en tekststreng som går over flere linjer!! funker ikke til alt tror jeg.

- response = requests.post(): her skjer selve magien for og få alt til ¨å funke. 
Vi sender med tre ting: url-en (hvor den skal), json={'query': query} (selve reisebestillingen vår i et format serveren forstår), og headers (hvem vi er).

- if response .status_code 200: status 200 betyr at alt er OK og hvis det står 404 finnes ikke nettside og 400/500 betyr ofte feil i koden eller feil med server.

- response.json()gjør om rå tekst behandlingen til vi fikk fra serveren til et ekte python format eller ordliste enklere.
- print(): veldig viktig så faktsik vi skriver ut hele resultatet i terminal

