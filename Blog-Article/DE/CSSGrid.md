# CSS-Grid
## Was ist CSSGrid
CSSGrid ist ein Konzept in CSS, welches dem Entwickler erlaubt, das Layouting für eine Website ohne eigene Berechnungen im Styling durchführen zu müssen. 

In CSSGrid wird (im besten Fall) jedem angezeigtem HTML-Element einem Bereich (im Nachfolgenden area genannt) zugeordnet, im folgenden Beispiel sind die 'header', 'main', 'aside' & 'footer':

```html 
<div id="my-beautiful-webside">
    <header class="header">HEADER</header>
    <main class="main">MAIN</main>
    <aside class="aside">ASIDE</aside>
    <footer class="footer" >FOOTER</footer>
</div>
``` 

Mit dem zugehörigen css: 

```css
.header{
    grid-area: header
}

.main{
    grid-area: main
}

.aside{
    grid-area: aside
}

.footer{
    grid-area: footer
}
```

Die grid-area zuweisungen allein bewirken leider jedoch nichts, um die zuvor definierten areas nutzen zu können ist es notwendig, der Webside die display-Eigenschaft 'grid' zuzuweisen und eine Vorlage (im Nachfolgenden template genannt) zu definieren: 

```css 
#my-beautiful-webside {
    display: grid;
    grid-area-template: 'header header header', 'main, main, aside', 'footer, footer, footer';
}
```

## Was sind die Vor- und Nachteile von CSSGrid?

| Vorteile                                                      | Are                                                   |
| ------------------------------------------------------------- |-------------------------------------------------------| 
| schnell und unkompliziert umgesetzt                           | Änderungen im Nachhinein unter Umständen zeitaufwändig|
| keine Berechnungen im Style-Sheet nötig                       | Anpassungen zur Nutzung im IE11 erforderlich          |
| eigene Einheit zur Festlegung der Höhe/ Breite einer Area     |                                                       |
