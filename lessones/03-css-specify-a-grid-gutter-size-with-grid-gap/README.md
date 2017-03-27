## Grid-gap and fr unit

```css
        .container {
            display: grid;
            height: 100vh;
            grid-gap: 10px 20px;
            /*
                grid-row-gap: 10px;
                grid-column-gap: 20px;
            */
            grid-template-columns: 1fr 2fr 1fr;
        }
```