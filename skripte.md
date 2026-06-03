# Linux Bash & Skripte 🧠

Zurück zum [Wiki Start](README.md)

## Verwandte Themen

* [Grundbefehle](befehle.md)
* [Netzwerk](netzwerk.md)
* [Benutzer & Rechte](benutzer.md)

---

## Inhalt

* Bash Grundlagen
* Variablen
* Ein- und Ausgabe
* Pipes
* Redirects
* Textverarbeitung
* Befehlsverlauf
* Aliase
* Shell-Konfiguration
* Beispielskripte
* Hilfe

---

## Bash Grundlagen

Ein Bash-Skript ist eine Textdatei mit Befehlen.

chmod +x script.sh → Ausführbar machen

./script.sh → Skript ausführen

bash script.sh → Alternativ

Erste Zeile eines Skripts:

#!/bin/bash

---

## Variablen

NAME="Linux" → Variable setzen

echo $NAME → Variable ausgeben

read NAME → Benutzereingabe

echo "Hallo $NAME" → Ausgabe

---

## Ein- und Ausgabe

echo "Hallo Welt" → Text ausgeben

cat datei.txt → Datei anzeigen

wc -l datei.txt → Zeilen zählen

---

## Pipes

Pipes verbinden die Ausgabe eines Befehls mit der Eingabe eines anderen.

Beispiel:

ls -l | grep ".txt"

ls | wc -l → Anzahl der Dateien zählen

ss -tulpen | grep ssh → Netzwerkports filtern

Weitere Befehle:

* [Grundbefehle](befehle.md)

---

## Redirects

ls > dateien.txt → Ausgabe in Datei schreiben

date >> log.txt → An Datei anhängen

command 2> fehler.log → Fehler umleiten

command > ausgabe.log 2>&1 → Alles umleiten

---

## Textverarbeitung

### grep

grep "Fehler" logfile.txt → Text suchen

grep -i "linux" datei.txt → Groß-/Kleinschreibung ignorieren

---

### cut

cut -d: -f1 /etc/passwd → Erstes Feld ausgeben

---

### sort

sort datei.txt → Datei sortieren

sort -n zahlen.txt → Numerisch sortieren

---

### uniq

sort namen.txt | uniq → Doppelte Zeilen entfernen

sort namen.txt | uniq -c → Zeilen zählen

---

### awk

awk '{print $1}' datei.txt → Erste Spalte ausgeben

awk '{print $1,$3}' datei.txt → Mehrere Spalten

---

### sed

sed 's/alt/neu/g' datei.txt → Text ersetzen

sed -n '1,10p' datei.txt → Zeilen anzeigen

---

### xargs

find . -name "*.tmp" | xargs rm → Dateien löschen

---

## Befehlsverlauf

history → Verlauf anzeigen

!! → Letzten Befehl wiederholen

!100 → Befehl Nummer 100 ausführen

---

## Aliase

alias ll='ls -lah' → Alias erstellen

alias → Aliase anzeigen

unalias ll → Alias entfernen

---

## Shell-Konfiguration

~/.bashrc → Benutzerspezifische Bash-Konfiguration

nano ~/.bashrc → Bearbeiten

source ~/.bashrc → Neu laden

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

* Backups
* Logauswertung
* Softwareinstallation
* Benutzerverwaltung
* Netzwerkprüfungen

Siehe auch:

* [Netzwerk](netzwerk.md)
* [Benutzer & Rechte](benutzer.md)

---

## Hilfe

man bash → Handbuch

help → Dokumentation

Weitere Themen:

* [Grundbefehle](befehle.md)
* [Netzwerk](netzwerk.md)
* [Benutzer & Rechte](benutzer.md)

