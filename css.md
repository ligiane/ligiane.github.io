# CSS

* **Box model:** Todo elemento no HTML é uma caixa. Controlamos seu tamanho com width, sua borda com border e ainda temos as margens externas e internas com margin e padding. Box model é como todas essas propriedades se relacionam pra determinar o tamanho final do elemento.

* **box-sizing: border-box:** indica que o tamanho da caixa levará em conta a borda -- ou seja, o width será a soma do conteúdo com a borda e o padding, diferente do comportamento padrão do box model.

---

[CSS first steps](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps)

[Reference - Codrops](https://tympanus.net/codrops/css_reference/)

[Devdocs](https://devdocs.io/css/)

[Keyword index - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Keyword_index)

[CSS Reference - W3C](https://www.w3schools.com/cssref/)

[Estelle Weyl - Slides](https://estelle.github.io/cssmastery)

[Train your CSS skills with online games](https://dev.to/paco_ita/train-your-css-skills-with-online-games-4ah3)

## Selectors

[CSS Selector Reference](https://www.w3schools.com/cssref/css_selectors.asp)

[Cascade and inheritance](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Cascade_and_inheritance)

[Slides](https://estelle.github.io/cssmastery/selectors/#slide1)

[Specifishity](http://specifishity.com/specifishity.pdf)

[Pseudo-classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)

[Pseudo-elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements)

[A Whole Bunch of Amazing Stuff Pseudo Elements Can Do](https://css-tricks.com/pseudo-element-roundup/)

[Generated Content](https://estelle.github.io/cssmastery/generated)

[The Shapes of CSS](https://css-tricks.com/the-shapes-of-css/)

## Layout

[Learn CSS Layout](https://learnlayout.com/)

[float](https://developer.mozilla.org/en-US/docs/Web/CSS/float)

[clear](https://developer.mozilla.org/en-US/docs/Web/CSS/clear)

## Media Queries

[Slides](https://estelle.github.io/cssmastery/media)

[Using media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)

[CSS Media Queries - Examples](https://www.w3schools.com/css/css3_mediaqueries_ex.asp)

[CSS Media Queries for Desktop, Tablet, Mobile](https://gist.github.com/gokulkrishh/242e68d1ee94ad05f488)

[@media](https://developer.mozilla.org/en-US/docs/Web/CSS/@media)

[@supports](https://developer.mozilla.org/en-US/docs/Web/CSS/@supports)

## Colors

[Slides](https://estelle.github.io/cssmastery/colors)

[Colors - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value)

## Appearance

[Appearance](https://developer.mozilla.org/en-US/docs/Web/CSS/appearance)

## Flexbox

[Slides](https://estelle.github.io/cssmastery/flexbox)

[Basic concepts of flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)

[A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

[Flexbox - Codepen blog](https://codepen.io/rikstar/post/flexbox)

[Flexbox playground - Codepen](https://codepen.io/enxaneta/full/adLPwv/)

[Flexbox Properties Demonstration - Codepen](https://codepen.io/justd/full/yydezN/)

[Flexbox Froggy Game](https://codepip.com/games/flexbox-froggy/)

## Tables

[Slides](https://estelle.github.io/cssmastery/tables)

## Grid CSS

[Slides](https://estelle.github.io/cssmastery/grid)

[CSS Grid Layout - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)

[Grid by Example](https://gridbyexample.com/examples)

[A Complete Guide to Grid CSS](https://css-tricks.com/snippets/css/complete-guide-grid/)

[Introduction to CSS Grid Layout](https://mozilladevelopers.github.io/playground/css-grid)

[CSS Grid Garden Game](https://cssgridgarden.com/)

[CSS Grid: illustrated introduction](https://dev.to/mustapha/css-grid-illustrated-introduction-52l5)

## Backgrounds & Borders

[Slides](https://estelle.github.io/cssmastery/borders/)

## Transforms

[Slides](https://estelle.github.io/cssmastery/transforms)

## Transitions and Animations

[Slides](https://estelle.github.io/cssmastery/animations/)

## clip-path

[clip-path - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/clip-path)

[Clippy tool](https://bennettfeely.com/clippy/)

[CSS and SVG Masks - Codepen](https://codepen.io/yoksel/full/fsdbu/)

## background-color hack to show page elemens

[My favorite CSS hack](https://dev.to/gajus/my-favorite-css-hack-32g3)

```css
* {
  background-color: rgba(255, 0, 0, 0.2);
}
* * {
  background-color: rgba(0, 255, 0, 0.2);
}
* * * {
  background-color: rgba(0, 0, 255, 0.2);
}
* * * * {
  background-color: rgba(255, 0, 255, 0.2);
}
* * * * * {
  background-color: rgba(0, 255, 255, 0.2);
}
* * * * * * {
  background-color: rgba(255, 255, 0, 0.2);
}
* * * * * * * {
  background-color: rgba(255, 0, 0, 0.2);
}
* * * * * * * * {
  background-color: rgba(0, 255, 0, 0.2);
}
* * * * * * * * * {
  background-color: rgba(0, 0, 255, 0.2);
}
```

## Using CSS to highlight images with no alt tags

```css
img:not([alt]) {
  filter: grayscale(100%);
}
```
