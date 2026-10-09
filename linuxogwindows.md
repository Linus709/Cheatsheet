# Linux
ofte lurt og kjøre disse to linjer først for og få siste programvare
- sudo apt update: finner oppdateringer i linux pi
- sudo apt upgrade: instalerer oppdateringer i linux pi
- sudo apt install git: versjonshåndterig og overføring av filer
- sudo apt install openssh-server: installerer ssh serveren
- sudo apt install ufw: en brannmur
- sudo ufw enable: for og skru på brannmur
- sudo ufw status: sjekker status på brannmur om den er på eller ikke
- ip a: sjekker netverks status
- ls: er det samme som dir bare i linux
- ls -a: viser skjulte filer på linux som eksempel ssh key
- systemctl status ssh: sjekker om windows og linux er tilkoblet sammen
- ping -c 3 8.8.8.8: sjekker om internett ditt funker ser du time og bytes er det bra
- ssh linus@ipadresseher: åpner windows husk riktig navn til enhet og ip addresse
- git clone git@github.com:Linus709/oppgaveigithubssh.git: kloner ssh key nettadresse på repo 
- nano: åpner opp github repo
-  sudo ufw allow 8080/tcp: åpner brannmur gir accses til localhost så nettside kan åpnes.
- ipconfig: Viser internett informasjon

PI login
- ssh linus@10.200.3.16

Linux terminal med pi
- sudo apt install python3-venv: Laster ned python på linux
- sudo apt install python3-pip: laster ned pip
-  python3 -m venv .prosjekt: lager virtuelt miljø på linux
- source .filnavndubestemmer/bin/activate
- pip install flask: laster ned flask 
- kontroll shift p i visualstudio code så skrive remote ssh conect ...: dette gjør så jeg kan jeg koble til rasperry pi på¨windows vscode
- hostname -I: viser ipadressen på rasp pi

Linux databaser med pi
- sudo ufw allow 5000/tcp: vil midlertidlig ikke la pi brannmur blokke connection
- sudo apt install mariadb-server: lager en server til min pi
- CREATE DATABASE flaskeDB;: lager en database inn i mariaddb server
- CREATE USER "linus"@"localhost" IDENTIFIED BY "1234";:Lager en bruker som har passord 1234 i server databasen
-  mariadb -u linus -p: dette kan jeg gjøre når jeg har lagd databsen for å gå enkelt inn og skrive inn passord jeg lagde.
- use flaskeDB;: det gjør så jeg bruker flask i databasen
- select * from flasketyper;: viser hva jeg har lagt inn i databasen tror jeg
- pip install mariadb: laster ned mariadb i linux
