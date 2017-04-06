# api documentation for  [csscomb (v4.0.1)](http://csscomb.com/)  [![npm package](https://img.shields.io/npm/v/npmdoc-csscomb.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-csscomb) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-csscomb.svg)](https://travis-ci.org/npmdoc/node-npmdoc-csscomb)
#### CSS coding style formatter

[![NPM](https://nodei.co/npm/csscomb.png?downloads=true)](https://www.npmjs.com/package/csscomb)

[![apidoc](https://npmdoc.github.io/node-npmdoc-csscomb/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-csscomb_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-csscomb/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-csscomb/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-csscomb/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Mikhail Troshev",
        "email": "mishanga@yandex-team.ru"
    },
    "bin": {
        "csscomb": "./bin/csscomb"
    },
    "bugs": {
        "url": "https://github.com/csscomb/csscomb.js/issues"
    },
    "dependencies": {
        "babel-polyfill": "6.23.0",
        "glob": "latest",
        "gonzales-pe": "^3.4.7",
        "minimatch": "3.0.2",
        "minimist": "1.1.x",
        "vow": "0.4.4",
        "vow-fs": "0.3.2"
    },
    "description": "CSS coding style formatter",
    "devDependencies": {
        "babel-cli": "^6.11.4",
        "babel-plugin-transform-es2015-destructuring": "^6.9.0",
        "babel-plugin-transform-strict-mode": "^6.11.3",
        "jscs": "2.1.0",
        "jshint": "2.8.0",
        "mocha": "1.20.1"
    },
    "directories": {},
    "dist": {
        "shasum": "a4b0139d7cf6223d635b6652ad31af0ee3e32331",
        "tarball": "https://registry.npmjs.org/csscomb/-/csscomb-4.0.1.tgz"
    },
    "engines": {
        "node": ">= 0.10.0"
    },
    "files": [
        "bin",
        "config",
        "lib"
    ],
    "gitHead": "4bbdac36231d93199687004e2890e760412dc9fd",
    "homepage": "http://csscomb.com/",
    "license": "MIT",
    "main": "./lib/csscomb.js",
    "maintainers": [
        {
            "name": "tonyganch",
            "email": "tonyganch+github@gmail.com"
        }
    ],
    "name": "csscomb",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/csscomb/csscomb.js.git"
    },
    "scripts": {
        "build": "./scripts/build.sh",
        "coverage": "./scripts/coverage.sh",
        "prepublish": "./scripts/build.sh",
        "test": "./scripts/build.sh && ./scripts/test.sh",
        "watch": "./scripts/watch.sh"
    },
    "version": "4.0.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module csscomb](#apidoc.module.csscomb)
1.  [function <span class="apidocSignatureSpan">csscomb.</span>detectInFile (file, options)](#apidoc.element.csscomb.detectInFile)
1.  [function <span class="apidocSignatureSpan">csscomb.</span>detectInString (text, options)](#apidoc.element.csscomb.detectInString)
1.  [function <span class="apidocSignatureSpan">csscomb.</span>getConfig (name)](#apidoc.element.csscomb.getConfig)
1.  [function <span class="apidocSignatureSpan">csscomb.</span>getCustomConfig (configPath)](#apidoc.element.csscomb.getCustomConfig)
1.  [function <span class="apidocSignatureSpan">csscomb.</span>getCustomConfigPath (configPath)](#apidoc.element.csscomb.getCustomConfigPath)
1.  [function <span class="apidocSignatureSpan">csscomb.</span>plugin (methods)](#apidoc.element.csscomb.plugin)
1.  object <span class="apidocSignatureSpan">csscomb.</span>errors
1.  object <span class="apidocSignatureSpan">csscomb.</span>plugin.prototype

#### [module csscomb.errors](#apidoc.module.csscomb.errors)
1.  [function <span class="apidocSignatureSpan">csscomb.errors.</span>configParsingError (configPath)](#apidoc.element.csscomb.errors.configParsingError)
1.  [function <span class="apidocSignatureSpan">csscomb.errors.</span>implementSetValue (valueType)](#apidoc.element.csscomb.errors.implementSetValue)
1.  [function <span class="apidocSignatureSpan">csscomb.errors.</span>missingName ()](#apidoc.element.csscomb.errors.missingName)
1.  [function <span class="apidocSignatureSpan">csscomb.errors.</span>missingSetValue ()](#apidoc.element.csscomb.errors.missingSetValue)
1.  [function <span class="apidocSignatureSpan">csscomb.errors.</span>missingSyntax ()](#apidoc.element.csscomb.errors.missingSyntax)
1.  [function <span class="apidocSignatureSpan">csscomb.errors.</span>missingTemplateFile (file)](#apidoc.element.csscomb.errors.missingTemplateFile)
1.  [function <span class="apidocSignatureSpan">csscomb.errors.</span>twoPluginsWithSameName (pluginName)](#apidoc.element.csscomb.errors.twoPluginsWithSameName)
1.  [function <span class="apidocSignatureSpan">csscomb.errors.</span>unacceptableBoolean (pattern)](#apidoc.element.csscomb.errors.unacceptableBoolean)
1.  [function <span class="apidocSignatureSpan">csscomb.errors.</span>unacceptableNumber ()](#apidoc.element.csscomb.errors.unacceptableNumber)
1.  [function <span class="apidocSignatureSpan">csscomb.errors.</span>unacceptableString (pattern)](#apidoc.element.csscomb.errors.unacceptableString)
1.  [function <span class="apidocSignatureSpan">csscomb.errors.</span>unacceptableValueType (valueType, accepts)](#apidoc.element.csscomb.errors.unacceptableValueType)

#### [module csscomb.plugin](#apidoc.module.csscomb.plugin)
1.  [function <span class="apidocSignatureSpan">csscomb.</span>plugin (methods)](#apidoc.element.csscomb.plugin.plugin)

#### [module csscomb.plugin.prototype](#apidoc.module.csscomb.plugin.prototype)
1.  [function <span class="apidocSignatureSpan">csscomb.plugin.prototype.</span>validate ()](#apidoc.element.csscomb.plugin.prototype.validate)
1.  object <span class="apidocSignatureSpan">csscomb.plugin.prototype.</span>accepts
1.  object <span class="apidocSignatureSpan">csscomb.plugin.prototype.</span>lint
1.  object <span class="apidocSignatureSpan">csscomb.plugin.prototype.</span>name
1.  object <span class="apidocSignatureSpan">csscomb.plugin.prototype.</span>process
1.  object <span class="apidocSignatureSpan">csscomb.plugin.prototype.</span>syntax
1.  object <span class="apidocSignatureSpan">csscomb.plugin.prototype.</span>value
1.  object <span class="apidocSignatureSpan">csscomb.plugin.prototype.</span>value_



# <a name="apidoc.module.csscomb"></a>[module csscomb](#apidoc.module.csscomb)

#### <a name="apidoc.element.csscomb.detectInFile"></a>[function <span class="apidocSignatureSpan">csscomb.</span>detectInFile (file, options)](#apidoc.element.csscomb.detectInFile)
- description and source-code
```javascript
function detectInFile(file, options) {
  var stylesheet = fs.readFileSync(file, 'utf8');
  return CSScomb.detectInString(stylesheet, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.csscomb.detectInString"></a>[function <span class="apidocSignatureSpan">csscomb.</span>detectInString (text, options)](#apidoc.element.csscomb.detectInString)
- description and source-code
```javascript
function detectInString(text, options) {
  var result;
  var handlers = [];

  if (!text) return text;

  var optionNames = fs.readdirSync(__dirname + '/options');
  optionNames.forEach(function (option) {
    option = option.slice(0, -3);
    if (options && options.indexOf(option) < 0) return;
    try {
      handlers.push(getHandler(option));
    } catch (e) {
      let message = '\nFailed to load "${option}" option:\n${e.message}';
      console.warn(message);
    }
  });

  var tree = cssToAST(text);
  var detectedOptions = detectInTree(tree, handlers);
  result = getDetectedOptions(detectedOptions, handlers);

  // Handle conflicting options with spaces around braces:
  var blockIndent = result['block-indent'];
  var spaceAfterOpeningBrace = result['space-after-opening-brace'];

  if (typeof blockIndent === 'string' && spaceAfterOpeningBrace && spaceAfterOpeningBrace.indexOf('\n') > -1) {
    result['space-after-opening-brace'] = '\n';
  }

  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.csscomb.getConfig"></a>[function <span class="apidocSignatureSpan">csscomb.</span>getConfig (name)](#apidoc.element.csscomb.getConfig)
- description and source-code
```javascript
function getConfig(name) {
  const DEFAULT_CONFIG_NAME = 'csscomb';
  name = name || DEFAULT_CONFIG_NAME;

  if (typeof name !== 'string') {
    throw new Error('Config name must be a string.');
  }

  let CONFIG_DIR_PATH = '../config';
  let dir = '${__dirname}/${CONFIG_DIR_PATH}';
  let availableConfigsNames = fs.readdirSync(dir).map(function (configFileName) {
    return configFileName.split('.')[0]; // Strip file extension(s)
  });

  if (availableConfigsNames.indexOf(name) < 0) {
    let configsNamesAsString = availableConfigsNames.map(function (configName) {
      return '\'' + configName + '\'';
    }).join(', ');
    let message = '"${name}" is not a valid config name. Try one
                   of the following: ${configsNamesAsString}.';
    throw new Error(format(message));
  }

  return require(CONFIG_DIR_PATH + '/' + name + '.json');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.csscomb.getCustomConfig"></a>[function <span class="apidocSignatureSpan">csscomb.</span>getCustomConfig (configPath)](#apidoc.element.csscomb.getCustomConfig)
- description and source-code
```javascript
function getCustomConfig(configPath) {
  var config;
  configPath = configPath || CSScomb.getCustomConfigPath();

  try {
    config = JSON.parse(fs.readFileSync(configPath, 'utf8'));
  } catch (e) {
    config = null;
  }

  return config;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.csscomb.getCustomConfigPath"></a>[function <span class="apidocSignatureSpan">csscomb.</span>getCustomConfigPath (configPath)](#apidoc.element.csscomb.getCustomConfigPath)
- description and source-code
```javascript
function getCustomConfigPath(configPath) {
  var HOME = process.env.HOME || process.env.HOMEPATH || process.env.USERPROFILE;

  configPath = configPath || path.join(process.cwd(), '.csscomb.json');

  // If we've finally found a config, return its path:
  if (fs.existsSync(configPath)) return fs.realpathSync(configPath);

  // If we are in HOME dir already and yet no config file, return a default
  // one from our package.
  // If project is located not under HOME, compare to root instead.
  // Since there appears to be no good way to get root path in
  // Windows, assume that if current dir has no parent dir, we're in
  // root.
  var dirname = path.dirname(configPath);
  var parentDirname = path.dirname(dirname);
  if (dirname === HOME || dirname === parentDirname) return null;

  // If there is no config in this directory, go one level up and look for
  // a config there:
  configPath = path.join(parentDirname, '.csscomb.json');
  return CSScomb.getCustomConfigPath(configPath);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.csscomb.plugin"></a>[function <span class="apidocSignatureSpan">csscomb.</span>plugin (methods)](#apidoc.element.csscomb.plugin)
- description and source-code
```javascript
plugin = function (methods) {
  for (let method in methods) {
    this[method] = typeof method === 'function' ? methods[method].bind(this) : methods[method];
  }

  this.validate();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.csscomb.errors"></a>[module csscomb.errors](#apidoc.module.csscomb.errors)

#### <a name="apidoc.element.csscomb.errors.configParsingError"></a>[function <span class="apidocSignatureSpan">csscomb.errors.</span>configParsingError (configPath)](#apidoc.element.csscomb.errors.configParsingError)
- description and source-code
```javascript
configParsingError(configPath) {
  return 'Error parsing configuration file ${configPath}.';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.csscomb.errors.implementSetValue"></a>[function <span class="apidocSignatureSpan">csscomb.errors.</span>implementSetValue (valueType)](#apidoc.element.csscomb.errors.implementSetValue)
- description and source-code
```javascript
implementSetValue(valueType) {
  if (typeof valueType === 'undefined') throw new Error();

  return format('If you see this message and you are not
      a developer adding a new option, please open an issue here:
      https://github.com/csscomb/core/issues/new\n
      For option to accept values of type "${valueType}"
      you need to implement custom \'setValue()\' method.');
}
```
- example usage
```shell
...

if (valueType = 'string') {
  if (!value.match(pattern)) throw new Error(Errors.unacceptableString(pattern));
  this.value_ = value;
  return this.value_;
}

throw new Error(Errors.implementSetValue(valueType));
  },

  validate() {
if (typeof this.name !== 'string' || !this.name) throw new Error(Errors.missingName());

if (!Array.isArray(this.syntax) || this.syntax.length === 0) throw new Error(Errors.missingSyntax());
...
```

#### <a name="apidoc.element.csscomb.errors.missingName"></a>[function <span class="apidocSignatureSpan">csscomb.errors.</span>missingName ()](#apidoc.element.csscomb.errors.missingName)
- description and source-code
```javascript
missingName() {
  return 'Plugin must have a valid \'name\' property.';
}
```
- example usage
```shell
...
      return this.value_;
    }

    throw new Error(Errors.implementSetValue(valueType));
  },

  validate() {
    if (typeof this.name !== 'string' || !this.name) throw new Error(Errors.missingName());

    if (!Array.isArray(this.syntax) || this.syntax.length === 0) throw new Error(Errors.missingSyntax());

    if (typeof this.accepts !== 'object' && typeof this.setValue !== 'function') throw new Error(Errors.missingSetValue());
  }
};
...
```

#### <a name="apidoc.element.csscomb.errors.missingSetValue"></a>[function <span class="apidocSignatureSpan">csscomb.errors.</span>missingSetValue ()](#apidoc.element.csscomb.errors.missingSetValue)
- description and source-code
```javascript
missingSetValue() {
  return format('Plugin must either implemet \'setValue()\' method
      or provide \'accepts\' object with acceptable values.');
}
```
- example usage
```shell
...
  },

  validate() {
    if (typeof this.name !== 'string' || !this.name) throw new Error(Errors.missingName());

    if (!Array.isArray(this.syntax) || this.syntax.length === 0) throw new Error(Errors.missingSyntax());

    if (typeof this.accepts !== 'object' && typeof this.setValue !== 'function') throw new Error(Errors.missingSetValue());
  }
};

module.exports = Plugin;
...
```

#### <a name="apidoc.element.csscomb.errors.missingSyntax"></a>[function <span class="apidocSignatureSpan">csscomb.errors.</span>missingSyntax ()](#apidoc.element.csscomb.errors.missingSyntax)
- description and source-code
```javascript
missingSyntax() {
  return 'Plugin must list supported syntaxes.';
}
```
- example usage
```shell
...

    throw new Error(Errors.implementSetValue(valueType));
  },

  validate() {
    if (typeof this.name !== 'string' || !this.name) throw new Error(Errors.missingName());

    if (!Array.isArray(this.syntax) || this.syntax.length === 0) throw new Error(Errors.missingSyntax());

    if (typeof this.accepts !== 'object' && typeof this.setValue !== 'function') throw new Error(Errors.missingSetValue());
  }
};

module.exports = Plugin;
...
```

#### <a name="apidoc.element.csscomb.errors.missingTemplateFile"></a>[function <span class="apidocSignatureSpan">csscomb.errors.</span>missingTemplateFile (file)](#apidoc.element.csscomb.errors.missingTemplateFile)
- description and source-code
```javascript
missingTemplateFile(file) {
  return format('Template configuration file ${file}
                 was not found.');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.csscomb.errors.twoPluginsWithSameName"></a>[function <span class="apidocSignatureSpan">csscomb.errors.</span>twoPluginsWithSameName (pluginName)](#apidoc.element.csscomb.errors.twoPluginsWithSameName)
- description and source-code
```javascript
twoPluginsWithSameName(pluginName) {
  if (typeof pluginName === 'undefined') throw new Error();

  return format('You're trying to use one plugin twice:
      ${pluginName}. Please make sure there are not two different
      plugins with the same name.');
}
```
- example usage
```shell
...
   * @param {Object} options
   * @return {Comb}
   */
  use(options) {
// Check whether plugin with the same is already used.
let pluginName = options.name;
if (this._pluginAlreadyUsed(pluginName)) {
  if (this.verbose) console.warn(Errors.twoPluginsWithSameName(pluginName));
  return;
}

let plugin = new Plugin(options);

plugin.syntax.forEach(function (s) {
  this.supportedSyntaxes.add(s);
...
```

#### <a name="apidoc.element.csscomb.errors.unacceptableBoolean"></a>[function <span class="apidocSignatureSpan">csscomb.errors.</span>unacceptableBoolean (pattern)](#apidoc.element.csscomb.errors.unacceptableBoolean)
- description and source-code
```javascript
unacceptableBoolean(pattern) {
  if (typeof pattern === 'undefined') throw new Error();

  return 'Value must be one of the following: ${pattern.join(', ')}.';
}
```
- example usage
```shell
...
  this.value_ = this.setValue(value);
  return this.value_;
}

if (!pattern) throw new Error(Errors.unacceptableValueType(valueType, this.accepts));

if (valueType === 'boolean') {
  if (pattern.indexOf(value) < 0) throw new Error(Errors.unacceptableBoolean(pattern));
  this.value_ = value;
  return this.value_;
}

if (valueType === 'number') {
  if (value !== parseInt(value)) throw new Error(Errors.unacceptableNumber());
  this.value_ = new Array(value + 1).join(' ');
...
```

#### <a name="apidoc.element.csscomb.errors.unacceptableNumber"></a>[function <span class="apidocSignatureSpan">csscomb.errors.</span>unacceptableNumber ()](#apidoc.element.csscomb.errors.unacceptableNumber)
- description and source-code
```javascript
unacceptableNumber() {
  return 'Value must be an integer.';
}
```
- example usage
```shell
...
if (valueType === 'boolean') {
  if (pattern.indexOf(value) < 0) throw new Error(Errors.unacceptableBoolean(pattern));
  this.value_ = value;
  return this.value_;
}

if (valueType === 'number') {
  if (value !== parseInt(value)) throw new Error(Errors.unacceptableNumber());
  this.value_ = new Array(value + 1).join(' ');
  return this.value_;
}

if (valueType = 'string') {
  if (!value.match(pattern)) throw new Error(Errors.unacceptableString(pattern));
  this.value_ = value;
...
```

#### <a name="apidoc.element.csscomb.errors.unacceptableString"></a>[function <span class="apidocSignatureSpan">csscomb.errors.</span>unacceptableString (pattern)](#apidoc.element.csscomb.errors.unacceptableString)
- description and source-code
```javascript
unacceptableString(pattern) {
  if (typeof pattern === 'undefined') throw new Error();

  return 'Value must match pattern ${pattern}.';
}
```
- example usage
```shell
...
  if (valueType === 'number') {
    if (value !== parseInt(value)) throw new Error(Errors.unacceptableNumber());
    this.value_ = new Array(value + 1).join(' ');
    return this.value_;
  }

  if (valueType = 'string') {
    if (!value.match(pattern)) throw new Error(Errors.unacceptableString(pattern));
    this.value_ = value;
    return this.value_;
  }

  throw new Error(Errors.implementSetValue(valueType));
},
...
```

#### <a name="apidoc.element.csscomb.errors.unacceptableValueType"></a>[function <span class="apidocSignatureSpan">csscomb.errors.</span>unacceptableValueType (valueType, accepts)](#apidoc.element.csscomb.errors.unacceptableValueType)
- description and source-code
```javascript
unacceptableValueType(valueType, accepts) {
  if (typeof valueType === 'undefined' || typeof accepts === 'undefined') throw new Error();

  return format('The option does not accept values of type
      ${valueType}.\nValue\'s type must be one the following:
      ${Object.keys(accepts).join(', ')}.');
}
```
- example usage
```shell
...
let pattern = this.accepts && this.accepts[valueType];

if (this.setValue) {
  this.value_ = this.setValue(value);
  return this.value_;
}

if (!pattern) throw new Error(Errors.unacceptableValueType(valueType, this.accepts));

if (valueType === 'boolean') {
  if (pattern.indexOf(value) < 0) throw new Error(Errors.unacceptableBoolean(pattern));
  this.value_ = value;
  return this.value_;
}
...
```



# <a name="apidoc.module.csscomb.plugin"></a>[module csscomb.plugin](#apidoc.module.csscomb.plugin)

#### <a name="apidoc.element.csscomb.plugin.plugin"></a>[function <span class="apidocSignatureSpan">csscomb.</span>plugin (methods)](#apidoc.element.csscomb.plugin.plugin)
- description and source-code
```javascript
plugin = function (methods) {
  for (let method in methods) {
    this[method] = typeof method === 'function' ? methods[method].bind(this) : methods[method];
  }

  this.validate();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.csscomb.plugin.prototype"></a>[module csscomb.plugin.prototype](#apidoc.module.csscomb.plugin.prototype)

#### <a name="apidoc.element.csscomb.plugin.prototype.validate"></a>[function <span class="apidocSignatureSpan">csscomb.plugin.prototype.</span>validate ()](#apidoc.element.csscomb.plugin.prototype.validate)
- description and source-code
```javascript
validate() {
  if (typeof this.name !== 'string' || !this.name) throw new Error(Errors.missingName());

  if (!Array.isArray(this.syntax) || this.syntax.length === 0) throw new Error(Errors.missingSyntax());

  if (typeof this.accepts !== 'object' && typeof this.setValue !== 'function') throw new Error(Errors.missingSetValue());
}
```
- example usage
```shell
...
let Errors = require('./errors');

let Plugin = function (methods) {
for (let method in methods) {
  this[method] = typeof method === 'function' ? methods[method].bind(this) : methods[method];
}

this.validate();
};

Plugin.prototype = {
/**
 * Plugin's name.
 * @type {String}
 */
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
