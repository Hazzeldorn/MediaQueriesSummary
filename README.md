# MediaQueries webcl Talk
Präsentation zu CSS Media Queries im Modul webcl an der FHNW

## Ideen für die Präsentation
- Kurze Präsentation zu Media-Queries
- Kurzer Überblick über verschiedene Einheiten (px, em, rem, %, vw, vh etc.) und deren Effek
- Best-Practices / Don'ts  (evtl. Inspiration von Frameworks wie Bootstrap?)
- Einfache Github-Pages Webseite mit Beispielen zum selber Ausprobieren freigeben (an Stelle eines Live-Demos um Zeit zu sparen)

---

## Was sind Media Queries?
Seit CSS3 können ganze Stylesheets oder einzelne Regeln abhängig vom Gerätetyp oder der Bildschirmgrösse aktiviert bzw. deaktiviert werden. Dies wird mit Media Queries umgesetzt, was inzwischen das A & O von responsivem Webdesign darstellt.

### Beispiele
Eine Media Query wird üblicherweise mit dem `@media`-Attribut und den dazugehörenden Regeln definiert:
```
/* Abhängig von Bildschirmgrösse */
@media only screen and (min-width: 768px) { ... }

/* Abhängig von Bildformat */
@media only screen and (orientation: landscape) { ... }

/* Abhängig von Ausgabesoftware */
@media print { ... }
```
Um Ressourcen zu sparen, kann man auch unterschiedliche Stylesheets für unterschiedliche Ausgabegeräte laden und die `media`-Regeln direkt in den `<link>` tag schreiben:
```
<link rel="stylesheet" type="text/css" href="print.css" media="print" />
```
Ausser im Internet Explorer gibt es zusätzlich die Möglichkeit, Media Queries zu verschachteln:
```
@media only screen and (max-width: 750px) {
  p {
    font-weight: bold;
  }
  @media (min-height: 500px) {
    p {
      background: yellow;
    }
  }
}
```


## Quellen
- https://www.w3schools.com/css/css_rwd_mediaqueries.asp
- https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries
- https://caniuse.com/?search=media%20queries
- https://www.bram.us/2021/01/11/nested-media-queries/
- https://www.w3.org/TR/mediaqueries-5/
