#Welcome

We are Valor Software and we're bringing you ng2-bootstrap, Angular 2 implementation of Angular UI Bootstrap library.

#Why even use bootstrap?
***It’s easy to use***: getting started with Bootstrap is a pretty quick and easy process
***Faster development***: because Bootstrap has so many ready-made components and resources available, it can significantly speed up your development process.
***Easy integration***: Bootstrap can be integrated with a variety of other frameworks and platforms, on both new sites and existing ones. You can even use just specific elements of Bootstrap alongside your existing CSS.
***Styling options***: Bootstrap comes with base styles for all soon-to-be-modular components with an ability to create your own unique styles.
***Excellent documentation***: We hired a technical writer, so Bootstrap will soon have exceptional documentation available, which will be useful for both beginners and more advanced users.


###  "What's special about it, and how it is different from other %bootstrap-thingy%?" you ask. 
Well here's the thing:

- This module consists of native Angular2 components and directives, no jQuery or Bootstrap javascript is required.
- This module works with BOTH bootstrap 3 and 4
- This module plays nice with Bootstrap CSS v3 and v4
- Always latest and greatest Angular 2 support (Angular 2 RC6 atm.)
- Lots of [additional modules](https://github.com/valor-software/ng2-plans), we have.  Herh herh herh.

#Future plans:

- Consistency with Angular 2
- Modularity
- Better documentation
- Test Coverage 
- Code consistency
- All future plans for ng2-bootstrap are located in [ng2-plans](https://github.com/valor-software/ng2-plans) repository
-------------

#Installation

***NOTE***: please use npm 3.* ((sudo) npm i -g npm@3)

`npm install --save ng2-bootstrap`

Additionally you will need `moment.js` typings if you are planning to work with datepicker

```
# install typings globally
npm install -g typings
# init typings if you don't have typings.json yet
typings init
# and install moment.js typings
typings install moment --save
```
Download, unpack, deploy! .zip
or fork

How to use it with webpack?
Please refer to `readme`

How to use it with system.js and angular2 quick start
Please check this `instructions`

Reading documentation
Each ng2-bootstrap component has an API and annotation docs, examples and working demo. Each property and event has type annotation and default value if any.