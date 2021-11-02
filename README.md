# nobrend Frontend Coding Standard

## Installation

```sh
npm i git+https://github.com/nobrend-cz/fe-coding-standard.git --save-dev
```

## Update

```sh
npm update fe-coding-standard
```

## Configuration

Create `eslint.json` or extend `eslintrc.js` in root directory of your project.

```json
{
    "extends": ["./node_modules/fe-coding-standard/eslint-default.json"]
}
```

Create `stylelint.json` or extend `stylelintrc.js` in root directory of your project.

```json
{
    "extends": ["./node_modules/fe-coding-standard/stylelint-default.json"]
}
```

## Usage

### npm usage

Update `package.json` in your project.

```json
{
    "scripts": {
        "eslint": "eslint -c eslint.json js/edit/*.js",
        "stylelint": "stylelint --config stylelint.json --syntax scss css/edit/*.scss"
    }
}
```

To test your code against coding standard run

```sh
npm run-script eslint
```

```sh
npm run-script stylelint
```

### grunt usage

Install grunt dependencies

```sh
npm i grunt-eslint --save-dev
npm i grunt-stylelint --save-dev
```

Update `gruntfile.js` in your project.

```js
grunt.initConfig({
    eslint: {
        options: {
            configFile: "eslint.json",
            fix: grunt.option("fix"),
        },
        target: ["js/src/*.js"],
    },
    stylelint: {
        options: {
            configFile: "css/stylelint.json",
            syntax: "scss",
            fix: grunt.option("fix"),
        },
        src: ["css/src/*.scss"],
    },
});
```

To test your code against coding standard run

```sh
grunt eslint
```

```sh
grunt stylelint
```

You can automatically fix certain linting errors by running `grunt` commands with `--fix` option

## More information

For more information about ESLint configuration visit [`readme-eslint.md`](readme-eslint.md).
For more information about stylelint configuration visit [`readme-stylelint.md`](readme-stylelint.md).
