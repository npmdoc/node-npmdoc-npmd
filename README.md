# api documentation for  [npmd (v1.4.0)](https://github.com/dominictarr/npmd)  [![npm package](https://img.shields.io/npm/v/npmdoc-npmd.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-npmd) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-npmd.svg)](https://travis-ci.org/npmdoc/node-npmdoc-npmd)
#### distributed npm client

[![NPM](https://nodei.co/npm/npmd.png?downloads=true)](https://www.npmjs.com/package/npmd)

[![apidoc](https://npmdoc.github.io/node-npmdoc-npmd/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-npmd_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-npmd/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-npmd/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-npmd/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Dominic Tarr",
        "email": "dominic.tarr@gmail.com",
        "url": "http://dominictarr.com"
    },
    "bin": {
        "npmd": "./index.js"
    },
    "bugs": {
        "url": "https://github.com/dominictarr/npmd/issues"
    },
    "dependencies": {
        "add-deps": "~1.2.0",
        "get-deps": "~2.0.4",
        "levelup": "~0.18.2",
        "medeadown": "~1.0.6",
        "mkdirp": "~0.5.0",
        "npmd-bin": "1.2",
        "npmd-build": "~0.1.3",
        "npmd-cache": "~4.3.1",
        "npmd-config": "~1.2.2",
        "npmd-install": "~5.1.2",
        "npmd-resolve": "~7.8.0",
        "npmd-tree": "~3.3.4",
        "to-camel-case": "~0.2.0"
    },
    "description": "distributed npm client",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "fc98f9ecbc8814c2651183436b0a4b3da0d3e3aa",
        "tarball": "https://registry.npmjs.org/npmd/-/npmd-1.4.0.tgz"
    },
    "gitHead": "88d73e1072e4632bc4f472a641bc16106e63561e",
    "homepage": "https://github.com/dominictarr/npmd",
    "license": "MIT",
    "maintainers": [
        {
            "name": "dominictarr",
            "email": "dominic.tarr@gmail.com"
        }
    ],
    "name": "npmd",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/dominictarr/npmd.git"
    },
    "scripts": {
        "build": "browserify client.js > static/bundle.js",
        "test": "./test.sh"
    },
    "version": "1.4.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module npmd](#apidoc.module.npmd)
1.  object <span class="apidocSignatureSpan">npmd.</span>add
1.  object <span class="apidocSignatureSpan">npmd.</span>dependents
1.  object <span class="apidocSignatureSpan">npmd.</span>help
1.  object <span class="apidocSignatureSpan">npmd.</span>install
1.  object <span class="apidocSignatureSpan">npmd.</span>packages
1.  object <span class="apidocSignatureSpan">npmd.</span>readme
1.  object <span class="apidocSignatureSpan">npmd.</span>resolve
1.  object <span class="apidocSignatureSpan">npmd.</span>tree
1.  object <span class="apidocSignatureSpan">npmd.</span>versions

#### [module npmd.add](#apidoc.module.npmd.add)
1.  [function <span class="apidocSignatureSpan">npmd.add.</span>cli (db)](#apidoc.element.npmd.add.cli)

#### [module npmd.dependents](#apidoc.module.npmd.dependents)
1.  [function <span class="apidocSignatureSpan">npmd.dependents.</span>cli (db)](#apidoc.element.npmd.dependents.cli)

#### [module npmd.help](#apidoc.module.npmd.help)
1.  [function <span class="apidocSignatureSpan">npmd.help.</span>cli (db, config)](#apidoc.element.npmd.help.cli)

#### [module npmd.install](#apidoc.module.npmd.install)
1.  [function <span class="apidocSignatureSpan">npmd.install.</span>commands (db, cache, config)](#apidoc.element.npmd.install.commands)

#### [module npmd.packages](#apidoc.module.npmd.packages)
1.  [function <span class="apidocSignatureSpan">npmd.packages.</span>cli (db, config)](#apidoc.element.npmd.packages.cli)

#### [module npmd.readme](#apidoc.module.npmd.readme)
1.  [function <span class="apidocSignatureSpan">npmd.readme.</span>cli (db, config)](#apidoc.element.npmd.readme.cli)

#### [module npmd.resolve](#apidoc.module.npmd.resolve)
1.  [function <span class="apidocSignatureSpan">npmd.resolve.</span>cli (db, cache)](#apidoc.element.npmd.resolve.cli)
1.  [function <span class="apidocSignatureSpan">npmd.resolve.</span>db (db, cache, config)](#apidoc.element.npmd.resolve.db)

#### [module npmd.tree](#apidoc.module.npmd.tree)
1.  [function <span class="apidocSignatureSpan">npmd.tree.</span>cli (db)](#apidoc.element.npmd.tree.cli)

#### [module npmd.versions](#apidoc.module.npmd.versions)
1.  [function <span class="apidocSignatureSpan">npmd.versions.</span>cli (db, config)](#apidoc.element.npmd.versions.cli)



# <a name="apidoc.module.npmd"></a>[module npmd](#apidoc.module.npmd)



# <a name="apidoc.module.npmd.add"></a>[module npmd.add](#apidoc.module.npmd.add)

#### <a name="apidoc.element.npmd.add.cli"></a>[function <span class="apidocSignatureSpan">npmd.add.</span>cli (db)](#apidoc.element.npmd.add.cli)
- description and source-code
```javascript
cli = function (db) {

  db.commands.push(function (db, config, cb) {
    var args = config._.slice()
    if(args.shift() !== 'add') return
    addDeps(process.cwd(), args, config, cb)
    return true
  })

}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.npmd.dependents"></a>[module npmd.dependents](#apidoc.module.npmd.dependents)

#### <a name="apidoc.element.npmd.dependents.cli"></a>[function <span class="apidocSignatureSpan">npmd.dependents.</span>cli (db)](#apidoc.element.npmd.dependents.cli)
- description and source-code
```javascript
cli = function (db) {
    var seen = {}
    db.commands.push(function (db, config, cb) {
        var args = config._.slice();
        if (args.shift() != "dependents") return;

        var modulenames = args;

        db.sublevel('ver').createReadStream({
        }).on('data', function (data) {
            var pkg = data.value;

            if (pkg.hasOwnProperty("dependencies") && pkg.dependencies != null) {
                var all = true;

                modulenames.forEach(function (modulename) {
                    if (!pkg.dependencies.hasOwnProperty(modulename))
                        all = false;
                });

                // TODO: pipe this off into some stream other than process.stdout
                if (all === true)
                    if (config.verbose)
                        console.log(pkg.name + "@" + pkg.version)
                    else {
                        if(seen[pkg.name]) return
                        seen[pkg.name] = true
                        console.log(pkg.name);
                    }
            }
        }).on('end', cb);

        return true;
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.npmd.help"></a>[module npmd.help](#apidoc.module.npmd.help)

#### <a name="apidoc.element.npmd.help.cli"></a>[function <span class="apidocSignatureSpan">npmd.help.</span>cli (db, config)](#apidoc.element.npmd.help.cli)
- description and source-code
```javascript
cli = function (db, config) {

  db.commands.push(function (db, cache, config, cb) {
    if(config._[0] !== 'help') return

    fs.createReadStream(__dirname + '/../docs/' + (config._[1] || 'help') + '.md')
    .on('end', cb)
    .on('error', function () {
      fs.readdir(__dirname + '/../docs/', function (err, list) {
        console.log('npmd help \n  ' +
          list
          .map(function (e) { return e.replace(/.md$/, '') })
          .filter(function (e) { return e!== 'help' })
          .sort().join(', ')
        )
        cb()
      })
      fs.createReadStream(__dirname + '/../docs/' + (config._[1] || 'help') + '.md')

    })
    .pipe(process.stdout)

    return true
  })
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.npmd.install"></a>[module npmd.install](#apidoc.module.npmd.install)

#### <a name="apidoc.element.npmd.install.commands"></a>[function <span class="apidocSignatureSpan">npmd.install.</span>commands (db, cache, config)](#apidoc.element.npmd.install.commands)
- description and source-code
```javascript
commands = function (db, cache, config) {

  if(!cache.get) throw new Error('must have cache')
  var install = require('npmd-install')(cache)

  db.commands.push(function (db, cache, config, cb) {
    var args = config._.slice()
    if('install' !== args.shift()) return

    var _args = args.slice(), data = ''
    if(!process.stdin.isTTY)
      process.stdin
        .on('data', function (d) { data += d })
        .on('end', function () { doInstall(JSON.parse(data)) })
    else
      db.resolve(args.slice(), config, function (err, tree) {
        if(err) return cb(err)
        doInstall(tree)
      })

    function doInstall (tree) {
      install(tree, config, function (err, installed) {
        if(err) return cb(err)

        if(config.save || config.saveDev)
          addDeps(config.path || process.cwd(), installed, config, next)
        else next()

        function next () {

          build(_args[0], config, function (err) {

            _args = _args.map(function (e) {
              e = e.split('@').shift()
              if(/^[./]/.test(e)) return e
              return config.global
                ? path.join(config.prefix, 'lib', 'node_modules', e)
                : path.join(process.cwd(), 'node_modules', e)
            })

            bin.all(_args, config.bin, config, function (err) {
              cb(err, installed)
            })

          })

        }
      })
    }


    return true
  })
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.npmd.packages"></a>[module npmd.packages](#apidoc.module.npmd.packages)

#### <a name="apidoc.element.npmd.packages.cli"></a>[function <span class="apidocSignatureSpan">npmd.packages.</span>cli (db, config)](#apidoc.element.npmd.packages.cli)
- description and source-code
```javascript
cli = function (db, config) {
  db.commands.push(function (db, config, cb) {
    var args = config._.slice()
    if(args.shift() != 'packages') return
    var module = args.shift() || ''
    db.sublevel('pkg').createReadStream({
      min: module , max: module + '~',
      keys: false
    }).on('data', function (data) {
      var pkg = data
      if(config.long)
        console.log(JSON.stringify(pkg, null, 2))
      else
        console.log(pkg.name)
    })
    .on('end', cb)
    return true
  })
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.npmd.readme"></a>[module npmd.readme](#apidoc.module.npmd.readme)

#### <a name="apidoc.element.npmd.readme.cli"></a>[function <span class="apidocSignatureSpan">npmd.readme.</span>cli (db, config)](#apidoc.element.npmd.readme.cli)
- description and source-code
```javascript
cli = function (db, config) {
  db.commands.push(function (db, config, cb) {
    var args = config._.slice()
    if(args.shift() != 'readme') return
    var module = args.shift()
    db.sublevel('pkg').get(module, function (err, data) {
      // console.log(arguments)
      if(err) return cb(err)
      if(!data.readme)
        console.log('sorry, readme file not found.')
      else
        console.log(data.readme)

      cb(null, data.readme || data)
    })
    return true
  })
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.npmd.resolve"></a>[module npmd.resolve](#apidoc.module.npmd.resolve)

#### <a name="apidoc.element.npmd.resolve.cli"></a>[function <span class="apidocSignatureSpan">npmd.resolve.</span>cli (db, cache)](#apidoc.element.npmd.resolve.cli)
- description and source-code
```javascript
cli = function (db, cache) {
  db.commands.push(function (db, cache, config, cb) {
    var args = config._.slice()
    var cmd = args.shift()

    if(cmd === 'resolve') {
      db.resolve(args, config,
        function (err, tree) {
          if(err) return cb(err)
          cb(null, tree)
      })

      return true
    }

  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.npmd.resolve.db"></a>[function <span class="apidocSignatureSpan">npmd.resolve.</span>db (db, cache, config)](#apidoc.element.npmd.resolve.db)
- description and source-code
```javascript
db = function (db, cache, config) {

  var resolve = createResolve(null, cache, config)
  db.methods.resolve = {type: 'async'}
  db.resolve = function (module, opts, cb) {
    if(!cb) cb = opts, opts = {}
    if(opts.hash) opts.greedy = false

    if(!module || !module.length)
      module = deps(process.cwd(), config)

    ls(function (err, tree) {
      if(err) return cb(err)
      resolve(module,
          merge({
            greedy: opts.greedy,
            available: tree
          }, config),
        cb
      )
    })
  }
}
```
- example usage
```shell
...
  })
}

function addDb (db, cache, config) {
  db.config = config
  plugins.forEach(function (e) {
    if('function' === typeof e.db)
      e.db(db, cache, config)
  })
}

//TODO: make a middleware like thing but with
//cli commands.

function execCommands (db, config, cb) {
...
```



# <a name="apidoc.module.npmd.tree"></a>[module npmd.tree](#apidoc.module.npmd.tree)

#### <a name="apidoc.element.npmd.tree.cli"></a>[function <span class="apidocSignatureSpan">npmd.tree.</span>cli (db)](#apidoc.element.npmd.tree.cli)
- description and source-code
```javascript
cli = function (db) {
  db.commands.push(function (db, cache, config, cb) {
    var args = config._.slice()
    var cmd = args.shift()

    if(cmd == 'tree') {
      tree.tree(config.installPath, config, function (err, tree) {
        if(err) throw err
        cb(null, tree)
      })
    }
    else if(cmd == 'ls')
      tree.ls(config.installPath, function (err, tree) {
        if(err) throw err
        cb(null, tree)
      })
    else
      return

    return true
  })
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.npmd.versions"></a>[module npmd.versions](#apidoc.module.npmd.versions)

#### <a name="apidoc.element.npmd.versions.cli"></a>[function <span class="apidocSignatureSpan">npmd.versions.</span>cli (db, config)](#apidoc.element.npmd.versions.cli)
- description and source-code
```javascript
cli = function (db, config) {
  db.commands.push(function (db, config, cb) {
    var args = config._.slice()
    if(args.shift() != 'versions') return
    var module = args.shift()
    db.sublevel('ver').createReadStream({
      min: module + '!', max: module + '!~'
    }).on('data', function (data) {
      var pkg = data.value
      if(config.long)
        console.log(pkg)
      else
        console.log(pkg.name + '@' + pkg.version)
    })
    .on('end', cb)
    return true
  })
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
