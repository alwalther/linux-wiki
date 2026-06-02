# Linux Grundbefehle 🐧

Zurück zum [Wiki Start](README.md)

## Verwandte Themen

- [Netzwerk](netzwerk.md)
- [Benutzer & Rechte](benutzer.md)
- [Bash & Skripte](skripte.md)

---

## Inhalt

- Navigation
- Dateien & Ordner
- Dateiinhalt anzeigen
- Dateisuche
- Dateiinformationen
- Links
- Archivierung & Backup
- Speicherplatz
- Softwareverwaltung
- Systeminformationen
- Hilfe

---

## Navigation

Aktuelles Verzeichnis anzeigen:

pwd

Verzeichnisinhalt anzeigen:

ls

Detaillierte Ansicht:

ls -l

Versteckte Dateien anzeigen:

ls -la

Verzeichnis wechseln:

cd /pfad/zum/verzeichnis

Ins Home-Verzeichnis wechseln:

cd ~

---

## Dateien & Ordner

Datei erstellen:

touch datei.txt

Ordner erstellen:

mkdir ordner

Datei kopieren:

cp quelle.txt ziel.txt

Datei verschieben oder umbenennen:

mv alt.txt neu.txt

Datei löschen:

rm datei.txt

Ordner rekursiv löschen:

rm -r ordner

Leeren Ordner löschen:

rmdir ordner

---

## Dateiinhalt anzeigen

Kompletten Inhalt anzeigen:

cat datei.txt

Seitenweise anzeigen:

less datei.txt

Erste 10 Zeilen:

head datei.txt

Letzte 10 Zeilen:

tail datei.txt

Zeilen zählen:

wc -l datei.txt

Weitere Textverarbeitung wird in [Bash & Skripte](skripte.md) behandelt.

---

## Dateisuche

Dateien rekursiv suchen:

find . -name "*.txt"

Dateien nach Typ suchen:

find . -type f

Ordner suchen:

find . -type d

Schnelle Suche über Datenbank:

locate dateiname

Suchdatenbank aktualisieren:

sudo updatedb

---

## Dateiinformationen

Dateityp bestimmen:

file datei.txt

Dateidetails anzeigen:

stat datei.txt

Prüfsumme berechnen:

md5sum image.iso

---

## Links

Softlink erstellen:

ln -s quelle ziel

Hardlink erstellen:

ln quelle ziel

---

## Archivierung & Backup

Archiv erstellen:

tar -czf backup.tar.gz ordner/

Archiv entpacken:

tar -xzf backup.tar.gz

Verzeichnisse synchronisieren:

rsync -av quelle/ ziel/

---

## Speicherplatz

Datenträgerbelegung anzeigen:

df -h

Ordnergrößen anzeigen:

du -sh *

Blockgeräte anzeigen:

lsblk

Eingehängte Dateisysteme anzeigen:

mount

---

## Softwareverwaltung

Paketliste aktualisieren:

sudo apt update

Pakete aktualisieren:

sudo apt upgrade

Paket installieren:

sudo apt install paketname

Paket entfernen:

sudo apt remove paketname

Installierte Pakete suchen:

apt list --installed

---

## Systeminformationen

Kernel anzeigen:

uname -a

Hostname anzeigen:

hostname

Hostinformationen anzeigen:

hostnamectl

Distribution anzeigen:

lsb_release -a

Systemlaufzeit anzeigen:

uptime

Aktuelles Datum:

date

---

## Hilfe

Handbuch anzeigen:

man befehl

Kurzhilfe anzeigen:

befehl --help

Siehe auch:

- [Netzwerk](netzwerk.md)
- [Benutzer & Rechte](benutzer.md)
- [Bash & Skripte](skripte.md)

