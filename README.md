# Ember-CLI-Password-Strength

This addon is an Ember-CLI wrapper for [zxcvbn](https://github.com/dropbox/zxcvbn), a "realistic password strength estimator".
In addition to bringing that package into your project, Ember-CLI-Password-Strength exposes a `password-strength` shim 
as an ES6 module you can import anywhere in your application, rather than using the Bower package's global variable.

## Installation

`ember install ember-cli-password-strength`

## Usage

Simply import the `password-strength` shim into your project:

```javascript
//components/foo.js
import Ember from 'ember';
import strength from 'password-strength';

const { Component, computed } = Ember;

export default Component.extend({
  password: '',

  strength: computed('password', function () {
    return strength(this.get('password'));
  })
});
```

Full documentation for the strength checking method can be found [here](https://github.com/dropbox/zxcvbn#usage).

## Contributing

This README outlines the details of collaborating on this Ember addon.

### Installation

* `git clone git@github.com:elwayman02/ember-cli-password-strength.git`
* `cd ember-cli-password-strength`
* `npm install`
* `bower install`

### Running

* `ember server`
* Visit your app at http://localhost:4200.

### Running Tests

* `npm test` (Runs `ember try:testall` to test your addon against multiple Ember versions)
* `ember test`
* `ember test --server`

### Building

* `ember build`

For more information on using ember-cli, visit [http://www.ember-cli.com/](http://www.ember-cli.com/).
