# Cockpit

Installer und Updates für Cockpit, die Desktop-App, die mehrere Claude Code Sessions als echte Terminals in einem Fenster zeigt. Der Quellcode liegt nicht hier.

## Installieren (Windows 10 und 11)

1. Unter [Releases](https://github.com/constantinktz/cockpit-releases/releases/latest) die Datei `Cockpit_…_x64-setup.exe` laden.
2. Starten. Der Installer ist nicht mit einem Zertifikat signiert, Windows fragt deshalb einmal nach: „Weitere Informationen“ › „Trotzdem ausführen“.
3. Vorher nötig: [Git for Windows](https://git-scm.com/downloads/win) und mindestens eine CLI, etwa Claude Code, Codex oder Antigravity (agy). Details in `Zuerst lesen.txt` im selben Release.

## Updates

Cockpit sucht selbst nach neuen Versionen und zeigt dann oben rechts „Update x.y.z“. Jedes Update ist mit einem eigenen Schlüssel signiert, Cockpit installiert nichts anderes. Von Hand: Einstellungen › Allgemein › „Nach Updates suchen“.

## Fehler melden

Einstellungen › Allgemein › „Diagnose kopieren“ und den Text mitschicken. Tokens und der Benutzerordner sind darin schon entfernt.

### Logs

Cockpit schreibt Warnungen, Fehler und Abstürze in eine Logdatei, höchstens 2 MB:

- **Windows:** `%LOCALAPPDATA%\de.constantin.cockpit\logs\cockpit.log`, also etwa `C:\Users\<name>\AppData\Local\de.constantin.cockpit\logs\cockpit.log`. Am schnellsten: Win+R, `%LOCALAPPDATA%\de.constantin.cockpit\logs` eingeben, Enter.
- **macOS:** `~/Library/Logs/de.constantin.cockpit/cockpit.log`

In Cockpit öffnet Einstellungen › Allgemein › „Logs öffnen“ den Ordner direkt, ebenso „Logs öffnen“ in der Befehlspalette (Strg+K). Die Datei kann Pfade und Projektnamen enthalten, vor dem Weitergeben kurz drüberschauen. Die letzten 200 Zeilen stecken auch schon in „Diagnose kopieren“.
