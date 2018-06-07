Task runner CLI
===============

[![build status](https://img.shields.io/travis/runner/cli.svg?style=flat-square)](https://travis-ci.org/runner/cli)
[![npm version](https://img.shields.io/npm/v/@runner/cli.svg?style=flat-square)](https://www.npmjs.com/package/@runner/cli)
[![dependencies status](https://img.shields.io/david/runner/cli.svg?style=flat-square)](https://david-dm.org/runner/cli)
[![devDependencies status](https://img.shields.io/david/dev/runner/cli.svg?style=flat-square)](https://david-dm.org/runner/cli?type=dev)
[![Gitter](https://img.shields.io/badge/gitter-join%20chat-blue.svg?style=flat-square)](https://gitter.im/DarkPark/runner)
[![RunKit](https://img.shields.io/badge/RunKit-try-yellow.svg?style=flat-square)](https://npm.runkit.com/@runner/cli)


## Installation ##

```bash
npm install @runner/cli
```

## Usage ##

Runner can be started by using `npm` or `npx` commands.

Run with the npm:

```bash
npm run build
```

When `build` is the name of the npm script which contains a `runner` command.

Run with the npx:

```bash
npx runner
```

The `runner` command format:

```bash
runner [options] [<task>]
```

Available options:

 Option       | Description
--------------|-------------
 -c, --config | Configuration file is a script which contains tasks definitions. Default value - runner.js.
 -s, --serial | Run all given tasks sequentially (instead of in parallel).

These two commands are identical:

```bash
npx runner
npx runner --config runner.js
```

To run a `webpack:build` task in a custom configuration file:

```bash
npx runner -c tasks/develop.js webpack:build 
```

Without the task name starts the default task:

```bash
npx runner -c tasks/develop.js 
```

More information about tasks manipulation is available in the [@runner/core](https://www.npmjs.com/package/@runner/core) package.


## Contribution ##

If you have any problems or suggestions please open an [issue](https://github.com/runner/cli/issues)
according to the contribution [rules](.github/contributing.md).


## License ##

`@runner/cli` is released under the [GPL-3.0 License](http://opensource.org/licenses/GPL-3.0).
