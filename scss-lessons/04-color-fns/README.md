[SCSS DOC](http://sass-lang.com/documentation/Sass/Script/Functions.html)

```scss
$lighten_base: lighten($base, 25%);
$darken_base: darken($base, 25%);

$clb: complement($base);
$cllb: complement($lighten_base);
$cldb: complement($darken_base);

$light-color: scale_color($base, $alpha: -50%);
$dark-color: scale_color($base, $saturation: -35%);

background-image: linear-gradient($clb, $cllb, $cldb);
```