# javascript basic quiz

- What are the five primitive values in JavaScript? (There are six if you consider ES6).
    number, string , boolean , symbol(ES6), undifined, object
    
- How do you declare and assign variables in JavaScript?
    자바스크립트에서는 var 키워드를 사용하여 변수를 선언함.
	  자바스크립트에서는 선언되지 않은 변수를 사용하려고 하거나 접근하려고 하면 오류가 발생한다.
	  단, 선언되지 않은 변수를 초기화할 경우에는 자동으로 선언을 먼저 한 후 초기화를 진행한다.

- What’s the difference between const, let and var?
    let, const 키워드는 block-scoped, 즉 블록(중괄호) 내부에 let, const 키워드로 선언된 변수는 외부 스코프에 영향을 주지 않는다.
	  let, const는 ECMA6에서 도입된 키워드며, var로 인해 발생하는 혼란스럽고 불 명확한 코드작성을 피하기 위해 만들어 졌다.
	  따라서 let, const 사용을 선호해야 한다.

- How do you use the following conditionals?
  - if
    if (표현식) {
	    표현식의 결과가 참일 때 실행하고자 하는 실행문;
	  }
  
  - if else
    if (표현식1) {	
    	    표현식1의 결과가 참일 때 실행하고자 하는 실행문;
	  } else if (표현식2) {
            표현식2의 결과가 참일 때 실행하고자 하는 실행문;
	  } else {
    	    표현식1의 결과도 거짓이고, 표현식2의 결과도 거짓일 때 실행하고자 하는 실행문;
	  }
    
  - else
    if (표현식) {
   	    표현식의 결과가 참일 때 실행하고자 하는 실행문;	
	  } else {
        표현식의 결과가 거짓일 때 실행하고자 하는 실행문;
	  }
   
- How do you use a for loop?
    for (초기식; 표현식; 증감식) {
    	표현식의 결과가 참인 동안 반복적으로 실행하고자 하는 실행문;
	  }	

- What is an array?
    자바스크립트에서 배열(array)은 이름과 인덱스로 참조되는 정렬된 값의 집합으로 정의된다.
	  배열을 구성하는 각각의 값을 배열 요소(element)라고 하며, 배열에서의 위치를 가리키는 숫자를 인덱스(index)라고 한다.

  - How do you put values into arrays?
    arr[1] = 10;      // 배열의 두 번째 요소에 숫자 10을 대입함. 배열의 길이는 1에서 2로 늘어남.

  - How to you get values out of arrays?
    document.write 사용 ("배열 arr의 요소에는 [" + arr + "]가 있습니다."); // 배열의 요소를 모두 출력함.
    
  - How do you remove a value from an array?
    delete arr[2];    // 배열의 세 번째 요소를 삭제함. 하지만 배열의 길이는 변하지 않음.
  
  - How do you loop through every value of an array?
    for문을 사용하여 출력한다.
  
- What is an object?
    객체란 이름(name)과 값(value)으로 구성된 프로퍼티(property)의 정렬되지 않은 집합이다.
    
  - How do you put values into objects? 
	  객체를 생성한 뒤 프로퍼티에 값을 선언한다.
    
  - How do you get values out from objects? 
	  객체이름.프로퍼티이름 또는 객체이름["프로퍼티이름"]으로 값을 참조
    
  - How do you remove a property from an object?
    delete 객체이름.프로퍼티이름; 위와 같이 delete 키워드를 사용하여 삭제
  
  - How do you loop through every value of an object?
    반복문을 사용하여 객체의 모든 값을 열거할 수 있다.
  
  - What is a method on an object?
    객체의 프로퍼티 값으로 함수가 선언되면 메소드라고 한다. 
  
  - How do you define methods?   
	  객체에 대해 다루게 될때 객체가 가지고 있는 일종의 동작이다.
	  함수와의 차이점은 객체를 통하여 동작을 실행한다는 점이다. 
    
  - How do you call/invoke a method?
    	var myObj = { myFn: function () { return '메소드 패턴입니다.' 	
		    } 
	    }; console.log(myObj.myFn());
  	위와같이 객체의 프로퍼티 값으로 함수를 선언해서 호출한다.
  
- What is a function?
	  함수(function)란 하나의 특별한 목적의 작업을 수행하도록 설계된 독립적인 블록을 의미합니다.
  	이러한 함수는 필요할 때마다 호출하여 해당 작업을 반복해서 수행할 수 있습니다.
	
  - How do you define functions?
    1.함수의 이름
	  2. 괄호 안에 쉼표(,)로 구분되는 함수의 매개변수(parameter)
	  3. 중괄호({})로 둘러싸인 자바스크립트 실행문
      function 함수이름(매개변수1, 매개변수2,...) {
   	    함수가 호출되었을 때 실행하고자 하는 실행문;
	    }
      
  - How do you call/invoke/execute functions?
    정의된 함수는 프로그램 내에서 호출되어야 비로서 실행됩니다.
	  일반적인 함수의 호출은 함수의 정의문과 같은 형태로 호출할 수 있습니다.
	  ex)var sum = addNum(3, 5); 
    
  - How do you pass arguments into a function?  
    파라미터를 사용하여 함서의 정의에서 전달받은 인수를 함수 내부로 전달한다.
    
  - What does the return keyword do in a function?
	  함수안에서 명령문들을 실행하다가 return을 만나면 함수를 빠져 나가게 됩니다.
	  그리고 return이 가지고 있는값을 반환합니다.
    
---
## Reference
[ Learning Javascript from Scratch (The Baby Phase)](https://zellwk.com/)
