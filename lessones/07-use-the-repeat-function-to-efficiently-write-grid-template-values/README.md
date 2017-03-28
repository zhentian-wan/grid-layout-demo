## Repeat

Using repeat:
```css
            grid-template-columns:
                repeat(
                    3, /*each row has 3 repeat items*/
                    minmax(10px, auto)
                    minmax(20px, auto)
                    minmax(40px, auto)
                    minmax(80px, auto)
                );
```

Add named grid line:

so that we can reuse those later
```css
        .container {
            display: grid;
            grid-gap: 10px;
            height: 100vh;
            grid-template-columns:
                [start] repeat(
                    3, /*each row has 3 repeat items*/
                    [col-xs-start] minmax(10px, auto)
                    [col-xs-end col-sm-start] minmax(20px, auto)
                    [col-sm-end col-md-start] minmax(40px, auto)
                    [col-md-end col-lg-start] minmax(80px, auto)
                    [col-lg-end]
                ) [end];
        }

        .box:nth-of-type(26){
            grid-column: col-sm-start / end;
        }
```