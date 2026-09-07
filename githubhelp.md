# windows
Github guide to push files from terminal to github

First time making repo and pushing files into it

First 
- cd filnavn: Først må du få deg inn i mappen du skal pushe inn i github med cd command

lage lokalt reopsitory
- git init
- git add .: Add all your project files to staging
- git commit -m "initial commit": Create your first commit

koble sammen lokalt repo med github repo
- git branch -M main: Rename your default branch to 'main'
- git remote add origin PASTE_YOUR_COPIED_URL_HERE: Link your local folder to your online GitHub

Siste kode pushe filene inn til github repo
- git push -u origin main: Push your files and set the default upstream branch

vanlig bruk etter oppsett av repo(altså oppdatere endringer osv)
- git pull
- git add .
- git commit -m "skriv noe her"
- git push

