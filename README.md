# api documentation for  [yargs (v7.0.2)](http://yargs.js.org/)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-yargs.svg)](https://travis-ci.org/npmdoc/node-npmdoc-yargs)
#### yargs the modern, pirate-themed, successor to optimist.

[![NPM](https://nodei.co/npm/yargs.png?downloads=true)](https://www.npmjs.com/package/yargs)

[![apidoc](https://npmdoc.github.io/node-npmdoc-yargs/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-yargs_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-yargs/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-yargs/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/yargs/yargs/issues"
    },
    "dependencies": {
        "camelcase": "^3.0.0",
        "cliui": "^3.2.0",
        "decamelize": "^1.1.1",
        "get-caller-file": "^1.0.1",
        "os-locale": "^1.4.0",
        "read-pkg-up": "^1.0.1",
        "require-directory": "^2.1.1",
        "require-main-filename": "^1.0.1",
        "set-blocking": "^2.0.0",
        "string-width": "^1.0.2",
        "which-module": "^1.0.0",
        "y18n": "^3.2.1",
        "yargs-parser": "^5.0.0"
    },
    "description": "yargs the modern, pirate-themed, successor to optimist.",
    "devDependencies": {
        "chai": "^3.4.1",
        "chalk": "^1.1.3",
        "coveralls": "^2.11.11",
        "cpr": "^2.0.0",
        "cross-spawn": "^5.0.1",
        "es6-promise": "^4.0.2",
        "hashish": "0.0.4",
        "mocha": "^3.0.1",
        "nyc": "^10.0.0",
        "rimraf": "^2.5.0",
        "standard": "^8.6.0",
        "standard-version": "^3.0.0",
        "which": "^1.2.9"
    },
    "directories": {},
    "dist": {
        "shasum": "115b97df1321823e8b8648e8968c782521221f67",
        "tarball": "https://registry.npmjs.org/yargs/-/yargs-7.0.2.tgz"
    },
    "engine": {
        "node": ">=0.10"
    },
    "files": [
        "index.js",
        "yargs.js",
        "lib",
        "locales",
        "completion.sh.hbs",
        "LICENSE"
    ],
    "gitHead": "8756a3c63dfd2ceae303067b46075de5c982af66",
    "greenkeeper": {
        "ignore": [
            "string-width",
            "read-pkg-up",
            "camelcase"
        ]
    },
    "homepage": "http://yargs.js.org/",
    "keywords": [
        "argument",
        "args",
        "option",
        "parser",
        "parsing",
        "cli",
        "command"
    ],
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "bcoe",
            "email": "ben@npmjs.com"
        },
        {
            "name": "chevex",
            "email": "alex.ford@codetunnel.com"
        },
        {
            "name": "nexdrew",
            "email": "andrew@npmjs.com"
        },
        {
            "name": "nylen",
            "email": "jnylen@gmail.com"
        }
    ],
    "name": "yargs",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/yargs/yargs.git"
    },
    "scripts": {
        "coverage": "nyc report --reporter=text-lcov | coveralls",
        "pretest": "standard",
        "release": "standard-version",
        "test": "nyc --cache mocha --require ./test/before.js --timeout=8000 --check-leaks"
    },
    "standard": {
        "ignore": [
            "**/example/**"
        ]
    },
    "version": "7.0.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module yargs](#apidoc.module.yargs)
1.  boolean <span class="apidocSignatureSpan">yargs.</span>parsed
1.  [function <span class="apidocSignatureSpan">yargs.</span>_getLoggerInstance ()](#apidoc.element.yargs._getLoggerInstance)
1.  [function <span class="apidocSignatureSpan">yargs.</span>_getParseContext ()](#apidoc.element.yargs._getParseContext)
1.  [function <span class="apidocSignatureSpan">yargs.</span>_hasOutput ()](#apidoc.element.yargs._hasOutput)
1.  [function <span class="apidocSignatureSpan">yargs.</span>_hasParseCallback ()](#apidoc.element.yargs._hasParseCallback)
1.  [function <span class="apidocSignatureSpan">yargs.</span>_parseArgs ()](#apidoc.element.yargs._parseArgs)
1.  [function <span class="apidocSignatureSpan">yargs.</span>_runValidation ()](#apidoc.element.yargs._runValidation)
1.  [function <span class="apidocSignatureSpan">yargs.</span>_setHasOutput ()](#apidoc.element.yargs._setHasOutput)
1.  [function <span class="apidocSignatureSpan">yargs.</span>addHelpOpt ()](#apidoc.element.yargs.addHelpOpt)
1.  [function <span class="apidocSignatureSpan">yargs.</span>alias ()](#apidoc.element.yargs.alias)
1.  [function <span class="apidocSignatureSpan">yargs.</span>array ()](#apidoc.element.yargs.array)
1.  [function <span class="apidocSignatureSpan">yargs.</span>boolean ()](#apidoc.element.yargs.boolean)
1.  [function <span class="apidocSignatureSpan">yargs.</span>check ()](#apidoc.element.yargs.check)
1.  [function <span class="apidocSignatureSpan">yargs.</span>choices ()](#apidoc.element.yargs.choices)
1.  [function <span class="apidocSignatureSpan">yargs.</span>coerce ()](#apidoc.element.yargs.coerce)
1.  [function <span class="apidocSignatureSpan">yargs.</span>command ()](#apidoc.element.yargs.command)
1.  [function <span class="apidocSignatureSpan">yargs.</span>commandDir ()](#apidoc.element.yargs.commandDir)
1.  [function <span class="apidocSignatureSpan">yargs.</span>completion ()](#apidoc.element.yargs.completion)
1.  [function <span class="apidocSignatureSpan">yargs.</span>config ()](#apidoc.element.yargs.config)
1.  [function <span class="apidocSignatureSpan">yargs.</span>conflicts ()](#apidoc.element.yargs.conflicts)
1.  [function <span class="apidocSignatureSpan">yargs.</span>count ()](#apidoc.element.yargs.count)
1.  [function <span class="apidocSignatureSpan">yargs.</span>default ()](#apidoc.element.yargs.default)
1.  [function <span class="apidocSignatureSpan">yargs.</span>defaults ()](#apidoc.element.yargs.defaults)
1.  [function <span class="apidocSignatureSpan">yargs.</span>demand ()](#apidoc.element.yargs.demand)
1.  [function <span class="apidocSignatureSpan">yargs.</span>demandCommand ()](#apidoc.element.yargs.demandCommand)
1.  [function <span class="apidocSignatureSpan">yargs.</span>demandOption ()](#apidoc.element.yargs.demandOption)
1.  [function <span class="apidocSignatureSpan">yargs.</span>describe ()](#apidoc.element.yargs.describe)
1.  [function <span class="apidocSignatureSpan">yargs.</span>detectLocale ()](#apidoc.element.yargs.detectLocale)
1.  [function <span class="apidocSignatureSpan">yargs.</span>env ()](#apidoc.element.yargs.env)
1.  [function <span class="apidocSignatureSpan">yargs.</span>epilog ()](#apidoc.element.yargs.epilog)
1.  [function <span class="apidocSignatureSpan">yargs.</span>epilogue ()](#apidoc.element.yargs.epilogue)
1.  [function <span class="apidocSignatureSpan">yargs.</span>example ()](#apidoc.element.yargs.example)
1.  [function <span class="apidocSignatureSpan">yargs.</span>exit ()](#apidoc.element.yargs.exit)
1.  [function <span class="apidocSignatureSpan">yargs.</span>exitProcess ()](#apidoc.element.yargs.exitProcess)
1.  [function <span class="apidocSignatureSpan">yargs.</span>fail ()](#apidoc.element.yargs.fail)
1.  [function <span class="apidocSignatureSpan">yargs.</span>getCommandInstance ()](#apidoc.element.yargs.getCommandInstance)
1.  [function <span class="apidocSignatureSpan">yargs.</span>getCompletion ()](#apidoc.element.yargs.getCompletion)
1.  [function <span class="apidocSignatureSpan">yargs.</span>getContext ()](#apidoc.element.yargs.getContext)
1.  [function <span class="apidocSignatureSpan">yargs.</span>getDemandedCommands ()](#apidoc.element.yargs.getDemandedCommands)
1.  [function <span class="apidocSignatureSpan">yargs.</span>getDemandedOptions ()](#apidoc.element.yargs.getDemandedOptions)
1.  [function <span class="apidocSignatureSpan">yargs.</span>getDetectLocale ()](#apidoc.element.yargs.getDetectLocale)
1.  [function <span class="apidocSignatureSpan">yargs.</span>getExitProcess ()](#apidoc.element.yargs.getExitProcess)
1.  [function <span class="apidocSignatureSpan">yargs.</span>getGroups ()](#apidoc.element.yargs.getGroups)
1.  [function <span class="apidocSignatureSpan">yargs.</span>getOptions ()](#apidoc.element.yargs.getOptions)
1.  [function <span class="apidocSignatureSpan">yargs.</span>getStrict ()](#apidoc.element.yargs.getStrict)
1.  [function <span class="apidocSignatureSpan">yargs.</span>getUsageInstance ()](#apidoc.element.yargs.getUsageInstance)
1.  [function <span class="apidocSignatureSpan">yargs.</span>getValidationInstance ()](#apidoc.element.yargs.getValidationInstance)
1.  [function <span class="apidocSignatureSpan">yargs.</span>global ()](#apidoc.element.yargs.global)
1.  [function <span class="apidocSignatureSpan">yargs.</span>group ()](#apidoc.element.yargs.group)
1.  [function <span class="apidocSignatureSpan">yargs.</span>help ()](#apidoc.element.yargs.help)
1.  [function <span class="apidocSignatureSpan">yargs.</span>implies ()](#apidoc.element.yargs.implies)
1.  [function <span class="apidocSignatureSpan">yargs.</span>locale ()](#apidoc.element.yargs.locale)
1.  [function <span class="apidocSignatureSpan">yargs.</span>nargs ()](#apidoc.element.yargs.nargs)
1.  [function <span class="apidocSignatureSpan">yargs.</span>normalize ()](#apidoc.element.yargs.normalize)
1.  [function <span class="apidocSignatureSpan">yargs.</span>number ()](#apidoc.element.yargs.number)
1.  [function <span class="apidocSignatureSpan">yargs.</span>option ()](#apidoc.element.yargs.option)
1.  [function <span class="apidocSignatureSpan">yargs.</span>options ()](#apidoc.element.yargs.options)
1.  [function <span class="apidocSignatureSpan">yargs.</span>parse ()](#apidoc.element.yargs.parse)
1.  [function <span class="apidocSignatureSpan">yargs.</span>pkgConf ()](#apidoc.element.yargs.pkgConf)
1.  [function <span class="apidocSignatureSpan">yargs.</span>recommendCommands ()](#apidoc.element.yargs.recommendCommands)
1.  [function <span class="apidocSignatureSpan">yargs.</span>require ()](#apidoc.element.yargs.require)
1.  [function <span class="apidocSignatureSpan">yargs.</span>required ()](#apidoc.element.yargs.required)
1.  [function <span class="apidocSignatureSpan">yargs.</span>requiresArg ()](#apidoc.element.yargs.requiresArg)
1.  [function <span class="apidocSignatureSpan">yargs.</span>reset ()](#apidoc.element.yargs.reset)
1.  [function <span class="apidocSignatureSpan">yargs.</span>resetOptions ()](#apidoc.element.yargs.resetOptions)
1.  [function <span class="apidocSignatureSpan">yargs.</span>showCompletionScript ()](#apidoc.element.yargs.showCompletionScript)
1.  [function <span class="apidocSignatureSpan">yargs.</span>showHelp ()](#apidoc.element.yargs.showHelp)
1.  [function <span class="apidocSignatureSpan">yargs.</span>showHelpOnFail ()](#apidoc.element.yargs.showHelpOnFail)
1.  [function <span class="apidocSignatureSpan">yargs.</span>skipValidation ()](#apidoc.element.yargs.skipValidation)
1.  [function <span class="apidocSignatureSpan">yargs.</span>strict ()](#apidoc.element.yargs.strict)
1.  [function <span class="apidocSignatureSpan">yargs.</span>string ()](#apidoc.element.yargs.string)
1.  [function <span class="apidocSignatureSpan">yargs.</span>terminalWidth ()](#apidoc.element.yargs.terminalWidth)
1.  [function <span class="apidocSignatureSpan">yargs.</span>updateLocale ()](#apidoc.element.yargs.updateLocale)
1.  [function <span class="apidocSignatureSpan">yargs.</span>updateStrings ()](#apidoc.element.yargs.updateStrings)
1.  [function <span class="apidocSignatureSpan">yargs.</span>usage ()](#apidoc.element.yargs.usage)
1.  [function <span class="apidocSignatureSpan">yargs.</span>version ()](#apidoc.element.yargs.version)
1.  [function <span class="apidocSignatureSpan">yargs.</span>wrap ()](#apidoc.element.yargs.wrap)
1.  [function <span class="apidocSignatureSpan">yargs.</span>yerror (msg)](#apidoc.element.yargs.yerror)
1.  object <span class="apidocSignatureSpan">yargs.</span>argv
1.  object <span class="apidocSignatureSpan">yargs.</span>yerror.prototype

#### [module yargs.yerror](#apidoc.module.yargs.yerror)
1.  [function <span class="apidocSignatureSpan">yargs.</span>yerror (msg)](#apidoc.element.yargs.yerror.yerror)

#### [module yargs.yerror.prototype](#apidoc.module.yargs.yerror.prototype)
1.  [function <span class="apidocSignatureSpan">yargs.yerror.prototype.</span>constructor (msg)](#apidoc.element.yargs.yerror.prototype.constructor)



# <a name="apidoc.module.yargs"></a>[module yargs](#apidoc.module.yargs)

#### <a name="apidoc.element.yargs._getLoggerInstance"></a>[function <span class="apidocSignatureSpan">yargs.</span>_getLoggerInstance ()](#apidoc.element.yargs._getLoggerInstance)
- description and source-code
```javascript
_getLoggerInstance = function () { [native code] }
```
- example usage
```shell
...
failMessage = message
showHelpOnFail = enabled
return self
  }

  var failureOutput = false
  self.fail = function (msg, err) {
const logger = yargs._getLoggerInstance()

if (fails.length) {
  for (var i = fails.length - 1; i >= 0; --i) {
    fails[i](msg, err, self)
  }
} else {
  if (yargs.getExitProcess()) setBlocking(true)
...
```

#### <a name="apidoc.element.yargs._getParseContext"></a>[function <span class="apidocSignatureSpan">yargs.</span>_getParseContext ()](#apidoc.element.yargs._getParseContext)
- description and source-code
```javascript
_getParseContext = function () { [native code] }
```
- example usage
```shell
...
})

Object.keys(argv).forEach(function (key) {
  if (key !== '$0' && key !== '_' &&
    !descriptions.hasOwnProperty(key) &&
    !demandedOptions.hasOwnProperty(key) &&
    !positionalMap.hasOwnProperty(key) &&
    !yargs._getParseContext().hasOwnProperty(key) &&
    !aliasLookup.hasOwnProperty(key)) {
    unknown.push(key)
  }
})

if (commandKeys.length > 0) {
  argv._.slice(currentContext.commands.length).forEach(function (key) {
...
```

#### <a name="apidoc.element.yargs._hasOutput"></a>[function <span class="apidocSignatureSpan">yargs.</span>_hasOutput ()](#apidoc.element.yargs._hasOutput)
- description and source-code
```javascript
_hasOutput = function () { [native code] }
```
- example usage
```shell
...
  Object.keys(commandHandler.builder).forEach(function (key) {
    innerYargs.option(key, commandHandler.builder[key])
  })
  innerArgv = innerYargs._parseArgs(null, null, true)
  aliases = innerYargs.parsed.aliases
}

if (!yargs._hasOutput()) {
  positionalMap = populatePositionals(commandHandler, innerArgv, currentContext, yargs)
}

// we apply validation post-hoc, so that custom
// checks get passed populated positional arguments.
if (!yargs._hasOutput()) yargs._runValidation(innerArgv, aliases, positionalMap, yargs.parsed.error)
...
```

#### <a name="apidoc.element.yargs._hasParseCallback"></a>[function <span class="apidocSignatureSpan">yargs.</span>_hasParseCallback ()](#apidoc.element.yargs._hasParseCallback)
- description and source-code
```javascript
_hasParseCallback = function () { [native code] }
```
- example usage
```shell
...
        logger.error(failMessage)
      }
    }

    err = err || new YError(msg)
    if (yargs.getExitProcess()) {
      return yargs.exit(1)
    } else if (yargs._hasParseCallback()) {
      return yargs.exit(1, err)
    } else {
      throw err
    }
  }
}
...
```

#### <a name="apidoc.element.yargs._parseArgs"></a>[function <span class="apidocSignatureSpan">yargs.</span>_parseArgs ()](#apidoc.element.yargs._parseArgs)
- description and source-code
```javascript
_parseArgs = function () { [native code] }
```
- example usage
```shell
...
  // and did not explicitly set a usage() string, then apply the
  // original command string as usage() for consistent behavior with
  // options object below.
  if (yargs.parsed === false) {
    if (typeof yargs.getUsageInstance().getUsage() === 'undefined') {
      yargs.usage('$0 ' + (parentCommands.length ? parentCommands.join(' ') + ' ' : '') + commandHandler.original)
    }
    innerArgv = innerYargs ? innerYargs._parseArgs(null, null, true) : yargs._parseArgs(null, null, true)
  } else {
    innerArgv = yargs.parsed.argv
  }

  if (innerYargs && yargs.parsed === false) aliases = innerYargs.parsed.aliases
  else aliases = yargs.parsed.aliases
} else if (typeof commandHandler.builder === 'object') {
...
```

#### <a name="apidoc.element.yargs._runValidation"></a>[function <span class="apidocSignatureSpan">yargs.</span>_runValidation ()](#apidoc.element.yargs._runValidation)
- description and source-code
```javascript
_runValidation = function () { [native code] }
```
- example usage
```shell
...

if (!yargs._hasOutput()) {
  positionalMap = populatePositionals(commandHandler, innerArgv, currentContext, yargs)
}

// we apply validation post-hoc, so that custom
// checks get passed populated positional arguments.
if (!yargs._hasOutput()) yargs._runValidation(innerArgv, aliases, positionalMap, yargs.parsed.error)

if (commandHandler.handler && !yargs._hasOutput()) {
  yargs._setHasOutput()
  commandHandler.handler(innerArgv)
}

if (command) currentContext.commands.pop()
...
```

#### <a name="apidoc.element.yargs._setHasOutput"></a>[function <span class="apidocSignatureSpan">yargs.</span>_setHasOutput ()](#apidoc.element.yargs._setHasOutput)
- description and source-code
```javascript
_setHasOutput = function () { [native code] }
```
- example usage
```shell
...
}

// we apply validation post-hoc, so that custom
// checks get passed populated positional arguments.
if (!yargs._hasOutput()) yargs._runValidation(innerArgv, aliases, positionalMap, yargs.parsed.error)

if (commandHandler.handler && !yargs._hasOutput()) {
  yargs._setHasOutput()
  commandHandler.handler(innerArgv)
}

if (command) currentContext.commands.pop()
numFiles = currentContext.files.length - numFiles
if (numFiles > 0) currentContext.files.splice(numFiles * -1, numFiles)
...
```

#### <a name="apidoc.element.yargs.addHelpOpt"></a>[function <span class="apidocSignatureSpan">yargs.</span>addHelpOpt ()](#apidoc.element.yargs.addHelpOpt)
- description and source-code
```javascript
addHelpOpt = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.yargs.alias"></a>[function <span class="apidocSignatureSpan">yargs.</span>alias ()](#apidoc.element.yargs.alias)
- description and source-code
```javascript
alias = function () { [native code] }
```
- example usage
```shell
...

count.js:

''''javascript
#!/usr/bin/env node
var argv = require('yargs')
    .count('verbose')
    .alias('v', 'verbose')
    .argv;

VERBOSE_LEVEL = argv.verbose;

function WARN()  { VERBOSE_LEVEL >= 0 && console.log.apply(console, arguments); }
function INFO()  { VERBOSE_LEVEL >= 1 && console.log.apply(console, arguments); }
function DEBUG() { VERBOSE_LEVEL >= 2 && console.log.apply(console, arguments); }
...
```

#### <a name="apidoc.element.yargs.array"></a>[function <span class="apidocSignatureSpan">yargs.</span>array ()](#apidoc.element.yargs.array)
- description and source-code
```javascript
array = function () { [native code] }
```
- example usage
```shell
...
works in bash or perl.

If 'yargs' is executed in an environment that embeds node and there's no script name (e.g.
[Electron](http://electron.atom.io/) or [nw.js](http://nwjs.io/)), it will ignore the first parameter since it
expects it to be the script name. In order to override this behavior, use '.parse(process.argv.slice(1))'
instead of '.argv' and the first parameter won't be ignored.

<a name="array"></a>.array(key)
----------

Tell the parser to interpret 'key' as an array. If '.array('foo')' is set,
'--foo foo bar' will be parsed as '['foo', 'bar']' rather than as ''foo''.

<a name="boolean"></a>.boolean(key)
-------------
...
```

#### <a name="apidoc.element.yargs.boolean"></a>[function <span class="apidocSignatureSpan">yargs.</span>boolean ()](#apidoc.element.yargs.boolean)
- description and source-code
```javascript
boolean = function () { [native code] }
```
- example usage
```shell
...
---------------------------------------------------------

boolean_single.js:

''''javascript
#!/usr/bin/env node
var argv = require('yargs')
    .boolean('v')
    .argv
;
console.dir(argv.v);
console.dir(argv._);
''''

***
...
```

#### <a name="apidoc.element.yargs.check"></a>[function <span class="apidocSignatureSpan">yargs.</span>check ()](#apidoc.element.yargs.check)
- description and source-code
```javascript
check = function () { [native code] }
```
- example usage
```shell
...
'process.argv', that string won't get set as the value of 'key'.

'key' will default to 'false', unless a 'default(key, undefined)' is
explicitly set.

If 'key' is an array, interpret all the elements as booleans.

.check(fn, [global=true])
----------

Check that certain conditions are met in the provided arguments.

'fn' is called with two arguments, the parsed 'argv' hash and an array of options and their aliases.

If 'fn' throws or returns a non-truthy value, show the thrown error, usage information, and
...
```

#### <a name="apidoc.element.yargs.choices"></a>[function <span class="apidocSignatureSpan">yargs.</span>choices ()](#apidoc.element.yargs.choices)
- description and source-code
```javascript
choices = function () { [native code] }
```
- example usage
```shell
...

If 'fn' throws or returns a non-truthy value, show the thrown error, usage information, and
exit.

'global' indicates whether 'check()' should be enabled both
at the top-level and for each sub-command.

<a name="choices"></a>.choices(key, choices)
----------------------

Limit valid values for 'key' to a predefined set of 'choices', given as an array
or as an individual value.

'''js
var argv = require('yargs')
...
```

#### <a name="apidoc.element.yargs.coerce"></a>[function <span class="apidocSignatureSpan">yargs.</span>coerce ()](#apidoc.element.yargs.coerce)
- description and source-code
```javascript
coerce = function () { [native code] }
```
- example usage
```shell
...
    alias: 's',
    describe: 'choose a size',
    choices: ['xs', 's', 'm', 'l', 'xl']
  })
  .argv
'''

<a name="coerce"></a>.coerce(key, fn)
----------------

Provide a synchronous function to coerce or transform the value(s) given on the
command line for 'key'.

The coercion function should accept one argument, representing the parsed value
from the command line, and should return a new value or throw an error. The
...
```

#### <a name="apidoc.element.yargs.command"></a>[function <span class="apidocSignatureSpan">yargs.</span>command ()](#apidoc.element.yargs.command)
- description and source-code
```javascript
command = function () { [native code] }
```
- example usage
```shell
...

line_count.js:

''''javascript
#!/usr/bin/env node
var argv = require('yargs')
.usage('Usage: $0 <command> [options]')
.command('count', 'Count the lines in a file')
.example('$0 count -f foo.js', 'count the lines in the given file')
.alias('f', 'file')
.nargs('f', 1)
.describe('f', 'Load a file')
.demandOption(['f'])
.help('h')
.alias('h', 'help')
...
```

#### <a name="apidoc.element.yargs.commandDir"></a>[function <span class="apidocSignatureSpan">yargs.</span>commandDir ()](#apidoc.element.yargs.commandDir)
- description and source-code
```javascript
commandDir = function () { [native code] }
```
- example usage
```shell
...

'''js
yargs.command('get <source> [proxy]', 'make a get HTTP request', require('my-module'))
  .help()
  .argv
'''

.commandDir(directory, [opts])
------------------------------

Apply command modules from a directory relative to the module calling this method.

This allows you to organize multiple commands into their own modules under a
single directory and apply all of them at once instead of calling
'.command(require('./dir/module'))' multiple times.
...
```

#### <a name="apidoc.element.yargs.completion"></a>[function <span class="apidocSignatureSpan">yargs.</span>completion ()](#apidoc.element.yargs.completion)
- description and source-code
```javascript
completion = function () { [native code] }
```
- example usage
```shell
...
exports.desc = 'Delete tracked branches gone stale for remotes'
exports.builder = {}
exports.handler = function (argv) {
  console.log('pruning remotes %s', [].concat(argv.name).concat(argv.names).join(', '))
}
'''

.completion([cmd], [description], [fn])
---------------------------------------

Enable bash-completion shortcuts for commands and options.

'cmd': When present in 'argv._', will result in the '.bashrc' completion script
being outputted. To enable bash completions, concat the generated script to your
'.bashrc' or '.bash_profile'.
...
```

#### <a name="apidoc.element.yargs.config"></a>[function <span class="apidocSignatureSpan">yargs.</span>config ()](#apidoc.element.yargs.config)
- description and source-code
```javascript
config = function () { [native code] }
```
- example usage
```shell
...
        resolve(['apple', 'banana'])
      }, 10)
    })
  })
  .argv;
'''

<a name="config"></a>.config([key], [description], [parseFn])
-------------------------------------------------------------
.config(object)
---------------

Tells the parser that if the option specified by 'key' is passed in, it
should be interpreted as a path to a JSON config file. The file is loaded
and parsed, and its properties are set as arguments. Because the file is
...
```

#### <a name="apidoc.element.yargs.conflicts"></a>[function <span class="apidocSignatureSpan">yargs.</span>conflicts ()](#apidoc.element.yargs.conflicts)
- description and source-code
```javascript
conflicts = function () { [native code] }
```
- example usage
```shell
...
  foo: 1,
  bar: 2,
  '$0': 'test.js' }
'''

Note that a configuration object may extend from a JSON file using the '"extends"' property. When doing so, the '"extends"' value
 should be a path (relative or absolute) to the extended JSON file.

<a name="conflicts"></a>.conflicts(x, y)
----------------------------------------------

Given the key 'x' is set, the key 'y' must not be set.

Optionally '.conflicts()' can accept an object specifying multiple conflicting keys.

<a name="count"></a>.count(key)
...
```

#### <a name="apidoc.element.yargs.count"></a>[function <span class="apidocSignatureSpan">yargs.</span>count ()](#apidoc.element.yargs.count)
- description and source-code
```javascript
count = function () { [native code] }
```
- example usage
```shell
...
----------------------------------------------------------------------

count.js:

''''javascript
#!/usr/bin/env node
var argv = require('yargs')
    .count('verbose')
    .alias('v', 'verbose')
    .argv;

VERBOSE_LEVEL = argv.verbose;

function WARN()  { VERBOSE_LEVEL >= 0 && console.log.apply(console, arguments); }
function INFO()  { VERBOSE_LEVEL >= 1 && console.log.apply(console, arguments); }
...
```

#### <a name="apidoc.element.yargs.default"></a>[function <span class="apidocSignatureSpan">yargs.</span>default ()](#apidoc.element.yargs.default)
- description and source-code
```javascript
default = function () { [native code] }
```
- example usage
```shell
...
------------------

default_singles.js:

''''javascript
#!/usr/bin/env node
var argv = require('yargs')
    .default('x', 10)
    .default('y', 10)
    .argv
;
console.log(argv.x + argv.y);
''''

***
...
```

#### <a name="apidoc.element.yargs.defaults"></a>[function <span class="apidocSignatureSpan">yargs.</span>defaults ()](#apidoc.element.yargs.defaults)
- description and source-code
```javascript
defaults = function () { [native code] }
```
- example usage
```shell
...
------------

Interpret 'key' as a boolean flag, but set its parsed value to the number of
flag occurrences rather than 'true' or 'false'. Default value is thus '0'.

<a name="default"></a>.default(key, value, [description])
---------------------------------------------------------
.defaults(key, value, [description])
------------------------------------

**Note:** The '.defaults()' alias is deprecated. It will be
removed in the next major version.

Set 'argv[key]' to 'value' if no option was specified in 'process.argv'.
...
```

#### <a name="apidoc.element.yargs.demand"></a>[function <span class="apidocSignatureSpan">yargs.</span>demand ()](#apidoc.element.yargs.demand)
- description and source-code
```javascript
demand = function () { [native code] }
```
- example usage
```shell
...
Optionally, 'description' can also be provided and will take precedence over
displaying the value in the usage instructions:

'''js
.default('timeout', 60000, '(one-minute)')
'''

<a name="demand"></a>.demand(count, [max], [msg]) [DEPRECATED]
--------------------

'demand()' has been deprecated, please instead see ['demandOption()'](#demandOption) and
['demandCommand()'](#demandCommand).

<a name="demandOption"></a>.demandOption(key, [msg | boolean])
------------------------------
...
```

#### <a name="apidoc.element.yargs.demandCommand"></a>[function <span class="apidocSignatureSpan">yargs.</span>demandCommand ()](#apidoc.element.yargs.demandCommand)
- description and source-code
```javascript
demandCommand = function () { [native code] }
```
- example usage
```shell
...
-----------------------------------------

demand_count.js:

''''javascript
#!/usr/bin/env node
var argv = require('yargs')
    .demandCommand(2)
    .argv;
console.dir(argv);
''''

***

	$ ./demand_count.js a
...
```

#### <a name="apidoc.element.yargs.demandOption"></a>[function <span class="apidocSignatureSpan">yargs.</span>demandOption ()](#apidoc.element.yargs.demandOption)
- description and source-code
```javascript
demandOption = function () { [native code] }
```
- example usage
```shell
...

area.js:

''''javascript
#!/usr/bin/env node
var argv = require('yargs')
    .usage('Usage: $0 -w [num] -h [num]')
    .demandOption(['w','h'])
    .argv;

console.log("The area is:", argv.w * argv.h);
''''

***
...
```

#### <a name="apidoc.element.yargs.describe"></a>[function <span class="apidocSignatureSpan">yargs.</span>describe ()](#apidoc.element.yargs.describe)
- description and source-code
```javascript
describe = function () { [native code] }
```
- example usage
```shell
...
#!/usr/bin/env node
var argv = require('yargs')
    .usage('Usage: $0 <command> [options]')
    .command('count', 'Count the lines in a file')
    .example('$0 count -f foo.js', 'count the lines in the given file')
    .alias('f', 'file')
    .nargs('f', 1)
    .describe('f', 'Load a file')
    .demandOption(['f'])
    .help('h')
    .alias('h', 'help')
    .epilog('copyright 2015')
    .argv;

var fs = require('fs');
...
```

#### <a name="apidoc.element.yargs.detectLocale"></a>[function <span class="apidocSignatureSpan">yargs.</span>detectLocale ()](#apidoc.element.yargs.detectLocale)
- description and source-code
```javascript
detectLocale = function () { [native code] }
```
- example usage
```shell
...
<a name="describe"></a>.describe(key, desc)
--------------------

Describe a 'key' for the generated usage information.

Optionally '.describe()' can take an object that maps keys to descriptions.

.detectLocale(boolean)
-----------

Should yargs attempt to detect the os' locale? Defaults to 'true'.

.env([prefix])
--------------
...
```

#### <a name="apidoc.element.yargs.env"></a>[function <span class="apidocSignatureSpan">yargs.</span>env ()](#apidoc.element.yargs.env)
- description and source-code
```javascript
env = function () { [native code] }
```
- example usage
```shell
...
Optionally '.describe()' can take an object that maps keys to descriptions.

.detectLocale(boolean)
-----------

Should yargs attempt to detect the os' locale? Defaults to 'true'.

.env([prefix])
--------------

Tell yargs to parse environment variables matching the given prefix and apply
them to argv as though they were command line arguments.

Use the "__" separator in the environment variable to indicate nested options.
(e.g. prefix_nested__foo => nested.foo)
...
```

#### <a name="apidoc.element.yargs.epilog"></a>[function <span class="apidocSignatureSpan">yargs.</span>epilog ()](#apidoc.element.yargs.epilog)
- description and source-code
```javascript
epilog = function () { [native code] }
```
- example usage
```shell
...
    .example('$0 count -f foo.js', 'count the lines in the given file')
    .alias('f', 'file')
    .nargs('f', 1)
    .describe('f', 'Load a file')
    .demandOption(['f'])
    .help('h')
    .alias('h', 'help')
    .epilog('copyright 2015')
    .argv;

var fs = require('fs');
var s = fs.createReadStream(argv.file);

var lines = 0;
s.on('data', function (buf) {
...
```

#### <a name="apidoc.element.yargs.epilogue"></a>[function <span class="apidocSignatureSpan">yargs.</span>epilogue ()](#apidoc.element.yargs.epilogue)
- description and source-code
```javascript
epilogue = function () { [native code] }
```
- example usage
```shell
...
'''

Env var parsing is disabled by default, but you can also explicitly disable it
by calling '.env(false)', e.g. if you need to undo previous configuration.

.epilog(str)
------------
.epilogue(str)
--------------

A message to print at the end of the usage instructions, e.g.

'''js
var argv = require('yargs')
.epilogue('for more information, find our manual at http://example.com');
...
```

#### <a name="apidoc.element.yargs.example"></a>[function <span class="apidocSignatureSpan">yargs.</span>example ()](#apidoc.element.yargs.example)
- description and source-code
```javascript
example = function () { [native code] }
```
- example usage
```shell
...
line_count.js:

''''javascript
#!/usr/bin/env node
var argv = require('yargs')
.usage('Usage: $0 <command> [options]')
.command('count', 'Count the lines in a file')
.example('$0 count -f foo.js', 'count the lines in the given file')
.alias('f', 'file')
.nargs('f', 1)
.describe('f', 'Load a file')
.demandOption(['f'])
.help('h')
.alias('h', 'help')
.epilog('copyright 2015')
...
```

#### <a name="apidoc.element.yargs.exit"></a>[function <span class="apidocSignatureSpan">yargs.</span>exit ()](#apidoc.element.yargs.exit)
- description and source-code
```javascript
exit = function () { [native code] }
```
- example usage
```shell
...
'''js
var argv = require('yargs')
  .fail(function (msg, err, yargs) {
    if (err) throw err // preserve stack
    console.error('You broke it!')
    console.error(msg)
    console.error('You should be doing', yargs.help())
    process.exit(1)
  })
  .argv
'''

.getCompletion(args, done);
---------------------------
...
```

#### <a name="apidoc.element.yargs.exitProcess"></a>[function <span class="apidocSignatureSpan">yargs.</span>exitProcess ()](#apidoc.element.yargs.exitProcess)
- description and source-code
```javascript
exitProcess = function () { [native code] }
```
- example usage
```shell
...
-------------------

Give some example invocations of your program. Inside 'cmd', the string
'$0' will get interpolated to the current script name or node command for the
present script similar to how '$0' works in bash or perl.
Examples will be printed out as part of the help message.

<a name="exitprocess"></a>.exitProcess(enable)
----------------------------------

By default, yargs exits the process when the user passes a help flag, uses the
'.version' functionality, or when validation fails. Calling
'.exitProcess(false)' disables this behavior, enabling further actions after
yargs have been validated.
...
```

#### <a name="apidoc.element.yargs.fail"></a>[function <span class="apidocSignatureSpan">yargs.</span>fail ()](#apidoc.element.yargs.fail)
- description and source-code
```javascript
fail = function () { [native code] }
```
- example usage
```shell
...

The coercion function should accept one argument, representing the parsed value
from the command line, and should return a new value or throw an error. The
returned value will be used as the value for 'key' (or one of its aliases) in
'argv'.

If the function throws, the error will be treated as a validation
failure, delegating to either a custom ['.fail()'](#fail) handler or printing
the error message in the console.

Coercion will be applied to a value after
all other modifications, such as ['.normalize()'](#normalize).

_Examples:_
...
```

#### <a name="apidoc.element.yargs.getCommandInstance"></a>[function <span class="apidocSignatureSpan">yargs.</span>getCommandInstance ()](#apidoc.element.yargs.getCommandInstance)
- description and source-code
```javascript
getCommandInstance = function () { [native code] }
```
- example usage
```shell
...
  }

  // check for unknown arguments (strict-mode).
  self.unknownArguments = function (argv, aliases, positionalMap) {
const aliasLookup = {}
const descriptions = usage.getDescriptions()
const demandedOptions = yargs.getDemandedOptions()
const commandKeys = yargs.getCommandInstance().getCommands()
const unknown = []
const currentContext = yargs.getContext()

Object.keys(aliases).forEach(function (key) {
  aliases[key].forEach(function (alias) {
    aliasLookup[alias] = key
  })
...
```

#### <a name="apidoc.element.yargs.getCompletion"></a>[function <span class="apidocSignatureSpan">yargs.</span>getCompletion ()](#apidoc.element.yargs.getCompletion)
- description and source-code
```javascript
getCompletion = function () { [native code] }
```
- example usage
```shell
...
    console.error(msg)
    console.error('You should be doing', yargs.help())
    process.exit(1)
  })
  .argv
'''

.getCompletion(args, done);
---------------------------

Allows to programmatically get completion choices for any line.

'args': An array of the words in the command line to complete.

'done': The callback to be called with the resulting completions.
...
```

#### <a name="apidoc.element.yargs.getContext"></a>[function <span class="apidocSignatureSpan">yargs.</span>getContext ()](#apidoc.element.yargs.getContext)
- description and source-code
```javascript
getContext = function () { [native code] }
```
- example usage
```shell
...
  self.hasDefaultCommand = function () {
return !!defaultCommand
  }

  self.runCommand = function (command, yargs, parsed) {
var aliases = parsed.aliases
var commandHandler = handlers[command] || handlers[aliasMap[command]] || defaultCommand
var currentContext = yargs.getContext()
var numFiles = currentContext.files.length
var parentCommands = currentContext.commands.slice()

// what does yargs look like after the buidler is run?
var innerArgv = parsed.argv
var innerYargs = null
var positionalMap = {}
...
```

#### <a name="apidoc.element.yargs.getDemandedCommands"></a>[function <span class="apidocSignatureSpan">yargs.</span>getDemandedCommands ()](#apidoc.element.yargs.getDemandedCommands)
- description and source-code
```javascript
getDemandedCommands = function () { [native code] }
```
- example usage
```shell
...

  var defaultGroup = 'Options:'
  self.help = function () {
normalizeAliases()

// handle old demanded API
var demandedOptions = yargs.getDemandedOptions()
var demandedCommands = yargs.getDemandedCommands()
var groups = yargs.getGroups()
var options = yargs.getOptions()
var keys = Object.keys(
  Object.keys(descriptions)
  .concat(Object.keys(demandedOptions))
  .concat(Object.keys(demandedCommands))
  .concat(Object.keys(options.default))
...
```

#### <a name="apidoc.element.yargs.getDemandedOptions"></a>[function <span class="apidocSignatureSpan">yargs.</span>getDemandedOptions ()](#apidoc.element.yargs.getDemandedOptions)
- description and source-code
```javascript
getDemandedOptions = function () { [native code] }
```
- example usage
```shell
...
  }

  var defaultGroup = 'Options:'
  self.help = function () {
normalizeAliases()

// handle old demanded API
var demandedOptions = yargs.getDemandedOptions()
var demandedCommands = yargs.getDemandedCommands()
var groups = yargs.getGroups()
var options = yargs.getOptions()
var keys = Object.keys(
  Object.keys(descriptions)
  .concat(Object.keys(demandedOptions))
  .concat(Object.keys(demandedCommands))
...
```

#### <a name="apidoc.element.yargs.getDetectLocale"></a>[function <span class="apidocSignatureSpan">yargs.</span>getDetectLocale ()](#apidoc.element.yargs.getDetectLocale)
- description and source-code
```javascript
getDetectLocale = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.yargs.getExitProcess"></a>[function <span class="apidocSignatureSpan">yargs.</span>getExitProcess ()](#apidoc.element.yargs.getExitProcess)
- description and source-code
```javascript
getExitProcess = function () { [native code] }
```
- example usage
```shell
...
    const logger = yargs._getLoggerInstance()

    if (fails.length) {
for (var i = fails.length - 1; i >= 0; --i) {
  fails[i](msg, err, self)
}
    } else {
if (yargs.getExitProcess()) setBlocking(true)

// don't output failure message more than once
if (!failureOutput) {
  failureOutput = true
  if (showHelpOnFail) yargs.showHelp('error')
  if (msg) logger.error(msg)
  if (failMessage) {
...
```

#### <a name="apidoc.element.yargs.getGroups"></a>[function <span class="apidocSignatureSpan">yargs.</span>getGroups ()](#apidoc.element.yargs.getGroups)
- description and source-code
```javascript
getGroups = function () { [native code] }
```
- example usage
```shell
...
  var defaultGroup = 'Options:'
  self.help = function () {
normalizeAliases()

// handle old demanded API
var demandedOptions = yargs.getDemandedOptions()
var demandedCommands = yargs.getDemandedCommands()
var groups = yargs.getGroups()
var options = yargs.getOptions()
var keys = Object.keys(
  Object.keys(descriptions)
  .concat(Object.keys(demandedOptions))
  .concat(Object.keys(demandedCommands))
  .concat(Object.keys(options.default))
  .reduce(function (acc, key) {
...
```

#### <a name="apidoc.element.yargs.getOptions"></a>[function <span class="apidocSignatureSpan">yargs.</span>getOptions ()](#apidoc.element.yargs.getOptions)
- description and source-code
```javascript
getOptions = function () { [native code] }
```
- example usage
```shell
...
    postProcessPositional(yargs, argv, cmd)
    addCamelCaseExpansions(argv, cmd)
  }
}

// TODO move positional arg logic to yargs-parser and remove this duplication
function postProcessPositional (yargs, argv, key) {
  var coerce = yargs.getOptions().coerce[key]
  if (typeof coerce === 'function') {
    try {
      argv[key] = coerce(argv[key])
    } catch (err) {
      yargs.getUsageInstance().fail(err.message, err)
    }
  }
...
```

#### <a name="apidoc.element.yargs.getStrict"></a>[function <span class="apidocSignatureSpan">yargs.</span>getStrict ()](#apidoc.element.yargs.getStrict)
- description and source-code
```javascript
getStrict = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.yargs.getUsageInstance"></a>[function <span class="apidocSignatureSpan">yargs.</span>getUsageInstance ()](#apidoc.element.yargs.getUsageInstance)
- description and source-code
```javascript
getUsageInstance = function () { [native code] }
```
- example usage
```shell
...
// up a yargs chain and possibly returns it.
innerYargs = commandHandler.builder(yargs.reset(parsed.aliases))
// if the builder function did not yet parse argv with reset yargs
// and did not explicitly set a usage() string, then apply the
// original command string as usage() for consistent behavior with
// options object below.
if (yargs.parsed === false) {
  if (typeof yargs.getUsageInstance().getUsage() === 'undefined') {
    yargs.usage('$0 ' + (parentCommands.length ? parentCommands.join(' ') + ' ' : '') + commandHandler.original)
  }
  innerArgv = innerYargs ? innerYargs._parseArgs(null, null, true) : yargs._parseArgs(null, null, true)
} else {
  innerArgv = yargs.parsed.argv
}
...
```

#### <a name="apidoc.element.yargs.getValidationInstance"></a>[function <span class="apidocSignatureSpan">yargs.</span>getValidationInstance ()](#apidoc.element.yargs.getValidationInstance)
- description and source-code
```javascript
getValidationInstance = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.yargs.global"></a>[function <span class="apidocSignatureSpan">yargs.</span>global ()](#apidoc.element.yargs.global)
- description and source-code
```javascript
global = function () { [native code] }
```
- example usage
```shell
...
  .getCompletion(['./test.js', '--foo'], function (completions) {
    console.log(completions)
  })
'''

Outputs the same completion choices as './test.js --foo'<kbd>TAB</kbd>: '--foobar' and '--foobaz'

<a name="global"></a>.global(globals, [global=true])
------------

Indicate that an option (or group of options) should not be reset when a command
is executed, as an example:

'''js
var argv = require('yargs')
...
```

#### <a name="apidoc.element.yargs.group"></a>[function <span class="apidocSignatureSpan">yargs.</span>group ()](#apidoc.element.yargs.group)
- description and source-code
```javascript
group = function () { [native code] }
```
- example usage
```shell
...
'''

If the 'foo' command is executed the 'all' option will remain, but the 'none'
option will have been eliminated.

Options default to being global.

<a name="group"></a>.group(key(s), groupName)
--------------------

Given a key, or an array of keys, places options under an alternative heading
when displaying usage instructions, e.g.,

'''js
var yargs = require('yargs')(['--help'])
...
```

#### <a name="apidoc.element.yargs.help"></a>[function <span class="apidocSignatureSpan">yargs.</span>help ()](#apidoc.element.yargs.help)
- description and source-code
```javascript
help = function () { [native code] }
```
- example usage
```shell
...
    .usage('Usage: $0 <command> [options]')
    .command('count', 'Count the lines in a file')
    .example('$0 count -f foo.js', 'count the lines in the given file')
    .alias('f', 'file')
    .nargs('f', 1)
    .describe('f', 'Load a file')
    .demandOption(['f'])
    .help('h')
    .alias('h', 'help')
    .epilog('copyright 2015')
    .argv;

var fs = require('fs');
var s = fs.createReadStream(argv.file);
...
```

#### <a name="apidoc.element.yargs.implies"></a>[function <span class="apidocSignatureSpan">yargs.</span>implies ()](#apidoc.element.yargs.implies)
- description and source-code
```javascript
implies = function () { [native code] }
```
- example usage
```shell
...
  .usage("$0 -operand1 number -operand2 number -operation [add|subtract]")
  .help()
  .argv
'''

Later on, 'argv' can be retrieved with 'yargs.argv'.

<a name="implies"></a>.implies(x, y)
--------------

Given the key 'x' is set, it is required that the key 'y' is set.

Optionally '.implies()' can accept an object specifying multiple implications.

.locale()
...
```

#### <a name="apidoc.element.yargs.locale"></a>[function <span class="apidocSignatureSpan">yargs.</span>locale ()](#apidoc.element.yargs.locale)
- description and source-code
```javascript
locale = function () { [native code] }
```
- example usage
```shell
...
<a name="implies"></a>.implies(x, y)
--------------

Given the key 'x' is set, it is required that the key 'y' is set.

Optionally '.implies()' can accept an object specifying multiple implications.

.locale()
---------

Return the locale that yargs is currently using.

By default, yargs will auto-detect the operating system's locale so that
yargs-generated help content will display in the user's language.
...
```

#### <a name="apidoc.element.yargs.nargs"></a>[function <span class="apidocSignatureSpan">yargs.</span>nargs ()](#apidoc.element.yargs.nargs)
- description and source-code
```javascript
nargs = function () { [native code] }
```
- example usage
```shell
...
''''javascript
#!/usr/bin/env node
var argv = require('yargs')
.usage('Usage: $0 <command> [options]')
.command('count', 'Count the lines in a file')
.example('$0 count -f foo.js', 'count the lines in the given file')
.alias('f', 'file')
.nargs('f', 1)
.describe('f', 'Load a file')
.demandOption(['f'])
.help('h')
.alias('h', 'help')
.epilog('copyright 2015')
.argv;
...
```

#### <a name="apidoc.element.yargs.normalize"></a>[function <span class="apidocSignatureSpan">yargs.</span>normalize ()](#apidoc.element.yargs.normalize)
- description and source-code
```javascript
normalize = function () { [native code] }
```
- example usage
```shell
...
'argv'.

If the function throws, the error will be treated as a validation
failure, delegating to either a custom ['.fail()'](#fail) handler or printing
the error message in the console.

Coercion will be applied to a value after
all other modifications, such as ['.normalize()'](#normalize).

_Examples:_

'''js
var argv = require('yargs')
.coerce('file', function (arg) {
  return require('fs').readFileSync(arg, 'utf8')
...
```

#### <a name="apidoc.element.yargs.number"></a>[function <span class="apidocSignatureSpan">yargs.</span>number ()](#apidoc.element.yargs.number)
- description and source-code
```javascript
number = function () { [native code] }
```
- example usage
```shell
...
Optionally '.nargs()' can take an object of 'key'/'narg' pairs.

<a name="normalize"></a>.normalize(key)
---------------

The key provided represents a path and should have 'path.normalize()' applied.

<a name="number"></a>.number(key)
------------

Tell the parser to always interpret 'key' as a number.

If 'key' is an array, all elements will be parsed as numbers.

If the option is given on the command line without a value, 'argv' will be
...
```

#### <a name="apidoc.element.yargs.option"></a>[function <span class="apidocSignatureSpan">yargs.</span>option ()](#apidoc.element.yargs.option)
- description and source-code
```javascript
option = function () { [native code] }
```
- example usage
```shell
...
Optionally '.choices()' can take an object that maps multiple keys to their
choices.

Choices can also be specified as 'choices' in the object given to 'option()'.

'''js
var argv = require('yargs')
  .option('size', {
    alias: 's',
    describe: 'choose a size',
    choices: ['xs', 's', 'm', 'l', 'xl']
  })
  .argv
'''
...
```

#### <a name="apidoc.element.yargs.options"></a>[function <span class="apidocSignatureSpan">yargs.</span>options ()](#apidoc.element.yargs.options)
- description and source-code
```javascript
options = function () { [native code] }
```
- example usage
```shell
...
--help      Show help                        [boolean]

Missing required arguments: run, path
Please provide both run and path arguments to work with this tool
'''

If a 'boolean' value is given, it controls whether the option is demanded;
this is useful when using '.options()' to specify command line parameters.

'''javascript
// demand individual options within the option constructor
require('yargs')
.options({
  'run': {
    alias: 'r',
...
```

#### <a name="apidoc.element.yargs.parse"></a>[function <span class="apidocSignatureSpan">yargs.</span>parse ()](#apidoc.element.yargs.parse)
- description and source-code
```javascript
parse = function () { [native code] }
```
- example usage
```shell
...

You can pass in the 'process.argv' yourself:

''''javascript
require('yargs')([ '-x', '1', '-y', '2' ]).argv
''''

or use '.parse()' to do the same thing:

''''javascript
require('yargs').parse([ '-x', '1', '-y', '2' ])
''''

The rest of these methods below come in just before the terminating '.argv'.
...
```

#### <a name="apidoc.element.yargs.pkgConf"></a>[function <span class="apidocSignatureSpan">yargs.</span>pkgConf ()](#apidoc.element.yargs.pkgConf)
- description and source-code
```javascript
pkgConf = function () { [native code] }
```
- example usage
```shell
...
parser.parse(bot.userText, function (err, argv, output) {
  if (output) bot.respond(output)
})
'''

***Note:*** Providing a callback to 'parse()' disables the ['exitProcess' setting](#exitprocess) until after the callback is invoked
.

.pkgConf(key, [cwd])
------------

Similar to ['config()'](#config), indicates that yargs should interpret the object from the specified key in package.json
as a configuration object.

'cwd' can optionally be provided, the package.json will be read
from this location.
...
```

#### <a name="apidoc.element.yargs.recommendCommands"></a>[function <span class="apidocSignatureSpan">yargs.</span>recommendCommands ()](#apidoc.element.yargs.recommendCommands)
- description and source-code
```javascript
recommendCommands = function () { [native code] }
```
- example usage
```shell
...
as a configuration object.

'cwd' can optionally be provided, the package.json will be read
from this location.

Note that a configuration stanza in package.json may extend from an identically keyed stanza in another package.json file using
the '"extends"' property. When doing so, the '"extends"' value should be a path (relative or absolute) to the extended package.json
 file.

.recommendCommands()
---------------------------

Should yargs provide suggestions regarding similar commands if no matching
command is found?

.require(key, [msg | boolean])
------------------------------
...
```

#### <a name="apidoc.element.yargs.require"></a>[function <span class="apidocSignatureSpan">yargs.</span>require ()](#apidoc.element.yargs.require)
- description and source-code
```javascript
require = function () { [native code] }
```
- example usage
```shell
...

.recommendCommands()
---------------------------

Should yargs provide suggestions regarding similar commands if no matching
command is found?

.require(key, [msg | boolean])
------------------------------
.required(key, [msg | boolean])
------------------------------

An alias for ['demand()'](#demand). See docs there.

<a name="requiresArg"></a>.requiresArg(key)
...
```

#### <a name="apidoc.element.yargs.required"></a>[function <span class="apidocSignatureSpan">yargs.</span>required ()](#apidoc.element.yargs.required)
- description and source-code
```javascript
required = function () { [native code] }
```
- example usage
```shell
...
---------------------------

Should yargs provide suggestions regarding similar commands if no matching
command is found?

.require(key, [msg | boolean])
------------------------------
.required(key, [msg | boolean])
------------------------------

An alias for ['demand()'](#demand). See docs there.

<a name="requiresArg"></a>.requiresArg(key)
-----------------
...
```

#### <a name="apidoc.element.yargs.requiresArg"></a>[function <span class="apidocSignatureSpan">yargs.</span>requiresArg ()](#apidoc.element.yargs.requiresArg)
- description and source-code
```javascript
requiresArg = function () { [native code] }
```
- example usage
```shell
...
.require(key, [msg | boolean])
------------------------------
.required(key, [msg | boolean])
------------------------------

An alias for ['demand()'](#demand). See docs there.

<a name="requiresArg"></a>.requiresArg(key)
-----------------

Specifies either a single option key (string), or an array of options that
must be followed by option values. If any option value is missing, show the
usage information and exit.

The default behavior is to set the value of any key not followed by an
...
```

#### <a name="apidoc.element.yargs.reset"></a>[function <span class="apidocSignatureSpan">yargs.</span>reset ()](#apidoc.element.yargs.reset)
- description and source-code
```javascript
reset = function () { [native code] }
```
- example usage
```shell
...
Specifies either a single option key (string), or an array of options that
must be followed by option values. If any option value is missing, show the
usage information and exit.

The default behavior is to set the value of any key not followed by an
option value to 'true'.

<a name="reset"></a>.reset()
--------

Reset the argument object built up so far. This is useful for
creating nested command line interfaces. Use [global](#global)
to specify keys that should not be reset.

'''js
...
```

#### <a name="apidoc.element.yargs.resetOptions"></a>[function <span class="apidocSignatureSpan">yargs.</span>resetOptions ()](#apidoc.element.yargs.resetOptions)
- description and source-code
```javascript
resetOptions = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.yargs.showCompletionScript"></a>[function <span class="apidocSignatureSpan">yargs.</span>showCompletionScript ()](#apidoc.element.yargs.showCompletionScript)
- description and source-code
```javascript
showCompletionScript = function () { [native code] }
```
- example usage
```shell
...

  console.log('world!');
} else {
  yargs.showHelp();
}
'''

.showCompletionScript()
----------------------

Generate a bash completion script. Users of your application can install this
script in their '.bashrc', and yargs will provide completion shortcuts for
commands and options.

.showHelp(consoleLevel='error')
...
```

#### <a name="apidoc.element.yargs.showHelp"></a>[function <span class="apidocSignatureSpan">yargs.</span>showHelp ()](#apidoc.element.yargs.showHelp)
- description and source-code
```javascript
showHelp = function () { [native code] }
```
- example usage
```shell
...
    .usage('$0 world')
    .help('h')
    .example('$0 world', 'print the world message!')
    .argv

  console.log('world!');
} else {
  yargs.showHelp();
}
'''

.showCompletionScript()
----------------------

Generate a bash completion script. Users of your application can install this
...
```

#### <a name="apidoc.element.yargs.showHelpOnFail"></a>[function <span class="apidocSignatureSpan">yargs.</span>showHelpOnFail ()](#apidoc.element.yargs.showHelpOnFail)
- description and source-code
```javascript
showHelpOnFail = function () { [native code] }
```
- example usage
```shell
...

'''js
yargs.showHelp("log"); //prints to stdout using console.log()
'''

Later on, 'argv' can be retrieved with 'yargs.argv'.

.showHelpOnFail(enable, [message])
----------------------------------

By default, yargs outputs a usage string if any error is detected. Use the
'.showHelpOnFail()' method to customize this behavior. If 'enable' is 'false',
the usage string is not output. If the 'message' parameter is present, this
message is output after the error message.
...
```

#### <a name="apidoc.element.yargs.skipValidation"></a>[function <span class="apidocSignatureSpan">yargs.</span>skipValidation ()](#apidoc.element.yargs.skipValidation)
- description and source-code
```javascript
skipValidation = function () { [native code] }
```
- example usage
```shell
...
'''
$ node line_count.js
Missing argument value: f

Specify --help for available options
'''

<a name="skipValidation"></a>.skipValidation(key)
-----------------

Specifies either a single option key (string), or an array of options.
If any of the options is present, yargs validation is skipped.

.strict([global=true])
---------
...
```

#### <a name="apidoc.element.yargs.strict"></a>[function <span class="apidocSignatureSpan">yargs.</span>strict ()](#apidoc.element.yargs.strict)
- description and source-code
```javascript
strict = function () { [native code] }
```
- example usage
```shell
...

<a name="skipValidation"></a>.skipValidation(key)
-----------------

Specifies either a single option key (string), or an array of options.
If any of the options is present, yargs validation is skipped.

.strict([global=true])
---------

Any command-line argument given that is not demanded, or does not have a
corresponding description, will be reported as an error.

'global' indicates whether 'strict()' should be enabled both
at the top-level and for each sub-command.
...
```

#### <a name="apidoc.element.yargs.string"></a>[function <span class="apidocSignatureSpan">yargs.</span>string ()](#apidoc.element.yargs.string)
- description and source-code
```javascript
string = function () { [native code] }
```
- example usage
```shell
...

''''javascript
var argv = require('yargs')
    .alias('f', 'file')
    .demandOption('f')
    .default('f', '/etc/passwd')
    .describe('f', 'x marks the spot')
    .string('f')
    .argv
;
''''

Optionally '.options()' can take an object that maps keys to 'opt' parameters.

''''javascript
...
```

#### <a name="apidoc.element.yargs.terminalWidth"></a>[function <span class="apidocSignatureSpan">yargs.</span>terminalWidth ()](#apidoc.element.yargs.terminalWidth)
- description and source-code
```javascript
terminalWidth = function () { [native code] }
```
- example usage
```shell
...

<a name="wrap"></a>.wrap(columns)
--------------

Format usage output to wrap at 'columns' many columns.

By default wrap will be set to 'Math.min(80, windowWidth)'. Use '.wrap(null)' to
specify no column limit (no right-align). Use '.wrap(yargs.terminalWidth())' to
maximize the width of yargs' usage instructions.

parsing tricks
==============

stop parsing
------------
...
```

#### <a name="apidoc.element.yargs.updateLocale"></a>[function <span class="apidocSignatureSpan">yargs.</span>updateLocale ()](#apidoc.element.yargs.updateLocale)
- description and source-code
```javascript
updateLocale = function () { [native code] }
```
- example usage
```shell
...
This can be useful if you need to preserve leading zeros in an input.

If 'key' is an array, interpret all the elements as strings.

'.string('_')' will result in non-hyphenated arguments being interpreted as strings,
regardless of whether they resemble numbers.

.updateLocale(obj)
------------------
.updateStrings(obj)
------------------

Override the default strings used by yargs with the key/value
pairs provided in 'obj':
...
```

#### <a name="apidoc.element.yargs.updateStrings"></a>[function <span class="apidocSignatureSpan">yargs.</span>updateStrings ()](#apidoc.element.yargs.updateStrings)
- description and source-code
```javascript
updateStrings = function () { [native code] }
```
- example usage
```shell
...
If 'key' is an array, interpret all the elements as strings.

'.string('_')' will result in non-hyphenated arguments being interpreted as strings,
regardless of whether they resemble numbers.

.updateLocale(obj)
------------------
.updateStrings(obj)
------------------

Override the default strings used by yargs with the key/value
pairs provided in 'obj':

'''js
var argv = require('yargs')
...
```

#### <a name="apidoc.element.yargs.usage"></a>[function <span class="apidocSignatureSpan">yargs.</span>usage ()](#apidoc.element.yargs.usage)
- description and source-code
```javascript
usage = function () { [native code] }
```
- example usage
```shell
...
-------------------------------------------------

area.js:

''''javascript
#!/usr/bin/env node
var argv = require('yargs')
    .usage('Usage: $0 -w [num] -h [num]')
    .demandOption(['w','h'])
    .argv;

console.log("The area is:", argv.w * argv.h);
''''

***
...
```

#### <a name="apidoc.element.yargs.version"></a>[function <span class="apidocSignatureSpan">yargs.</span>version ()](#apidoc.element.yargs.version)
- description and source-code
```javascript
version = function () { [native code] }
```
- example usage
```shell
...

Set a usage message to show which commands to use. Inside 'message', the string
'$0' will get interpolated to the current script name or node command for the
present script similar to how '$0' works in bash or perl.

'opts' is optional and acts like calling '.options(opts)'.

<a name="version"></a>.version([option], [description], [version])
----------------------------------------

Add an option (e.g. '--version') that displays the version number (given by the
'version' parameter) and exits the process.

If no arguments are passed to 'version' ('.version()'), yargs will parse the 'package.json'
of your module and use its 'version' value. The default value of 'option' is '--version'.
...
```

#### <a name="apidoc.element.yargs.wrap"></a>[function <span class="apidocSignatureSpan">yargs.</span>wrap ()](#apidoc.element.yargs.wrap)
- description and source-code
```javascript
wrap = function () { [native code] }
```
- example usage
```shell
...
  builder: (yargs) => yargs.default('value', 'true'),
  handler: (argv) => {
    console.log('setting ${argv.key} to ${argv.value}')
  }
})
.demandCommand()
.help()
.wrap(72)
.argv
'''

'''
$ ./svc.js help
Commands:
start [app]              Start up an app            [aliases: run, up]
...
```

#### <a name="apidoc.element.yargs.yerror"></a>[function <span class="apidocSignatureSpan">yargs.</span>yerror (msg)](#apidoc.element.yargs.yerror)
- description and source-code
```javascript
function YError(msg) {
  this.name = 'YError'
  this.message = msg || 'yargs error'
  Error.captureStackTrace(this, YError)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.yargs.yerror"></a>[module yargs.yerror](#apidoc.module.yargs.yerror)

#### <a name="apidoc.element.yargs.yerror.yerror"></a>[function <span class="apidocSignatureSpan">yargs.</span>yerror (msg)](#apidoc.element.yargs.yerror.yerror)
- description and source-code
```javascript
function YError(msg) {
  this.name = 'YError'
  this.message = msg || 'yargs error'
  Error.captureStackTrace(this, YError)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.yargs.yerror.prototype"></a>[module yargs.yerror.prototype](#apidoc.module.yargs.yerror.prototype)

#### <a name="apidoc.element.yargs.yerror.prototype.constructor"></a>[function <span class="apidocSignatureSpan">yargs.yerror.prototype.</span>constructor (msg)](#apidoc.element.yargs.yerror.prototype.constructor)
- description and source-code
```javascript
function YError(msg) {
  this.name = 'YError'
  this.message = msg || 'yargs error'
  Error.captureStackTrace(this, YError)
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
