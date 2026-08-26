# bericht49-site

Drei statische Seiten für den Kanal **Bericht49** und die Upload-Anwendung
**Bericht49 Uploader**. Sie werden für die App-Verifizierung bei den
Videoplattformen gebraucht: Dort muss eine öffentlich erreichbare Adresse für
Nutzungsbedingungen und Datenschutzerklärung angegeben werden.

| Datei | Inhalt |
|---|---|
| `index.html` | Was Bericht49 ist, die drei Profile, Kontakt, Impressum |
| `terms.html` | Nutzungsbedingungen für den Bericht49 Uploader |
| `privacy.html`| Datenschutzerklärung für Website und Anwendung |
| `style.css`   | gemeinsames Stylesheet, Kanalfarben |

Kein Framework, kein Skript, keine Schriftart und kein Bild von fremden
Servern – die Seiten funktionieren aus dem Dateisystem heraus genauso wie auf
GitHub Pages. Das Favicon steckt als Data-URI im HTML.

Farben wie im Video (`engine/config.py` des Engine-Projekts):
Hintergrund `#121a3a`, Akzent `#f7b731`.

## Noch einzutragen

Alle offenen Stellen stehen im HTML als `<span class="platzhalter">[…]</span>`
und werden auf der Seite gelb hinterlegt angezeigt – sie sind also nicht zu
übersehen. Zu ersetzen sind:

- Vor- und Nachname des Betreibers (Impressum, Nutzungsbedingungen, Datenschutz)
- Straße, Hausnummer, PLZ und Ort
- E-Mail-Adresse
- Bundesland für die zuständige Datenschutz-Aufsichtsbehörde
- Stand-Datum auf `terms.html` und `privacy.html`
- USt-IdNr.-Zeile im Impressum: eintragen oder streichen

Die Profil-Links zeigen auf YouTube, TikTok und Instagram, jeweils
`@bericht49`. Wenn eine andere Plattform gemeint ist, in `index.html` ändern.

## Vorschau

Die Dateien lassen sich direkt im Browser öffnen. Alternativ:

```bash
py -m http.server 8000
```

## Veröffentlichen

GitHub Pages, Branch `main`, Ordner `/` (root). Danach sind die Seiten unter
`https://<konto>.github.io/bericht49-site/` erreichbar.
