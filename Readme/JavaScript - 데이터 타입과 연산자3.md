# [참조 타입의 특성]

<ul>
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

