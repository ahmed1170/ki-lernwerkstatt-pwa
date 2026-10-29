# KI-Lernwerkstatt

Eine kleine Progressive Web App für alle, die sich mit Betriebswirtschaft und künstlicher Intelligenz beschäftigen. Sie läuft ohne externe Bibliotheken und kann nach dem ersten Laden auch offline verwendet werden.

**[KI-Lernwerkstatt öffnen](https://ahmed1170.github.io/ki-lernwerkstatt-pwa/)** – der Link funktioniert, sobald GitHub Pages für dieses Repository eingerichtet ist.

## Funktionen

- **Karteikarten:** Zehn vorbefüllte Karten zu KI- und BWL-Grundlagen, eigene Karten und ein persönlicher Lernfortschritt.
- **Kostenrechner:** Vergleich von Frontier- und Mini- beziehungsweise lokalen Modellen anhand von Tokenmengen, Preisen, Betriebskosten und einmaligen Einführungskosten. Die Werte sind Annahmen und keine aktuellen Anbieterpreise.
- **Notizen und Sicherung:** Lernstand, eigene Karten, Notizen und Rechnerwerte werden lokal im Browser gespeichert und lassen sich als JSON exportieren und importieren. Ein Import ersetzt die vorhandenen lokalen Daten.
- **Installierbar:** App-Manifest und Service Worker ermöglichen die Nutzung als installierbare Web-App und den Offline-Zugriff nach dem ersten erfolgreichen Laden.

## Nutzung und Installation

Die Seite über den Link oben öffnen. Auf iPhone oder iPad in Safari **Teilen → Zum Home-Bildschirm** wählen; auf Android im Browsermenü **App installieren** oder **Zum Startbildschirm hinzufügen**. Auf Desktop-Systemen bieten unterstützte Browser eine Installationsoption in der Adressleiste oder im Menü.

Für Offline-Nutzung muss die App zunächst über HTTPS geöffnet werden, damit der Service Worker die Dateien zwischenspeichern kann. Browserdaten sind geräte- und browserspezifisch und können beim Löschen der Websitedaten verloren gehen; eine JSON-Sicherung ist daher sinnvoll.

## Aufbau und Veröffentlichung

`index.html` enthält Oberfläche und Logik; `manifest.webmanifest` beschreibt die App, `sw.js` verwaltet den versionierten Cache und die PNG-Dateien sind die lokalen App-Icons. Alle Ressourcen verwenden relative Pfade und benötigen keine externen CDNs oder Tracker.

Für GitHub Pages unter **Settings → Pages** den Branch `main` und den Ordner `/ (root)` als Quelle auswählen. Die Veröffentlichung kann einige Minuten dauern. Bei Änderungen an zwischengespeicherten Dateien die Cache-Version in `sw.js` erhöhen.

