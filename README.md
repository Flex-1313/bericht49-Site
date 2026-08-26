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

## Angaben

Betreiber, Anschrift, E-Mail und die zuständige Aufsichtsbehörde sind
eingetragen (Stand 26.08.2026). Ändert sich etwas, steht es an diesen Stellen:

- `index.html` – Impressum (Betreiber, Anschrift, E-Mail, Verantwortlicher
  nach § 18 Abs. 2 MStV) und der Kontaktabschnitt darüber
- `terms.html` – § 1 (Betreiber mit Anschrift), § 8 (Kontakt), Stand-Datum
- `privacy.html` – Abschnitt 1 (Verantwortlicher), Abschnitt 5
  (Aufsichtsbehörde), Stand-Datum

Eine USt-IdNr. gibt es nicht; die Zeile fehlt deshalb im Impressum. § 5 DDG
verlangt sie nur, wenn eine vorhanden ist.

Die Profil-Links zeigen auf YouTube, TikTok und Instagram, jeweils
`@bericht49`. Wenn eine andere Plattform gemeint ist, in `index.html` ändern.

## URL-Verifizierung

`tiktokuu4xI6SZXcZCfO2uXDtDKjY7SUvLayIq.txt` im Wurzelverzeichnis ist die
Signaturdatei für die URL-Prefix-Verifizierung im TikTok-Entwicklerportal
(Prefix `https://flex-1313.github.io/bericht49-Site/`). Sie darf nicht
verändert oder gelöscht werden, solange die App dort registriert ist.

Für die Verifizierung gilt: nur die Adresse **mit** Schrägstrich am Ende
benutzen. Ohne ihn antwortet GitHub Pages mit 301, und TikTok wertet eine
Weiterleitung als ungültig.

## Vorschau

Die Dateien lassen sich direkt im Browser öffnen. Alternativ:

```bash
py -m http.server 8000
```

## Veröffentlichen

GitHub Pages, Branch `main`, Ordner `/` (root). Danach sind die Seiten unter
`https://<konto>.github.io/bericht49-site/` erreichbar.
