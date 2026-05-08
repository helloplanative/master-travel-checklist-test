# Einfache Anleitung für Netlify-Test

## Ziel
Du willst diese Version gratis auf Netlify testen. Dafür brauchst du:

- Netlify Account
- GitHub Account
- diese entpackten Projektdateien

Du musst nichts programmieren.

## Schritt 1: ZIP entpacken
Entpacke die Datei `master-travel-checklist-v2-netlify-functions.zip`.

Danach hast du einen Ordner `master-travel-checklist-v2-netlify-functions`.

Darin müssen sichtbar sein:

- index.html
- styles.css
- app.js
- netlify.toml
- package.json
- Ordner netlify
- Ordner data
- README.md

## Schritt 2: GitHub öffnen
Gehe zu github.com und melde dich an. Falls du keinen Account hast, erstelle einen kostenlosen Account.

## Schritt 3: Neues Repository erstellen
Klicke auf `New repository`.

Name: `master-travel-checklist-test`

Dann `Create repository` klicken.

## Schritt 4: Dateien hochladen
Im neuen Repository klicke auf `uploading an existing file`.

Ziehe den Inhalt des entpackten Projektordners in das GitHub-Fenster.

Wichtig: Auch der Ordner `netlify/functions` muss dabei sein.

Unten bei Commit message: `first upload`

Dann `Commit changes` klicken.

## Schritt 5: Netlify mit GitHub verbinden
Gehe zu app.netlify.com.

Klicke auf:

`Add new site` → `Import an existing project` → `GitHub`

Erlaube Netlify den Zugriff auf dein GitHub Repository.

## Schritt 6: Repository auswählen
Wähle `master-travel-checklist-test`.

## Schritt 7: Einstellungen in Netlify
Build command: leer lassen

Publish directory: `.`

Dann `Deploy` klicken.

## Schritt 8: Testen
Öffne die Netlify-Adresse.

Testbeispiel:

- Zielland: Uganda
- Nationalität: Austria
- Passland: Austria
- Wohnsitz: Austria
- Ausgangsland: Austria
- Reisezweck: Tourismus
- Aufenthaltstage: 14

Dann `Checkliste erstellen` klicken.

## Wenn es nicht funktioniert
Wenn die Meldung erscheint, dass die Checkliste nicht erstellt werden konnte, prüfe in Netlify:

`Site configuration` → `Functions`

Dort sollte `travel-check` sichtbar sein.

Wenn nicht, wurde der Ordner `netlify/functions` nicht richtig hochgeladen.

## Später mit deiner Website verbinden
Für den Test bleibt die App auf Netlify.

Später gibt es drei Möglichkeiten:

1. Subdomain auf Netlify zeigen lassen, z. B. `checklist.planative.net`
2. Tool als Link oder iframe in deine Website einbinden
3. Tool auf eigenen Webspace übertragen

Achtung: Normale FTP-Webspaces können Netlify Functions nicht ausführen. Für eine eigene Website brauchst du dann ein kleines Backend oder du lässt die API-Schicht weiter bei Netlify laufen.
