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


Things to know:

* If importing partial file, won't generate a new css file
* If importing normal scss file, it will generate a new css file

So when we should use partial import or not, you can think that 
**whether this file should be used when app first loading?** 
If it **yes**, then use partial import, if **not**, then normal import.
The reason behind that is because browser will loading main css (the main.scss file that import other scss files ) file first.
 After this main.css file loaded, then browser will start loading other css file.
  
* Only partial file's variable can be shared across the rest of partial file. But it also require you import that partial file which has variables defines into main.scss file before the rest partial files.
  
```scss
/*
 About using variable

 There are tow cases when using variable

 1. none partial file (provider) + none partial file
    Variable only available for its own file scope.
    If you want to use one variable inside file A from file B
    You have to import file A into file B.

 2. partial file (provider) + none partial file
    If you have an variable defined in partial file, and you want to
    use it inside none partial file, you also need to import partial
    file into none partial file.

 3. partial file (provider) + partial file
    If you have an variable defined in partial file A, and you want to use it
    inside another partial file B, you have to import file A into main.scss file
    before you import file B into main.scss. Then you can use variable inside file A
    inside file B.
*/
```  