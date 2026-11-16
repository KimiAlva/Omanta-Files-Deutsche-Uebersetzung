# Omanta (Files) – Deutsche Übersetzung

Deutsche Übersetzung für **Omanta**, einen Dateimanager für
[Omarchy](https://omarchy.org) (Paketname `omanta`, Fenstertitel „Files“).

Basierend auf **Omanta v0.1.33** (Quelltext:
[28allday/omanta](https://github.com/28allday/omanta)).

## Inhalt

| Datei | Beschreibung |
|---|---|
| `omanta_de.ts` | Qt-Übersetzungsquelle (XML), 427 Strings, vollständig übersetzt |
| `omanta_de.qm` | Kompilierte Übersetzung für die Laufzeit |

## Voraussetzungen

Diese Übersetzung setzt eine Omanta-Version voraus, die Übersetzungen zur
Laufzeit lädt (`QTranslator`). Die Dateisuche erfolgt in folgenden Pfaden
(in dieser Reihenfolge):

1. `$OMANTA_TRANSLATIONS_DIR`
2. `<appdir>/../share/omanta/translations`
3. `/usr/local/share/omanta/translations`
4. `/usr/share/omanta/translations`
5. `~/.local/share/omanta/translations`

Liegt die `.qm` in einem dieser Verzeichnisse und ist die Systemsprache auf
Deutsch gesetzt, erscheint Omanta automatisch auf Deutsch. Fehlt die Datei,
fällt die Anwendung auf Englisch zurück.

## Installation

```bash
# Systemweit (pacman/Arch)
sudo install -Dm644 omanta_de.qm /usr/share/omanta/translations/omanta_de.qm

# oder lokal für den aktuellen Benutzer
install -Dm644 omanta_de.qm ~/.local/share/omanta/translations/omanta_de.qm
```

Anschließend Omanta neu starten. Die Sprache folgt der Locale (`LANG=de_DE.UTF-8`
bzw. `LANGUAGE=de`).

## Übersetzung aktualisieren

Die folgenden Befehle laufen im **Omanta-Quellrepository** (nicht in diesem
Repo), in dem `src/` und `qml/` liegen:

```bash
# Strings neu extrahieren
lupdate6 src qml -ts omanta_de.ts

# Übersetzen (z. B. mit Qt Linguist)
linguist omanta_de.ts

# Kompilieren
lrelease6 omanta_de.ts -qm omanta_de.qm
```

Die aktualisierten Dateien anschließend in dieses Repository übernehmen.

## Mitwirken

Pull Requests und Korrekturen sind willkommen. Bitte bei Änderungen die
Platzhalter (`%1`, `%n`, `…`) unverändert lassen und die `.qm` neu bauen.

## Lizenz

Die Übersetzung folgt dem Lizenzmodell des Omanta-Projekts. Omanta selbst
steht unter seiner eigenen Lizenz (siehe Upstream-Repository).