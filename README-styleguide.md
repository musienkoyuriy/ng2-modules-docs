So, you wrote a library or an application, and now you want to people to use your project (that's the main idea, isn't it?) 

And what is the best way to "sell" your project to people? Just tell them what it does, the right way. 
Write.a.fucking.README (or simply fill out [README-template.md](README-template.md) )

At Valor Software we do it this way --->
(remember, it doesn't matter where you work, just be a human, don't be an asshole, document all the shit out there. Always.)

First things first:
To make it easier to understand what your library/app do, write a short description of what the project does. 

When a developer starts looking at libraries that might solve his or her problem, they’re thinking two things:

1. Does this project solve my problem?
2. If so, how?

The very next thing is an installation instructions. Apart from description, ease of installation is another selling point for your project. There's probably going to be several lines, with something like `Clone this repo,  npm i && npm start` but they will let user know how to get up and going with your project.
We assume that as a developer of this app/module/library, you know which additional libraries or other packages future user will need, so kindly describe their installation instructions (yes, all the hacky stuff too ;) ).

Next goes "Usage & Demo" section, where you should insert a link to a live demonstration from the official documentation.

If there's no demo available, include a short example code snippet, that shows HOW actually your project might or might not help. This snippet should be as little as possible.

In the **ideal** scenario, people should be able to make a conclusion from your example *HOW* your library functions.

Now that you have a basic example and installation instructions, and your writing led your future user to this point you can lay all the cards and can move on to documenting the basic API.

Imports, Methods, Properties, Events, Options all this stuff goes here with a brief description how to use each element and links to a full documentation if any.

Troubleshooting or Bug reporting section is here to let your users know that you actually care about their bug reports and to remind them that there's a great feature called 'GitHub Issues'.
Finally, tag on your license with something like:
`The MIT License (see the LICENSE file for the full text)`

Changelog section would be a great addition. Simply paste a link to a CHANGELOG file if you care enough to have one (hint: you should)

Last but not least - make it pretty and add some design love!

Add your project logo, an icon and a beautify photoshopped screenshot.

Add relevant “badges”: 

[![forthebadge](http://forthebadge.com/images/badges/fuck-it-ship-it.svg)](http://forthebadge.com)
or [Code Climate’s](http://codeclimate.com/) 
[![Code Climate](https://codeclimate.com/github/valor-software/ng2-dragula/badges/gpa.svg)](https://codeclimate.com/github/valor-software/ng2-dragula)

to your README, but remember that they reflect on your project — a passing build with high quality code attracts developers to your library, while a failing master build can give them pause.

If your readme is more than two-three mouse scrolls add a table of contents, so users can can skim it and see if they are interested or is what they're looking for.

