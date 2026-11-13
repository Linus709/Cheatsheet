Komandoer i SELECT
SELECT *: velger alle
SELECT id: velger bestemt id
SEEECT tittel, sjanger, pris:denne betyr at du kan velge det du vil og hente det fra tabellen.
FROM i komandoer
FROM tabellnavn: from er hvilken tabell vi vil ha informasjon fra
WHERE i komandoer filtrering
WHERE id = 20: dette spesifiserer id i kolonnen og velge id som er lik 20
EKSEMPEL AV HEL KOMANDO AV ALT DETTE
SELECT * FROM spill
WHERE ÅR = 2023
skriver ut fifa 24

SELECT sjanger, pris FROM spill

SELECT * FROM spill
WHERE ar > 2015 

mariadb TERMINAL
mariadb -u root -p: 

mer komandoer
CREATE DATABASE TABELLNAVNHER; denne lager databasen inne i useren på mariadb
USE TABELLNAVNHER; denne intialiserer databasen med tabellen



LINUX:

hvordan få mariadb på linux/pi-en min
- sudo apt update: viktig og kjøre først
- sudo apt install mariadb-server: laster ned mariadb server
- sudo apt install mariadb-client: (Kun hvis du vil bruke grensesnittet på pi)
- sudo systemctl start mariadb: starter system server
- sudo systemctl enable mariadb: enabler system server
- sudo mariadb: starter altså får meg inn i mariadb
