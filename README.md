# GENERAL Katalog-Studio 2026/27

Webshop / Konfigurator auf Basis der GENERAL Klimaanlagen-Preisliste 2026/27 (gültig ab 01.07.2026).
Eine einzige Datei (`index.html`), keine Abhängigkeiten, läuft komplett offline im Browser.
Alle Preise netto. Produktfotos stammen aus dem Katalog und sind in der Datei eingebettet.

## Auf GitHub veröffentlichen (GitHub Pages)

1. Auf github.com → **New repository** → Name z. B. `katalog-studio` → anlegen.
2. **Add file → Upload files** → `index.html` und `README.md` hochladen → **Commit changes**.
3. **Settings → Pages** → Source: **Deploy from a branch**, Branch: **main** / **/(root)** → **Save**.
4. Nach 1–2 Minuten erreichbar unter `https://DEIN-BENUTZERNAME.github.io/katalog-studio/`
5. Auf dem iPhone in Safari öffnen → Teilen → **Zum Home-Bildschirm**.

Bei einem **privaten** Repository ist GitHub Pages nur mit GitHub Pro/Team nutzbar.
Bei einem öffentlichen Repository kann jeder mit dem Link die Nettopreise sehen.

## Eingebaute Logik

- **Single-Split:** Set + Wanne + Reparaturschalter von der jeweiligen Doppelseite, Kältemittelleitungen
  in zölliger und metrischer Ausführung, Kondensatpumpe nur bei Geräten ohne integrierte Pumpe.
- **Multi-Split:** Indexsummen- und kW-Prüfung gegen S. 94/95, Warnung bei Überschreitung,
  Anschlussleitungen je Inneneinheit-Rohrmaß.
- **Simultan:** nur zugelassene Kombinationen, Verteiler als Pflichtposition.
- **VRF:** Auslastungsprüfung 50–130 %, **n−1 Verteiler bei n Inneneinheiten**, jeder Verteiler nach der
  Leistung dimensioniert, die hinter ihm noch anliegt (Klasse sinkt mit jedem Abzweig).
  Hauptstrecke und Anschlussleitungen je Inneneinheit getrennt, Pflichtzubehör automatisch.
- **Analyse:** Kundentext → Räume mit 100 W/m², Gerätevorschlag, Multi-Alternative.
- **Ausgabe:** Bestelltext / Angebot (Rabatt + Monteurstunden) / Intern mit frei wählbarem Empfänger.

## Eigene Daten

- **Signatur** (Name, Telefon, E-Mail): Tab *Ausgabe* → Modus *Angebot* → „Signatur bearbeiten".
- **Regionalcenter**: dort ebenfalls über „Regionalcenter verwalten".
- **Interner Empfänger**: im Modus *Intern* frei eintragbar.

Alle Eingaben werden lokal im Browser gespeichert (localStorage), nichts verlässt das Gerät.
