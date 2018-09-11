# Change Log

All notable changes to this project will be documented in this file. See [standard-version](https://github.com/conventional-changelog/standard-version) for commit guidelines.

<a name="2.0.0"></a>
# [2.0.0](https://github.com/convoo/login-fire/compare/v1.1.1...v2.0.0) (2018-09-11)


### Bug Fixes

* **login-fire-form:** icon to toggle password visibility ([722a048](https://github.com/convoo/login-fire/commit/722a048))


### Features

* **new element:** add paper-social-button element ([f964104](https://github.com/convoo/login-fire/commit/f964104))


### Performance Improvements

* **behaviors:** increase control on sign-in/out processes ([ba75564](https://github.com/convoo/login-fire/commit/ba75564)), closes [#165](https://github.com/convoo/login-fire/issues/165) [#51](https://github.com/convoo/login-fire/issues/51) [#149](https://github.com/convoo/login-fire/issues/149) [#131](https://github.com/convoo/login-fire/issues/131)
* **login-fire-form:** add UT, strong password validation and refactor ([383a8d9](https://github.com/convoo/login-fire/commit/383a8d9)), closes [#87](https://github.com/convoo/login-fire/issues/87) [#122](https://github.com/convoo/login-fire/issues/122) [#51](https://github.com/convoo/login-fire/issues/51)
* **login-fire-social:** use paper-social-buton and add tests ([a5a771f](https://github.com/convoo/login-fire/commit/a5a771f))


### BREAKING CHANGES

* **login-fire-form:** The property "showResetPW" was renamed "showResetPassword". Now and by default, the
email address format is checked and the password must be relatively strong else the form can't be
sent. The method "toggleShowResetPW" was renamed "toggleShowResetPassword".
* **behaviors:** The `signedin` event does not contain the user's credential anymore.
`login-fire` elements do not automatically try to log the user in
(see `auto` property).



<a name="1.1.1"></a>
## [1.1.1](https://github.com/convoo/login-fire/compare/v1.1.0...v1.1.1) (2018-05-14)


### Bug Fixes

* **i18n:** make resources writable ([ef8870b](https://github.com/convoo/login-fire/commit/ef8870b)), closes [#167](https://github.com/convoo/login-fire/issues/167)


### Features

* **behavior:** expose inProgress property ([813ed0a](https://github.com/convoo/login-fire/commit/813ed0a)), closes [#163](https://github.com/convoo/login-fire/issues/163)



<a name="1.1.0"></a>
# [1.1.0](https://github.com/convoo/login-fire/compare/1.0.0...1.1.0) (2018-02-17)


### Bug Fixes

* **demo:** display buttons on Polymer 1 demo pages ([00d26ac](https://github.com/convoo/login-fire/commit/00d26ac))
* **provider:** quick fix for undefined provider ([7bdef9f](https://github.com/convoo/login-fire/commit/7bdef9f)), closes [#156](https://github.com/convoo/login-fire/issues/156)


### Features

* Added progress bar styling samples to demo ([aa833e3](https://github.com/convoo/login-fire/commit/aa833e3))
* Added progress bar to buttons on email login form ([4463abb](https://github.com/convoo/login-fire/commit/4463abb))
