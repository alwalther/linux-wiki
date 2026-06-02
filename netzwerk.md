# Linux Netzwerk 🌐

Zurück zum [Wiki Start](README.md)

## Verwandte Themen

- [Grundbefehle](befehle.md)
- [Benutzer & Rechte](benutzer.md)
- [Bash & Skripte](skripte.md)

---

## Inhalt

- Netzwerkgrundlagen
- IP-Adressen & Interfaces
- Verbindung testen
- DNS
- Routing
- SSH
- SSH-Schlüssel
- Dateiübertragung
- Netzwerkanalyse
- NetworkManager
- Hilfe

---

## Netzwerkgrundlagen

Jedes Gerät in einem Netzwerk besitzt eine eindeutige IP-Adresse.

Wichtige Begriffe:

- IP-Adresse
- Subnetzmaske
- Gateway
- DNS-Server
- MAC-Adresse

---

## IP-Adressen & Interfaces

Alle Netzwerkinterfaces anzeigen:

ip a

Netzwerkgeräte anzeigen:

ip link

IP-Adresse schnell anzeigen:

hostname -I

Detaillierte Informationen anzeigen:

ip addr show

---

## Verbindung testen

Erreichbarkeit eines Hosts prüfen:

ping google.com

Nur 4 Pakete senden:

ping -c 4 google.com

Webseite abrufen:

curl https://example.com

Datei herunterladen:

wget https://example.com/datei.txt

---

## DNS

DNS übersetzt Hostnamen in IP-Adressen.

DNS-Server anzeigen:

cat /etc/resolv.conf

DNS-Abfrage durchführen:

dig openai.com

DNS-Konfiguration anzeigen:

resolvectl status

Namensauflösung testen:

host openai.com

---

## Routing

Routingtabelle anzeigen:

ip route

Standard-Gateway anzeigen:

ip route | grep default

Beispiel:

default via 192.168.1.1 dev wlan0

---

## SSH

SSH ermöglicht den sicheren Fernzugriff auf Linux-Systeme.

Verbindung herstellen:

ssh user@server

Beispiel:

ssh admin@192.168.1.100

SSH wird häufig zusammen mit Benutzerkonten verwendet.

Siehe auch:

- [Benutzer & Rechte](benutzer.md)

---

## SSH-Schlüssel

Neuen Schlüssel erzeugen:

ssh-keygen -t ed25519

Öffentlichen Schlüssel anzeigen:

cat ~/.ssh/id_ed25519.pub

Schlüssel auf Server kopieren:

ssh-copy-id user@server

Vorteile:

- keine Passwortübertragung
- höhere Sicherheit
- automatisierte Anmeldungen

---

## Dateiübertragung

Datei per SCP kopieren:

scp datei.txt user@server:/home/user/

Verzeichnis kopieren:

scp -r ordner user@server:/home/user/

SFTP starten:

sftp user@server

---

## Netzwerkanalyse

ARP-Tabelle anzeigen:

arp -a

Offene Verbindungen anzeigen:

ss -tulpen

Netzwerkscan durchführen:

nmap 192.168.1.0/24

Domaininformationen abrufen:

whois openai.com

---

## NetworkManager

Status anzeigen:

nmcli device status

Verbindungen anzeigen:

nmcli connection show

WLANs suchen:

nmcli device wifi list

---

## Typische Fehlersuche

1. Hat das Gerät eine IP-Adresse?

ip a

2. Ist das Gateway erreichbar?

ping 192.168.1.1

3. Funktioniert DNS?

ping google.com

4. Funktioniert nur die IP?

ping 8.8.8.8

Wenn IP funktioniert, aber Namen nicht:

DNS-Konfiguration prüfen.

---

## Hilfe

Handbuch anzeigen:

man ip

Handbuch für SSH:

man ssh

Weitere Themen:

- [Grundbefehle](befehle.md)
- [Benutzer & Rechte](benutzer.md)
- [Bash & Skripte](skripte.md)

