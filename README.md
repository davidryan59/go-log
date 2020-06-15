## go-log

[![npm version](https:badge.fury.io/js/go-log.svg)](https:badge.fury.io/js/go-log)
[![Downloads per month](https://img.shields.io/npm/dy/go-log.svg?maxAge=31536000)](https://github.com/davidryan59/go-log)
[![Build status](https://travis-ci.org/davidryan59/go-log.svg?master)](https://travis-ci.org/davidryan59)

### Classes

**Logger** - log messages to the console

### Quick start

Do `npm install go-log` in your Javascript npm project directory. Then in a Javascript file:

``` js
import { Logger } from 'go-log'
const log = new Logger()
log.warn('You have successfully warned using go-log')
```

### Description

Logger - log various priorities of message to console

Usage:
``` js
const logger = new Logger({
   level: 7,
   shy: false,
   hideLevel: false,
})
logger.fatal('A fatal error')
logger.error('An error')
logger.warn('A warning')
logger.success('A success')
logger.info('An info')
logger.debug('A debug')
logger.trace('A trace')
logger.debug({ text: 'Text can be supplied as an object' })
logger.success({ obj: { or: 'you', can: 'log', any: 'object' } })
```

Log levels:
n = 0: log nothing
n = 1: only log fatal
n = 2: + errors
n = 3: + warnings
n = 4: + successes and new objects
n = 5: + info
n = 6: + debug
n = 7: + trace

shy = false: (default) logger prefixes its messages with its own name, helps to know how many loggers there are, which one is speaking
shy = true:  logger doesn't give its name when logging

hideLevel = false: (default) logger always shows the message level
hideLevel = true:  logger hides the level if is below FATAL, ERROR or WARNING
