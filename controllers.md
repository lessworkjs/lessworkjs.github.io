# Controllers
Controllers contain the code to be executed by your routes.

These files are `autoloaded` as `functions` in your `serverless` configuration.

## Create a controller

Controllers are created with the `work` command.


```bash
node work make:controller HelloWorld
```

This creates the file `app/Http/Controllers/HelloWorldController.js`.

```js
'use strict';

class HelloWorldController extends require('lesswork-framework/Controller') {
  get() {
    response.success({
      hello: 'world'
    });
  }
}

module.exports = HelloWorldController;
```