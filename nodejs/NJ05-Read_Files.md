## Node.JS 파일 읽기

```js
var fs = require('fs');

// readFile(<dir>, <encoding option>, <callback>)
fs.readFile('sample.txt', 'utf8', function(err, data){
  console.log(data);
});
```

자세한 내용은 아래 내용을 참조하도록 한다.

[Node.js fs.readFile document](https://nodejs.org/dist/latest-v10.x/docs/api/fs.html#fs_fs_readfile_path_options_callback)