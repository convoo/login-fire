# Login-Fire

<p align="center">
  <img alt="login-fire" src="LoginFire400.png" width="200">
</p>

<p align="center">
Simple way to add authentication to your app using firebase.
</p>

<p align="center">
  <a href="https://beta.webcomponents.org/element/convoo/login-fire"><img src="https://img.shields.io/badge/webcomponents.org-published-blue.svg"></a>
  <a href="https://gitter.im/convoo/login-fire"><img src="https://img.shields.io/badge/gitter-join%20chat-brightgreen.svg"></a>
  <a href="http://waffle.io/convoo/login-fire"><img src="https://badge.waffle.io/convoo/login-fire.svg?label=In%20Progress&title=In%20Progress"></a>
</p>

---

## Install

```
bower install login-fire --save
```


## \<login-fire\>

Add email and password authentication as well as social provider authentication to your app. 
If you want to only add social authentication or only email authentication please use \<social-login-fire\> or \<email-login-fire\> instead
until [issue 27](https://github.com/convoo/login-fire/issues/27) is closed.

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
<login-fire email-password anonymous twitter github google facebook app-name="login" user="{{user}}" signed-in="{{signedIn}}"></login-fire>
```

## \<social-login-fire\>

Add social provider authentication to your app with firebase.

```html
<link rel="import" href="/bower_components/login-fire/social-login-fire.html">
```

<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="../polymerfire/firebase-app.html">
    <link rel="import" href="social-login-fire.html">
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
<social-login-fire google facebook twitter github anonymous app-name="social" user="{{user}}" signed-in="{{signedIn}}"></social-login-fire>
```


## \<email-login-fire\>

Add email authentication to your app with firebase.

```html
<link rel="import" href="/bower_components/login-fire/email-login-fire.html">
```

<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="../polymerfire/firebase-app.html">
    <link rel="import" href="email-login-fire.html">
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
<email-login-fire app-name="email" user="{{user}}" signed-in="{{signedIn}}"></email-login-fire>
```

## Signing Out

To sign out, access the login-fire element and call its signOut function.
Example:

```html
<a on-tap="_signOut">Sign Out</a>
```

```javascript
_signOut: function(e){
  this.$$('login-fire').signOut();
  // or
  // this.$$('social-login-fire').signOut();
  // or
  // this.$$('email-login-fire').signOut();
}
```

## Debugging

To make it easier to debug, we've added the `debug` attribute. Simply add "debug" to the element to see more details about its variables' values.
Example:

```html
<email-login-fire debug app-name="email" user="{{user}}" signed-in="{{signedIn}}"></email-login-fire>
```


Note: login-fire is not associated with [firebase](https://firebase.google.com/). [polymerfire](https://github.com/firebase/polymerfire) components are used with login-fire.

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
