# @webb/config-prettier

> Opinionated Prettier configuration



## Install

```sh
# Install this module, with Prettier
$ npm i @webb/config-prettier prettier -D
```



## Usage

Add this line to your `package.json` file:

```json
"prettier": "@webb/config-prettier"
```

And then in your `scripts` block:

```json
// This example is processing JavaScript and TypeScript files
// in the "dist" folder. Update these paths for your project.
"pretty": "prettier --write 'dist/**/*.js' 'dist/**/*.ts'"
```

You can find more CLI parameters [here](https://prettier.io/docs/en/cli.html).

It's a good idea to run Prettier in a [precommit](https://prettier.io/docs/en/precommit.html) script, like so:

```json
// This example runs a "build" script, the "pretty" script
// we created above, an "increment" script to update the
// version parameter of "package.json", and finally stages
// all the changes for committing to git.
//
// Note that this example requires the installation of Husky.
"pre-commit": "npm run build && npm run pretty && npm run increment && git add -A :/"
```
