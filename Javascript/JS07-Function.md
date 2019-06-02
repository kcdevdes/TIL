##함수

함수(function)이란 하나의 로직을 재실행 할 수 있도록 하는 묶음으로 코드의 재사용성을 높혀주는 역할을 하게 된다.

## 함수의 형식

```js
function function_name([args....[,args]]) {
  code
  
  return return_value
}
```



## 함수의 정의와 호출

function뒤에 함수의 이름이 오고, 소괄호가 따라온다. 소괄호에는 인자라는 값이 차례로 들어는데, 이 값은 함수를 호출할 때 함수의 로직으로 전달될 변수다. 인자는 생략이 가능하다. 함수를 호출했을 때 실행하게 될 부분이 중괄호 안쪽이다.

```js
// 내용을 0부터 9까지 출력하는 함수이다.
function numbering() {
  i = 0;
  while (i < 10) {
    document.write('number : ' + i);
    i += 1;
  }
}

numbering(); // 호출
```



## 입력과 출력

함수는 입력과 출력이 이루어 지는데 첫번째로 return이다.

### return

```js
function get_member() {
  return 'string';
}

get_number();

//결과는 string
```

### 인자

```js
function get_argument(arg) {
  return arg*10;
}

get_argument(10);
//결과는 100
```

return은 함수 내부에서 처리된 최종값을 호출한 곳으로 보내주고, 동시에 함수의 실행을 중지하는 역할을 지니고 있다.

인자는 함수가 실행될 떄 처음 함수에 입력값을 주어 함수의 결과를 매번 바꿀수 있게 된다. 이 인자는 복수의 형태로도 가능하다.

## 함수의 형태

자바스크립트는 함수를 정의하는 또 다른 방법을 제공하여 준다. 아래의 방법은 변수의 값을 초기화하기 위해 함수를 선언한 모습니다.

```js
var numbering = function () {
  i = 0;
  while (i < 10) {
    i += 1;
  }
}

numbering();
```

내용은 위의 예제와 동일하다.