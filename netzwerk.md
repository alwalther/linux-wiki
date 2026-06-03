# Linux Netzwerk 🌐

Zurück zum [Wiki Start](README.md)

## Verwandte Themen

* [Grundbefehle](befehle.md)
* [Benutzer & Rechte](benutzer.md)
* [Bash & Skripte](skripte.md)

---

## Inhalt

* Netzwerkgrundlagen
* IP-Adressen & Interfaces
* Verbindung testen
* DNS
* Routing
* SSH
* SSH-Schlüssel
* Dateiübertragung
* Netzwerkanalyse
* NetworkManager
* Hilfe

---

## Netzwerkgrundlagen

Jedes Gerät in einem Netzwerk besitzt eine eindeutige IP-Adresse.

Wichtige Begriffe:

* IP-Adresse
* Subnetzmaske
* Gateway
* DNS-Server
* MAC-Adresse

---

## IP-Adressen & Interfaces

ip a → Alle Netzwerkinterfaces anzeigen

ip link → Netzwerkgeräte anzeigen

hostname -I → IP-Adresse schnell anzeigen

ip addr show → Detaillierte Informationen anzeigen

---

## Verbindung testen

ping google.com → Erreichbarkeit eines Hosts prüfen

ping -c 4 google.com → Nur 4 Pakete senden

curl [https://example.com](https://example.com) → Webseite abrufen

wget [https://example.com/datei.txt](https://example.com/datei.txt) → Datei herunterladen

---

## DNS

DNS übersetzt Hostnamen in IP-Adressen.

cat /etc/resolv.conf → DNS-Server anzeigen

dig openai.com → DNS-Abfrage durchführen

resolvectl status → DNS-Konfiguration anzeigen

host openai.com → Namensauflösung testen

---

## Routing

ip route → Routingtabelle anzeigen

ip route | grep default → Standard-Gateway anzeigen

Beispiel:

default via 192.168.1.1 dev wlan0

---

## SSH

SSH ermöglicht den sicheren Fernzugriff auf Linux-Systeme.

ssh user@server → Verbindung herstellen

ssh admin@192.168.1.100 → Beispiel

SSH wird häufig zusammen mit Benutzerkonten verwendet.

Siehe auch:

* [Benutzer & Rechte](benutzer.md)

---

## SSH-Schlüssel

ssh-keygen -t ed25519 → Neuen Schlüssel erzeugen

cat ~/.ssh/id_ed25519.pub → Öffentlichen Schlüssel anzeigen

ssh-copy-id user@server → Schlüssel auf Server kopieren

Vorteile:

* keine Passwortübertragung
* höhere Sicherheit
* automatisierte Anmeldungen

---

## Dateiübertragung

scp datei.txt user@server:/home/user/ → Datei per SCP kopieren

scp -r ordner user@server:/home/user/ → Verzeichnis kopieren

sftp user@server → SFTP starten

---

## Netzwerkanalyse

arp -a → ARP-Tabelle anzeigen

ss -tulpen → Offene Verbindungen anzeigen

nmap 192.168.1.0/24 → Netzwerkscan durchführen

whois openai.com → Domaininformationen abrufen

---

## NetworkManager

nmcli device status → Status anzeigen

nmcli connection show → Verbindungen anzeigen

nmcli device wifi list → WLANs suchen

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

man ip → Handbuch anzeigen

man ssh → Handbuch für SSH

Weitere Themen:

* [Grundbefehle](befehle.md)
* [Benutzer & Rechte](benutzer.md)
* [Bash & Skripte](skripte.md)

