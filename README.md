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

# Sequelize

```js
var task = Task.build({ title: 'foo', description: 'bar', deadline: new Date() })
task.save();

vas task = Task.create({ title: 'foo', description: 'bar', deadline: new Date() });

task.title = "b";
task.save();

task.updateAttributes({title: "b"})

task.destroy();


User.bulkCreate([{ username: 'barfooz', isAdmin: true }, { username: 'foo', isAdmin: true }])
User.update({title: "B"}, {id: 1})

```