## 배열

배열(array)란 연관된 데이터를 모아서 통으로 관리하기 위한 데이터 타입니다. 변수가 하나의 데이터를 저장하기 위한 것이라면 배열은 여러 개의 데이터를 하나의 변수에 저장하기 위한 것이라고 할 수 있다.

## 배열의 생성

기본적으로 배열은 [] (대괄호)를 사용하여 준다. 대괄호 안에 데이터를 콘마로 구분하여 나열하면 된다.

```js 
var member = ['this', 'is', 'sparta']
```

이를 꺼낼려면 아래와 같은 방식을 사용하면 된다.

```js
var member = ['this', 'is', 'sparta'];
alert(member[0]); // this
alert(member[1]); // is
alert(member[2]); // sparta
```

## 배열의 사용

배열은 반복문과 결합하였을 때 데이터를 한번에 모두 꺼낼수 있게 된다.

```js
function get_members() {
  return ['this', 'is', 'sparta'];
}

members = get_members();

//<array>.length는 해당 array의 길이를 반환합니다.
for (var i = 0; i < members.length; i++) {
  document.write(members[i]);
  document.write('<br />');
}
```



## 배열의 조작

### 추가

배열의 끝에 원소를 추가하는 방법이다. push 는 인자로 전달된 값을 배열에 추가하는 명령이다.

```js
var list = [1,2,3,4,5];
list.push(6);
alert(list); // 1,2,3,4,5,6
```

다음은 복수의 원소를 추가하는 방법이다. concat은 인자로 전달된 배열을 추가한다.

```js
var list = [1,2,3,4,5];
list = list.concat ([6,7,8]);
alert(list); // 1,2,3,4,5,6,7,8
```

다음은 배열의 시작점에 원소를 추가하는 방법이다. unshift로 진행한다.

```js
var list = [1,2,3,4,5,6];
list.unshift(7,8);
alert(list); // 7,8,1,2,3,4,5,6
```

다음은 원하는 곳에 원하는 값을 추가하는 방법이다. splice()함수이다. 첫번째 인자에서 2번째 인자에 해당하는 원소의 숫자만큼의 값을 배열로부터 제거 후, 세번째 인자부터 전달된 인자들을 첫번째 인자의 원소 뒤에 추가한다.

```js
var list = [1,2,3,4];
list.splice(2,0, 10);
alert(list); // 1,2,10,3,4
```

### 제거

shift는 첫 원소를 지우는 역할을 한다.

```js
var list = [1,2,3,4,5];
list.shift();
alert(list);// 2,3,4,5
```

pop은 끝에서 부터 원소를 제거한다.

```js
var list = [1,2,3,4,5];
list.pop();
alert(list); // 1,2,3,4
```

### 정렬

다음은 정렬하는 방법이다.

```js
var list = ['c', 'a', 'b', 'd'];
list.sort();
alert(list); // a,b,c,d
```

역순 정렬은 아래와 같다.

```js
var list = ['c', 'a', 'b', 'd'];
list.reverse();
alert(list); // d,c,b,a
```

