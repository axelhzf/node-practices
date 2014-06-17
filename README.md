# Sinon sandbox

```js
var expect = require("chai").expect;
var sinon = require("sinon");

var sandbox;

beforeEach(function () {
  sandbox = sinon.sandbox.create();
});

afterEach(function () {
  sandbox.restore();
});

describe("", function () {
  it("", function () {
    sandbox.stub(obj, "method", function () {});
  });
});
```

# co

## simple block

```js
var co = require("co");
co(function* () {
  yield a();
  yield b();
})();
```

## test block

```js
var co = require("co");
it("...", function (done) {
  co(function () {

  })(done);
});
```

## co-parallel

```js
var co = require("co");
var parallel = require("co-parallel");

var urls = [
  'http://google.com',
  'http://yahoo.com',
  'http://facebook.com'
];

function* get() {
  ...
}

co(function *() {
  var reqs = url.map(get);
  var res = yield parallel(reqs, 2);
})();
```