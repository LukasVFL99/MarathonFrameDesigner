# Marathon Frame Designer (Web)

Statische Web-App ohne Backend: GPX-Strecke als Vektor, Layout-Vorlage (Platzierungen aus der Desktop-Version),
Datenfelder, Snap-to-Grid, Bib-/Medaillen-Platzhalter, Export als SVG/PNG und 1:1-Druck bzw. Vektor-PDF.
Standard: 30 x 45 cm, Raster 1 mm, Medaille Ø 60 mm.

## Auf GitHub Pages veröffentlichen
1. Neues Repository anlegen (z. B. `marathon-frame-designer`), `index.html` und `README.md` hochladen (Add file > Upload files, Branch `main`)
2. Settings > Pages > Source: **Deploy from a branch**, Branch `main`, Ordner `/ (root)` > Save
3. Nach ca. 1 Minute erreichbar unter `https://<dein-user>.github.io/marathon-frame-designer/`

Updates: geänderte `index.html` im Repo ersetzen, Seite neu laden.

## Bedienung
- Layout-Vorlage: Felder ausfüllen, "Layout anwenden". Textänderungen wirken sofort, von Hand verschobene Elemente bleiben stehen
- GPX laden: Strecke landet automatisch in der Layout-Box (mittig, Seitenverhältnis bleibt)
- Elemente mit der Maus ziehen (rasten am Raster ein), Pfeiltasten verschieben um ein Raster (Shift = 10x), Entf löscht
- Mausrad = Zoom, Hintergrund ziehen = verschieben, "Einpassen" setzt die Ansicht zurück
- Der Zustand wird automatisch im Browser gespeichert; "Projekt speichern/laden" als JSON-Datei für Backup oder anderes Gerät

## Drucken / PDF in Originalgröße
- "1:1, Seite = Rahmengröße": Druckdialog öffnen, Ziel "Als PDF speichern", Ränder "Keine", Skalierung 100 %. Ergebnis: Vektor-PDF in exakt 300 x 450 mm
- "1:1 gekachelt": Rahmen wird auf mehrere Seiten (A4/A3/Letter) mit Überlappung verteilt, jede Seite ist beschriftet
- Echte Drucker haben einen unbedruckbaren Rand, deshalb Überlappung >= 10 mm lassen

## Schriften
Standard ist Oswald (Google Fonts, wird beim Aufruf geladen und beim Export in SVG/PNG/PDF eingebettet).
Offline oder ohne Google-Zugriff fällt die Seite auf Arial Narrow/Arial zurück.
Wer keine Google-Server einbinden will: Schriftdatei ins Repo legen und per `@font-face` in `index.html` einbinden.
