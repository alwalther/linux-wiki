# Linux Bash & Skripte 🧠

Zurück zum Wiki: README.md

## Basics
- echo → Ausgabe
- bash script.sh → Skript ausführen

## Pipes & Redirects

| Symbol | Bedeutung |
|------|-----------|
| \| | verbindet Befehle (Pipe) |
| > | überschreibt Datei |
| >> | hängt an Datei an |
| 2> | Fehlerausgabe umleiten |

## Beispiele
ls -l | grep txt
cat file | wc -l

## Logik
- && → nur wenn erfolgreich
- || → wenn Fehler

## Script Beispiel
#!/bin/bash
echo "Hello Linux"
