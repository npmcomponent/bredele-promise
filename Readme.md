*This repository is a mirror of the [component](http://component.io) module [bredele/promise](http://github.com/bredele/promise). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/bredele-promise`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# promise

  > It feelds good to reinvent the wheel

  Promises implementation based on [emitter](htp://github.com/component/emitter). It follows [A+ spec](http://promises-aplus.github.io/promises-spec/).

## Installation

  Install with [component](http://component.io):

    $ component install bredele/promise

  Install with [nodejs](http://nodejs.orh):

    $ npm install bredele-promise

## API

### .then(fulfilled, rejected)

 Register callbacks to receive either a promise’s eventual value or the reason why the promise cannot be fulfilled .

```js
promise.then(function() {
  //on fulfilled
}, function() {
  //on rejected
});
```

 `then` arguments are optionals

### .resolve(value)

 Resolve/Fulfill promise with optional value.

```js
promise.resolve();
```

### .reject(reason)

 Reject promise with optional reason.

```js
promise.reject();
```

### .state

 Promise state is `pending` by default and may transition to either the `fulfilled` or `rejected` state.
 A promise which is `fulfilled` or `rejected` can not transition to another state.

```js
promise.state;
```

 `state` is private and should not be changed outside of the [`resolve`](#resolve) or [`reject`](#reject) handlers.


## Note

`promise` is part of a collection of asynchronous patterns based on [emitter](http://github.com/component/emitter):
  - [states](http://github.com/bredele/states)
  - [doors](http://github.com/bredele/doors)
  - [emitter-queue](http://github.com/bredele/emitter-queue)


## License

  The MIT License (MIT)

  Copyright (c) 2014 <copyright holders>

  Permission is hereby granted, free of charge, to any person obtaining a copy
  of this software and associated documentation files (the "Software"), to deal
  in the Software without restriction, including without limitation the rights
  to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
  copies of the Software, and to permit persons to whom the Software is
  furnished to do so, subject to the following conditions:

  The above copyright notice and this permission notice shall be included in
  all copies or substantial portions of the Software.

  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
  LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
  THE SOFTWARE.
