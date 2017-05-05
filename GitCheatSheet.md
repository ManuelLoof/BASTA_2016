

# Git Cheat Sheet #

## Basics ##

    git Init

Initialisiert ein neues Git Repository.

    git add name
    git add *

Fügt Dateien dem Repository hinzu.

    git commit -m "Comment"

Check die Daten ein.

    git config color.ui true

Farbige Konsolenausgabe.

    git clone Verzeichnis

Holt sich ein Repository vom Server und legt eine lokale
Arbeitskopie an.

    git remote add origin https://github.com/ManuelLoof/BASTA_2016.git
    git push -u origin master

Logt sich auf GitHub ein und überträgt die Daten aus der Arbeitskopie auf den Server.

    git log --pretty=format:"%h - %an, %ar : %s"
    
Gibt die alle commit messages für das Projekt aus.
