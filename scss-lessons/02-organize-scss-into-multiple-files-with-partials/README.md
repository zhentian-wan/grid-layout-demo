## Organize SCSS into Multiple Files with Partials

If we import scss file into another scss file as partials, it doesn't
generate extra css file.

```scss
.color {
  color: blue;
}

@import "color";
```

```scss
// _color.scss

.red {
  color: lighten(red, 15%);
}
```

It generates only one css file:
```css
.color {
  color: blue; }

.red {
  color: #ff4d4d; }
```

If we don't use partials, then it generate another css file.

