### 자바스크립트에서의 숫자

* 자바스크립트는 큰따옴표, 작은따옴표가 붙지 않은 숫자는 숫자로 인식한다.

  ```javascript
  alert(1+1);
  2
  ```

  

* 만약 따옴표가 붙게 되면 문자로 인식하게 된다.

  ```js
  alert("1+1");
  1+1
  ```

  

### 자바스크립트의 연산

* 사칙연산

  * 더하기는 +

    ```javascript
    1+1 // 2
    ```

    

  * 빼기는 -

    ```javascript
    10-2 // 8
    ```

    

  * 곱하기는 *

    ```javascript
    2*5 // 10
    ```

    

  * 나누기는 /

    ```javascript
    10/2 // 5
    ```

    

  * 제곱은 **

    ```javascript
    2**10 // 1024
    ```

* 좀 더 복잡한 연산

  ```javascript
  Math.pow(3,2); // 3의 2승
  Math.round(10,6); // 10.6의 반올림
  Math.ceil(10.2); // 10.2의 올림
  Math.floor(10.6); // 10.6의 내림
  Math.sqrt(9); // 9의 제곱근
  Math.random(0) // 0 ~ 1.0의 랜덤한 숫자
  ```



### 문자

문자는 ""(큰 따옴표), ''(작은 따옴표)로 감싸주어야 한다. 이를 String이라 한다.

```js
alert("this is example");
alert('this is example');
// 두 명령의 결과는 동일하다.
```

또한 typeof 연산자를 사용하면 데이터 형을 알아낼 수 있다.

```js
alert(typeof '1');
// String형
alert(typeof 1);
// number
```

만약 ''내부에 ''를 사용하고 싶을 땐 아래의 방법을 사용한다.

```js
alert('this is my 'Macbook''); // Error
alert('this is my \'Macbook\'') // OK
```

문자의 덧셈과 길이는 아래의 방식으로 구한다.

```js
alert("Hello!" + "World!");
// Result : Hello!World!
alert("Hello World!".length);
// Result : 12
```

