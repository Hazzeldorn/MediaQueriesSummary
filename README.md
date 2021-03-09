# Media Queries Summary

Seit CSS3 können ganze Stylesheets oder einzelne Regeln abhängig z.B. vom Gerätetyp oder der Bildschirmgrösse aktiviert bzw. deaktiviert werden. Dies wird mit Media Queries umgesetzt, welche inzwischen das A & O von responsivem Webdesign darstellen.

### Beispiele
Eine Media Query wird mit dem `@media`-Attribut und den dazugehörenden Regeln definiert:
```CSS
/* Abhängig von der Bildschirmgrösse */
@media screen and (min-width: 768px) { ... }

/* Abhängig vom Bildformat */
@media screen and (orientation: landscape) { ... }

/* Abhängig von der Ausgabesoftware */
@media print { ... }
```
Um Ressourcen zu sparen, können die `media`-Regeln direkt in den `<link>` tag geschrieben werden. Dadurch werden für unterschiedliche Ausgabegeräte eigene Stylesheets geladen.
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
- [Demo 1 &ndash; Mobile first breakpoints](https://hazzeldorn.github.io/MediaQueriesSummary/demo/demo-1.html)
- [Demo 2 &ndash; Print](https://hazzeldorn.github.io/MediaQueriesSummary/demo/demo-2.html)
- [Demo 3 &ndash; Device orientation & query nesting](https://hazzeldorn.github.io/MediaQueriesSummary/demo/demo-3.html)
- [Demo 4 &ndash; Multiple conditions (OR)](https://hazzeldorn.github.io/MediaQueriesSummary/demo/demo-4.html)
- [Demo 5 &ndash; NOT Keyword & Version 4 Features](https://hazzeldorn.github.io/MediaQueriesSummary/demo/demo-5.html)
- [Demo 6 &ndash; Responsive website example](https://hazzeldorn.github.io/MediaQueriesSummary/demo/demo-6.html)


---


### Quellen
- https://www.w3schools.com/css/css_rwd_mediaqueries.asp
- https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries
- https://caniuse.com/?search=media%20queries
- https://www.bram.us/2021/01/11/nested-media-queries/
- https://www.w3.org/TR/mediaqueries-5/
- https://bradfrost.com/blog/post/7-habits-of-highly-effective-media-queries/
