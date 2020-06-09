
# bezeichnet ein Kommentar und soll nicht mit eingegeben werden

# Alle branches anzeigen
git brach -a

# Alles Upstreams anzeigen
git remote show origin

# Auf branch Wechseln
git checkout #branch_name

# Auf branch Wechseln und erzeugen, falls esr nicht existiert
git checkout -b #branch_name

# Änderungen auf dem Server überprüfen (server->local)
git fetch

# Änderung vom Server übertragen (server->local->merge)
git pull

# Änderungen auf den Server übertragen (local->server)
git push

# Änderungen auf einen neuen Branch auf dem Server übertragen (local->server)
git push -u origin #branch_name

# File in das Tracking hinzufügen
git add #file

# Änderungen eines bestimmten files

# Alle getrackten Änderungen commiten
git commit -m „#your_comment“

# Admin
git config --global core.editor „‘D:/Notepad++/notepad++.exe‘ -multiInst -notabbar -nosession -noPlugin“