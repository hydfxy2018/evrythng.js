# evrythng.js [![Build Status](https://travis-ci.org/evrythng/evrythng.js.svg?branch=v5.x)](https://travis-ci.org/evrythng/evrythng.js) [![Coverage Status](https://coveralls.io/repos/github/evrythng/evrythng.js/badge.svg?branch=v5.x)](https://coveralls.io/github/evrythng/evrythng.js?branch=v5.x)
[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](http://standardjs.com)

## TODO
* [x] - Unit tests for Property
* [x] - Unit tests for Product resources
* [x] - Add Action entity
* [x] - Solve Collection circular reference problem
* [x] - Unit tests for Action
* [x] - Add Geolocation utils
* [x] - Unit tests for Thng resources
* [ ] - Add Location entity
* [ ] - Complete collection entity
* [x] - Replace individual fetchMock.mocks with apiMock
* [ ] - Unit tests for url utils
* [ ] - Reconsider ES6 module stubbing with aggregator modules and named exports (https://github.com/eventualbuddha/rollup-plugin-stub)

## Getting started

### Install evrythng.js using npm.

```javascript
npm install evrythng
```

Then require it into any module.

```javascript
const EVT = require('evrythng')

EVT.api({
  url: '/thngs'
  method: 'get'
}).then(console.log)
```

### Browser

To use evrythng from a browser, download `dist/evrythng.min.js` or use a CDN such as CDNJS or jsDelivr.

Then, add it as a script tag to your page:

```html
<script src="evrythng.min.js"></script>
<script>
    EVT.api({
      url: '/thngs'
      method: 'get'
    }).then(console.log)
</script>
```

Or use an AMD loader (such as RequireJS):

```javascript
require(['./evrythng.min.js'], EVT => {
    EVT.api({
      url: '/thngs'
      method: 'get'
    }).then(console.log)
})
```

If you're using browserify, the `evrythng` npm module also works from the browser.
