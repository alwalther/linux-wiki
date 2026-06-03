# Linux Bash & Skripte 🧠

Zurück zum [Wiki Start](README.md)

## Verwandte Themen

- [Grundbefehle](befehle.md)
- [Netzwerk](netzwerk.md)
- [Benutzer & Rechte](benutzer.md)

---

## Inhalt

- Bash Grundlagen
- Variablen
- Ein- und Ausgabe
- Pipes
- Redirects
- Textverarbeitung
- Befehlsverlauf
- Aliase
- Shell-Konfiguration
- Beispielskripte
- Hilfe

---

## Bash Grundlagen

Ein Bash-Skript ist eine Textdatei mit Befehlen.

Ausführbar machen:

chmod +x script.sh

Skript ausführen:

./script.sh

Alternativ:

bash script.sh

Erste Zeile eines Skripts:

#!/bin/bash

---

## Variablen

Variable setzen:

NAME="Linux"

Variable ausgeben:

echo $NAME

Benutzereingabe:

read NAME

Ausgabe:

echo "Hallo $NAME"

---

## Ein- und Ausgabe

Text ausgeben:

echo "Hallo Welt"

Datei anzeigen:

cat datei.txt

Zeilen zählen:

wc -l datei.txt

---

## Pipes

Pipes verbinden die Ausgabe eines Befehls mit der Eingabe eines anderen.

Beispiel:

ls -l | grep ".txt"

Anzahl der Dateien zählen:

ls | wc -l

Netzwerkports filtern:

ss -tulpen | grep ssh

Weitere Befehle:

- [Grundbefehle](befehle.md)

---

## Redirects

Ausgabe in Datei schreiben:

ls > dateien.txt

An Datei anhängen:

date >> log.txt

Fehler umleiten:

command 2> fehler.log

Alles umleiten:

command > ausgabe.log 2>&1

---

## Textverarbeitung

### grep

Text suchen:

grep "Fehler" logfile.txt

Groß-/Kleinschreibung ignorieren:

grep -i "linux" datei.txt

---

### cut

Erstes Feld ausgeben:

cut -d: -f1 /etc/passwd

---

### sort

Datei sortieren:

sort datei.txt

Numerisch sortieren:

sort -n zahlen.txt

---

### uniq

Doppelte Zeilen entfernen:

sort namen.txt | uniq

Zeilen zählen:

sort namen.txt | uniq -c

---

### awk

Erste Spalte ausgeben:

awk '{print $1}' datei.txt

Mehrere Spalten:

awk '{print $1,$3}' datei.txt

---

### sed

Text ersetzen:

sed 's/alt/neu/g' datei.txt

Zeilen anzeigen:

sed -n '1,10p' datei.txt

---

### xargs

Dateien löschen:

find . -name "*.tmp" | xargs rm

---

## Befehlsverlauf

Verlauf anzeigen:

history

Letzten Befehl wiederholen:

!!

Befehl Nummer 100 ausführen:

!100

---

## Aliase

Alias erstellen:

alias ll='ls -lah'

Aliase anzeigen:

alias

Alias entfernen:

unalias ll

---

## Shell-Konfiguration

Benutzerspezifische Bash-Konfiguration:

~/.bashrc

Bearbeiten:

nano ~/.bashrc

Neu laden:

source ~/.bashrc

---

## Beispielskript

Backup-Verzeichnis erstellen:

#!/bin/bash

mkdir -p backup

cp *.txt backup/

echo "Backup abgeschlossen"

---

## Praktisches Beispiel

Dateien zählen:

#!/bin/bash

ANZAHL=$(ls | wc -l)

echo "Dateien: $ANZAHL"

---

## Automatisierung

Skripte können genutzt werden für:

- Backups
- Logauswertung
- Softwareinstallation
- Benutzerverwaltung
- Netzwerkprüfungen

Siehe auch:

- [Netzwerk](netzwerk.md)
- [Benutzer & Rechte](benutzer.md)

---

## Hilfe

Handbuch:

man bash

Dokumentation:

help

Weitere Themen:

- [Grundbefehle](befehle.md)
- [Netzwerk](netzwerk.md)
- [Benutzer & Rechte](benutzer.md)

