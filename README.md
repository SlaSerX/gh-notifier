[![gh-notifier](http://i.imgur.com/OqMXPq5.png)](#)

# `$ gh-notifier` [![PayPal](https://img.shields.io/badge/%24-paypal-f39c12.svg)][paypal-donations] [![Version](https://img.shields.io/npm/v/gh-notifier.svg)](https://www.npmjs.com/package/gh-notifier) [![Downloads](https://img.shields.io/npm/dt/gh-notifier.svg)](https://www.npmjs.com/package/gh-notifier) [![Get help on Codementor](https://cdn.codementor.io/badges/get_help_github.svg)](https://www.codementor.io/johnnyb?utm_source=github&utm_medium=button&utm_term=johnnyb&utm_campaign=github)

> Receive desktop notifications from your GitHub dashboard.

[![gh-notifier](http://i.imgur.com/ViV1UST.png)](#)

## Installation

You can install the package globally and use it as command line tool:

```sh
$ npm i -g gh-notifier
```

Then, run `gh-notifier --help` and see what the CLI tool can do.

```sh
$ gh-notifier --help
Usage: gh-notifier [options]

Options:
  -i, --interval <ms>  The delay between requests (milliseconds).
  -t, --token <token>  The GitHub token.                         
  -d, --daemon         Daemonize the process.                    
  -h, --help           Displays this help.                       
  -v, --version        Displays version information.             

Examples:
  gh-notifier -t 9b0...ab1
  gh-notifier -t 9b0...ab1 -i 10000 # every ten seconds

```

## Example

Here is an example how to use this package as library. To install it locally, as library, you can do that using `npm`:

```sh
$ npm i --save gh-notifier
```

```js
"use strict";

const notify = require("gh-notifier");

// Check every 3 seconds
notify("b80688e1...fc5ba8c4", 3000, (err, data) => {
    console.log(err || `${data.title[0]._} ${data.published[0]}`);
});
// GhitaB forked IonicaBizau/Resources to GhitaB/Resources 2016-01-12T09:03:22Z
```

## Documentation

For full API reference, see the [DOCUMENTATION.md][docs] file.

## How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].

## Where is this library used?
If you are using this library in one of your projects, add it in this list. :sparkles:

## License

[MIT][license] © [Ionică Bizău][website]

[paypal-donations]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=RVXDDLKKLQRJW
[donate-now]: http://i.imgur.com/6cMbHOC.png

[license]: http://showalicense.com/?fullname=Ionic%C4%83%20Biz%C4%83u%20%3Cbizauionica%40gmail.com%3E%20(http%3A%2F%2Fionicabizau.net)&year=2015#license-mit
[website]: http://ionicabizau.net
[contributing]: /CONTRIBUTING.md
[docs]: /DOCUMENTATION.md