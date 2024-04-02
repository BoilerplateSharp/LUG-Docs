---
title: How to Flexbox
description: Eine kurze Einleitung zur Display flex Eigenschaft in CSS
---

Die Flexbox in CSS ist ein ein-Dimensionales Layout, welches uns diverse Einstellungen für die Plazierung von Kind-Elementen gibt.

Die folgenden Grafiken stammen von [css-tricks.com](https://css-tricks.com/snippets/css/a-guide-to-flexbox/).

![](https://css-tricks.com/wp-content/uploads/2018/10/01-container.svg)

```css
.container {
  display: flex;
}
```

![the four possible values of flex-direction being shown: top to bottom, bottom to top, right to left, and left to right](https://css-tricks.com/wp-content/uploads/2018/10/flex-direction.svg)

```css
.container {
  flex-direction: row | column;
}
```

![two rows of boxes, the first wrapping down onto the second](https://css-tricks.com/wp-content/uploads/2018/10/flex-wrap.svg)

```css
.container {
  flex-wrap: nowrap | wrap;
}
```

![flex items within a flex container demonstrating the different spacing options](https://css-tricks.com/wp-content/uploads/2018/10/justify-content.svg)

```css
.container {
  justify-content: flex | flex | center | space-around;
}
```

![demonstration of differnet alignment options, like all boxes stuck to the top of a flex parent, the bottom, stretched out, or along a baseline](https://css-tricks.com/wp-content/uploads/2018/10/align-items.svg)

```css
.container {
  align-items: start | end | center | stretch | baseline;
}
```

