# notes

## removeEventListener

```js
elmt.addEventListener('click', function handler(ev) {
    // do some stuff
    this.removeEventListener(ev.type, handler);
});
```

## vertical scroll amount

```js
window.pageYOffset
```
[cross-browser](https://github.com/yields/scrolltop): `npm install scrolltop`

```js
var st = require('scrolltop');
console.log(st());
```

## scroll events with requestAnimationFrame

```js
var scrolltop = require('scrolltop');
var rafScroll = require('raf-scroll');
var offset = myElmt.offsetTop;

// parallax -- scroll at 1/3 normal speed
function update() {
  var scr = scrolltop();
  myElmt.style.top = (offset - (scr*0.3)) + 'px';
}

rafScroll.init();
rafScroll.add(update);
```

## accessible for clients without JS

index.html
```html
<!DOCTYPE html>
<html lang="en" class="no-js">
<head>
  <script>
    document.querySelector('html').className = '';
  </script>
</head>
<body>
  <div class="hidden">my content</div>
</body>
</html>
```

style.css
```css
.hidden {
  opactiy: 0;
}
.no-js .hidden {
  opactiy: 1 !important;
}
```
