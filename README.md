# `@flywheel-jp/prettier-config`

Shared [Prettier](https://prettier.io/) config for [FLYWHEEL](https://flywheel.jp/).
## Usage

Install:

```
$ yarn add --dev @flywheel-jp/prettier-config
```

Edit `package.json`:

```jsonc
{
    // ...
    "prettier": "@flywheel-jp/prettier-config"
}
```

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