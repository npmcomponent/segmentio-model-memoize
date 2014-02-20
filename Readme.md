*This repository is a mirror of the [component](http://component.io) module [segmentio/model-memoize](http://github.com/segmentio/model-memoize). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/segmentio-model-memoize`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# model-memoize

  Memoizes the model objects returned from the server to reduce outbound requests and speed up initial page loading.

## Installation

    $ component install segmentio/model-memoize

## Examples

  Just `use` the plugin:

```js
var memoize = require('model-memoize');
var model = require('model');

var Person = model('person')
  .use(memoize)
  .attr('id')
  .attr('name');
```

  You can also pass in an array of models to be memoized from the beginning, which is useful for passing in models served from the server on initial page load:

```js
var Person = model('person')
  .attr('id')
  .attr('name')
  .use(memoize(window.people)); // array of `person` objects
```

  If you're passing in an array, make sure to define your Model's attributes first.

## License

  MIT
