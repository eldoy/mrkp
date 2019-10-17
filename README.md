# MRKP

Create HTML with a single Javascript function.

Isomorphic, works in both the browser and in Node. Only 218 bytes minified.

### Install
```
npm i mrkp
```

### Usage
In node:
```javascript
var h = require('mrkp')
```

In the browser:
```html
<script src="/js/mrkp.min.js>
<script>
function h(n,t,e,i){return"<"+(n||"")+((e=Object.keys(e||{}).map(function(n){return!0===e[n]?n:n+'="'+e[n]+'"'})).length?" "+e.join(" "):"")+">"+(t||"")+("string"==typeof i?i:(i||[]).join(""))+(null===t?"":"</"+n+">")}
</script>
```

Make HTML:
```javascript
h('div', 'Content', { class: 'active' }, [
  h('ul', '', {}, [
    h('li', 'Meat'),
    h('li', 'Milk'),
    h('li', 'Butter')
  ])
])
```
MIT Licensed. Enjoy!
