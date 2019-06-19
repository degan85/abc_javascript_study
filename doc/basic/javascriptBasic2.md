# javascript basic 2

* 아래 참조 사이트에 들어가서 크롬 개발자차을 열고(F12) 소스들을 직접 타이핑합니다.
* 결과를 직접 확인하고 여기에 해당 소스를 다시 작성하고 정리합니다.

변수와 타입
var a;
typeof a;				        // "undefined"

a = "hello world";
typeof a;				        // "string"

a = 42;
typeof a;				        // "number"

a = true;
typeof a;				        // "boolean"

a = null;
typeof a;				          // "object" 버그다.

a = undefined;
typeof a;				          // "undefined"

a = { b: "c" };
typeof a;	                 // "object"


var obj = {
	a: "hello world",
	b: 42,
	c: true
};

오브젝트
obj.a;		// "hello world"
obj.b;		// 42
obj.c;		// true

obj["a"];	// "hello world"
obj["b"];	// 42
obj["c"];	// true

var obj = {
	a: "hello world",
	b: 42
};

var b = "a";

obj[b];			// "hello world"
obj["b"];		// 42

배열
var arr = [
	"hello world",
	42,
	true
];

arr[0];			// "hello world"
arr[1];			// 42
arr[2];			// true
arr.length;		// 3

typeof arr;		// "object"

함수
function foo() {
	return 42;
}

foo.bar = "hello world";

typeof foo;			   // "function"
typeof foo();		    // "number"
typeof foo.bar;	    	// "string"

내장 함수
var a = "hello world";
var b = 3.14159;

a.length;				// 11 배열의 길이
a.toUpperCase();		// "HELLO WORLD" 대문자화
b.toFixed(4);			// "3.1416"  소수점 4째자리 반올림

비교 연산자
var a = "42";

var b = Number( a );

a;				// "42"
b;				// 42 -- 숫자

var a = "42";

var b = a * 1;	// "42" implicitly coerced to 42 here

a;				// "42"
b;				// 42 -- 숫자

var a = "42";
var b = 42;

a == b;			// true
a === b;		// false

var a = [1,2,3];
var b = [1,2,3];
var c = "1,2,3";

a == c;		// true
b == c;		// true
a == b;		// false

var a = 41;
var b = "42";
var c = "43";

a < b;		// true
b < c;		// true

var a = 42;
var b = "foo";

a < b;		// false
a > b;		// false
a == b;		// false


함수 스코프

var a = 2;

foo();					

function foo() {
	a = 3
	console.log( a );    
	var a;			   	
}

console.log( a );	// 2

내부함수는 외부함수에 접근 가능하나 외부함수는 불가능
function foo() {
	var a = 1;
	function bar() {
		var b = 2;
		function baz() {
			var c = 3;
			console.log( a, b, c );	// 1 2 3
		}
		baz();
		console.log( a, b );		// 1 2
	}
	bar();
	console.log( a );				// 1
}

foo();

function foo() {
	a = 1;	// 선언하지 않은변수
}

foo();
a;			// 자동 전역변수 초기화 (안좋은습관)


function foo() {
	var a = 1;
	if (a >= 1) {
		let b = 2;
		while (b < 5) {
			let c = b * 2;
			b++;
			console.log( a + c );
		}
	}
}

foo();
// 5 7 9

조건문
if & else if 문

if (a == 2) {
}
else if (a == 10) {
}
else if (a == 42) {
}
else {
}

switch문

switch (a) {
	case 2:
		// do something
		break;
	case 10:
		// do another thing
		break;
	case 42:
		// do yet another thing
		break;
	default:
		// fallback to here
}


switch (a) {
	case 2:
	case 10:
		break;
	case 42:
		break;
	default:
}

삼항연산자 
var a = 42;

var b = (a > 41) ? "hello" : "world";

보통if문의 단축으로 쓰임

// if (a > 41) {
//    b = "hello";
// }
// else {
//    b = "world";
// }

strict모드

함수내에 strict모드 선언
function foo() {
	"use strict";
  
	function bar() {

	}
}

전역에 strict모드 선언

"use strict";

function foo() {
	function bar() {
	}
}


function foo() {
	"use strict";	
	a = 1;			// `var` 가 없어서 에러
}

foo();


--------------------------------------------------------------중간저장 









---
## Reference
[You Don't Know JS: Up & Going](https://github.com/getify/You-Dont-Know-JS/blob/master/up%20%26%20going/ch2.md)
