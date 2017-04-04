## Nest grid

You can nest grid layout.

```html
<div class="grid grid--level-1">
    <div class="grid-item">1</div>
    <div class="grid-item">2</div>
    <div class="grid-item">3</div>
    <div class="grid grid--level-2">
        <div class="grid-item">i</div>
        <div class="grid-item">ii</div>
        <div class="grid-item">iii</div>
        <div class="grid-item">iv</div>
        <div class="grid-item">v</div>
        <div class="grid-item">vi</div>
    </div>
    <div class="grid-item">5</div>
    <div class="grid-item">6</div>
</div>
```

Then target each level to apply different layout:
```css
            display: grid;
        }

        .grid--level-1 {
            height: 100vh;
            grid-gap: 20px;
            grid-template-columns:
                repeat(auto-fill, minmax(200px, auto));
        }

        .grid--level-1 > .grid-item {
            background-color: cadetblue;
        }

        .grid--level-2 {
            grid-gap: 15px;
            color: white;
            grid-template-columns: repeat(3, auto);
        }

        .grid--level-2 > .grid-item {
            background-color: rebeccapurple;
        }
```

[DEMO](https://embed.plnkr.co/oG03AxTprC0F3Vq7OTgB/)