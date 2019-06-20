# DOM

#### 아래 질문에 대해 검색하고 셈플 코드를 넣어보세요.(html, js)

- HTML과 DOM에 대해 정리하세요.
    1.HTML: HTML은 HyperText Markup Language의 약자다.
            웹 페이지는 HTML 문서라고도 불리며, HTML 태그들로 구성된다. 
            각각의 HTML 태그는 웹 페이지의 디자인이나 기능을 결정하는데 사용된다.
    
    2.DOM: DOM은 HTML 문서에 대한 인터페이스이다. 첫째로 뷰 포트에 무엇을 렌더링 할지 결정하기 위해 사용되며,
           둘째로는 페이지의 콘텐츠 및 구조, 그리고 스타일이 자바스크립트 프로그램에 의해 수정되기 위해 사용된다.
           
  - DOM을 브라우저가 생성하는 과정을 정리하세요.
          객체를 생성하여 트리구조로 연결시킨다. 이 트리 데이터 구조는 부모-자식 관계도 포함되며, 우리가 알고있는 HTML이 생성되는 것이다.
          이것을 DOM(Document Object Model) 이라 하며, 트리 구조로 되어 있어서 DOM 트리 라고도 한다.
    
- DOM selector에 대해 정리하세요.

  - jquery
 
    $(셀렉터 표현 문자열)
    
    ex)  <script> 
        $(document).ready(function() { 
            var sel = $('*'); 
            console.log(sel);
        });
     </script> 
     
  - vanilla js
  
    document.querySelector( 'selector' )
      
- DOM에 이벤트를 처리해보세요.
   
  


- react관련해서 virtual DOM을 정리해보세요.
