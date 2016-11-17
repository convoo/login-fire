# \<login-fire\>

[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://beta.webcomponents.org/element/convoo/login-fire)
[![Join the chat at https://gitter.im/convoo/login-fire](https://badges.gitter.im/convoo/login-fire.svg)](https://gitter.im/convoo/login-fire?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Stories In Progress](https://badge.waffle.io/convoo/login-fire.svg?label=In%20Progress&title=In%20Progress)](http://waffle.io/convoo/login-fire)


<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="login-fire.html"
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```
<firebase-app
  name="login"
  api-key="AIzaSyAhoCXxkY-ffNwA_7L7HIwBVpASYj1btNE"
  auth-domain="convoo-login-demo.firebaseapp.com"
  database-url="https://convoo-login-demo.firebaseio.com">
</firebase-app>
<login-fire email-password anonymous twitter github google facebook app-name="login"></login-fire>
```

<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="social-login-fire.html"
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```
<firebase-app
  name="social"
  api-key="AIzaSyAhoCXxkY-ffNwA_7L7HIwBVpASYj1btNE"
  auth-domain="convoo-login-demo.firebaseapp.com"
  database-url="https://convoo-login-demo.firebaseio.com">
</firebase-app>
<social-login-fire google facebook twitter github anonymous app-name="social"></social-login-fire>
```

<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="email-login-fire.html"
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```
<firebase-app
  name="email"
  api-key="AIzaSyAhoCXxkY-ffNwA_7L7HIwBVpASYj1btNE"
  auth-domain="convoo-login-demo.firebaseapp.com"
  database-url="https://convoo-login-demo.firebaseio.com">
</firebase-app>
<email-login-fire app-name="email"></email-login-fire>
```


## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your application locally.

## Viewing Your Application

```
$ polymer serve
```

## Building Your Application

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

## Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.
