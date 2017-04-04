# api documentation for  [npm-run (v4.1.2)](https://github.com/timoxley/npm-run)  [![npm package](https://img.shields.io/npm/v/npmdoc-npm-run.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-npm-run) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-npm-run.svg)](https://travis-ci.org/npmdoc/node-npmdoc-npm-run)
#### Run executables for locally-installed packages without using ./node_modules/.bin

[![NPM](https://nodei.co/npm/npm-run.png?downloads=true)](https://www.npmjs.com/package/npm-run)

[![apidoc](https://npmdoc.github.io/node-npmdoc-npm-run/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-npm-run_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-npm-run/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-npm-run/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-npm-run/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Tim Oxley"
    },
    "bin": {
        "npm-run": "bin/npm-run.js"
    },
    "bugs": {
        "url": "https://github.com/timoxley/npm-run/issues"
    },
    "dependencies": {
        "cross-spawn": "^5.1.0",
        "minimist": "^1.2.0",
        "npm-path": "^2.0.3",
        "npm-which": "^3.0.1",
        "serializerr": "^1.0.3",
        "sync-exec": "^0.6.2"
    },
    "description": "Run executables for locally-installed packages without using ./node_modules/.bin",
    "devDependencies": {
        "bl": "^1.2.0",
        "standard": "^9.0.0",
        "tape": "^4.6.3"
    },
    "directories": {
        "test": "test"
    },
    "dist": {
        "shasum": "1030e1ec56908c89fcc3fa366d03a2c2ba98eb99",
        "tarball": "https://registry.npmjs.org/npm-run/-/npm-run-4.1.2.tgz"
    },
    "engines": {
        "node": ">=4.2.0"
    },
    "gitHead": "80a842e1509b8faaefaca65f06a8c23c2c971a2b",
    "homepage": "https://github.com/timoxley/npm-run",
    "keywords": [
        "npm",
        "path",
        "executable",
        ".bin",
        "run"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "timoxley",
            "email": "secoif@gmail.com"
        }
    ],
    "name": "npm-run",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/timoxley/npm-run.git"
    },
    "scripts": {
        "lint": "standard",
        "test": "tape test/*.js && npm run lint"
    },
    "version": "4.1.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module npm-run](#apidoc.module.npm-run)
1.  [function <span class="apidocSignatureSpan">npm-run.</span>exec (command, options, fn)](#apidoc.element.npm-run.exec)
1.  [function <span class="apidocSignatureSpan">npm-run.</span>execSync (command, options)](#apidoc.element.npm-run.execSync)
1.  [function <span class="apidocSignatureSpan">npm-run.</span>spawn (command, args, options, fn)](#apidoc.element.npm-run.spawn)
1.  [function <span class="apidocSignatureSpan">npm-run.</span>spawnSync (command, args, options)](#apidoc.element.npm-run.spawnSync)
1.  [function <span class="apidocSignatureSpan">npm-run.</span>sync (command, options)](#apidoc.element.npm-run.sync)



# <a name="apidoc.module.npm-run"></a>[module npm-run](#apidoc.module.npm-run)

#### <a name="apidoc.element.npm-run.exec"></a>[function <span class="apidocSignatureSpan">npm-run.</span>exec (command, options, fn)](#apidoc.element.npm-run.exec)
- description and source-code
```javascript
function npmExec(command, options, fn) {
  var a = normalizeExecArgs(command, options, fn)
  command = a[0]
  options = a[1]
  fn = a[2]
  return exec(command, augmentOptionsSync(options), fn)
}
```
- example usage
```shell
...

The API of 'npm-run' basically wraps core 'child_process' methods (exec, spawn, etc) such that locally install package executables
 will be on the PATH when the command runs.

## npmRun(command[, options], callback)

Alias of npmRun.exec.

## npmRun.exec(command[, options], callback)

Takes same arguments as node's [exec](https://nodejs.org/api/child_process.html#child_process_child_process_exec_command_options_callback
).

'''js
npmRun.exec('mocha --debug-brk --sort', {cwd: __dirname + '/tests'}, function (err, stdout, stderr) {
// err Error or null if there was no error
// stdout Buffer|String
...
```

#### <a name="apidoc.element.npm-run.execSync"></a>[function <span class="apidocSignatureSpan">npm-run.</span>execSync (command, options)](#apidoc.element.npm-run.execSync)
- description and source-code
```javascript
function npmExecSync(command, options) {
  var a = normalizeExecArgs(command, options)
  command = a[0]
  options = a[1]
  return execSync(command, augmentOptionsSync(options))
}
```
- example usage
```shell
...
})
'''

## npmRun.sync(command[, options])

Alias of npmRun.execSync

## npmRun.execSync(command[, options])

Takes same arguments as node's [execSync](https://nodejs.org/api/child_process.html#child_process_child_process_execsync_command_options
).

'''js
var stdout = npmRun.execSync(
'mocha --debug-brk --sort',
{cwd: __dirname + '/tests'}
...
```

#### <a name="apidoc.element.npm-run.spawn"></a>[function <span class="apidocSignatureSpan">npm-run.</span>spawn (command, args, options, fn)](#apidoc.element.npm-run.spawn)
- description and source-code
```javascript
function npmSpawn(command, args, options, fn) {
  var a = normalizeSpawnArgs(command, args, options, fn)
  command = a[0]
  args = a[1]
  options = a[2]
  fn = a[3]
  return spawn(command, args, augmentOptionsSync(options), fn)
}
```
- example usage
```shell
...
{cwd: __dirname + '/tests'}
)
child.stdout // stdout Buffer|String
child.stderr // stderr Buffer|String
child.status // exit code
'''

## npmRun.spawn(command[, args][, options])

Takes same arguments as node's [spawn](https://nodejs.org/api/child_process.html#child_process_child_process_spawn_command_args_options
).

'''js
var child = npmRun.spawn(
'mocha',
'--debug-brk --sort'.split(' '),
...
```

#### <a name="apidoc.element.npm-run.spawnSync"></a>[function <span class="apidocSignatureSpan">npm-run.</span>spawnSync (command, args, options)](#apidoc.element.npm-run.spawnSync)
- description and source-code
```javascript
function npmSpawnSync(command, args, options) {
  var a = normalizeSpawnArgs(command, args, options)
  command = a[0]
  args = a[1]
  options = a[2]
  return spawn.sync(command, args, augmentOptionsSync(options))
}
```
- example usage
```shell
...
var stdout = npmRun.execSync(
'mocha --debug-brk --sort',
{cwd: __dirname + '/tests'}
)
stdout // command output as Buffer|String
'''

## npmRun.spawnSync(command[, args][, options])

Takes same arguments as node's [spawnSync](https://nodejs.org/api/child_process.html#child_process_child_process_spawnsync_command_args_options
).

'''js
var child = npmRun.spawnSync(
'mocha',
'--debug-brk --sort'.split(' '),
...
```

#### <a name="apidoc.element.npm-run.sync"></a>[function <span class="apidocSignatureSpan">npm-run.</span>sync (command, options)](#apidoc.element.npm-run.sync)
- description and source-code
```javascript
function npmExecSync(command, options) {
  var a = normalizeExecArgs(command, options)
  command = a[0]
  options = a[1]
  return execSync(command, augmentOptionsSync(options))
}
```
- example usage
```shell
...
npmRun.exec('mocha --debug-brk --sort', {cwd: __dirname + '/tests'}, function (err, stdout, stderr) {
  // err Error or null if there was no error
  // stdout Buffer|String
  // stderr Buffer|String
})
'''

## npmRun.sync(command[, options])

Alias of npmRun.execSync

## npmRun.execSync(command[, options])

Takes same arguments as node's [execSync](https://nodejs.org/api/child_process.html#child_process_child_process_execsync_command_options
).
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
