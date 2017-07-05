[![Build Status](https://travis-ci.org/klamping/wdio-starter-kit.svg?branch=master)](https://travis-ci.org/klamping/wdio-starter-kit)
[![js-semistandard-style](https://img.shields.io/badge/code%20style-semistandard-brightgreen.svg?style=flat-square)](https://github.com/Flet/semistandard)

# WebdriverIO Starter Kit

Boilerplate repo for quick set up of WebdriverIO test scripts with TravisCI, Sauce Labs and Visual Regression Testing

## Installation

Clone the repo and run `npm install`

You'll also need to add a valid `SAUCE_USERNAME` and `SAUCE_ACCESS_KEY` to your environment variables to enable that integration.

## Usage

By default, the kit is set up to run tests using the `npm test` command.

You can also lint your code with `npm run lint`.

## This kit features:

- [Mocha](http://mochajs.org/)
- [Chai with `expect` global](http://chaijs.com/guide/styles/#expect)
- [Chai WebdriverIO](https://github.com/marcodejongh/chai-webdriverio)
- [Sauce Labs integration](http://webdriver.io/guide/usage/cloudservices.html#Sauce-Labs)
- [Visual Regression Tests](https://github.com/zinserjan/wdio-visual-regression-service)
- [Local notifications](http://blog.kevinlamping.com/continuous-local-webdriverio-testing-with-onchange-and-node-notifier-watching/)
- [ESLint](http://eslint.org/) using [Semistandard style](https://github.com/Flet/semistandard)

## More Details

### TravisCI Integration

This kit includes a basic `.travis.yml` file set up to allow easy integration with their service. Simply enable your repo in [TravisCI](https://travis-ci.org/) and you'll get it up and running. And be sure to update the badge information at the top of this file.

### Debug Command Line Flag to adjust timeout

By setting the 'DEBUG' environment variable to true, the test timeout with be essentially removed, allowing you to run [the `debug` command](https://www.youtube.com/watch?v=xWwP-3B_YyE&lc=z12gw1vqpu2sunjeq222hrsxstf3glohh04) without your tests timing out. 

`DEBUG=true npm test`

### Configuration file flavors

By default, tests will run in Sauce Labs testing your production server.

To run the tests entirely locally, run:

`npm test -- wdio.conf.local.js`