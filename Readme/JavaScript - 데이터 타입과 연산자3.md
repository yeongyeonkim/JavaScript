# [참조 타입의 특성]

<h2>객체 비교</h2>
동등 연산자(==)는 객체의 프로퍼티값이 아닌<br>
<b>참조 값</b>을 비교한다.

```
var a = 1;
var b = 1;

var objA = { value: 1 };
var objB = { value: 1 };
var objC = objB;

console.log(a == b); // true
console.log(objA == objB); // false
console.log(objB == objC); // true
```

***

# [프로토타입]
> 자바스크립트의 모든 객체는 자신의 부모 역할을 하는 객체와 연결되어 있다.<br>
객체지향의 상속 개념과 같이 부모 객체의 프로퍼티를 마치 자신의 것 처럼 쓸 수 있는데<br>
이런 부모 객체를 <b>프로토타입</b>이라고 부른다.

```
var my = { name : 'my', age : 26 };
console.log(my.toString()); // 오류가 일어나지 않는다.
```

toString(), valueOf()등과 같은 모든 객체에서 호출 가능한<br>
자바스크립트 기본 내장 메서드가 포함되어 있다.

***

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
