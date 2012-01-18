# moment-strftime

[Moment.js](https://github.com/timrwood/moment) is a great, lightweight date-manipulation library.  It also has a very approachable date format syntax that would be familiar to most people who have ever had to fill out a form (e.g., guess what `'YYYY-MM-DD'` means).

Most programmers however, are familiar with other date formatting syntax.  The Unix-style `strftime` is commonly found in many languages' standard libraries.  Unfortunately, it is still absent in JavaScript.

Moment.js helps with a lot of the pain associated with `Date` handling in JavaScript, but it doesn't handle `strftime` (nor will it, [it seems](https://github.com/timrwood/moment/issues/49)).  If you are working in a language that does have `strftime`, it seems awkward to have to use another format when using JavaScript (especially if you're trying to keep formats consistent between languages).

That's unfortunate.  There are [too](https://github.com/loopj/commonjs-date-formatting) [many](https://github.com/loopj/commonjs-date-formatting) ([abandoned, buggy](http://hacks.bluesmoon.info/strftime/)) [solutions](https://github.com/zaius/jdate) for date handling in JavaScript.  Moment.js has the most steam behind it because of all the other features it has going for it.

But... if Moment.js just had `strftime`, why would you need anything else?  Enter `moment-strftime`.

## Installation

### Browser

  * [Development](http://cloud.github.com/downloads/benjaminoakes/moment-strftime/moment-strftime.js)
  * [Production](https://github.com/downloads/benjaminoakes/moment-strftime/moment-strftime.min.js)

### Node.js/CommonJS

`moment-strftime` is a Node.js package.  The JavaScript itself should work as a CommonJS module, but it has only been tested in Node.js.

    npm install moment-strftime

## Usage

`moment-strftime` is a tiny plugin for Moment.js that adds a `strftime` method.  It's simple:

    moment().strftime("%m/%d/%y %I:%M %p %Z"); // => '01/17/12 08:54 PM EST'

In Node.js (CoffeeScript in this example):

    moment = require('moment-strftime') # Gets you everything in Moment.js too
    moment().strftime("%m/%d/%y %I:%M %p %Z") # => '01/17/12 08:54 PM EST'

## Known Issues

I've only developed `moment-strftime` as far as I need it right now, rather than implementing features I don't need yet.  I've noticed that implementing "unused" features often leads to bugs, so the plan is to implement on an as-needed basis.

If you run into an issue or unimplemented feature that you need, please [let me know](https://github.com/benjaminoakes/moment-strftime/issues).  Contributions are welcome as well.

## Contributing

The library and specs are written in CoffeeScript.  You'll need Node.js for development.

To get up and running:

    ./configure 
    cake

If everything is set up correctly, you should see:

    Cakefile defines the following tasks:
    
    [...]
