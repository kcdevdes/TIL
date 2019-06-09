## 파일을 읽는 것으로 본문을 제작하기

readFile 함수로 인해 우린 본문의 내용을 실시간으로 긁어올 수 있게 되었다.

이것을 이용해 data란 폴더를 제작하고, 그 안에 HTML, CSS, JavaScript에 대한 설명을 적은 파일들을 요청이 들어올때 마다 긁어올 수 있게 된다.

```js
var http = require('http');
var fs = require('fs');
var url = require('url');
 
var app = http.createServer(function(request,response){
    var _url = request.url;
    var queryData = url.parse(_url, true).query;
    var title = queryData.id;

    console.log(queryData.id);
	  // 아무런 id 값이 없으면 HTML을 default로 지정한다.
    if(_url == '/'){ 
      queryData.id = 'HTML'
    }
    if(_url == '/favicon.ico'){
      return response.writeHead(404);
    }
    response.writeHead(200);
    fs.readFile(`data/${queryData.id}`, 'utf8', function(err, description){
      var template = `
      <!doctype html>
      <html>
      <head>
        <title>WEB1 - ${title}</title>
        <meta charset="utf-8">
      </head>
      <body>
        <h1><a href="/">WEB</a></h1>
        <ul>
          <li><a href="/?id=HTML">HTML</a></li>
          <li><a href="/?id=CSS">CSS</a></li>
          <li><a href="/?id=JavaScript">JavaScript</a></li>
        </ul>
        <h2>${title}</h2>
        <p>${description}</p> 
      </body>
      </html>
      `;

      response.end(template);
    });

});
```

