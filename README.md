# GENERAL Katalog-Studio 2026/27

Webshop / Konfigurator auf Basis der GENERAL Klimaanlagen-Preisliste 2026/27 (gültig ab 01.07.2026).
Eine einzige Datei (`index.html`), keine Abhängigkeiten, läuft komplett offline im Browser.
Alle Preise netto.

**Bilder:** Für Premium-Wandmodelle (weiß und anthrazit) sind Produktfotos und Szenen-Banner hinterlegt.
Alle übrigen Geräte nutzen Bauform-Silhouetten. Weitere Bilder lassen sich in `data.assets`
(Schlüssel `prod:NAME` und `ban:NAME`) und `data.assetMap` (Serienname → Schlüssel) ergänzen.

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
- **Auslegungs-Import:** Datei per Drag & Drop oder Auswahl laden (TXT, CSV, XLSX, PDF, JSON) oder Text
  einfügen. Erkannt werden Artikelnummern, Modellbezeichnungen und vollständige **Fujitsu-Anlagen-
  protokolle**: Materialliste 1.1 (Modell | Menge | Typ), Rohrleitungstabelle 1.2 (Längen je Durchmesser
  → 25-m-Ringe) und Kältemittelmenge 1.3. Typbezeichnungen aus älteren Auslegungen (z. B. AUXB007GLEH)
  werden über Baureihe und Baugröße dem aktuellen Nachfolger zugeordnet und als solche markiert;
  Verteiler-Typen (UTP-AX054A/090A/180A/567A, UTP-BX…) werden direkt auf die Katalog-Artikelnummern
  gemappt. Pflichtzubehör zum erkannten Außengerät kommt automatisch dazu. Mengen sind korrigierbar,
  mehrdeutige Typen lassen sich je Position umstellen – danach direkt „Als Angebot übernehmen".
  Hinweis: PDF und XLSX benötigen beim ersten Mal eine Internetverbindung (Lesemodule von cdnjs);
  offline funktionieren TXT, CSV und eingefügter Text uneingeschränkt.
- **Kopfbild:** oben auf allen Seiten, per ✕ ausblendbar und über die schmale Leiste wieder einblendbar.
- **Suche:** globale Suchleiste über alle Sets, Innen- und Außeneinheiten, VRF und Zubehör
  (Modell, Serie oder Artikelnummer, mehrere Begriffe kombinierbar).
- **Analyse:** Kundentext → Räume mit 100 W/m². Je Raum ist das vorgeschlagene Gerät über ein
  Auswahlfeld frei änderbar (alle Sets, nach Serie gruppiert, mit Auslastungsanzeige),
  dazu „Alle Sets übernehmen" und die Multi-Alternative.
- **Zubehör-Sheets:** sämtliche Kondensatpumpen (Refco Vamp-F / Vamp-X / Vamp-CDK inkl. Adapter,
  S. 213) und Fernbedienungen stehen bei jedem System zur Auswahl (eingeklappt); empfohlen wird nur,
  was das gewählte Gerät wirklich braucht. Siccom/Eckerle stehen als Vorgängerprogramm weiterhin im
  Zubehör-Tab, werden aber nicht mehr vorgeschlagen.
- **Kältemittelleitungen:** je Leitungsart getrennt (Flüssigkeit / Sauggas), jeweils zöllig mit
  metrischer Alternative. Über 19,05 mm zöllig bzw. 22,00 mm metrisch führt der Katalog keine
  Ringware – dort erscheint ein Hinweis auf Stangenware statt eines falschen Artikels.
- **Ausgabe:** Bestelltext / Angebot (Rabatt + Monteurstunden) / Intern mit frei wählbarem Empfänger.

## Eigene Daten

- **Signatur** (Name, Telefon, E-Mail): Tab *Ausgabe* → Modus *Angebot* → „Signatur bearbeiten".
- **Regionalcenter**: dort ebenfalls über „Regionalcenter verwalten".
- **Interner Empfänger**: im Modus *Intern* frei eintragbar.

Alle Eingaben werden lokal im Browser gespeichert (localStorage), nichts verlässt das Gerät.
