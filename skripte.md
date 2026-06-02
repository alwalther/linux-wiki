# Linux Bash Skripte Grundlagen

## Grundsyntax

- echo "Text" → Ausgabe
- bash script.sh → Skript ausführen

## Pipes & Redirects

- command1 | command2 → Ausgabe weiterleiten
- > → überschreiben
- >> → anhängen
- 2> → Fehler umleiten

## Beispiele

- ls -l | grep txt → nur txt Dateien filtern
- cat datei.txt | wc -l → Zeilen zählen

## Logische Operatoren

- && → nur wenn vorher erfolgreich
- || → wenn vorher fehlschlägt
