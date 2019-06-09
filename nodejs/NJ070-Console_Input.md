## Node.js가 동작 중일 떄 console로 input하기

```js
var args = process.argv;
console.log(args[2]); // input.js 이후로 들어가는 인수이다.
console.log('A');
console.log('B');
if (args[2] === '1'){
    console.log('C1');
} else {
    console.log('C2');
}
console.log('D');
```

실용성은 없지만 콘솔로 값을 입력 받고 싶을 때에 유용한 방식이라 할 수 있겠다.