Ember load initializers
===========

About
-----

This is a fork of the official Ember load initializers. Added auto discover of exported initializers inside of a service.

```

/* inside service/my-service.js */

export default Ember.Service.extend({

    sayHello: function() {
    
        console.log("Hello from service");
    
    }

});

Initializer = {
  name: 'sayHello',
  initialize: function(container, app) {
    app.inject('route', 'sayHello', 'service:my-service');
  }
}


export {Initializer};
```

Ember loadInitializers is a tiny package to autoload your initializer files in EAK and ember-cli.

License
-------

Ember loadInitializers is [MIT Licensed](https://github.com/ember-cli/ember-load-initializers/blob/master/LICENSE.md).
