# Linux Bash & Skripte 🧠

Zurück zum [Wiki Start](README.md)

---

## ⚙️ Grundlagen

- echo "text" → Ausgabe
- bash script.sh → Skript ausführen

---

## 🔗 Pipes & Redirects

| Symbol | Bedeutung |
|------|-----------|
| | | Ausgabe verbinden |
| > | Datei überschreiben |
| >> | Datei anhängen |
| 2> | Fehler umleiten |

---

## 🧪 Beispiele

ls -l | grep ".md"
cat file.txt | wc -l

---

## 🔁 Logik

- && → nur wenn vorher erfolgreich
- || → wenn Fehler

---

## 📜 Beispiel Script

#!/bin/bash

echo "Start"
ls -l
echo "Ende"

---

## 🚀 Mini Automation

mkdir test && cd test && touch file.txt
