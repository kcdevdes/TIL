## 조건문

조건문이란 주어진 조건에 따라서 애플리케이션을 다르게 동작하도록 하는 것이다.

## if

조건문은 if로 시작한다. if뒤에 나오는 괄호에는 조건이 있고 조건이 될 수 있는 값은 Boolean이다. Boolean의 값이 true이면 조건이 담겨진 괄호 다음의 중괄호 구문이 실행된다.

```js
if (/*조건식*/) {/*실행문*/}
```

```js
if (true){
  alert('true');
}
```



## else

if만으론 안되는 좀 더 복잡한 상황을 처리하는데 사용된다.

```js
if (true){
  // true이면 이 곳
  alert(1);
} else {
  
  // 아니면 이곳이다.
  alert(2);
}
```



## else if

else를 넣어도 2가지 밖에 처리할 수 없지만 else if를 사용하면 좀 더 많은 조건을 추가할 수 있다.

```js
var num = 3;
if (num == 1) {
  alert (1);
} else if (num == 2) {
  alert (2);
} else if (num == 3) {
  alert (3);
} else {
  alert ("We don\'t know");
}
```



## 실제로 응용해보기

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset = "utf-8" />
  </head>
  <body>
    <script>
 			var id = prompt ('아이디를 입력하여 주세요');
      if (id == 'root') {
 				alert ("최고 관리자 입니다.");       
      } else {
        alert ('Guest입니다.');
      }
    </script>
  </body>
</html>
```



## 실제로 응용해보기 2

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset = "utf-8" />
  </head>
  <body>
    <script>
 			var id = prompt ('아이디를 입력하여 주세요');
      if (id == 'root') {
 				var password = prompt('비밀번호를 입력해주세요');
        if (password == 'root'){
          alert ('인증 되었습니다.');
        } else {
          alert ('인증되지 않았습니다.');
        }
      } else {
        alert ('Guest입니다.');
      }
    </script>
  </body>
</html>
```



## 논리 연산자

* && (AND)

  * 좌항과 우항이 모두 참일 때 참이 되는 연산자이다. 이러한 연산자를 AND 연산자라고 한다.

    ```js
    var id = prompt ('아이디를 입력하여 주세요');
    var password = prompt('비밀번호를 입력해주세요');
    
    if (id == 'root' && password == '1234') {
      alert ('해제되었습니다.');
    }
    ```

    

* || (OR)

  * 좌우항 중에서 하나라도 true이면 모두 true가 되는 형태이다.

  * 특이한 것은 (1번 조건) || (2번 조건) || (3번 조건) 을 하여도 문제는 없는 것이다.

    

* ! 연산자

  * 부정을 나타내며 Boolean의 값을 역전시킨다.



## 예외

* **0 and 1**

  * 0은 false의 값을 대변할 수 있고, 1은 true의 값을 대변할 수 있다.

* **기타 false로 간주되는 데이터 형**

  ```js
  if ('') // 빈 문자열
  if (undefined) // 선언되지 않음
  if (a) // 값이 할당되지 않은 변수
  if (null) // null
  if (NaN) // NaN
    
  // 모두 false이다.
  ```

  