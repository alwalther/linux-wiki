# Linux Netzwerk 🌐

Zurück zum [Wiki Start](README.md)

---

## 📡 IP & Interfaces

- ip a → IP anzeigen
- ip link → Netzwerkgeräte
- hostname -I → schnelle IP

---

## 🌍 Verbindung testen

- ping google.com → Verbindung prüfen
- curl https://example.com → HTTP Request
- wget url → Datei herunterladen

---

## 🚪 Ports & Dienste

- ss -tulpen → offene Ports
- ps aux → laufende Prozesse

---

## 🔧 DNS Probleme

Wenn Internet nicht geht:

1. ping 8.8.8.8
2. ping google.com
3. cat /etc/resolv.conf

---

## 🧠 Debugging

- ip route → Routing prüfen
- systemctl status NetworkManager → Netzwerkstatus
