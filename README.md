# api documentation for  [ical (v0.5.0)](https://github.com/peterbraden/ical.js)  [![npm package](https://img.shields.io/npm/v/npmdoc-ical.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-ical) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-ical.svg)](https://travis-ci.org/npmdoc/node-npmdoc-ical)
#### A tolerant, minimal icalendar parser

[![NPM](https://nodei.co/npm/ical.png?downloads=true)](https://www.npmjs.com/package/ical)

[![apidoc](https://npmdoc.github.io/node-npmdoc-ical/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-ical_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-ical/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-ical/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-ical/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Peter Braden",
        "email": "peterbraden@peterbraden.co.uk",
        "url": "peterbraden.co.uk"
    },
    "bugs": {
        "url": "https://github.com/peterbraden/ical.js/issues"
    },
    "dependencies": {
        "request": "2.68.0",
        "rrule": "2.0.0"
    },
    "description": "A tolerant, minimal icalendar parser",
    "devDependencies": {
        "underscore": "1.3.0",
        "vows": "0.7.0"
    },
    "directories": {},
    "dist": {
        "shasum": "71a0e58aa0cc30019da25f29286e0c033601b06f",
        "tarball": "https://registry.npmjs.org/ical/-/ical-0.5.0.tgz"
    },
    "gitHead": "585ca8b73b34b90c7174de9efd8c57a42002f106",
    "homepage": "https://github.com/peterbraden/ical.js",
    "keywords": [
        "ical",
        "ics",
        "calendar"
    ],
    "main": "index.js",
    "maintainers": [
        {
            "name": "peterbraden",
            "email": "peterbraden@peterbraden.co.uk"
        }
    ],
    "name": "ical",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/peterbraden/ical.js.git"
    },
    "scripts": {
        "test": "./node_modules/vows/bin/vows ./test/test.js"
    },
    "version": "0.5.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module ical](#apidoc.module.ical)
1.  [function <span class="apidocSignatureSpan">ical.</span>fromURL (url, opts, cb)](#apidoc.element.ical.fromURL)
1.  [function <span class="apidocSignatureSpan">ical.</span>handleObject (name, val, params, ctx, stack, line)](#apidoc.element.ical.handleObject)
1.  [function <span class="apidocSignatureSpan">ical.</span>parseFile (filename)](#apidoc.element.ical.parseFile)
1.  [function <span class="apidocSignatureSpan">ical.</span>parseICS (str)](#apidoc.element.ical.parseICS)
1.  object <span class="apidocSignatureSpan">ical.</span>node_ical
1.  object <span class="apidocSignatureSpan">ical.</span>objectHandlers

#### [module ical.node_ical](#apidoc.module.ical.node_ical)
1.  [function <span class="apidocSignatureSpan">ical.node_ical.</span>fromURL (url, opts, cb)](#apidoc.element.ical.node_ical.fromURL)
1.  [function <span class="apidocSignatureSpan">ical.node_ical.</span>parseFile (filename)](#apidoc.element.ical.node_ical.parseFile)

#### [module ical.objectHandlers](#apidoc.module.ical.objectHandlers)
1.  [function <span class="apidocSignatureSpan">ical.objectHandlers.</span>BEGIN (component, params, curr, stack)](#apidoc.element.ical.objectHandlers.BEGIN)
1.  [function <span class="apidocSignatureSpan">ical.objectHandlers.</span>CATEGORIES (val, params, curr)](#apidoc.element.ical.objectHandlers.CATEGORIES)
1.  [function <span class="apidocSignatureSpan">ical.objectHandlers.</span>COMPLETED (val, params, curr)](#apidoc.element.ical.objectHandlers.COMPLETED)
1.  [function <span class="apidocSignatureSpan">ical.objectHandlers.</span>DESCRIPTION (val, params, curr)](#apidoc.element.ical.objectHandlers.DESCRIPTION)
1.  [function <span class="apidocSignatureSpan">ical.objectHandlers.</span>DTEND (val, params, curr)](#apidoc.element.ical.objectHandlers.DTEND)
1.  [function <span class="apidocSignatureSpan">ical.objectHandlers.</span>DTSTART (val, params, curr)](#apidoc.element.ical.objectHandlers.DTSTART)
1.  [function <span class="apidocSignatureSpan">ical.objectHandlers.</span>END (val, params, curr, stack)](#apidoc.element.ical.objectHandlers.END)
1.  [function <span class="apidocSignatureSpan">ical.objectHandlers.</span>FREEBUSY (val, params, curr)](#apidoc.element.ical.objectHandlers.FREEBUSY)
1.  [function <span class="apidocSignatureSpan">ical.objectHandlers.</span>GEO (val, params, curr)](#apidoc.element.ical.objectHandlers.GEO)
1.  [function <span class="apidocSignatureSpan">ical.objectHandlers.</span>LOCATION (val, params, curr)](#apidoc.element.ical.objectHandlers.LOCATION)
1.  [function <span class="apidocSignatureSpan">ical.objectHandlers.</span>PERCENT-COMPLETE (val, params, curr)](#apidoc.element.ical.objectHandlers.PERCENT-COMPLETE)
1.  [function <span class="apidocSignatureSpan">ical.objectHandlers.</span>RRULE (val, params, curr, stack, line)](#apidoc.element.ical.objectHandlers.RRULE)
1.  [function <span class="apidocSignatureSpan">ical.objectHandlers.</span>SUMMARY (val, params, curr)](#apidoc.element.ical.objectHandlers.SUMMARY)
1.  [function <span class="apidocSignatureSpan">ical.objectHandlers.</span>TRANSP (val, params, curr)](#apidoc.element.ical.objectHandlers.TRANSP)
1.  [function <span class="apidocSignatureSpan">ical.objectHandlers.</span>UID (val, params, curr)](#apidoc.element.ical.objectHandlers.UID)
1.  [function <span class="apidocSignatureSpan">ical.objectHandlers.</span>URL (val, params, curr)](#apidoc.element.ical.objectHandlers.URL)



# <a name="apidoc.module.ical"></a>[module ical](#apidoc.module.ical)

#### <a name="apidoc.element.ical.fromURL"></a>[function <span class="apidocSignatureSpan">ical.</span>fromURL (url, opts, cb)](#apidoc.element.ical.fromURL)
- description and source-code
```javascript
fromURL = function (url, opts, cb){
  if (!cb)
    return;
  request(url, opts, function(err, r, data){
    if (err)
      return cb(err, null);
    cb(undefined, ical.parseICS(data));
  })
}
```
- example usage
```shell
...

Parses a string with an ICS File

    var data = ical.parseFile(filename)

Reads in the specified iCal file, parses it and returns the parsed data

    ical.fromURL(url, options, function(err, data) {} )

Use the request library to fetch the specified URL ('''opts''' gets passed on to the '''request()''' call), and call the function
 with the result (either an error or the data).



## Example 1 - Print list of upcoming node conferences (see example.js)
'''javascript
...
```

#### <a name="apidoc.element.ical.handleObject"></a>[function <span class="apidocSignatureSpan">ical.</span>handleObject (name, val, params, ctx, stack, line)](#apidoc.element.ical.handleObject)
- description and source-code
```javascript
handleObject = function (name, val, params, ctx, stack, line){
  var self = this

  if(self.objectHandlers[name])
    return self.objectHandlers[name](val, params, ctx, stack, line)

  //handling custom properties
  if(name.match(/X\-[\w\-]+/) && stack.length > 0) {
      //trimming the leading and perform storeParam
      name = name.substring(2);
      return (storeParam(name))(val, params, ctx, stack, line);
  }

  return storeParam(name.toLowerCase())(val, params, ctx);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ical.parseFile"></a>[function <span class="apidocSignatureSpan">ical.</span>parseFile (filename)](#apidoc.element.ical.parseFile)
- description and source-code
```javascript
parseFile = function (filename){
  return ical.parseICS(fs.readFileSync(filename, 'utf8'))
}
```
- example usage
```shell
...

## API ##

    ical.parseICS(str)

Parses a string with an ICS File

    var data = ical.parseFile(filename)

Reads in the specified iCal file, parses it and returns the parsed data

    ical.fromURL(url, options, function(err, data) {} )

Use the request library to fetch the specified URL ('''opts''' gets passed on to the '''request()''' call), and call the function
 with the result (either an error or the data).
...
```

#### <a name="apidoc.element.ical.parseICS"></a>[function <span class="apidocSignatureSpan">ical.</span>parseICS (str)](#apidoc.element.ical.parseICS)
- description and source-code
```javascript
parseICS = function (str){
  var self = this
  var lines = str.split(/\r?\n/)
  var ctx = {}
  var stack = []

  for (var i = 0, ii = lines.length, l = lines[0]; i<ii; i++, l=lines[i]){
    //Unfold : RFC#3.1
    while (lines[i+1] && /[ \t]/.test(lines[i+1][0])) {
      l += lines[i+1].slice(1)
      i += 1
    }

    var kv = l.split(":")

    if (kv.length < 2){
      // Invalid line - must have k&v
      continue;
    }

    // Although the spec says that vals with colons should be quote wrapped
    // in practise nobody does, so we assume further colons are part of the
    // val
    var value = kv.slice(1).join(":")
      , kp = kv[0].split(";")
      , name = kp[0]
      , params = kp.slice(1)

    ctx = self.handleObject(name, value, params, ctx, stack, l) || {}
  }

   // type and params are added to the list of items, get rid of them.
   delete ctx.type
   delete ctx.params

   return ctx
}
```
- example usage
```shell
...

    npm install ical



## API ##

    ical.parseICS(str)

Parses a string with an ICS File

    var data = ical.parseFile(filename)

Reads in the specified iCal file, parses it and returns the parsed data
...
```



# <a name="apidoc.module.ical.node_ical"></a>[module ical.node_ical](#apidoc.module.ical.node_ical)

#### <a name="apidoc.element.ical.node_ical.fromURL"></a>[function <span class="apidocSignatureSpan">ical.node_ical.</span>fromURL (url, opts, cb)](#apidoc.element.ical.node_ical.fromURL)
- description and source-code
```javascript
fromURL = function (url, opts, cb){
  if (!cb)
    return;
  request(url, opts, function(err, r, data){
    if (err)
      return cb(err, null);
    cb(undefined, ical.parseICS(data));
  })
}
```
- example usage
```shell
...

Parses a string with an ICS File

    var data = ical.parseFile(filename)

Reads in the specified iCal file, parses it and returns the parsed data

    ical.fromURL(url, options, function(err, data) {} )

Use the request library to fetch the specified URL ('''opts''' gets passed on to the '''request()''' call), and call the function
 with the result (either an error or the data).



## Example 1 - Print list of upcoming node conferences (see example.js)
'''javascript
...
```

#### <a name="apidoc.element.ical.node_ical.parseFile"></a>[function <span class="apidocSignatureSpan">ical.node_ical.</span>parseFile (filename)](#apidoc.element.ical.node_ical.parseFile)
- description and source-code
```javascript
parseFile = function (filename){
  return ical.parseICS(fs.readFileSync(filename, 'utf8'))
}
```
- example usage
```shell
...

## API ##

    ical.parseICS(str)

Parses a string with an ICS File

    var data = ical.parseFile(filename)

Reads in the specified iCal file, parses it and returns the parsed data

    ical.fromURL(url, options, function(err, data) {} )

Use the request library to fetch the specified URL ('''opts''' gets passed on to the '''request()''' call), and call the function
 with the result (either an error or the data).
...
```



# <a name="apidoc.module.ical.objectHandlers"></a>[module ical.objectHandlers](#apidoc.module.ical.objectHandlers)

#### <a name="apidoc.element.ical.objectHandlers.BEGIN"></a>[function <span class="apidocSignatureSpan">ical.objectHandlers.</span>BEGIN (component, params, curr, stack)](#apidoc.element.ical.objectHandlers.BEGIN)
- description and source-code
```javascript
BEGIN = function (component, params, curr, stack){
  stack.push(curr)

  return {type:component, params:params}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ical.objectHandlers.CATEGORIES"></a>[function <span class="apidocSignatureSpan">ical.objectHandlers.</span>CATEGORIES (val, params, curr)](#apidoc.element.ical.objectHandlers.CATEGORIES)
- description and source-code
```javascript
CATEGORIES = function (val, params, curr) {
  storeParam(val, params, curr)
  curr[name] = val ? val.split(separatorPattern) : []
  return curr
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ical.objectHandlers.COMPLETED"></a>[function <span class="apidocSignatureSpan">ical.objectHandlers.</span>COMPLETED (val, params, curr)](#apidoc.element.ical.objectHandlers.COMPLETED)
- description and source-code
```javascript
COMPLETED = function (val, params, curr){

  // Store as string - worst case scenario
  storeParam(name)(val, undefined, curr)

  if (params && params[0] === "VALUE=DATE") {
    // Just Date

    var comps = /^(\d{4})(\d{2})(\d{2})$/.exec(val);
    if (comps !== null) {
      // No TZ info - assume same timezone as this computer
      curr[name] = new Date(
        comps[1],
        parseInt(comps[2], 10)-1,
        comps[3]
      );

      return addTZ(curr, name, params);
    }
  }


  //typical RFC date-time format
  var comps = /^(\d{4})(\d{2})(\d{2})T(\d{2})(\d{2})(\d{2})(Z)?$/.exec(val);
  if (comps !== null) {
    if (comps[7] == 'Z'){ // GMT
      curr[name] = new Date(Date.UTC(
        parseInt(comps[1], 10),
        parseInt(comps[2], 10)-1,
        parseInt(comps[3], 10),
        parseInt(comps[4], 10),
        parseInt(comps[5], 10),
        parseInt(comps[6], 10 )
      ));
      // TODO add tz
    } else {
      curr[name] = new Date(
        parseInt(comps[1], 10),
        parseInt(comps[2], 10)-1,
        parseInt(comps[3], 10),
        parseInt(comps[4], 10),
        parseInt(comps[5], 10),
        parseInt(comps[6], 10)
      );
    }
  }

  return addTZ(curr, name, params)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ical.objectHandlers.DESCRIPTION"></a>[function <span class="apidocSignatureSpan">ical.objectHandlers.</span>DESCRIPTION (val, params, curr)](#apidoc.element.ical.objectHandlers.DESCRIPTION)
- description and source-code
```javascript
DESCRIPTION = function (val, params, curr){
  var data;
  if (params && params.length && !(params.length==1 && params[0]==='CHARSET=utf-8')){
    data = {params:parseParams(params), val:text(val)}
  }
  else
    data = text(val)

  var current = curr[name];
  if (Array.isArray(current)){
    current.push(data);
    return curr;
  }

  if (current != null){
    curr[name] = [current, data];
    return curr;
  }

  curr[name] = data;
  return curr
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ical.objectHandlers.DTEND"></a>[function <span class="apidocSignatureSpan">ical.objectHandlers.</span>DTEND (val, params, curr)](#apidoc.element.ical.objectHandlers.DTEND)
- description and source-code
```javascript
DTEND = function (val, params, curr){

  // Store as string - worst case scenario
  storeParam(name)(val, undefined, curr)

  if (params && params[0] === "VALUE=DATE") {
    // Just Date

    var comps = /^(\d{4})(\d{2})(\d{2})$/.exec(val);
    if (comps !== null) {
      // No TZ info - assume same timezone as this computer
      curr[name] = new Date(
        comps[1],
        parseInt(comps[2], 10)-1,
        comps[3]
      );

      return addTZ(curr, name, params);
    }
  }


  //typical RFC date-time format
  var comps = /^(\d{4})(\d{2})(\d{2})T(\d{2})(\d{2})(\d{2})(Z)?$/.exec(val);
  if (comps !== null) {
    if (comps[7] == 'Z'){ // GMT
      curr[name] = new Date(Date.UTC(
        parseInt(comps[1], 10),
        parseInt(comps[2], 10)-1,
        parseInt(comps[3], 10),
        parseInt(comps[4], 10),
        parseInt(comps[5], 10),
        parseInt(comps[6], 10 )
      ));
      // TODO add tz
    } else {
      curr[name] = new Date(
        parseInt(comps[1], 10),
        parseInt(comps[2], 10)-1,
        parseInt(comps[3], 10),
        parseInt(comps[4], 10),
        parseInt(comps[5], 10),
        parseInt(comps[6], 10)
      );
    }
  }

  return addTZ(curr, name, params)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ical.objectHandlers.DTSTART"></a>[function <span class="apidocSignatureSpan">ical.objectHandlers.</span>DTSTART (val, params, curr)](#apidoc.element.ical.objectHandlers.DTSTART)
- description and source-code
```javascript
DTSTART = function (val, params, curr){

  // Store as string - worst case scenario
  storeParam(name)(val, undefined, curr)

  if (params && params[0] === "VALUE=DATE") {
    // Just Date

    var comps = /^(\d{4})(\d{2})(\d{2})$/.exec(val);
    if (comps !== null) {
      // No TZ info - assume same timezone as this computer
      curr[name] = new Date(
        comps[1],
        parseInt(comps[2], 10)-1,
        comps[3]
      );

      return addTZ(curr, name, params);
    }
  }


  //typical RFC date-time format
  var comps = /^(\d{4})(\d{2})(\d{2})T(\d{2})(\d{2})(\d{2})(Z)?$/.exec(val);
  if (comps !== null) {
    if (comps[7] == 'Z'){ // GMT
      curr[name] = new Date(Date.UTC(
        parseInt(comps[1], 10),
        parseInt(comps[2], 10)-1,
        parseInt(comps[3], 10),
        parseInt(comps[4], 10),
        parseInt(comps[5], 10),
        parseInt(comps[6], 10 )
      ));
      // TODO add tz
    } else {
      curr[name] = new Date(
        parseInt(comps[1], 10),
        parseInt(comps[2], 10)-1,
        parseInt(comps[3], 10),
        parseInt(comps[4], 10),
        parseInt(comps[5], 10),
        parseInt(comps[6], 10)
      );
    }
  }

  return addTZ(curr, name, params)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ical.objectHandlers.END"></a>[function <span class="apidocSignatureSpan">ical.objectHandlers.</span>END (val, params, curr, stack)](#apidoc.element.ical.objectHandlers.END)
- description and source-code
```javascript
END = function (val, params, curr, stack){
  if (curr.rrule) {
    var rule = curr.rrule.replace('RRULE:', '');
    if (rule.indexOf('DTSTART') === -1) {
      rule += ';DTSTART=' + curr.start.toISOString().replace(/[-:]/g, '');
      rule = rule.replace(/\.[0-9]{3}/, '');
    }
    curr.rrule = rrule.fromString(rule);
  }
  return originalEnd.call(this, val, params, curr, stack);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ical.objectHandlers.FREEBUSY"></a>[function <span class="apidocSignatureSpan">ical.objectHandlers.</span>FREEBUSY (val, params, curr)](#apidoc.element.ical.objectHandlers.FREEBUSY)
- description and source-code
```javascript
FREEBUSY = function (val, params, curr){
  var fb = addFBType({}, params);
  curr[name] = curr[name] || []
  curr[name].push(fb);

  storeParam(val, params, fb);

  var parts = val.split('/');

  ['start', 'end'].forEach(function (name, index) {
    dateParam(name)(parts[index], params, fb);
  });

  return curr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ical.objectHandlers.GEO"></a>[function <span class="apidocSignatureSpan">ical.objectHandlers.</span>GEO (val, params, curr)](#apidoc.element.ical.objectHandlers.GEO)
- description and source-code
```javascript
GEO = function (val, params, curr){
  storeParam(val, params, curr)
  var parts = val.split(';');
  curr[name] = {lat:Number(parts[0]), lon:Number(parts[1])};
  return curr
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ical.objectHandlers.LOCATION"></a>[function <span class="apidocSignatureSpan">ical.objectHandlers.</span>LOCATION (val, params, curr)](#apidoc.element.ical.objectHandlers.LOCATION)
- description and source-code
```javascript
LOCATION = function (val, params, curr){
  var data;
  if (params && params.length && !(params.length==1 && params[0]==='CHARSET=utf-8')){
    data = {params:parseParams(params), val:text(val)}
  }
  else
    data = text(val)

  var current = curr[name];
  if (Array.isArray(current)){
    current.push(data);
    return curr;
  }

  if (current != null){
    curr[name] = [current, data];
    return curr;
  }

  curr[name] = data;
  return curr
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ical.objectHandlers.PERCENT-COMPLETE"></a>[function <span class="apidocSignatureSpan">ical.objectHandlers.</span>PERCENT-COMPLETE (val, params, curr)](#apidoc.element.ical.objectHandlers.PERCENT-COMPLETE)
- description and source-code
```javascript
PERCENT-COMPLETE = function (val, params, curr){
  var data;
  if (params && params.length && !(params.length==1 && params[0]==='CHARSET=utf-8')){
    data = {params:parseParams(params), val:text(val)}
  }
  else
    data = text(val)

  var current = curr[name];
  if (Array.isArray(current)){
    current.push(data);
    return curr;
  }

  if (current != null){
    curr[name] = [current, data];
    return curr;
  }

  curr[name] = data;
  return curr
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ical.objectHandlers.RRULE"></a>[function <span class="apidocSignatureSpan">ical.objectHandlers.</span>RRULE (val, params, curr, stack, line)](#apidoc.element.ical.objectHandlers.RRULE)
- description and source-code
```javascript
RRULE = function (val, params, curr, stack, line){
  curr.rrule = line;
  return curr
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ical.objectHandlers.SUMMARY"></a>[function <span class="apidocSignatureSpan">ical.objectHandlers.</span>SUMMARY (val, params, curr)](#apidoc.element.ical.objectHandlers.SUMMARY)
- description and source-code
```javascript
SUMMARY = function (val, params, curr){
  var data;
  if (params && params.length && !(params.length==1 && params[0]==='CHARSET=utf-8')){
    data = {params:parseParams(params), val:text(val)}
  }
  else
    data = text(val)

  var current = curr[name];
  if (Array.isArray(current)){
    current.push(data);
    return curr;
  }

  if (current != null){
    curr[name] = [current, data];
    return curr;
  }

  curr[name] = data;
  return curr
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ical.objectHandlers.TRANSP"></a>[function <span class="apidocSignatureSpan">ical.objectHandlers.</span>TRANSP (val, params, curr)](#apidoc.element.ical.objectHandlers.TRANSP)
- description and source-code
```javascript
TRANSP = function (val, params, curr){
  var data;
  if (params && params.length && !(params.length==1 && params[0]==='CHARSET=utf-8')){
    data = {params:parseParams(params), val:text(val)}
  }
  else
    data = text(val)

  var current = curr[name];
  if (Array.isArray(current)){
    current.push(data);
    return curr;
  }

  if (current != null){
    curr[name] = [current, data];
    return curr;
  }

  curr[name] = data;
  return curr
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ical.objectHandlers.UID"></a>[function <span class="apidocSignatureSpan">ical.objectHandlers.</span>UID (val, params, curr)](#apidoc.element.ical.objectHandlers.UID)
- description and source-code
```javascript
UID = function (val, params, curr){
  var data;
  if (params && params.length && !(params.length==1 && params[0]==='CHARSET=utf-8')){
    data = {params:parseParams(params), val:text(val)}
  }
  else
    data = text(val)

  var current = curr[name];
  if (Array.isArray(current)){
    current.push(data);
    return curr;
  }

  if (current != null){
    curr[name] = [current, data];
    return curr;
  }

  curr[name] = data;
  return curr
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.ical.objectHandlers.URL"></a>[function <span class="apidocSignatureSpan">ical.objectHandlers.</span>URL (val, params, curr)](#apidoc.element.ical.objectHandlers.URL)
- description and source-code
```javascript
URL = function (val, params, curr){
  var data;
  if (params && params.length && !(params.length==1 && params[0]==='CHARSET=utf-8')){
    data = {params:parseParams(params), val:text(val)}
  }
  else
    data = text(val)

  var current = curr[name];
  if (Array.isArray(current)){
    current.push(data);
    return curr;
  }

  if (current != null){
    curr[name] = [current, data];
    return curr;
  }

  curr[name] = data;
  return curr
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
