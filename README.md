[README.md](https://github.com/user-attachments/files/29959167/README.md)
# Dayline

Eine installierbare Web-App (PWA) für Tagesstruktur, Aufgaben mit Fristen, motivierende Zitate und einen Workline-Kalender für Arbeits-To-dos.

## Auf GitHub veröffentlichen (GitHub Pages)

1. Erstelle auf github.com ein neues, öffentliches Repository (z. B. `dayline`).
2. Lade **alle Dateien aus diesem Ordner** hoch (nicht den Ordner selbst, sondern seinen Inhalt):
   - `index.html`
   - `manifest.json`
   - `service-worker.js`
   - `icons/icon-192.png`
   - `icons/icon-512.png`
   - `icons/apple-touch-icon.png`

   Das geht entweder direkt im Browser über "Add file → Upload files" (Ordnerstruktur bleibt beim Ziehen-und-Ablegen erhalten) oder per Git:
   ```
   git init
   git add .
   git commit -m "Dayline PWA"
   git branch -M main
   git remote add origin https://github.com/DEIN-NUTZERNAME/dayline.git
   git push -u origin main
   ```
3. Im Repository zu **Settings → Pages** gehen.
4. Unter "Build and deployment" als Source **"Deploy from a branch"** wählen, Branch **main**, Ordner **/ (root)**, dann **Save**.
5. Nach ein bis zwei Minuten ist die App erreichbar unter:
   `https://DEIN-NUTZERNAME.github.io/dayline/`

## App installieren

- **Android / Desktop (Chrome, Edge):** Seite öffnen → es erscheint ein Installations-Icon in der Adressleiste oder ein Banner "App installieren".
- **iPhone (Safari):** Seite öffnen → Teilen-Symbol → "Zum Home-Bildschirm".

Danach startet Dayline wie eine eigene App, ohne Browser-Adressleiste.

## Wichtig zu wissen: Datenspeicherung

Deine Aufgaben werden lokal im Browser gespeichert (`localStorage`). Das bedeutet:

- Die Daten bleiben erhalten, solange du dieselbe Website im selben Browser auf demselben Gerät nutzt.
- Sie werden **nicht** automatisch zwischen mehreren Geräten synchronisiert (z. B. Handy und Laptop sehen unterschiedliche Aufgabenlisten).
- Löschst du die Browserdaten/den Cache, gehen auch die gespeicherten Aufgaben verloren.

Für eine geräteübergreifende Synchronisierung bräuchte es später ein echtes Backend (z. B. eine kleine Datenbank), das ist mit reinem HTML/JS auf GitHub Pages nicht möglich.

## Push-Benachrichtigungen

Auch als installierte PWA gilt: Erinnerungen erscheinen nur, solange die App geöffnet ist. Echte Push-Benachrichtigungen bei geschlossener App bräuchten einen eigenen Server, der Nachrichten aktiv verschickt — das ist mit dieser reinen Client-Struktur nicht abgedeckt.
