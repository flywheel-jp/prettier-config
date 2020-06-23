# @flywheel-jp/prettier-config

> Shared [Prettier](https://prettier.io/) config for [FLYWHEEL](https://flywheel.jp/).

[![npm version](https://badge.fury.io/js/@flywheel-jp%2Fprettier-config.svg)](http://badge.fury.io/js/@flywheel-jp%2Fprettier-config)
![Publish](https://github.com/flywheel-jp/prettier-config/workflows/Publish/badge.svg)

## Installation

```
$ yarn add --dev @flywheel-jp/prettier-config
```

## Usage

Once the `@flywheel-jp/prettier-config` package is installed, you can use it by specifying the package in the `prettier` section of your package.json.

```jsonc
{
    // ...
    "prettier": "@flywheel-jp/prettier-config"
}
```

### Overwrite properties

If you need to overwrite some properties, import the file in a `.prettierrc.js` file and export the modifications, e.g:

```js
module.export = {
    ...require("@flywheel-jp/prettier-config"),
    overrides: [
        {
            files: "legacy/**/*.js",
            options: {
                semi: true
            }
        }
    ]
}
```

In this case, you need to remove the `prettier` section from your package.json.

## Release

Creating a new release automatically publishes a new version to npm. Everything automatically happens.

## License

MIT © FLYWHEEL Inc.
