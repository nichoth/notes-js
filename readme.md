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
