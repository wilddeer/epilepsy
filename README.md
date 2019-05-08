So, apparently, you can dinamically changethe the color in `<meta name="theme-color" content="#ffffff">`.

[Chech it out in your mobile browser](https://wilddeer.github.io/epilepsy/)

```html
<meta name="theme-color" content="#ffffff">

<script>
    let lastIndex = 0;
    const colors = ['#ff0000', '#ffff00', '#00ff00', '#00ffff', '#0000ff', '#ff00ff'];
    const tag = document.querySelector('meta[name="theme-color"]');

    setInterval(() => {
        tag.setAttribute('content', colors[lastIndex]);
        lastIndex += 1;
        if (lastIndex === colors.length) lastIndex = 0;
    }, 100);
</script>
```
