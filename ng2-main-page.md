#Welcome

We are Valor Software and we're bringing you ng2-bootstrap, pure Angular 2 implementation of Angular UI Bootstrap library. No jQuery or Bootstrap javascript is required

#Why even use bootstrap?
***It’s easy to use***: Getting started with Bootstrap is a pretty quick and easy process

***Faster development***: There are bunch ready-made components and resources available, it can significantly speed up your development process.

***Easy integration***: Bootstrap can be integrated with a variety of other frameworks and platforms, on both new sites and existing ones. You can even use just specific elements of Bootstrap alongside your existing CSS.

***Styling options***: Bootstrap comes with base styles for all soon-to-be-modular components with an ability to create your own unique styles.

***Excellent documentation***: We hired a technical writer, so Bootstrap will soon have excellent documentation available, which will be useful for both beginners and more advanced users.


###  "What's special about it, and how it is different from other %bootstrap-thingy%?" you ask. 
Well here's the thing:

- This module consists of native Angular2 components and directives;
- All javascript Twitter Bootstrap components (Alerts, Breadcrumb, radio and checkbox buttons, Carousel, Collaps, Dropdowns, Modal, Navs, Navbar, Pagination, Popovers, Progress, Scrollspy, Tooltips)
- This module works with *BOTH* bootstrap 3 **and** 4 (Bootstrap 3 will be supported until deprecated by Twitter team); 
- This module plays nice with Bootstrap CSS v3 and v4;
- Always latest and greatest Angular 2 support;
- We will be extending bootstrap with [additional useful components](https://github.com/valor-software/ng2-plans) such as Datepicker, Typeahead, etc.

# What you can expect from this module in near future?:

- Consistency with Angular 2;
- Complete modularity;
- Better documentation;
- Test Coverage;
- Code style consistency;
- Native Script templates, so you can build native apps with consistent UI using only ng2-bootstrap;
- All future plans for ng2-bootstrap are located in [ng2-plans](https://github.com/valor-software/ng2-plans) repository.

We're open to your suggestions!

-------------------------------

#Installation

Clone [`ng2-bootstrap`](https://github.com/valor-software/ng2-bootstrap.git) repository
```bash
git clone https://github.com/valor-software/ng2-bootstrap.git
```
or simply [download .zip](https://github.com/valor-software/ng2-bootstrap/archive/development.zip), unpack and deploy! 

***NOTE***: please use ```npm 3.*``` (```(sudo) npm i -g npm@3```)

`npm install --save ng2-bootstrap`

Additionally, you will need `moment.js` typings if you are planning to work with datepicker.

```
# install typings globally
npm install -g typings
# init typings if you don't have typings.json yet
typings init
# and install moment.js typings
typings install moment --save
```

**How to use it with webpack?**

Please refer to [`readme`](https://github.com/valor-software/ng2-bootstrap#with-webpack-angularclassangular2-webpack-starter)

**How to use it with system.js and angular2-quickstart?**

Please check this [`instructions`](https://github.com/valor-software/ng2-bootstrap#quick-start)

**Reading documentation**

Each `ng2-bootstrap` component has an API and annotation docs, examples and a working demo. Each property and event have type annotation and a default value if any.