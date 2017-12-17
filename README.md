# Login-Fire

<p align="center">
  <img alt="login-fire" src="Login-Fire@4x.png" width="200">
</p>

<p align="center">
Simple way to add authentication to your app using <a href="https://firebase.google.com/docs/auth/">Firebase Auth</a>.
</p>

<p align="center">
  <a href="https://beta.webcomponents.org/element/convoo/login-fire"><img src="https://img.shields.io/badge/webcomponents.org-published-blue.svg"></a>
  <a href="https://gitter.im/convoo/login-fire"><img src="https://img.shields.io/badge/gitter-join%20chat-brightgreen.svg"></a>
  <a href="http://waffle.io/convoo/login-fire"><img src="https://badge.waffle.io/convoo/login-fire.svg?label=In%20Progress&title=In%20Progress"></a>
</p>

---

## Overview & Demo

The following elements are available:
* `<login-fire-button>` for single provider authentication
* `<login-fire-social>` for multiple provider authentication
* `<login-fire-form>` for email and password authentication 
* `<login-fire>` for all of the above.

The goal of the \<login-fire\> elements is to provide a simple to setup, elegant UI for authentication using [Firebase Auth](https://firebase.google.com/docs/auth/).

Our demo is available on [webcomponents.org](https://www.webcomponents.org/element/convoo/login-fire/demo/demo/index.html).

Note: login-fire is **not** associated with [Firebase](https://firebase.google.com/). This collection of components is based on [polymerfire](https://github.com/firebase/polymerfire).

## Install

```
bower install login-fire --save
```


## \<login-fire\>

Add authentication with email and password as well as federated identity providers (Google, Facebook, Twitter, GitHub, Anonymous) to your app. 

```html
<link rel="import" href="/bower_components/login-fire/login-fire.html">
```

<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="../polymerfire/firebase-app.html">
    <link rel="import" href="login-fire.html">
    <div>
      <template is="dom-bind">
        <next-code-block></next-code-block>
      </template>
    </div>
  </template>
</custom-element-demo>
```
-->
```html
<firebase-app
  name="login"
  api-key="AIzaSyAhoCXxkY-ffNwA_7L7HIwBVpASYj1btNE"
  auth-domain="convoo-login-demo.firebaseapp.com"
  database-url="https://convoo-login-demo.firebaseio.com">
</firebase-app>

<login-fire
  app-name="login"
  providers="google, facebook, twitter, github, anonymous" 
  user="{{user}}"
  signed-in="{{signedIn}}">
</login-fire>
```

## \<login-fire-social\>

Add multiple federated identity providers authentication to your app with [Firebase Auth API](https://firebase.google.com/docs/auth/).

```html
<link rel="import" href="/bower_components/login-fire/login-fire-social.html">
```

<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="../polymerfire/firebase-app.html">
    <link rel="import" href="login-fire-social.html">
    <div>
      <template is="dom-bind">
        <next-code-block></next-code-block>
      </template>
    </div>
  </template>
</custom-element-demo>
```
-->
```html
<firebase-app
  name="social"
  api-key="AIzaSyAhoCXxkY-ffNwA_7L7HIwBVpASYj1btNE"
  auth-domain="convoo-login-demo.firebaseapp.com"
  database-url="https://convoo-login-demo.firebaseio.com">
</firebase-app>

<login-fire-social
  app-name="social"
  providers="google, facebook, twitter, github, anonymous" 
  user="{{user}}"
  signed-in="{{signedIn}}">
</login-fire-social>
```


## \<login-fire-form\>

Add email-password authentication to your app with [Firebase Auth API](https://firebase.google.com/docs/auth/).

```html
<link rel="import" href="/bower_components/login-fire/login-fire-form.html">
```

<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="../polymerfire/firebase-app.html">
    <link rel="import" href="login-fire-form.html">
    <div>
      <template is="dom-bind">
        <next-code-block></next-code-block>
      </template>
    </div>
  </template>
</custom-element-demo>
```
-->
```html
<firebase-app
  name="email"
  api-key="AIzaSyAhoCXxkY-ffNwA_7L7HIwBVpASYj1btNE"
  auth-domain="convoo-login-demo.firebaseapp.com"
  database-url="https://convoo-login-demo.firebaseio.com">
</firebase-app>

<login-fire-form
  app-name="email"
  user="{{user}}"
  signed-in="{{signedIn}}">
</login-fire-form>
```

## \<login-fire-button\>

A button for a single federated identity provider (Google, Facebook, Twitter, GitHub, Anonymous) that allows users to sign-in to and sign-out from your app using [Firebase Auth API](https://firebase.google.com/docs/auth/).

```html
<link rel="import" href="/bower_components/login-fire/login-fire-button.html">
```
<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="../polymerfire/firebase-app.html">
    <link rel="import" href="login-fire-button.html">
    <div>
      <template is="dom-bind">
        <next-code-block></next-code-block>
      </template>
    </div>
  </template>
</custom-element-demo>
```
-->
```html
<firebase-app
  name="button"
  api-key="AIzaSyAhoCXxkY-ffNwA_7L7HIwBVpASYj1btNE"
  auth-domain="convoo-login-demo.firebaseapp.com"
  database-url="https://convoo-login-demo.firebaseio.com">
</firebase-app>

<login-fire-button app-name="button" provider="google" user="{{user}}"></login-fire-button>
<login-fire-button app-name="button" provider="facebook" user="{{user}}"></login-fire-button>
<login-fire-button app-name="button" user="{{user}}"></login-fire-button>
```

## Signing Out

To sign out, access a `login-fire` element and call its `signOut` function.

Example:

```html
<a on-tap="_signOut">Sign Out</a>
```

```javascript
_signOut: function(e){
  this.$$('login-fire').signOut();
  // or
  // this.$$('login-fire-button').signOut();
  // or
  // this.$$('login-fire-social').signOut();
  // or
  // this.$$('login-fire-form').signOut();
}
```

## Debugging

To make it easier to debug, we've added the `debug` attribute. Set the "debug" attribute of the element to `true` to see more details about its variables' values.

Example:

```html
<login-fire-form app-name="email" debug></login-fire-form>
```

### Styling

Style the buttons with CSS as you would a normal DOM element. A few custom properties and mixins are available. The detailed lists are on each element's documentation page.


## Contributing

### Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your application locally.

### Viewing Your Application

```
$ polymer serve
```

### Building Your Application

```
$ polymer build
```

This will create a `build/` folder with `bundled/` and `unbundled/` sub-folders
containing a bundled (Vulcanized) and unbundled builds, both run through HTML,
CSS, and JS optimizers.

You can serve the built versions by giving `polymer serve` a folder to serve
from:

```
$ polymer serve build/bundled
```

### Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.

### Workflow

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`

Optional but highly encouraged: Follow [this commit guide](https://conventionalcommits.org/)

4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request. :D

## License

[MIT](https://github.com/convoo/login-fire/blob/master/LICENSE)

## Credits

Logo: Fingerprint by Gregor Cresnar from the Noun Project