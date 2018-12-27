# [정규표현식]
: 문자열에서 특정한 문자를 찾아내는 도구.

<h2>컴파일</h2>
컴파일은 검출하고자 하는 패턴을 만드는 일.
우선 정규표현식 <b>객체</b>를 만들어야한다.


```
var pattern = /a/ 정규표현식 리터럴
var pattern = new RegExp('a') 정규표현식 객체 생성자
```

<ul>
  <li>정규표현식 리터럴</li>
     /와 /사이에 a가 바로 우리가 찾고자 하는 대상임을 컴퓨터에게 알려준다.<br>
  <p></p>
  <li>정규표현식 객체 생성자</li>
     RegularExpression의 약자로, 괄호안에 찾고자 하는 패턴이 a임을 알려준다.
</ul>

<h2>RegExp.exec()</h2>

```
console.log(pattern.exec('abcdef')); // ["a"]
```

문자열 a를 값으로 하는 <b>배열</b>을 리턴한다.

```
console.log(pattern.exec('bcdefg')); // null
```

<h2>RegExp.test()</h2>
  

  
