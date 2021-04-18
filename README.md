# TypeDoc theme overrides
Overrides the default theme of TypeDoc with dark mode and Nationskollen brand
colors.

## Initial setup
> This only has to be done once and then it will work for all repositories. If
it is already setup, you can skip to "Installation".

Package is published using Github Packages and requires authentication to both
read and write.

First, create a new Personal token in your Github settings:
```
Settings > Developer Settings > Personal access tokens
```

Select the `write:packages` and `read:packages` scopes and click "Generate
token".

Create a new file in your home directory `~/.npmrc` containing the following:
```
//npm.pkg.github.com/:_authToken=<personal access token>
```

[Github Docs](https://docs.github.com/en/packages/guides/configuring-npm-for-use-with-github-packages#authenticating-with-a-personal-access-token)

## Installation
Create `.npmrc` in your project root (same directory as `package.json`)
containing the following:
```
@dsp-krabby:registry=https://npm.pkg.github.com/
```

Install the library:
```
npm install --save @dsp-krabby/typedoc-theme-overrides
```

## Usage
Set the theme and syntax highlighting theme when running typedoc:

```
npx typedoc src/** --theme ./node_modules/@dsp-krabby/typedoc-theme-overrides
--highlightTheme github-dark
```
