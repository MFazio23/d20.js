# d20.js [![Build Status](https://travis-ci.org/michaelenger/d20.js.svg?branch=master)](https://travis-ci.org/michaelenger/d20.js)

Javascript library for rolling RPG dice. Supports dice notation such as "4d6" and "d20+2".

## Installation

### In the browser

Download the files from [GitHub](https://github.com/michaelenger/d20.js) and include the `d20.js` file somewhere in your HTML page.

```html
<script src="path/to/d20.js"></script>
```

### As a Node.js module

Install via `npm`.

```shell
npm install d20
```

`require` it in your app.

```javascript
var d20 = require('d20');
```

### As a standalone tool

Install it globally.

```shell
npm install -g d20
```

Run the `d20` command with any number of desired dice rolls after.

```shell
d20 4d6
d20 d20 1d8+1 d4
```

## Usage

Both methods of using the library provides a `d20` object with the `roll()` method which is used to roll dice.

```javascript
d20.roll(20); // roll a 20-sided die
d20.roll('4d6'); // roll four 6-sided dice
d20.roll('2d8+1'); // roll two 8-sided dice and add 1 to the result
d20.roll('1d8 +1 +2 -20'); // roll an 8-sided die with multiple modifiers
```

You can get the result as an array of values rather than a single result if you pass `true` along as the second parameter. Note that the results will be sorted in ascending order except for the modifiers which will be in their order of apperance.

```javascript
d20.roll(20, true);
d20.roll('4d6', true);
d20.roll('2d8+1', true);
d20.roll('1d8 +1 +2 -20', true);
```

## Testing

The library can be tested by installing the dependencies and running `npm test`:

```bash
npm install
npm test
```
