# AnyHTTP adapter for AngularJS

[AnyHTTP](https://github.com/argo-rest/any-http) adapter for the
[AngularJS](https://angularjs.org/) framework.

## Usage

This adapter is implemented as an ES6 module which can be installed
with [jspm](https://jspm.io) and loaded via
[SystemJS](https://github.com/systemjs/systemjs) as follows:

``` javascript
import 'any-http-angular';

import angular from 'angular';

var mod = angular.module('example', ['anyHttp']);

mod.factory('exampleFactory', ['anyHttp', function(anyHttp) {
  anyHttp.
    get('https://example.com').
    then(({body, headers}) => {
      console.log("body:", body);
      console.log("content-type:", headers['Content-Type']);
    });
}]);
```
