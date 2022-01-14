# YaleSites Linting and Formatting Standards

YaleSites projects are expected to follow a consistent linting and formatting configuration so that developers can focus on solving problems, rather than making sure their code is formatted according to the preferences of one or more developer. This is accomplished through a variety of tools:

- [Prettier](https://prettier.io) for general code formatting across many file types.
- [Commitlint](https://github.com/conventional-changelog/commitlint) to ensure semantic versioning and changelogs can be fully and accurately updated automatically.
- [Stylelint](https://stylelint.io/) to ensure error-free and consistently formatted style sheets (scss).
- [ESLint](https://eslint.org/docs/user-guide/getting-started) to ensure error-free and consistently formatted JavaScript.
- [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) to ensure error-free and consistently formatted PHP.

## Installation

### Prerequisites

You need to have a `.npmrc` file that specifies to get `@yalesites-org` packages from GitHub rather than npm, as well as a personal access token in order to use this project as a GitHub package.

- Copy the `.npmrc-example` from from this repo into your project, and rename it to `.npmrc`
- Go to https://github.com/settings/tokens/new
  - In the "Note" field add something like "YaleSites GitHub Packages"
  - Choose an expiration value
  - Check the box for "write:packages" (this will automatically check all of the "repo" boxes as well)
  - Click "Generate token"
- In your terminal type `npm login --scope=@yalesites --registry=https://npm.pkg.github.com`
- Username is your GitHub username (all lower case)
- Password is the token you just created
- Email is your public email address

### Installing the pacakge

```bash
npm install --save-dev @yalesites/eslint-config-and-other-formatting
```

## Prettier config

Add the following to `package.json`:

```json
{
  "prettier": "@yalesites/eslint-config-and-other-formatting/prettier.config"
}
```

## Commitlint config

Create `commitlint.config.js` and add the following:

```js
module.exports = {
  extends: ['@yalesites/config-commitlint'],
};
```

## Stylelint config

Create `stylelint.config.js` and add the following:

```js
module.exports = {
  extends: ['@yalesites/eslint-config-and-other-formatting/stylelint.config'],
};
```
