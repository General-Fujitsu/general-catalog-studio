# GENERAL Catalog Studio 2026/27

Statische Einzeldatei für GitHub Pages. Der komplette Katalogdatensatz ist direkt in `index.html` eingebettet. Es gibt keine Datenbank und keine Projektspeicherung.

## Funktionen

- Suche nach Artikelnummer, Modell, Leistung, Bauform, Farbe und Schlagworten
- Produktdetails mit Katalogseite und Katalogauszug
- Warenkorb/Artikelliste und Team-Stuttgart-Mailtext
- Kundenmail-Parser für Räume, Leistung, Rohrlänge und Zubehör
- Lokale PDF-/LV-/Auslegungsanalyse im Browser
- Export als TXT und CSV

## GitHub Pages

1. Neues Repository anlegen, z. B. `general-catalog-studio`.
2. `index.html` und die leere Datei `.nojekyll` in das Hauptverzeichnis des Repositories hochladen.
3. Repository öffnen: **Settings → Pages**.
4. Unter **Build and deployment** die Quelle **Deploy from a branch** wählen.
5. Branch **main**, Ordner **/(root)** wählen und speichern.
6. Nach der Bereitstellung erscheint die Webadresse im Bereich **Pages**.

## Datenschutz und Zugriff

Die Anwendung überträgt Projekttexte und eingelesene Dateien nicht an einen Server. PDF-Dateien werden mit PDF.js im Browser verarbeitet. Der in `index.html` eingebettete Katalog ist jedoch für jeden sichtbar, der Zugriff auf die GitHub-Pages-Adresse bzw. das Repository hat. Für rein internen Einsatz daher die Zugriffsart des Repositories und der Pages-Bereitstellung prüfen.

## Aktualisierung

Bei einem neuen Katalogstand muss der eingebettete Datensatz neu erzeugt und `index.html` ersetzt werden. Die Anwendung zeigt den Stand **Q3 2026 / Preiskatalog 2026–2027**.
