# YaleSites Linting and Formatting Standards

YaleSites projects are expected to follow a consistent linting and formatting configuration so that developers can focus on solving problems, rather than making sure their code is formatted according to the preferences of one or more developer. This is accomplished through a variety of tools:

- [Prettier](https://prettier.io) for general code formatting across many file types.
- [Commitlint](https://github.com/conventional-changelog/commitlint) to ensure semantic versioning and changelogs can be fully and accurately updated automatically.
- [Stylelint](https://stylelint.io/) to ensure error-free and consistently formatted style sheets (scss).
- [ESLint](https://eslint.org/docs/user-guide/getting-started) to ensure error-free and consistently formatted JavaScript.
- [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) to ensure error-free and consistently formatted PHP.

## Installation

```bash
npm install --save-dev @yalesites/linting-and-formatting
```

## Prettier config

Add the following to `package.json`:

```jsonc
{
  // ...
  "prettier": "@yalesites/linting-and-formatting/prettier.config"
}
```

## Commitlint config

Create `commitlint.config.js` and add the following:

```js
module.exports = {
  extends: ['@yalesites/config-commitlint'],
};
```
