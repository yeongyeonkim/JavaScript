# [기본 타입과 표준 메서드]

```
// 숫자 메서드 호출
var num = 0.5;
console.log(num.toExponential(1)); // '5.0e-1'

// 문자열 메서드 호출
console.log("test".charAt(2)); // 's'
```

객체처럼 호출할 수 있다.

***

# [연산자]

<h2>+ 연산자</h2>

```
var add1 = 1 + 2;
var add2 = 'my' + 'string';
var add3 = 1 + 'string';
console.log(add1); // 3
console.log(add2); // my string
console.log(add3); // 1string
```

<h2>동등연산자와 일치연산자</h2>

```
console.log(1 == '1'); // true
console.log(1 === '1'); // false
```

<h2>!! 연산자</h2>
피연산자를 불린값으로 변환하는 것.

```
console.log(!!0); // false
console.log(!!'string'); // true
console.log(!!''); // false
console.log(!!{}); // true
console.log(!!true); // true
console.log(!!null); // false
```

빈 객체라도 true로 변환되는 것을 주의해야 한다.
