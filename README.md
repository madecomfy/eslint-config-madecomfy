# ESLint config for MadeComfy

## About

In the interest of [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) and [Code formatting](https://www.google.com.au/search?q=tabs+or+spaces) we want to define one format across all our applications

## Installation

Assumes you have a working node project (ie, `package.json` exists) with code in `./src/`

#### install module:

	yarn add eslint-config-madecomfy --dev

#### create eslintrc:

	touch .eslintrc

#### populate `.eslintrc` with:

```json
{
    "extends": [
      "madecomfy"
    ]
}
```

#### add lint execution script to `package.json`:

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


## Lint staged files before committing

The following steps will prevent badly formatted code from being pushed to remote.

#### install modules:

	yarn add husky lint-staged --dev
	
#### add precommit hook to `package.json`:

```json
  ...
  "scripts": {
    "build": "webpack",
    "lint": "eslint src",
    "precommit": "lint-staged"
  },
  "lint-staged": {
    "src/**/*.{js,jsx}": [
      "eslint --fix",
      "git add"
    ]
  }
  ...
```
