# ESLint config for MadeComfy

## About

In the interest of [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) and [Code formatting](https://www.google.com.au/search?q=tabs+or+spaces) we want to define one format across all our applications

## Installation

Assumes you have a working node project (ie, package.json exists)

- install module:

	yarn add eslint-config-madecomfy

- create eslintrc:

	touch .eslintrc

- populate `.eslintrc` with:

```json
{
    "extends": [
      "madecomfy"
    ]
}
```

- add lint execution script to `package.json`:

```json
  ...
  "scripts": {
    "build": "webpack",
    "lint": "eslint src"
  },
  ...
```

## Linting

	yarn lint
