# Linux Benutzer & Rechte 👤

Zurück zum [Wiki Start](README.md)

---

## 👤 Benutzer

- whoami → aktueller Benutzer
- id → User + Gruppen
- adduser name → Benutzer erstellen
- passwd name → Passwort setzen

---

## 👥 Gruppen

- groups → anzeigen
- usermod -aG sudo user → Adminrechte geben

---

## 🔐 Rechte Modell

Linux Rechte bestehen aus:

- User (u)
- Group (g)
- Others (o)

---

## 📄 Rechte Beispiele

- chmod 755 file → volle Rechte für Owner
- chmod 644 file → Standard Datei
- chown user:group file → Besitzer ändern

---

## ⚠️ sudo

- sudo command → Adminrechte

Nur verwenden, wenn nötig!
