# TianTian Markt Website

Statische Beispiel-Webseite für den TianTian Markt.

## Struktur

```text
.
├── index.html
├── impressum.html
├── datenschutz.html
├── styles.css
├── script.js
├── favicon.svg
├── robots.txt
├── sitemap.xml
└── partials
    ├── nav.html
    └── footer.html
```

## Besonderheiten

- Statische HTML/CSS/JS-Webseite
- Sprachumschaltung per JavaScript: Deutsch, Englisch, Chinesisch, Japanisch
- Gemeinsame Navigation in `partials/nav.html`
- Gemeinsamer Footer in `partials/footer.html`
- Separate Seiten für Impressum und Datenschutz
- Dummy-Rechtstexte, die vor Veröffentlichung ersetzt/geprüft werden müssen

## Lokal testen

Da `nav.html` und `footer.html` per `fetch()` geladen werden, sollte die Seite über einen lokalen Webserver geöffnet werden, nicht direkt per Doppelklick als Datei.

Beispiel:

```bash
python3 -m http.server 8000
```

Dann öffnen:

```text
http://localhost:8000
```

## GitHub Pages

Alle Dateien in das Repository kopieren und GitHub Pages für den Branch aktivieren. Danach sollte die Seite statisch ausgeliefert werden.

## Vor Veröffentlichung anpassen

- Telefonnummer
- E-Mail-Adresse
- Impressumsdaten
- Datenschutzerklärung
- finale Domain in `sitemap.xml` und `robots.txt`
- echte Karten-/Standortintegration


## Hinweis zu Partials und lokalem Öffnen

`partials/nav.html` und `partials/footer.html` werden per JavaScript eingebunden.

Empfohlen zum lokalen Testen:

```bash
python3 -m http.server 8000
```

Danach öffnen:

```text
http://localhost:8000
```

Diese Version enthält zusätzlich einen JavaScript-Fallback, damit Navigation und Footer auch beim direkten Öffnen per `file://` angezeigt werden.
