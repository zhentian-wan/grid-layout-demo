## Name grid line

Syntax like:
```css
            grid-template-columns:
            [left-sidebar-start] 1fr
            [main-content-start] 2fr
            [right-sidebar-start] 1fr;
```
We can named those whatever we want to.

We can also give multi name to one column:
```css
            grid-template-columns:
            [left-sidebar-start] 1fr
            [left-sidebar-end main-content-start] 2fr
            [main-content-end right-sidebar-start] 1fr
            [right-sidebar-end];
```
And we tell what the last column line is `right-sidebar-end`, later we can use this name like:
```css
        .footer {
            grid-column: main-content-start / right-sidebar-end;
        }
```