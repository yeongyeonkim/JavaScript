# [정규표현식]
: 문자열에서 특정한 문자를 찾아내는 도구.

<h2>컴파일</h2>
컴파일은 검출하고자 하는 패턴을 만드는 일.
우선 정규표현식 <b>객체</b>를 만들어야한다.


```
var pattern = /a/ 정규표현식 리터럴
var pattern = new RegExp('a') 정규표현식 객체 생성자
```

<b>정규표현식 리터럴</b> :
     /와 /사이에 a가 바로 우리가 찾고자 하는 대상임을 컴퓨터에게 알려준다.<p></p>
     
<b>정규표현식 객체 생성자</b> :
     RegularExpression의 약자로, 괄호안에 찾고자 하는 패턴이 a임을 알려준다.<p></p><br>
     

> <h2>정규표현식 메소드 실행</h2>
     정규표현식을 컴파일해서 객체를 만들었다면 이제 문자열에서 원하는 문자를 찾아내야 한다.
<h3>RegExp.exec()</h3>

```
var pattern = /a/;
console.log(pattern.exec('abcdef')); // ["a"]
```

- 문자열 a를 값으로 하는 <b>배열</b>을 리턴한다.

```
var pattern = /a./;
pattern.exec('abcde'); //["ab"]
```
- 정규표현식을 실행시킬때 '.'이라는 것은 어떤 문자이건 간에 하나의 문자이면 되고 앞이 a인 것을 나타낸다.<br>
따라서 ["ab"]를 출력하게 된다.

```
var pattern = /a/;
console.log(pattern.exec('bcdefg')); // null
```
- 찾고자하는 대상안에 a라는 문자가 없기 때문에 null 리턴
<h3>RegExp.test()</h3>

```
var pattern = /a/;
console.log(pattern.test('abcdef')); // true
console.log(pattern.test('bcdefg')); // false
```

- test는 인자 안에 패턴에 해당되는 문자열이 있으면 true, 없으면 false를 리턴한다.
<p></p><br>

> <h2>문자열 메소드 실행</h2>

<h3>String.match()</h3>
RegExp.exec()와 비슷하다.

```
var pattern = /a/;
var str = 'abcdef';
str.match(pattern); // ["a"]
var str = 'bcdefg':
str.match(pattern); // null
```

<h3>String.replace()</h3>

```
var pattern = /a/;
var str = 'abcdef';
str.replace(pattern, 'A'); // "Abcdef"
```

문자열에서 패턴을 검색해서 이를 변경한 후에 변경된 값을 리턴한다.

<h2>정규표현식 옵션</h2>
옵션에 따라서 검출되는 데이터가 달라진다.
<h3>i</h3>

```
var xi = /a/;
"Abcde".match(xi); // null
var oi = /a/i;
"Abcde".match(oi); // "A"
```

검사를 원하는 패턴의 요소 뒤에 i를 붙이면. <br>대소문자를 구분하지 않고 검출한다.

<h3>g</h3>

```
var xg = /a/;
"abcdea".match(xg); // ["a"]
var og = /a/g;
"abcdea".match(og); // ["a", "a"]
```

패턴에 해당하는 문자열의 모든 요소를 리턴한다.

```
var ig = /a/ig;
"AabcdAa".match(ig); // ["A", "a", "A", "a"]
```

i,g를 같이 사용할 수 있다.

<h2>참고</h2>
- <a href="https://regexr.com/">정규표현식 </a>
- <a href="https://regexper.com/">정규표현식을 시각화</a>

<h2>캡처</h2>

```

```
