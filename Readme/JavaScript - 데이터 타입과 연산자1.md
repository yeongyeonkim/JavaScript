# [자바스크립트 기본 타입]
> 자바스크립트는 <b>느슨한 타입 체크 언어</b>이다.<br>
변수를 선언할 때 타입을 미리 정하지 않고, var라는 한 가지 키워드로만 변수를 선언한다.


<ul>

```
var intNum = 10; // 숫자 타입
var singleChar = 'a'; // 문자열 타입
var boolVar = true; // 불린 타입
var emptyVar; // undefined 타입
var nullVar = null // null 타입
```



<li><h2>숫자</h2>
모든 숫자를 64비트 부동 소수점 형태로 저장한다. (c언어의 double 타입과 유사) <br>
실수로 처리하므로 소수 부분을 버린 정수 부분만을 구하고 싶다면, Math.floor() 메서드를 사용하면 된다.

```
var num = 5 / 2;
console.log(num); // 2.5
console.log(Math.floor(num)); // 2
```

</li>
<li><h2>문자열</h2>
자바스크립트에서는 c언어의 char 타입과 같이<br>
문자 하나만을 별도로 나타내는 데이터 타입은 존재하지 않는다.<br>
따라서 길이가 1인 문자열 singleChar 변수를 사용한다.

```
var str = 'test';
console.log(str[0], str[1], str[2], str[3]); // test

str[0] = 'T';
console.log(str); // test
```

위 코드와 결과에서 
자바스크립트에서는 한 번 생성된 문자열은 읽기만 가능하지 수정은 불가능하다.
</li>
<li><h2>null과 undefined</h2>
두 타입 모두 '값이 비어있음'을 나타낸다.<br>
<b>undefined는 타입이자, 값을 나타낸다.</b>는 것에 주의한다.<br>

```
var nullVar = null;

console.log(typeof nullVar === null); // false
console.log(nullVar === null); // true
```

null 타입 변수인 nullVar의 typeof 결과가 null이 아니라 object이기 때문에 false 출력.<br>
typeof 연산자가 아닌, 일치 연산자(===)를 사용해서 변수의 값을 직접 확인해야 한다.
</li>
</ul>
