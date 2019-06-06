## Node.JS 웹서버 돌리기

Node.JS는 별도로 웹서버를 돌릴 수 있는 기능을 제공한다. 

우선 아래의 내용을 별도의 파일로 저장한다.

```js
var http = require('http');
var fs = require('fs');
var app = http.createServer(function(request,response){
    var url = request.url;
    if(request.url == '/'){
      url = '/index.html';
    }
    if(request.url == '/favicon.ico'){
      return response.writeHead(404);
    }
    response.writeHead(200);
    response.end(fs.readFileSync(__dirname + url));
 
});
app.listen(3000);
```

이후 해당 파일이 존재하는 디렉토리로 이동 후 아래의 명령을 입력한다.

```shell
$ node main.js # 해당 파일의 이름을 node로 실행한다.
```

