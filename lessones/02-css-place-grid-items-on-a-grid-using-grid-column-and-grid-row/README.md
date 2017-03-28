### Grid-column, Grid-row and Grid-template-columns


```css
        .container {
            display: grid;
            grid-gap: 15px;
            height: 100vh;
            grid-template-columns: 100px 200px auto auto;
        }
        
        .grid-item:nth-of-type(2) {
            grid-row: span 2;
            /* the same as
            grid-row-start: 2;
            */
        }

        .grid-item:nth-of-type(6) {
            grid-column: 3 / span 2;
            /* the same as
            grid-column-start: 3;
            grid-column-end 5
            */
        }        
```

[DEMO](https://embed.plnkr.co/E9YGSWpIPlWZJDtDtVyN/)

