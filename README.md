### pumpify
---
https://github.com/mafintosh/pumpify

```
npm install pumpify
```

```js
var pumpify = require('pumpify')
var tar = require('tar-fs')
var zlib = require('zlib')
bar fs = require('fs')
var untar = pumpify(zlib.createGunzip(), tar.extaract('output-folder'))
fs.createReadStream('some-gzipped-tarball.tgz').pipe(untar)

var untar = pumpify()
setTimeout(function(){
  untar.setPipeline(zlib.createGunzip(), tar.extract('output-folder'))
}, 1000)
fs.createReadStream('some-gzipped-tarball.tgz').pipe(untar)

```

```
```


