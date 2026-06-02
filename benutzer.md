# Linux Benutzer & Rechte 👤

Zurück zum [Wiki Start](README.md)

## Verwandte Themen

- [Grundbefehle](befehle.md)
- [Netzwerk](netzwerk.md)
- [Bash & Skripte](skripte.md)

---

## Inhalt

- Benutzerkonten
- Gruppen
- Benutzerinformationen
- Rechtekonzept
- chmod
- chown
- sudo
- Passwörter
- Wichtige Dateien
- Hilfe

---

## Benutzerkonten

Aktuellen Benutzer anzeigen:

whoami

Benutzerinformationen anzeigen:

id

Neuen Benutzer anlegen:

sudo adduser benutzername

Benutzer löschen:

sudo deluser benutzername

Benutzer mit Home-Verzeichnis löschen:

sudo deluser --remove-home benutzername

---

## Gruppen

Gruppen eines Benutzers anzeigen:

groups

Neue Gruppe anlegen:

sudo groupadd gruppenname

Benutzer einer Gruppe hinzufügen:

sudo usermod -aG gruppe benutzer

Benutzer aus Gruppe entfernen:

sudo gpasswd -d benutzer gruppe

Alle Gruppen anzeigen:

cat /etc/group

---

## Benutzerinformationen

Benutzerdaten ändern:

chfn

Login-Shell ändern:

chsh

UID und Gruppen anzeigen:

id

Aktive Benutzer anzeigen:

who

Letzte Anmeldungen anzeigen:

last

---

## Rechtekonzept

Linux verwendet drei Rechteklassen:

u = User (Besitzer)

g = Group (Gruppe)

o = Others (Andere)

Rechte:

r = read (lesen)

w = write (schreiben)

x = execute (ausführen)

Beispiel:

-rwxr-xr-x

Bedeutung:

Besitzer: lesen, schreiben, ausführen

Gruppe: lesen, ausführen

Andere: lesen, ausführen

---

## chmod

Rechte numerisch setzen:

chmod 755 datei

chmod 644 datei

Bedeutung:

7 = rwx

6 = rw-

5 = r-x

4 = r--

Rechte symbolisch setzen:

chmod u+x script.sh

chmod g-w datei.txt

---

## chown

Besitzer ändern:

sudo chown benutzer datei.txt

Besitzer und Gruppe ändern:

sudo chown benutzer:gruppe datei.txt

Rekursiv anwenden:

sudo chown -R benutzer:gruppe verzeichnis

---

## sudo

Befehl mit Administratorrechten ausführen:

sudo befehl

Root-Shell starten:

sudo -i

sudo-Konfiguration bearbeiten:

sudo visudo

---

## Passwörter

Eigenes Passwort ändern:

passwd

Passwort eines Benutzers ändern:

sudo passwd benutzer

Benutzer sperren:

sudo passwd -l benutzer

Benutzer entsperren:

sudo passwd -u benutzer

---

## Wichtige Dateien

Benutzerkonten:

/etc/passwd

Gruppen:

/etc/group

Passwortinformationen:

/etc/shadow

sudo-Konfiguration:

/etc/sudoers

---

## Sicherheitshinweise

- Root nur verwenden, wenn nötig
- sudo sparsam einsetzen
- starke Passwörter verwenden
- SSH-Schlüssel bevorzugen

Weitere Informationen zu SSH:

Siehe [Netzwerk](netzwerk.md)

---

## Hilfe

Handbuch anzeigen:

man chmod

man chown

man sudo

Weitere Themen:

- [Grundbefehle](befehle.md)
- [Netzwerk](netzwerk.md)
- [Bash & Skripte](skripte.md)

