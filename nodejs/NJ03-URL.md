## URL 다루기

아래의 샘플 URL이 있다.

```
http://opentutorials.org:3000/main?id=THML&page=12
```

이를 URL이라 하고 각 부분의 역할은 다음과 같다.

```
http	
```

Protocol

프로토콜로 어떠한 방식으로 웹서버가 연결이 되었는 지를 명시적으로 알려준다.

```
opentutorials.org
```

Host(Domain)

도메인으로 웹서버의 위치를 가르킨다.

```
3000	
```

Port

해당 웹서버에 연결하기 위한 포트 번호이다. http는 기본 80번 포트를 사용하지만 만약 다른 포트를 사용한다면 해당 포트로 접속을 시도해야한다.

```
main		
```

Path	

세부 주소이다. 웹서버 디렉토리로 접속하여 세부적으로 페이지에 접근할 수 있게 된다.

```
id=HTML&page=12
```

Query String

검색 문자열로 어떠한 내용을 웹서버에게 검색하고 싶을 때 전송하는 문자열이다.

## URL Query String 다루기

```js
var http = require('http');
var fs = require('fs');
var url = require('url'); // require은 import와 비슷하다. url은 nodejs의 모듈 중 하나이다.
 
var app = http.createServer(function(request,response){
	
  	// 내부적으로 들어오는 URL은 아래 _url로 들어오게 된다.
  	var _url = request.url;
    var queryData = url.parse(_url, true).query;
  
  	// queryData는 사용자가 입력한 url을 구별하여 query string을 구별한다.
  	// 만약, ?id=192 라면 queryData.id로 해당 값을 뽑아낼 수 있다.
    console.log(queryData.id);
  
    if(_url == '/'){
      _url = '/index.html';
    }
    if(_url == '/favicon.ico'){
      return response.writeHead(404);
    }
    response.writeHead(200);
    response.end(queryData.id);
 
});
app.listen(3000);
```

