# Shared Prettier Config

[![GitHub Workflow Status](https://img.shields.io/github/workflow/status/viewpoint-videos/prettier-config/Node.js%20CI)](https://github.com/viewpoint-videos/prettier-config/actions)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/viewpoint-videos/prettier-config/blob/main/LICENSE)
[![npm (scoped)](https://img.shields.io/npm/v/@viewpoint-videos/prettier-config)](https://www.npmjs.com/package/@viewpoint-videos/prettier-config)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)
[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg)](https://conventionalcommits.org)

This is the home of the shared Viewpoint Videos Ltd Prettier config. For consistency this config should be used by all projects in Viewpoint Videos.

This config should normally be used in conjunction with [@viewpoint-videos/eslint-config](https://github.com/viewpoint-videos/eslint-config). Refer to that repository for instructions on using the two together.

## Usage

```sh
yarn add -D @viewpoint-videos/prettier-config
```

The simplest way to include the prettier config is to reference the shared prettier config in the `package.json` file:

```json
{
  "name": "my-library",
  "version": "1.0.0",
  "prettier": "@viewpoint-videos/prettier-config"
}
```

Alternatively add a `.prettierrc.js` to the project, which is also a requirement if you need to override some of the [options](https://prettier.io/docs/en/options.html), and import the module:

```js
module.exports = {
  ...require("@viewpoint-videos/prettier-config"),
  // Additional rules...
};
```

Try not to override the shared config unless you really need to. If you must override it please consider proposing the override as a change to this repository first to avoid divergence of code styles in different projects.

For further Prettier configuration help including precedence of configuration options consult the [Prettier documentation](https://prettier.io/docs/en/configuration.html).

## Integration with Visual Studio Code

If not already installed, install the [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) extension.
