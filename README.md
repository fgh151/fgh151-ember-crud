# fgh151-ember-crud


## Installation

* `cd /projet/folder`
* `npm install fgh151-ember-crud`

## Running

* `ember g fgh152-crud foo`
* in `config/enviroment.js` add pod prefix, like
```js
module.exports = function(environment) {
  var ENV = {
    modulePrefix: 'project',
    podModulePrefix: 'project/pods',
    ...
  }
}
```

* Add rules to `app/router.js`:
```js
  ...
  this.route('foos', function() {
    this.route('show', { path: ':foo_id' });
    this.route('new');
    this.route('edit', { path: ':foo_id/edit' });
  });
  ...
```
