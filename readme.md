# notes

## removeEventListener

```js
elmt.addEventListener('click', function handler(ev) {
    this.removeEventListener(ev.type, handler);
});
```
