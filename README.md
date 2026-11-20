# Landingpage: Handgemachtes Hundehalsband mit Namensschild

Statische Seite, kein Build-Schritt nötig. Alles in `index.html` (HTML, CSS, JS).

## Dateien
- `index.html` Seite inkl. Konfigurator, Slider, FAQ-Akkordeon, SEO-Tags, FAQ-Schema
- `images/` deine Fotos (Dateinamen siehe `images/README.txt`)
- `impressum.html`, `datenschutz.html` Platzhalter, bitte mit echten Texten füllen
- `robots.txt`, `sitemap.xml`, `vercel.json` Hosting- und SEO-Dateien

## Lokal ansehen
`index.html` im Browser öffnen, oder `python3 -m http.server` im Ordner und http://localhost:8000 aufrufen.

## Deployment (Vercel, empfohlen)
**Variante A: ohne GitHub (am schnellsten)**
1. `npm i -g vercel`, im Ordner `vercel` ausführen, Fragen mit Enter bestätigen.
2. Für die Live-Version: `vercel --prod`.
3. Updates: Dateien ändern, erneut `vercel --prod`.

**Variante B: mit GitHub (automatische Updates)**
1. Ordner als neues GitHub-Repository hochladen.
2. Auf vercel.com "Add New Project", Repository wählen, Framework "Other", Deploy.
3. Ab jetzt veröffentlicht jede Änderung im Repository (Branch `main`) automatisch die Seite. Änderungen in anderen Branches bekommen einen Vorschau-Link.

**Eigene Domain:** In Vercel unter Project, Settings, Domains die Domain eintragen und die angezeigten DNS-Einträge beim Domain-Anbieter setzen.

Alternativen: Netlify (Ordner per Drag and Drop), GitHub Pages, oder jeder Webspace (Dateien per FTP hochladen).

## Vor dem Livegang (Checkliste)
- [ ] Alle `[Platzhalter]` ersetzen: Marke, Ort, Preis, Versand, Material, Lieferzeit, Größen-Tabelle (Rassen, cm, kg), Kundenzitate
- [ ] Bilder in `images/` ablegen
- [ ] `ORDER_EMAIL` im Script am Ende der `index.html` auf deine Adresse setzen. Der Button "Bestellen" öffnet aktuell eine E-Mail mit der Auswahl. Später durch Shop oder Zahlungslink ersetzbar.
- [ ] `SIZE_LIMITS` (Richtwerte für XS/S/M/L) an deine echte Größentabelle anpassen
- [ ] Domain `www.example.de` ersetzen in `index.html` (canonical, og:url, og:image), `robots.txt`, `sitemap.xml`
- [ ] **`<meta name="robots" content="noindex, nofollow">` aus `index.html` entfernen**, sonst taucht die Seite nie bei Google auf
- [ ] Product-Schema (auskommentiert in `index.html`) aktivieren, Preis eintragen
- [ ] Impressum und Datenschutzerklärung mit echten Texten füllen (Pflicht in Deutschland)
- [ ] Schriften selbst hosten (Google Fonts nachladen ist in der EU datenschutzrechtlich heikel), z. B. woff2-Dateien von Poppins und Nunito in `/fonts` und per `@font-face` einbinden
- [ ] Wenn du Cookies, Tracking oder Analytics einbindest: Cookie-Hinweis ergänzen
- [ ] Seite in Google Search Console anmelden und `sitemap.xml` einreichen
- [ ] Mit https://pagespeed.web.dev und auf einem echten Handy testen
