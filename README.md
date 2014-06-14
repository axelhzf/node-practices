# Sinon sandbox

````js
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
````
