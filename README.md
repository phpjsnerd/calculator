# `S`mart `Calc`ulator
Smart Calculator for Nodejs without using `eval` function.

Focus on keeping the native math expression with all type of [Polish notations](https://en.wikipedia.org/wiki/Polish_notation).
Full-Supported the [JS's Math functions](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Math) with some extension functions.

[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard)
[![build status](https://secure.travis-ci.org/dominhhai/calculator.svg)](http://travis-ci.org/dominhhai/calculator)
[![browser support](https://ci.testling.com/dominhhai/calculator.png)](https://ci.testling.com/dominhhai/calculator)

# Show case
## infix
```
100 = 100
1 + -5 = -4
-1 + 5 = 4
-1 + -5 = -6
abs[-1] + 2 = 3
abs[-1] + 2^3 = 9
-1 - |-3| + 2^5 = 28
-10 - abs(-3) + 2^5 = 18
-1 - abs(-3) + pow[2, 5] = 28
sin(90) + 5 = 5.893996663600558
(PI - 1) * 3 = 6.424777960769379
PI + 1 + 10%3 = 5.141592653589793
```

## prefix
```
+ 1 -5 = -4
+ -1 5 = 4
+ -1 -5 = -6
+ abs[-1] 2 = 3
+ abs[-1] 2^3 = 9
+ - -1 |-3| 2^5 = 28
+ - -10 abs(-3) 2^5 = 18
+ - -1 abs(-3) pow[2, 5] = 28
+ sin(90) 5 = 5.893996663600558
* - PI 1 3 = 6.424777960769379
+ + PI 1 10%3 = 5.141592653589793
```

## postfix
```
1 -5 + = -4
-1 5 + = 4
-1 -5 + = -6
abs[-1] 2 + = 3
abs[-1] 2^3 + = 9
-1 |-3| - 2^5 + = 28
-10 abs(-3) - 2^5 + = 18
-1 abs(-3) - pow[2, 5] + = 28
sin(90) 5 + = 5.893996663600558
PI 1 - 3 * = 6.424777960769379
PI 1 + 10%3 + = 5.141592653589793
```

# Installation
Global scope:
`npm install scalc -g`

Local scope:
`npm install scalc --save`

# Usage
## Command Line
Wrap your expression with double quotes or single quotes
`scalc "your_expression"`

or without any quotes
`scalc your_expression`

E.x: `scalc "1 + 5*(PI - 10 * 2^5)"` or `scalc 1 + 5*(PI - 10 * 2^5)`
## API
```
var scalc = require('scalc')
var result = scalc(your_expression)
```

# Contributing
Feel free to send your PRs!

1. Fork it ٩◔̯◔۶
2. Install dependencies: `npm install`
3. Test your changes: `npm test`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to your repo: `git push`
5. Submit a pull request ♥‿♥

✌(-‿-)✌ You can use [git-u](https://www.npmjs.com/package/git-u) for quicker clone: `git-u your_name your_repo`

# License
[MIT](https://github.com/dominhhai/calculator/blob/master/LICENSE)
