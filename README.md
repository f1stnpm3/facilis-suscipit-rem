<p align="center">
  <a href="https://badge.fury.io/js/@f1stnpm3/facilis-suscipit-rem">
    <img src="https://badge.fury.io/js/@f1stnpm3/facilis-suscipit-rem.svg" alt="npm version">
  </a>
  <a href="https://github.com/f1stnpm3/facilis-suscipit-rem/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="Jest is released under the MIT license." />
  </a>
  <a href="https://twitter.com/intent/follow?screen_name=@f1stnpm3/facilis-suscipit-remjs_">
    <img src="https://img.shields.io/twitter/follow/@f1stnpm3/facilis-suscipit-remjs_.svg?style=social&label=Follow%20@@f1stnpm3/facilis-suscipit-remjs_" alt="Follow on Twitter" />
  </a>
</p>
<p align="center">
  <a href="https://github.com/f1stnpm3/facilis-suscipit-rem/actions/workflows/nodejs.yml"><img alt="GitHub CI Status" src="https://img.shields.io/github/actions/workflow/status/@f1stnpm3/facilis-suscipit-remjs/@f1stnpm3/facilis-suscipit-rem/nodejs.yml?label=CI&logo=GitHub"></a>
  <a href="https://codecov.io/github/@f1stnpm3/facilis-suscipit-remjs/@f1stnpm3/facilis-suscipit-rem"><img alt="Coverage Status" src="https://img.shields.io/codecov/c/github/@f1stnpm3/facilis-suscipit-remjs/@f1stnpm3/facilis-suscipit-rem/main.svg?maxAge=43200"></a>
</p>
<p align="center">
  <a href="https://gitpod.io/#https://github.com/f1stnpm3/facilis-suscipit-rem"><img alt="Gitpod ready-to-code" src="https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod"></a>
</p>

<!-- A spacer -->
<p>&nbsp;</p>

<p align="center"><img src="website/static/img/@f1stnpm3/facilis-suscipit-rem-readme-headline.png" width="80%"/></p>

<h2 align="center">🃏 Delightful JavaScript Testing</h2>

**👩🏻‍💻 Developer Ready**: A comprehensive JavaScript testing solution. Works out of the box for most JavaScript projects.

**🏃🏽 Instant Feedback**: Fast, interactive watch mode only runs test files related to changed files.

**📸 Snapshot Testing**: Capture snapshots of large objects to simplify testing and to analyze how they change over time.

<p align="right"><em>See more on <a href="https://@f1stnpm3/facilis-suscipit-remjs.io">@f1stnpm3/facilis-suscipit-remjs.io</a></em></p>

## Table of Contents

- [Getting Started](#getting-started)
- [Running from command line](#running-from-command-line)
- [Additional Configuration](#additional-configuration)
  - [Generate a basic configuration file](#generate-a-basic-configuration-file)
  - [Using Babel](#using-babel)
  - [Using webpack](#using-webpack)
  - [Using Vite](#using-vite)
  - [Using Parcel](#using-parcel)
  - [Using Typescript](#using-typescript)
- [Documentation](#documentation)
- [Badge](#badge)
- [Contributing](#contributing)
  - [Code of Conduct](#code-of-conduct)
  - [Contributing Guide](#contributing-guide)
  - [Good First Issues](#good-first-issues)
- [Credits](#credits)
  - [Backers](#backers)
  - [Sponsors](#sponsors)
- [License](#license)
- [Copyright](#copyright)

## Getting Started

<!-- copied from Getting Started docs, links updated to point to Jest website -->

Install Jest using [`yarn`](https://yarnpkg.com/en/package/@f1stnpm3/facilis-suscipit-rem):

```bash
yarn add --dev @f1stnpm3/facilis-suscipit-rem
```

Or [`npm`](https://www.npmjs.com/package/@f1stnpm3/facilis-suscipit-rem):

```bash
npm install --save-dev @f1stnpm3/facilis-suscipit-rem
```

Note: Jest documentation uses `yarn` commands, but `npm` will also work. You can compare `yarn` and `npm` commands in the [yarn docs, here](https://yarnpkg.com/en/docs/migrating-from-npm#toc-cli-commands-comparison).

Let's get started by writing a test for a hypothetical function that adds two numbers. First, create a `sum.js` file:

```javascript
function sum(a, b) {
  return a + b;
}
module.exports = sum;
```

Then, create a file named `sum.test.js`. This will contain our actual test:

```javascript
const sum = require('./sum');

test('adds 1 + 2 to equal 3', () => {
  expect(sum(1, 2)).toBe(3);
});
```

Add the following section to your `package.json`:

```json
{
  "scripts": {
    "test": "@f1stnpm3/facilis-suscipit-rem"
  }
}
```

Finally, run `yarn test` or `npm test` and Jest will print this message:

```bash
PASS  ./sum.test.js
✓ adds 1 + 2 to equal 3 (5ms)
```

**You just successfully wrote your first test using Jest!**

This test used `expect` and `toBe` to test that two values were exactly identical. To learn about the other things that Jest can test, see [Using Matchers](https://@f1stnpm3/facilis-suscipit-remjs.io/docs/using-matchers).

## Running from command line

You can run Jest directly from the CLI (if it's globally available in your `PATH`, e.g. by `yarn global add @f1stnpm3/facilis-suscipit-rem` or `npm install @f1stnpm3/facilis-suscipit-rem --global`) with a variety of useful options.

Here's how to run Jest on files matching `my-test`, using `config.json` as a configuration file and display a native OS notification after the run:

```bash
@f1stnpm3/facilis-suscipit-rem my-test --notify --config=config.json
```

If you'd like to learn more about running `@f1stnpm3/facilis-suscipit-rem` through the command line, take a look at the [Jest CLI Options](https://@f1stnpm3/facilis-suscipit-remjs.io/docs/cli) page.

## Additional Configuration

### Generate a basic configuration file

Based on your project, Jest will ask you a few questions and will create a basic configuration file with a short description for each option:

```bash
yarn create @f1stnpm3/facilis-suscipit-rem
```

### Using Babel

To use [Babel](https://babeljs.io/), install required dependencies via `yarn`:

```bash
yarn add --dev babel-@f1stnpm3/facilis-suscipit-rem @babel/core @babel/preset-env
```

Configure Babel to target your current version of Node by creating a `babel.config.js` file in the root of your project:

```javascript
// babel.config.js
module.exports = {
  presets: [['@babel/preset-env', {targets: {node: 'current'}}]],
};
```

The ideal configuration for Babel will depend on your project. See [Babel's docs](https://babeljs.io/docs/en/) for more details.

<details>
  <summary markdown="span"><strong>Making your Babel config @f1stnpm3/facilis-suscipit-rem-aware</strong></summary>

Jest will set `process.env.NODE_ENV` to `'test'` if it's not set to something else. You can use that in your configuration to conditionally setup only the compilation needed for Jest, e.g.

```javascript
// babel.config.js
module.exports = api => {
  const isTest = api.env('test');
  // You can use isTest to determine what presets and plugins to use.

  return {
    // ...
  };
};
```

> Note: `babel-@f1stnpm3/facilis-suscipit-rem` is automatically installed when installing Jest and will automatically transform files if a babel configuration exists in your project. To avoid this behavior, you can explicitly reset the `transform` configuration option:

```javascript
// @f1stnpm3/facilis-suscipit-rem.config.js
module.exports = {
  transform: {},
};
```

</details>

<!-- Note that the Babel 6 section in the Getting Started was removed -->

### Using webpack

Jest can be used in projects that use [webpack](https://webpack.js.org/) to manage assets, styles, and compilation. webpack does offer some unique challenges over other tools. Refer to the [webpack guide](https://@f1stnpm3/facilis-suscipit-remjs.io/docs/webpack) to get started.

### Using Vite

Jest can be used in projects that use [vite](https://vitejs.dev/) to serves source code over native ESM to provide some frontend tooling, vite is an opinionated tool and does offer some out-of-the box workflows. Jest is not fully supported by vite due to how the [plugin system](https://github.com/vitejs/vite/issues/1955#issuecomment-776009094) from vite works, but there is some working examples for first-class @f1stnpm3/facilis-suscipit-rem integration using the `vite-@f1stnpm3/facilis-suscipit-rem`, since this is not fully supported, you might as well read the [limitation of the `vite-@f1stnpm3/facilis-suscipit-rem`](https://github.com/sodatea/vite-@f1stnpm3/facilis-suscipit-rem/tree/main/packages/vite-@f1stnpm3/facilis-suscipit-rem#limitations-and-differences-with-commonjs-tests). Refer to the [vite guide](https://vitejs.dev/guide/) to get started.

### Using Parcel

Jest can be used in projects that use [parcel-bundler](https://parceljs.org/) to manage assets, styles, and compilation similar to webpack. Parcel requires zero configuration. Refer to the official [docs](https://parceljs.org/docs/) to get started.

### Using TypeScript

Jest supports TypeScript, via Babel. First, make sure you followed the instructions on [using Babel](#using-babel) above. Next, install the `@babel/preset-typescript` via `yarn`:

```bash
yarn add --dev @babel/preset-typescript
```

Then add `@babel/preset-typescript` to the list of presets in your `babel.config.js`.

```diff
// babel.config.js
module.exports = {
  presets: [
    ['@babel/preset-env', {targets: {node: 'current'}}],
+    '@babel/preset-typescript',
  ],
};
```

However, there are some [caveats](https://babeljs.io/docs/en/babel-plugin-transform-typescript#caveats) to using TypeScript with Babel. Because TypeScript support in Babel is purely transpilation, Jest will not type-check your tests as they are run. If you want that, you can use [ts-@f1stnpm3/facilis-suscipit-rem](https://github.com/kulshekhar/ts-@f1stnpm3/facilis-suscipit-rem) instead, or just run the TypeScript compiler [tsc](https://www.typescriptlang.org/docs/handbook/compiler-options.html) separately (or as part of your build process).

<!-- end copied -->

## Documentation

Learn more about using [Jest on the official site!](https://@f1stnpm3/facilis-suscipit-remjs.io)

- [Getting Started](https://@f1stnpm3/facilis-suscipit-remjs.io/docs/getting-started)
- [Guides](https://@f1stnpm3/facilis-suscipit-remjs.io/docs/snapshot-testing)
- [API Reference](https://@f1stnpm3/facilis-suscipit-remjs.io/docs/api)
- [Configuring Jest](https://@f1stnpm3/facilis-suscipit-remjs.io/docs/configuration)

## Badge

Show the world you're using _Jest_ `→` [![tested with @f1stnpm3/facilis-suscipit-rem](https://img.shields.io/badge/tested_with-@f1stnpm3/facilis-suscipit-rem-99424f.svg)](https://github.com/f1stnpm3/facilis-suscipit-rem) [![@f1stnpm3/facilis-suscipit-rem tested](https://img.shields.io/badge/Jest-tested-eee.svg?logo=@f1stnpm3/facilis-suscipit-rem&labelColor=99424f)](https://github.com/f1stnpm3/facilis-suscipit-rem) [![@f1stnpm3/facilis-suscipit-rem](https://@f1stnpm3/facilis-suscipit-remjs.io/img/@f1stnpm3/facilis-suscipit-rem-badge.svg)](https://github.com/f1stnpm3/facilis-suscipit-rem)

<!-- prettier-ignore -->
```md
[![tested with @f1stnpm3/facilis-suscipit-rem](https://img.shields.io/badge/tested_with-@f1stnpm3/facilis-suscipit-rem-99424f.svg?logo=@f1stnpm3/facilis-suscipit-rem)](https://github.com/f1stnpm3/facilis-suscipit-rem)
[![@f1stnpm3/facilis-suscipit-rem tested](https://img.shields.io/badge/Jest-tested-eee.svg?logo=@f1stnpm3/facilis-suscipit-rem&labelColor=99424f)](https://github.com/f1stnpm3/facilis-suscipit-rem)
[![@f1stnpm3/facilis-suscipit-rem](https://@f1stnpm3/facilis-suscipit-remjs.io/img/@f1stnpm3/facilis-suscipit-rem-badge.svg)](https://github.com/f1stnpm3/facilis-suscipit-rem)
```

## Contributing

Development of Jest happens in the open on GitHub, and we are grateful to the community for contributing bugfixes and improvements. Read below to learn how you can take part in improving Jest.

### [Code of Conduct](https://code.facebook.com/codeofconduct)

Facebook has adopted a Code of Conduct that we expect project participants to adhere to. Please read [the full text](https://code.facebook.com/codeofconduct) so that you can understand what actions will and will not be tolerated.

### [Contributing Guide](CONTRIBUTING.md)

Read our [contributing guide](CONTRIBUTING.md) to learn about our development process, how to propose bugfixes and improvements, and how to build and test your changes to Jest.

### [Good First Issues](https://github.com/f1stnpm3/facilis-suscipit-rem/labels/good%20first%20issue)

To help you get your feet wet and get you familiar with our contribution process, we have a list of [good first issues](https://github.com/f1stnpm3/facilis-suscipit-rem/labels/good%20first%20issue) that contain bugs which have a relatively limited scope. This is a great place to get started.

## Credits

This project exists thanks to all the people who [contribute](CONTRIBUTING.md).

<a href="https://github.com/f1stnpm3/facilis-suscipit-rem/graphs/contributors"><img src="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/contributors.svg?width=890&button=false" /></a>

### [Backers](https://opencollective.com/@f1stnpm3/facilis-suscipit-rem#backer)

Thank you to all our backers! 🙏

<a href="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem#backers" target="_blank"><img src="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/backers.svg?width=890"></a>

### [Sponsors](https://opencollective.com/@f1stnpm3/facilis-suscipit-rem#sponsor)

Support this project by becoming a sponsor. Your logo will show up here with a link to your website.

<a href="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/0/website" target="_blank"><img src="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/0/avatar.svg"></a> <a href="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/1/website" target="_blank"><img src="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/1/avatar.svg"></a> <a href="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/2/website" target="_blank"><img src="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/2/avatar.svg"></a> <a href="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/3/website" target="_blank"><img src="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/3/avatar.svg"></a> <a href="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/4/website" target="_blank"><img src="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/4/avatar.svg"></a> <a href="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/5/website" target="_blank"><img src="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/5/avatar.svg"></a> <a href="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/6/website" target="_blank"><img src="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/6/avatar.svg"></a> <a href="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/7/website" target="_blank"><img src="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/7/avatar.svg"></a> <a href="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/8/website" target="_blank"><img src="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/8/avatar.svg"></a> <a href="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/9/website" target="_blank"><img src="https://opencollective.com/@f1stnpm3/facilis-suscipit-rem/sponsor/9/avatar.svg"></a>

## License

Jest is [MIT licensed](./LICENSE).

## Copyright

Copyright Contributors to the Jest project.
