
# [배열]
> 굳이 크기를 지정하지 않아도 되며, <br>
어느 위치에 어느 타입의 데이터를 저장하더라도 에러가 발생하지 않는다.

<h2>배열 리터럴</h2>
객체 리터럴이 중괄호를 사용했다면, 배열 리터럴은 대괄호를 사용한다.

```
var colorArr = ['red', 'green', 'blue'];
console.log(colorArr[0]); // red
console.log(colorArr[2]); // blue
```

<h2>length 프로퍼티</h2>

```
var arr = [ ];
arr[0] = 0; // 동적생성
arr[5] = 5;
arr[100] = 100;
console.log(arr.length); // 101
```

<h2>배열 표준 메서드</h2>
push()

```
var arr = ['zero', 'one'];

arr.push('two');
console.log(arr); // ['zero', 'one', 'two']

arr.length = 4;
arr.push('three');
console.log(arr); // ['zero', 'one', 'two', undefined, 'three']  //···★
```

<h2>배열 요소 삭제</h2>
배열도 객체이므로, delete 연산자를 사용할 수 있다.

```
var arr = ['a', 'b', 'c'];
delete arr[1];
console.log(arr); // ['a', undefined, 'c']
console.log(arr.length); // 3
```

요소의 값을 undefined로 설정할 뿐 원소 자체를 삭제하지는 않는다.<br>
때문에, <b>splice() 배열 메서드</b>를 사용한다.

<h3>※ splice(start, deleteCount, item...)</h3>
<ul>
  <li>start - 배열에서 시작 위치</li>
<li>deleteCount - start에서 지정한 시작 위치부터 삭제할 요소의 수</li>
  <li>item - 삭제할 위치에 추가할 </li>
  </ul>
  
```
var arr = ['a', 'b', 'c', 'd'];
arr.splice(2, 1); // 2번째 요소를 시작점으로 1개의 원소를 삭제.
console.log(arr); // ['a', 'b', 'd']
console.log(arr.length); // 3
```

<h2>Array() 생성자 함수</h2>

```
var a = new Array(3);
console.log(a); // [undefined, undefined, undefined]

var b = new Array(1, 2, 3);
console.log(b); // [1, 2, 3]
```

그렇다면, var c = new Array(1); 일땐 console.log(c)의 결과가 궁금해졌다.<br>
결과는 undefined 였다. 아무래도 괄호안의 인자 개수가 2개 이상인 경우에만 <br>
위 코드의 var b와 같은 결과를 얻어내는 것 같다.

