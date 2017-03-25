# api documentation for  [supertest (v3.0.0)](https://github.com/visionmedia/supertest#readme)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-supertest.svg)](https://travis-ci.org/npmdoc/node-npmdoc-supertest)
#### SuperAgent driven library for testing HTTP servers

[![NPM](https://nodei.co/npm/supertest.png?downloads=true)](https://www.npmjs.com/package/supertest)

[![apidoc](https://npmdoc.github.io/node-npmdoc-supertest/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-supertest_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-supertest/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-supertest/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "TJ Holowaychuk"
    },
    "bugs": {
        "url": "https://github.com/visionmedia/supertest/issues"
    },
    "dependencies": {
        "methods": "~1.1.2",
        "superagent": "^3.0.0"
    },
    "description": "SuperAgent driven library for testing HTTP servers",
    "devDependencies": {
        "body-parser": "~1.16.0",
        "cookie-parser": "~1.4.1",
        "eslint": "^3.14.1",
        "eslint-config-airbnb": "^12.0.0",
        "eslint-plugin-import": "1.16.0",
        "eslint-plugin-jsx-a11y": "2.2.3",
        "eslint-plugin-react": "6.4.1",
        "express": "~4.14.0",
        "mocha": "~3.2.0",
        "should": "~11.2.0"
    },
    "directories": {},
    "dist": {
        "shasum": "8d4bb68fd1830ee07033b1c5a5a9a4021c965296",
        "tarball": "https://registry.npmjs.org/supertest/-/supertest-3.0.0.tgz"
    },
    "engines": {
        "node": ">=4.0.0"
    },
    "gitHead": "199506d8dbfe0bb1434fc07c38cdcd1ab4c7c926",
    "homepage": "https://github.com/visionmedia/supertest#readme",
    "keywords": [
        "superagent",
        "request",
        "tdd",
        "bdd",
        "http",
        "test",
        "testing"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "tjholowaychuk",
            "email": "tj@vision-media.ca"
        },
        {
            "name": "gjohnson",
            "email": "gjj391@gmail.com"
        },
        {
            "name": "kof",
            "email": "oleg008@gmail.com"
        },
        {
            "name": "defunctzombie",
            "email": "shtylman@gmail.com"
        },
        {
            "name": "mikelax",
            "email": "mholtzman@gmail.com"
        }
    ],
    "name": "supertest",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/visionmedia/supertest.git"
    },
    "scripts": {
        "pretest": "npm install",
        "test": "eslint lib/**/*.js test/**/*.js && mocha --require should --reporter spec --check-leaks"
    },
    "version": "3.0.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module supertest](#apidoc.module.supertest)
1.  [function <span class="apidocSignatureSpan">supertest.</span>Test (app, method, path)](#apidoc.element.supertest.Test)
1.  [function <span class="apidocSignatureSpan">supertest.</span>agent (app, options)](#apidoc.element.supertest.agent)
1.  object <span class="apidocSignatureSpan">supertest.</span>Test.prototype
1.  object <span class="apidocSignatureSpan">supertest.</span>agent.prototype

#### [module supertest.Test](#apidoc.module.supertest.Test)
1.  [function <span class="apidocSignatureSpan">supertest.</span>Test (app, method, path)](#apidoc.element.supertest.Test.Test)

#### [module supertest.Test.prototype](#apidoc.module.supertest.Test.prototype)
1.  [function <span class="apidocSignatureSpan">supertest.Test.prototype.</span>_assertBody (body, res)](#apidoc.element.supertest.Test.prototype._assertBody)
1.  [function <span class="apidocSignatureSpan">supertest.Test.prototype.</span>_assertFunction (check, res)](#apidoc.element.supertest.Test.prototype._assertFunction)
1.  [function <span class="apidocSignatureSpan">supertest.Test.prototype.</span>_assertHeader (header, res)](#apidoc.element.supertest.Test.prototype._assertHeader)
1.  [function <span class="apidocSignatureSpan">supertest.Test.prototype.</span>_assertStatus (status, res)](#apidoc.element.supertest.Test.prototype._assertStatus)
1.  [function <span class="apidocSignatureSpan">supertest.Test.prototype.</span>assert (resError, res, fn)](#apidoc.element.supertest.Test.prototype.assert)
1.  [function <span class="apidocSignatureSpan">supertest.Test.prototype.</span>end (fn)](#apidoc.element.supertest.Test.prototype.end)
1.  [function <span class="apidocSignatureSpan">supertest.Test.prototype.</span>expect (a, b, c)](#apidoc.element.supertest.Test.prototype.expect)
1.  [function <span class="apidocSignatureSpan">supertest.Test.prototype.</span>serverAddress (app, path)](#apidoc.element.supertest.Test.prototype.serverAddress)

#### [module supertest.agent](#apidoc.module.supertest.agent)
1.  [function <span class="apidocSignatureSpan">supertest.</span>agent (app, options)](#apidoc.element.supertest.agent.agent)

#### [module supertest.agent.prototype](#apidoc.module.supertest.agent.prototype)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>acl (url, fn)](#apidoc.element.supertest.agent.prototype.acl)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>bind (url, fn)](#apidoc.element.supertest.agent.prototype.bind)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>checkout (url, fn)](#apidoc.element.supertest.agent.prototype.checkout)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>connect (url, fn)](#apidoc.element.supertest.agent.prototype.connect)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>copy (url, fn)](#apidoc.element.supertest.agent.prototype.copy)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>del (url, fn)](#apidoc.element.supertest.agent.prototype.del)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>delete (url, fn)](#apidoc.element.supertest.agent.prototype.delete)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>get (url, fn)](#apidoc.element.supertest.agent.prototype.get)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>head (url, fn)](#apidoc.element.supertest.agent.prototype.head)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>link (url, fn)](#apidoc.element.supertest.agent.prototype.link)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>lock (url, fn)](#apidoc.element.supertest.agent.prototype.lock)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>m-search (url, fn)](#apidoc.element.supertest.agent.prototype.m-search)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>merge (url, fn)](#apidoc.element.supertest.agent.prototype.merge)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>mkactivity (url, fn)](#apidoc.element.supertest.agent.prototype.mkactivity)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>mkcalendar (url, fn)](#apidoc.element.supertest.agent.prototype.mkcalendar)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>mkcol (url, fn)](#apidoc.element.supertest.agent.prototype.mkcol)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>move (url, fn)](#apidoc.element.supertest.agent.prototype.move)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>notify (url, fn)](#apidoc.element.supertest.agent.prototype.notify)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>options (url, fn)](#apidoc.element.supertest.agent.prototype.options)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>patch (url, fn)](#apidoc.element.supertest.agent.prototype.patch)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>post (url, fn)](#apidoc.element.supertest.agent.prototype.post)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>propfind (url, fn)](#apidoc.element.supertest.agent.prototype.propfind)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>proppatch (url, fn)](#apidoc.element.supertest.agent.prototype.proppatch)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>purge (url, fn)](#apidoc.element.supertest.agent.prototype.purge)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>put (url, fn)](#apidoc.element.supertest.agent.prototype.put)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>rebind (url, fn)](#apidoc.element.supertest.agent.prototype.rebind)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>report (url, fn)](#apidoc.element.supertest.agent.prototype.report)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>search (url, fn)](#apidoc.element.supertest.agent.prototype.search)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>subscribe (url, fn)](#apidoc.element.supertest.agent.prototype.subscribe)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>trace (url, fn)](#apidoc.element.supertest.agent.prototype.trace)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>unbind (url, fn)](#apidoc.element.supertest.agent.prototype.unbind)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>unlink (url, fn)](#apidoc.element.supertest.agent.prototype.unlink)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>unlock (url, fn)](#apidoc.element.supertest.agent.prototype.unlock)
1.  [function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>unsubscribe (url, fn)](#apidoc.element.supertest.agent.prototype.unsubscribe)



# <a name="apidoc.module.supertest"></a>[module supertest](#apidoc.module.supertest)

#### <a name="apidoc.element.supertest.Test"></a>[function <span class="apidocSignatureSpan">supertest.</span>Test (app, method, path)](#apidoc.element.supertest.Test)
- description and source-code
```javascript
function Test(app, method, path) {
  Request.call(this, method.toUpperCase(), path);
  this.redirects(0);
  this.buffer();
  this.app = app;
  this._asserts = [];
  this.url = typeof app === 'string'
    ? app + path
    : this.serverAddress(app, path);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent"></a>[function <span class="apidocSignatureSpan">supertest.</span>agent (app, options)](#apidoc.element.supertest.agent)
- description and source-code
```javascript
function TestAgent(app, options) {
  if (!(this instanceof TestAgent)) return new TestAgent(app, options);
  if (typeof app === 'function') app = http.createServer(app);  // eslint-disable-line no-param-reassign
  if (options) {
    this._ca = options.ca;
    this._key = options.key;
    this._cert = options.cert;
  }
  Agent.call(this);
  this.app = app;
}
```
- example usage
```shell
...

'''js
const request = require('supertest');
const should = require('should');
const express = require('express');
const cookieParser = require('cookie-parser');

describe('request.agent(app)', function() {
const app = express();
app.use(cookieParser());

app.get('/', function(req, res) {
  res.cookie('cookie', 'hey');
  res.send();
});
...
```



# <a name="apidoc.module.supertest.Test"></a>[module supertest.Test](#apidoc.module.supertest.Test)

#### <a name="apidoc.element.supertest.Test.Test"></a>[function <span class="apidocSignatureSpan">supertest.</span>Test (app, method, path)](#apidoc.element.supertest.Test.Test)
- description and source-code
```javascript
function Test(app, method, path) {
  Request.call(this, method.toUpperCase(), path);
  this.redirects(0);
  this.buffer();
  this.app = app;
  this._asserts = [];
  this.url = typeof app === 'string'
    ? app + path
    : this.serverAddress(app, path);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.supertest.Test.prototype"></a>[module supertest.Test.prototype](#apidoc.module.supertest.Test.prototype)

#### <a name="apidoc.element.supertest.Test.prototype._assertBody"></a>[function <span class="apidocSignatureSpan">supertest.Test.prototype.</span>_assertBody (body, res)](#apidoc.element.supertest.Test.prototype._assertBody)
- description and source-code
```javascript
_assertBody = function (body, res) {
  var isregexp = body instanceof RegExp;
  var a;
  var b;

  // parsed
  if (typeof body === 'object' && !isregexp) {
    try {
      assert.deepEqual(body, res.body);
    } catch (err) {
      a = util.inspect(body);
      b = util.inspect(res.body);
      return error('expected ' + a + ' response body, got ' + b, body, res.body);
    }
  } else if (body !== res.text) {
    // string
    a = util.inspect(body);
    b = util.inspect(res.text);

    // regexp
    if (isregexp) {
      if (!body.test(res.text)) {
        return error('expected body ' + b + ' to match ' + body, body, res.body);
      }
    } else {
      return error('expected ' + a + ' response body, got ' + b, body, res.body);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.Test.prototype._assertFunction"></a>[function <span class="apidocSignatureSpan">supertest.Test.prototype.</span>_assertFunction (check, res)](#apidoc.element.supertest.Test.prototype._assertFunction)
- description and source-code
```javascript
_assertFunction = function (check, res) {
  var err;
  try {
    err = check(res);
  } catch (e) {
    err = e;
  }
  if (err instanceof Error) return err;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.Test.prototype._assertHeader"></a>[function <span class="apidocSignatureSpan">supertest.Test.prototype.</span>_assertHeader (header, res)](#apidoc.element.supertest.Test.prototype._assertHeader)
- description and source-code
```javascript
_assertHeader = function (header, res) {
  var field = header.name;
  var actual = res.header[field.toLowerCase()];
  var fieldExpected = header.value;

  if (typeof actual === 'undefined') return new Error('expected "' + field + '" header field');
  // This check handles header values that may be a String or single element Array
  if ((actual instanceof Array && actual.toString() === fieldExpected) ||
    fieldExpected === actual) {
    return;
  }
  if (fieldExpected instanceof RegExp) {
    if (!fieldExpected.test(actual)) {
      return new Error('expected "' + field + '" matching ' +
        fieldExpected + ', got "' + actual + '"');
    }
  } else {
    return new Error('expected "' + field + '" of "' + fieldExpected + '", got "' + actual + '"');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.Test.prototype._assertStatus"></a>[function <span class="apidocSignatureSpan">supertest.Test.prototype.</span>_assertStatus (status, res)](#apidoc.element.supertest.Test.prototype._assertStatus)
- description and source-code
```javascript
_assertStatus = function (status, res) {
  var a;
  var b;
  if (res.status !== status) {
    a = http.STATUS_CODES[status];
    b = http.STATUS_CODES[res.status];
    return new Error('expected ' + status + ' "' + a + '", got ' + res.status + ' "' + b + '"');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.Test.prototype.assert"></a>[function <span class="apidocSignatureSpan">supertest.Test.prototype.</span>assert (resError, res, fn)](#apidoc.element.supertest.Test.prototype.assert)
- description and source-code
```javascript
assert = function (resError, res, fn) {
  var error;
  var i;

  // check for unexpected network errors or server not running/reachable errors
  // when there is no response and superagent sends back a System Error
  // do not check further for other asserts, if any, in such case
  // https://nodejs.org/api/errors.html#errors_common_system_errors
  var sysErrors = {
    ECONNREFUSED: 'Connection refused',
    ECONNRESET: 'Connection reset by peer',
    EPIPE: 'Broken pipe',
    ETIMEDOUT: 'Operation timed out'
  };

  if (!res && resError && (resError instanceof Error) && (resError.syscall === 'connect')
      && (Object.getOwnPropertyNames(sysErrors).indexOf(resError.code) >= 0)) {
    error = new Error(resError.code + ': ' + sysErrors[resError.code]);
    fn.call(this, error, null);
    return;
  }

  // asserts
  for (i = 0; i < this._asserts.length && !error; i += 1) {
    error = this._assertFunction(this._asserts[i], res);
  }

  // set unexpected superagent error if no other error has occurred.
  if (!error && resError instanceof Error && (!res || resError.status !== res.status)) {
    error = resError;
  }

  fn.call(this, error || null, res);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.Test.prototype.end"></a>[function <span class="apidocSignatureSpan">supertest.Test.prototype.</span>end (fn)](#apidoc.element.supertest.Test.prototype.end)
- description and source-code
```javascript
end = function (fn) {
  var self = this;
  var server = this._server;
  var end = Request.prototype.end;

  end.call(this, function(err, res) {
    if (server && server._handle) return server.close(assert);

    assert();

    function assert() {
      self.assert(err, res, fn);
    }
  });

  return this;
}
```
- example usage
```shell
...
});

request(app)
  .get('/user')
  .expect('Content-Type', /json/)
  .expect('Content-Length', '15')
  .expect(200)
  .end(function(err, res) {
    if (err) throw err;
  });
'''

  Here's an example with mocha, note how you can pass 'done' straight to any of the '.expect()' calls:

'''js
...
```

#### <a name="apidoc.element.supertest.Test.prototype.expect"></a>[function <span class="apidocSignatureSpan">supertest.Test.prototype.</span>expect (a, b, c)](#apidoc.element.supertest.Test.prototype.expect)
- description and source-code
```javascript
expect = function (a, b, c) {
  // callback
  if (typeof a === 'function') {
    this._asserts.push(a);
    return this;
  }
  if (typeof b === 'function') this.end(b);
  if (typeof c === 'function') this.end(c);

  // status
  if (typeof a === 'number') {
    this._asserts.push(this._assertStatus.bind(this, a));
    // body
    if (typeof b !== 'function' && arguments.length > 1) {
      this._asserts.push(this._assertBody.bind(this, b));
    }
    return this;
  }

  // header field
  if (typeof b === 'string' || typeof b === 'number' || b instanceof RegExp) {
    this._asserts.push(this._assertHeader.bind(this, { name: '' + a, value: b }));
    return this;
  }

  // body
  this._asserts.push(this._assertBody.bind(this, a));

  return this;
}
```
- example usage
```shell
...

app.get('/user', function(req, res) {
  res.status(200).json({ name: 'tobi' });
});

request(app)
  .get('/user')
  .expect('Content-Type', /json/)
  .expect('Content-Length', '15')
  .expect(200)
  .end(function(err, res) {
    if (err) throw err;
  });
'''
...
```

#### <a name="apidoc.element.supertest.Test.prototype.serverAddress"></a>[function <span class="apidocSignatureSpan">supertest.Test.prototype.</span>serverAddress (app, path)](#apidoc.element.supertest.Test.prototype.serverAddress)
- description and source-code
```javascript
serverAddress = function (app, path) {
  var addr = app.address();
  var port;
  var protocol;

  if (!addr) this._server = app.listen(0);
  port = app.address().port;
  protocol = app instanceof https.Server ? 'https' : 'http';
  return protocol + '://127.0.0.1:' + port + path;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.supertest.agent"></a>[module supertest.agent](#apidoc.module.supertest.agent)

#### <a name="apidoc.element.supertest.agent.agent"></a>[function <span class="apidocSignatureSpan">supertest.</span>agent (app, options)](#apidoc.element.supertest.agent.agent)
- description and source-code
```javascript
function TestAgent(app, options) {
  if (!(this instanceof TestAgent)) return new TestAgent(app, options);
  if (typeof app === 'function') app = http.createServer(app);  // eslint-disable-line no-param-reassign
  if (options) {
    this._ca = options.ca;
    this._key = options.key;
    this._cert = options.cert;
  }
  Agent.call(this);
  this.app = app;
}
```
- example usage
```shell
...

'''js
const request = require('supertest');
const should = require('should');
const express = require('express');
const cookieParser = require('cookie-parser');

describe('request.agent(app)', function() {
const app = express();
app.use(cookieParser());

app.get('/', function(req, res) {
  res.cookie('cookie', 'hey');
  res.send();
});
...
```



# <a name="apidoc.module.supertest.agent.prototype"></a>[module supertest.agent.prototype](#apidoc.module.supertest.agent.prototype)

#### <a name="apidoc.element.supertest.agent.prototype.acl"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>acl (url, fn)](#apidoc.element.supertest.agent.prototype.acl)
- description and source-code
```javascript
acl = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.bind"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>bind (url, fn)](#apidoc.element.supertest.agent.prototype.bind)
- description and source-code
```javascript
bind = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.checkout"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>checkout (url, fn)](#apidoc.element.supertest.agent.prototype.checkout)
- description and source-code
```javascript
checkout = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.connect"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>connect (url, fn)](#apidoc.element.supertest.agent.prototype.connect)
- description and source-code
```javascript
connect = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.copy"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>copy (url, fn)](#apidoc.element.supertest.agent.prototype.copy)
- description and source-code
```javascript
copy = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.del"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>del (url, fn)](#apidoc.element.supertest.agent.prototype.del)
- description and source-code
```javascript
del = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.delete"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>delete (url, fn)](#apidoc.element.supertest.agent.prototype.delete)
- description and source-code
```javascript
delete = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.get"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>get (url, fn)](#apidoc.element.supertest.agent.prototype.get)
- description and source-code
```javascript
get = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
...

'''js
const request = require('supertest');
const express = require('express');

const app = express();

app.get('/user', function(req, res) {
res.status(200).json({ name: 'tobi' });
});

request(app)
.get('/user')
.expect('Content-Type', /json/)
.expect('Content-Length', '15')
...
```

#### <a name="apidoc.element.supertest.agent.prototype.head"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>head (url, fn)](#apidoc.element.supertest.agent.prototype.head)
- description and source-code
```javascript
head = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.link"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>link (url, fn)](#apidoc.element.supertest.agent.prototype.link)
- description and source-code
```javascript
link = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.lock"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>lock (url, fn)](#apidoc.element.supertest.agent.prototype.lock)
- description and source-code
```javascript
lock = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.m-search"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>m-search (url, fn)](#apidoc.element.supertest.agent.prototype.m-search)
- description and source-code
```javascript
m-search = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.merge"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>merge (url, fn)](#apidoc.element.supertest.agent.prototype.merge)
- description and source-code
```javascript
merge = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.mkactivity"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>mkactivity (url, fn)](#apidoc.element.supertest.agent.prototype.mkactivity)
- description and source-code
```javascript
mkactivity = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.mkcalendar"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>mkcalendar (url, fn)](#apidoc.element.supertest.agent.prototype.mkcalendar)
- description and source-code
```javascript
mkcalendar = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.mkcol"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>mkcol (url, fn)](#apidoc.element.supertest.agent.prototype.mkcol)
- description and source-code
```javascript
mkcol = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.move"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>move (url, fn)](#apidoc.element.supertest.agent.prototype.move)
- description and source-code
```javascript
move = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.notify"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>notify (url, fn)](#apidoc.element.supertest.agent.prototype.notify)
- description and source-code
```javascript
notify = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.options"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>options (url, fn)](#apidoc.element.supertest.agent.prototype.options)
- description and source-code
```javascript
options = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.patch"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>patch (url, fn)](#apidoc.element.supertest.agent.prototype.patch)
- description and source-code
```javascript
patch = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.post"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>post (url, fn)](#apidoc.element.supertest.agent.prototype.post)
- description and source-code
```javascript
post = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
...
});
'''

Anything you can do with superagent, you can do with supertest - for example multipart file uploads!

'''js
request(app)
.post('/')
.field('name', 'my awesome avatar')
.attach('avatar', 'test/fixtures/homeboy.jpg')
...
'''

Passing the app or url each time is not necessary, if you're testing
the same host you may simply re-assign the request variable with the
...
```

#### <a name="apidoc.element.supertest.agent.prototype.propfind"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>propfind (url, fn)](#apidoc.element.supertest.agent.prototype.propfind)
- description and source-code
```javascript
propfind = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.proppatch"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>proppatch (url, fn)](#apidoc.element.supertest.agent.prototype.proppatch)
- description and source-code
```javascript
proppatch = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.purge"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>purge (url, fn)](#apidoc.element.supertest.agent.prototype.purge)
- description and source-code
```javascript
purge = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.put"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>put (url, fn)](#apidoc.element.supertest.agent.prototype.put)
- description and source-code
```javascript
put = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.rebind"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>rebind (url, fn)](#apidoc.element.supertest.agent.prototype.rebind)
- description and source-code
```javascript
rebind = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.report"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>report (url, fn)](#apidoc.element.supertest.agent.prototype.report)
- description and source-code
```javascript
report = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.search"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>search (url, fn)](#apidoc.element.supertest.agent.prototype.search)
- description and source-code
```javascript
search = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.subscribe"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>subscribe (url, fn)](#apidoc.element.supertest.agent.prototype.subscribe)
- description and source-code
```javascript
subscribe = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.trace"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>trace (url, fn)](#apidoc.element.supertest.agent.prototype.trace)
- description and source-code
```javascript
trace = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.unbind"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>unbind (url, fn)](#apidoc.element.supertest.agent.prototype.unbind)
- description and source-code
```javascript
unbind = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.unlink"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>unlink (url, fn)](#apidoc.element.supertest.agent.prototype.unlink)
- description and source-code
```javascript
unlink = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.unlock"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>unlock (url, fn)](#apidoc.element.supertest.agent.prototype.unlock)
- description and source-code
```javascript
unlock = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.supertest.agent.prototype.unsubscribe"></a>[function <span class="apidocSignatureSpan">supertest.agent.prototype.</span>unsubscribe (url, fn)](#apidoc.element.supertest.agent.prototype.unsubscribe)
- description and source-code
```javascript
unsubscribe = function (url, fn) {   // eslint-disable-line no-unused-vars
  var req = new Test(this.app, method.toUpperCase(), url);
  req.ca(this._ca);
  req.cert(this._cert);
  req.key(this._key);

  req.on('response', this._saveCookies.bind(this));
  req.on('redirect', this._saveCookies.bind(this));
  req.on('redirect', this._attachCookies.bind(this, req));
  this._attachCookies(req);

  return req;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
