# [자바스크립트 참조 타입(객체 타입)]
> 자바스크립트에서 객체는 단순히 '이름 : 값' 형태의 프로퍼티들을 저장하는<br>
컨테이너로서, <b>해시</b>라는 자료구조와 상당히 유사하다.<br>


<ul><h1>객체 생성</h1>
* 객체를 생성하는 방법은 크게 세 가지가 있다.
<h2>1. 기본 제공 Object() 객체 생성자 함수를 이용하는 방법</h2>

```
var my = new Object(); // Object(0를 이용한 빈 객체 my 생성

my.name = 'yeongyeon';
my.age = 26;
my.gender = 'male';

console.log(typeof my); // object
console.log(my); // { name : 'yeongyeon', age : 26, gender: 'male' }
```

빈 객체를 생성한 후, 몇 가지 프로퍼티들을 추가한 것.

<h2>2. 객체 리터럴</h2>

```
var my = {
  name : 'yeongyeon',
  age : 26,
  gender : 'male'
};

console.log(typeof my); // object
console.log(my); // { name : 'yeongyeon', age : 26, gender : 'male' }
```

중괄호안에 프로퍼티를 적고 그 프로퍼티가 추가된 객체를 생성.<br>
프로퍼티값으로 함수가 오는 경우 그러한 프로퍼티를 메서드라고 부른다.

<h2><a href="">3. 생성자 함수</a></h2>

***

<h2>객체 프로퍼티</h2>

```
var my = { name : 'my', major : 'computer engineering' };

console.log(my.name); // my
console.log(my['name']); // my     
console.log(my[name]); // undefined                 -> 1

my.major = 'electronics enginerring';                        
console.log(my.major); // electronics engineering   -> 2

my.age = 26;
console.log(my.age); // 26                          -> 3

delete my.name;
console.log(my.name); // undefined                  -> 4
```

1. 대괄호 표기법에서는 접근하려는 프로퍼티를 문자열 형태로 만들어야 한다.<br>
2. 기존 프로퍼티 갱신.<br>
3. 프로퍼티 <b>동적 생성</b><br>.
4. 프로퍼티 삭제.

</ul>
