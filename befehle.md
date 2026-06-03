# Linux Grundbefehle 🐧

Zurück zum [Wiki Start](README.md)

## Verwandte Themen

* [Netzwerk](netzwerk.md)
* [Benutzer & Rechte](benutzer.md)
* [Bash & Skripte](skripte.md)

---

## Inhalt

* Navigation
* Dateien & Ordner
* Dateiinhalt anzeigen
* Dateisuche
* Dateiinformationen
* Links
* Archivierung & Backup
* Speicherplatz
* Softwareverwaltung
* Systeminformationen
* Hilfe

---

## Navigation

pwd → Aktuelles Verzeichnis anzeigen

ls → Verzeichnisinhalt anzeigen

ls -l → Detaillierte Ansicht

ls -la → Versteckte Dateien anzeigen

cd /pfad/zum/verzeichnis → Verzeichnis wechseln

cd ~ → Ins Home-Verzeichnis wechseln

---

## Dateien & Ordner

touch datei.txt → Datei erstellen

mkdir ordner → Ordner erstellen

cp quelle.txt ziel.txt → Datei kopieren

mv alt.txt neu.txt → Datei verschieben oder umbenennen

rm datei.txt → Datei löschen

rm -r ordner → Ordner rekursiv löschen

rmdir ordner → Leeren Ordner löschen

---

## Dateiinhalt anzeigen

cat datei.txt → Kompletten Inhalt anzeigen

less datei.txt → Seitenweise anzeigen

head datei.txt → Erste 10 Zeilen

tail datei.txt → Letzte 10 Zeilen

wc -l datei.txt → Zeilen zählen

Weitere Textverarbeitung wird in [Bash & Skripte](skripte.md) behandelt.

---

## Dateisuche

find . -name "*.txt" → Dateien rekursiv suchen

find . -type f → Dateien nach Typ suchen

find . -type d → Ordner suchen

locate dateiname → Schnelle Suche über Datenbank

sudo updatedb → Suchdatenbank aktualisieren

---

## Dateiinformationen

file datei.txt → Dateityp bestimmen

stat datei.txt → Dateidetails anzeigen

md5sum image.iso → Prüfsumme berechnen

---

## Links

ln -s quelle ziel → Softlink erstellen

ln quelle ziel → Hardlink erstellen

---

## Archivierung & Backup

tar -czf backup.tar.gz ordner/ → Archiv erstellen

tar -xzf backup.tar.gz → Archiv entpacken

rsync -av quelle/ ziel/ → Verzeichnisse synchronisieren

---

## Speicherplatz

df -h → Datenträgerbelegung anzeigen

du -sh * → Ordnergrößen anzeigen

lsblk → Blockgeräte anzeigen

mount → Eingehängte Dateisysteme anzeigen

---

## Softwareverwaltung

sudo apt update → Paketliste aktualisieren

sudo apt upgrade → Pakete aktualisieren

sudo apt install paketname → Paket installieren

sudo apt remove paketname → Paket entfernen

apt list --installed → Installierte Pakete suchen

---

## Systeminformationen

uname -a → Kernel anzeigen

hostname → Hostname anzeigen

hostnamectl → Hostinformationen anzeigen

lsb_release -a → Distribution anzeigen

uptime → Systemlaufzeit anzeigen

date → Aktuelles Datum

---

## Hilfe

man befehl → Handbuch anzeigen

befehl --help → Kurzhilfe anzeigen

Siehe auch:

* [Netzwerk](netzwerk.md)
* [Benutzer & Rechte](benutzer.md)
* [Bash & Skripte](skripte.md)

