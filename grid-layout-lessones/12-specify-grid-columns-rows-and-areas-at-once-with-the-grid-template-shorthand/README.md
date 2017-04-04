## grid-template

We can use `grid-template-columns`, `grid-template-rows`& `grid-template-areas` to make up grid layout.

But is also a shorthand way to do so: `grid-template`.

```css
        .container {
            display: grid;
            height: 100vh;
            grid-gap: 10px;
            grid-template-areas:
                "nav-1 nav-2 nav-3"
                "main main nav-3";
            grid-template-columns: 2fr auto 1fr;
            grid-template-rows:
                [nav-start] 1fr
                [nav-end main-start] 5fr
                [main-end];
        }
```

The same as:

```css
        .container {
            display: grid;
            height: 100vh;
            grid-gap: 10px;
            grid-template:
                [nav-start] "nav-1 nav-2 nav-3" 1fr [nav-end]
                [main-start] "main main nav-3" 5fr [main-end]
                / 2fr auto 1fr;
        }
```

[Demo](https://embed.plnkr.co/lEJgGAZXTl6LEcwpCpNZ/)