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
