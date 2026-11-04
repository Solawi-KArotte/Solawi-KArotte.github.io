# Solawi-KArotte.github.io
Neue Solawi-KArotte Webseite (https://solawi-karotte.de)

# Der Inhalt der neuen Seite wird per GitHub Pages hier gehostet und regelmäßig aktualisiert: https://solawi-karotte.github.io/



## 📢 Mini-Banner Konfiguration & Logik

Die Texte und das Erntejahr im Mini-Banner werden dynamisch gesteuert. Alle Einstellungen dazu befinden sich in der Datei `main.js`.

### 1. Status der Anteile ändern (`anteileVerfuegbar`)

Suchen Sie in der `main.js` nach der Variable:

var anteileVerfuegbar = true;

anteileVerfuegbar = true;
Gibt folgenden Text aus:

"Lust auf frisches Bio-Gemüse aus Karlsruhe? Wir haben noch Anteile für [Erntejahr] zu vergeben."

anteileVerfuegbar = false;
Gibt folgenden Text aus:

"Lust auf frisches Bio-Gemüse aus Karlsruhe? Momentan sind leider alle Anteile vergeben, doch gerne kannst du dich auf die Warteliste setzen lassen."

### 2. Automatische Logik für das Erntejahr (harvestYear)
Das Erntejahr wird automatisch basierend auf dem aktuellen Datum berechnet (Erntejahr-Zyklus von September bis August des Folgejahres):

01. Januar – 31. August: Es wird das aktuelle Kalenderjahr angezeigt (z. B. 2026).

01. September – 31. Dezember: Das Banner schaltet automatisch auf das Folgejahr um (z. B. ab 01.09.2026 wird für 2027 geworben).

Hinweis: Das Jahr schaltet ab dem 1. September automatisch um. Es ist kein manuelles Eingreifen im Code erforderlich.

