### 01-getting up and running grid layout

Getting to know `grid-gap`, `grid-template-area` and `grid-area`.
 
```css
        .container {
            display: grid;
            grid-gap: 5px;
            grid-template-areas:
                    "header"
                    "section"
                    "aside-1"
                    "aside-2"
                    "footer";
        }
        
        
        header {
            grid-area: header;
        }
        
        @media (min-width: 700px) {
            .container {
                grid-template-areas:
                        "header header header"
                        "aside-1 section aside-2"
                        "footer footer footer";
            }
        }
               
```

