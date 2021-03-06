# MediaQueries Summary

## Was sind Media Queries?
Seit CSS3 können ganze Stylesheets oder einzelne Regeln abhängig vom Gerätetyp oder der Bildschirmgrösse aktiviert bzw. deaktiviert werden. Dies wird mit Media Queries umgesetzt, was inzwischen das A & O von responsivem Webdesign darstellt.

### Beispiele
Eine Media Query wird üblicherweise mit dem `@media`-Attribut und den dazugehörenden Regeln definiert:
```CSS
/* Abhängig von Bildschirmgrösse */
@media screen and (min-width: 768px) { ... }

/* Abhängig von Bildformat */
@media screen and (orientation: landscape) { ... }

/* Abhängig von Ausgabesoftware */
@media print { ... }
```
Um Ressourcen zu sparen, kann man auch unterschiedliche Stylesheets für unterschiedliche Ausgabegeräte laden und die `media`-Regeln direkt in den `<link>` tag schreiben:
```HTML
<link rel="stylesheet" type="text/css" href="print.css" media="print" />
```
Ausser im Internet Explorer gibt es zusätzlich die Möglichkeit, Media Queries zu verschachteln:
```CSS
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

### Demos
- [Mobile first breakpoints](https://hazzeldorn.github.io/MediaQueriesSummary/demo/demo-1.html)
- [Print](https://hazzeldorn.github.io/MediaQueriesSummary/demo/demo-2.html)
- [Device orientation & nesting](https://hazzeldorn.github.io/MediaQueriesSummary/demo/demo-3.html)
- [Multiple conditions (OR)](https://hazzeldorn.github.io/MediaQueriesSummary/demo/demo-4.html)
- [NOT Keywoard & Version 4 Features](https://hazzeldorn.github.io/MediaQueriesSummary/demo/demo-5.html)


## Quellen
- https://www.w3schools.com/css/css_rwd_mediaqueries.asp
- https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries
- https://caniuse.com/?search=media%20queries
- https://www.bram.us/2021/01/11/nested-media-queries/
- https://www.w3.org/TR/mediaqueries-5/
