# Linux Benutzer & Rechte 👤

Zurück zum [Wiki Start](README.md)

## Verwandte Themen

* [Grundbefehle](befehle.md)
* [Netzwerk](netzwerk.md)
* [Bash & Skripte](skripte.md)

---

## Inhalt

* Benutzerkonten
* Gruppen
* Benutzerinformationen
* Rechtekonzept
* chmod
* chown
* sudo
* Passwörter
* Wichtige Dateien
* Hilfe

---

## Benutzerkonten

whoami → Aktuellen Benutzer anzeigen

id → Benutzerinformationen anzeigen

sudo adduser benutzername → Neuen Benutzer anlegen

sudo deluser benutzername → Benutzer löschen

sudo deluser --remove-home benutzername → Benutzer mit Home-Verzeichnis löschen

---

## Gruppen

groups → Gruppen eines Benutzers anzeigen

sudo groupadd gruppenname → Neue Gruppe anlegen

sudo usermod -aG gruppe benutzer → Benutzer einer Gruppe hinzufügen

sudo gpasswd -d benutzer gruppe → Benutzer aus Gruppe entfernen

cat /etc/group → Alle Gruppen anzeigen

---

## Benutzerinformationen

chfn → Benutzerdaten ändern

chsh → Login-Shell ändern

id → UID und Gruppen anzeigen

who → Aktive Benutzer anzeigen

last → Letzte Anmeldungen anzeigen

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

chmod 755 datei → Rechte numerisch setzen

chmod 644 datei → Rechte numerisch setzen

Bedeutung:

7 = rwx

6 = rw-

5 = r-x

4 = r--

chmod u+x script.sh → Rechte symbolisch setzen

chmod g-w datei.txt → Rechte symbolisch setzen

---

## chown

sudo chown benutzer datei.txt → Besitzer ändern

sudo chown benutzer:gruppe datei.txt → Besitzer und Gruppe ändern

sudo chown -R benutzer:gruppe verzeichnis → Rekursiv anwenden

---

## sudo

sudo befehl → Befehl mit Administratorrechten ausführen

sudo -i → Root-Shell starten

sudo visudo → sudo-Konfiguration bearbeiten

---

## Passwörter

passwd → Eigenes Passwort ändern

sudo passwd benutzer → Passwort eines Benutzers ändern

sudo passwd -l benutzer → Benutzer sperren

sudo passwd -u benutzer → Benutzer entsperren

---

## Wichtige Dateien

/etc/passwd → Benutzerkonten

/etc/group → Gruppen

/etc/shadow → Passwortinformationen

/etc/sudoers → sudo-Konfiguration

---

## Sicherheitshinweise

* Root nur verwenden, wenn nötig
* sudo sparsam einsetzen
* starke Passwörter verwenden
* SSH-Schlüssel bevorzugen

Weitere Informationen zu SSH:

Siehe [Netzwerk](netzwerk.md)

---

## Hilfe

man chmod → Handbuch anzeigen

man chown → Handbuch anzeigen

man sudo → Handbuch anzeigen

Weitere Themen:

* [Grundbefehle](befehle.md)
* [Netzwerk](netzwerk.md)
* [Bash & Skripte](skripte.md)

