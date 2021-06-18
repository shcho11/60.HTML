# HTML 객체구조
- 객체들은 계층 구조로 이루어져 있다
- 최상위 객체는 Window객체, 그 아래에는 frames, document, history, location 객체가 있으며 각각의 객체들은 아래로 또 다른 객체들로 파생
Window 객체
- 자바 스크립트 브라우저 내장객체 중 최상위 객체. 전체 윈도우에 적용될 내용들을 가지고 있음.
- 윈도마다 하나씩 존재하는 객체이다. (윈도 창을 나타낼 때)
Document 객체
- 현재의 문서에 대한 내용을 가지고 있음.
- 제목, 배경색, 폼에 대한 속성을 가지고 있다.
- html 페이지마다 하나씩 존재하는 객체. (웹 페이지를 나타낼 때)

# 객체, 속성, 메서드
객체
- Javascript는 객체 지향적인 언어이다. 웹문서의 모든 요소들은 객체 개념으로 다루며 각각의 객체들은 속성과 메서드를 가짐.
- Javascript 에서 객체는 일반적으로 웹 브라우저와 관계되어 사용된다. 
  - 브라우저 객체 : 브라우저 윈도우, 웹 문서, 문서에 포함된 이미지, 폼 등과 같은 요소들이 하나의 '객체'가 된다.
  - 내장 객체 : 시간, 배열 등과 같이 JS 자체에 내장된 객체도 있음.
  - 사용자가 정의한 객체도 사용할 수 있음.
- 객체 지향적인 언어 : 실세계의 사물(객체)을 모델링하여 프로그래밍에 적용한 것.
- 객체들은 속성과 메서드를 가짐.


속성
- 객체의 특징, 성질 
- Javascript에서 각각의 객체들은 속성을 가짐.
- 하위 객체는 상위 객체의 속성이 됨
  - image는 하나의 객체이지만, document 객체의 속성이 됨.
  - document 객체는 배경색, 문서제목 등과 같은 속성을 가짐.
  - image 객체는 너비, 높이 등의 속성을 가짐.
  - 객체의 속성을 바꾸기 위해서는 도트(.)를 사용하여 구분함.

   객체.속성값 = "속성값"
   ex) document.bgColor = "green";
   

메서드
- 객체의 동작, 하는 일, 기능
- 메서드는 ()를 사용

   객체.메서드(값)
   ex) window.open()
   document.write()
   
- Javascript의 객체들은(브라우저 객체, 내장객체)은 이미 이러한 속성과 메서드가 정의되어 있음.

# 객체모형
Javascript 객체모형
- 자바스크립트에는 수많은 객체가 이미 정의되어 있음. 
   웹 브라우저와 관련있는 브라우저 객체 : window, document, frame, history, location, form, image, link, radio, text, navigator 등
   자바스크립트 자체애 내장된 내장객체 : Date, Math, String, Array 등
   
브라우저 객체모형
- 브라우저 객체는 브라우저 화면에 나타나는 모든 요소들을 포함하는 것으로, 계층적인 트리구조로 구성되어 있음.
- window 라는 최상위 객체에서 파생된 수많은 하위 객체를 포함
- 각각의 하위 객체들은 계층구조에 의해 정의되어 있으며, 접근할 수 있음.
- 브라우저 객체는 계층구조로 접근함

# 브라우저 객체에 접근하는 방법
<ol start="1">
<li>객체 이름으로 객체에 접근</li>
  객체 고유의 이름(태그의 name 속성에 지정된 값을) 사용
  window.document.form이름.입력상자이름
  ex) 
  <FORM NAME="frm1">
  아이디 : <INPUT TYPE="text" name="tel">
  var phone = window.document.frm1.tel.value;
  
<li>DOM Method 이용</li>
  document.getElementbyId()
  id값을 통해 해당 element 에 접근
  id에 대한 element를 가져온다(get)
  ex) 
  <FORM NAME = "frm1">
  아이디 : <INPUT TYPE="text" name="tel" id="tel">
  var phone = document.getElementbyId("tel").value;
</ol>
    
 DOM 이란?
    - 문서 객체 모델. 하나의 웹 문서를 객체화해서 문서의 구조에 접근할 수 있는 방법.

 참고 :
<a href="https://m.blog.naver.com/PostList.naver?blogId=bionic2030">참고 1. 만찐두빵의 프로그래밍 블로그</href><br>
<a href="https://aboooks.tistory.com/">참고 2. 지구별 안내서</href>
 

