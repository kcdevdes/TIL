## 반복문

반복문은 일정한 작업을 여러차례(혹은 무한대로) 반복하기 위한 문장이다

## 반복문의 문법

반복문의 문법은 몇가지가 있다. 각 구문은 서로 대체가 가능한 타입이다.

## while문

형식은 다음과 같다

```js
while (조건) {
  반복 실행할 코드
}
```

다음은 예시다.

```js
while(true) {
  document.write('everything is made up of coding </br>');
// document.write()는 자바스크립트를 이용해9서 웹페이지에 텍스트를 출력한다.
// 위 문장은 무한 반복을 일으키므로 중간에 실행이 중지될 것이다.
}
```

while문을 조금 더 효과적으로 사용하자면 반복 조건이 있겠다.

```js
var i = 0;
while (i < 10) {
  i++; // i를 1씩 증가시킨다.
  document.write('everything is made up of coding </br>'); // 반복이 실행될 때마다 document.wirte를 실행시킨다.
}
```



## for문

while문 보다 조금 더 세세하게 조정이 가능하다. 형식은 다음과 같다.

```js
for (<초기화>; <반복조건>; <반복시 실행되는 코드>) {
  <실행할 코드
}
```

즉, 이러한 형식으로 사용이 가능하다.

```js
for (var i = 0; i < 10; i++) {
  // i란 변수를 선언하고 이 변수는 반복시 1씩 증가하게 된다. 최종적으로 10으로 i가 바뀌게 되면, 반복은 종료되낟.
  document.write('this is repetitive word</br>');
}
```



## 반복문의 세세한 조정

* **break문**

  * 반복문을 중간에서 중지시킬때 필요한 문장으로 반복문을 탈출하는 역할을 하게 된다.

    ```js
    for (var i = 0; i < 10; i++) {
      if (i === 5) {
        break; // i가 5에 도달하면 break를 실행한다.
      }
      document.write('coding everybody' + i + '<br/>');
    }
    ```

* **continue문**

  * 실행을 즉시 반복하게 하는 문장으로 아래 코드 내용을 일절 무시하고, 바로 다시 반복문으로 넘어가게 된다.

    ```js
    for (var i = 0; i < 10; i++) {
      if (i === 5) {
        continue;
      }
        document.write("i'm hungry.." + i + '<br/>');
    }
    ```

    ```
    i'm hungry..0
    i'm hungry..1
    i'm hungry..2
    i'm hungry..3
    i'm hungry..4
    // 5가 없다. 뛰어넘어져 바로 반복문으로 올라갔기 때문이다.
    i'm hungry..6
    i'm hungry..7
    i'm hungry..8
    i'm hungry..9
    ```



## for문 중첩

모든 반복문은 중첩 또한 가능하다. 

```js
for (var i = 0; i < 10; i++) {
  for (var j = 0; j < 10; j++) {
    document.write('var i is' + i + 'var j is' + j + '<br/>');
  }
}
```

