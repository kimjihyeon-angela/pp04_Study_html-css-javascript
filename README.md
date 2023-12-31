# pp04_Study_html-css-javaScript
HTML/CSS, JavaScript에 대한 부족한 지식을 채우기 위한 공부용

## Class 1 html, css, javascript에 대한 기초

### Day 01
- html
    - Hyper Text Markup Language
    - 네트워크가 연결된 웹페이지에서 문서를 작성하고, 읽고, 공유하기 위해 만들어진 체계로 구조를 담당 
        => 공간을 만들고 그 공간을 무엇으로 채울지 결정하는 것
    - tag의 집합 
        - 태그 - 고유한 기능을 가진 약속된 명령어 
        - <시작 태그> 내용 </종료 태그> => 요소
          
              ex) <h1> Welcome to My Place </h1>
        - 자주 사용되는 tag
     
              <strong> : 굵게
              <u> : 밑줄
              <i> : 기울게
        - 빈태그
            - 내용, 종료태그 없이 시작태그만 작성하면 됨
              
                  <br> : 줄바꿈 태그
                  <hr> : 수평선 태그
        - 특정 기능이 있는 태그
          
              <button> 버튼 </button>
              <textarea> 입력창 </textarea>
              <img src="image.png" />
              <video muted = "muted" loop = "loop">
                <source src = "video.mp4">
              </video>
    - HTML의 핵심
        - 태그의 특징 : Inline, Block
        - 종속태그
            - 다른 태그와 함께 상호작용해야만 제대로 작동하는 태그 = 혼자서 작동할 수 없는 태그
            - ex) 선택박스태그, 목록태그 표태그
            - 선택박스태그 

                  <select> 
                    <option>태그를 사용해야 함 
                  </select>
            - 목록태그

                  <ol>
                    <li> li태그를 ol태그로 감싸면</li>
                    <li> 번호가 생김 </li>
                    <li> 따로 넘버링 하지 않아도 자동으로 번호가 붙음 </li>
                  </ol>
                  
                  <ul>
                    <li> li태그를 ul로 감싸면 </li>
                    <li> 번호가 아닌 기호가 생김 </li>
                    <li> 목록태그 </li>
                        <ul>
                            <li> ol </li>
                            <li> ul </li>
                            <li> dl </li>
                        </ul>
                  </ul>
              
                <ol>
                    <li> li태그를 ol태그로 감싸면</li>
                    <li> 번호가 생김 </li>
                    <li> 따로 넘버링 하지 않아도 자동으로 번호가 붙음 </li>
                </ol> <br> <hr> <br>
                <ul>
                   <li> li태그를 ul로 감싸면 </li>
                   <li> 번호가 아닌 기호가 생김 </li>
                   <li> 목록태그 </li>
                       <ul>
                           <li> ol </li>
                           <li> ul </li>
                           <li> dl </li>
                       </ul>
                </ul>
 
                  
        - HTML 문서 구조
            - 문서마다 양식이 모두 다르면 해석하는게 복잡해짐 => 최소한의 문서 구조를 통해 체계화
            - 검색엔진을 위한 <head>영역 + 브라우저에서 보여지는 <body> 영역
            - <head>영역
                - title, meta 태그
                - title : 브라우저 상단
         
                <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/head_title.jpg" width="600"/>

                [head - title]
                                   
                - meta : 인터넷에 검색 했을 때 밑에 설명 부분
             
                <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/head_meta.jpg" width="600"/>

                [head - meta]
                  
            - <body>영역

- css : 시각
- JavaScript : 기능

### Day 02
- css
    - HTML의 색, 크기, 정렬 등을 변경하여 꾸며주는 언어
    - 기본문법
        - 단일 속성 지정
            - 선택자 {속성 : 값;}
        - 다중 속성 지정
            - 선택자{
                속성 : 값;
                속성 : 값;
                속성 : 값;
                속성 : 값;
               }
    - 사용방법
        - html 태그 속성에 입력
            - 태그에 CSS 속성이 바로 기록되어 있어 별다른 지정이나 연결 필요 x
            
                    <a style="background-color: #ffee55; color: #36e52k;">
        - style 태그에 입력
            - 태그와 CSS 속성이 html 내에서 분리되어 있어 어떤 태그에 CSS 속성을 적용할 지 연결해 줘야 함

                    <head>
                        <style>
                            .listup{
                                color: red;
                                border:1px solid gray;
                            }
                        </style>
                    </head>

                    <body>
                        <div class="starter"></div>
                        <div class="listup"></div>
                        <div class="closer"></div>
                    </body>
        - css 파일 만들어 불러오기 (실무에서 주로 사용하는 방법)
            - 태그와 CSS 속성이 파일로 분리되어 있어 어떤 태그에 CSS 속성을 적용할지 연결해 줘야 함

                    <head>
                        <link href="./index.css" rel="stylesheet">
                    </head>

                    <body>
                        <div class="starter"></div>
                        <div class="listup"></div>
                        <div class="closer"></div>
                    </body>

                    index.css(파일)
                    .listup{
                        color: red;
                        border:1px solid gray;
                    }
    - CSS 선택자
        - 전체 선택자 : *
        - 태그 선택자 : 태그 이름 ex) div
        - class 선택자(중복 가능) : . + class 이름 ex) .container
        - id 선택자(중복 불가) : # + ID ex) #userInfo

    - 박스모델
        - html 태그들은 모두 박스모델로 이루어짐
        - margin : 박스의 바깥 여백
        - border : 박스의 기준이 되는 바깥 테두리
        - padding : 박스의 안쪽 여백
        - contents : 박스의 내용

    - 박스모델 화면 표시 방법
        - border box
            - 크기 중심이 바깥 테두기(border)
            - 박스 크기는 디자이너가 준 화면 크기와 일치, 안에 들어가는 contents의 크기가 변함
        - content box
            - 크기 중심이 내용(contents)
            - contents 가 고정되고 border의 크기가 변함
        - 실무에서는 디자이너에게 받은 화면의 크기와 일치시켜야 하기 때문에 border-box 사용

    - 정렬    
        - flex
            - 핵심 : 여러태그를 하나로 묶어서 정렬
            - 정렬기준 : 부모박스
        - position
            - 박스를 개별적으로 어디에 위치시킬것인지 지정해줌
            - 옵션 : absolute(절대위치), relative(부모박스 기준으로 상대 위치), fixed(화면 기준으로 절대 위치), static(기본설정)
        - grid

### Day 03
- 회원가입 화면 만들어 보기 (08_signup)

    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/signup1.jpg" width="600"/>

    [회원가입 화면]
    
    - br을 활용한 회원가입화면이기 때문에 다시 도전해보기 

- 회원가입화면 만들어 보기 (09_signup.html + 09_signup.css)

- 싸이월드 화면 만들어보기

    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/cyworld1.jpg" width="600"/>

    [싸이월드 화면]

    - background 설정 방법
    - outerbox 설정
    - 화면을 만들때
        - 하나하나 div로 다 나눠서 class 지정해줘야함
        - br 사용보다 div로 나눠 css에서 디자인해주기

### Day 04
- html
    - tag : 약속된 명령어
    - 브라우저 화면의 뼈대
- css
    - html로 만들어진 뼈대를 꾸미는 부분
- javascript
    - html과 css에서 다루지 못하는 모든 영역
    - 변수와 상수 : 데이터를 담는 공간(상자)
        - 변수 : 어떤 관계나 범위 안에서 여러가지 값으로 변할 수 있는 수
        - 상수 : 변할 수 없는 수
        - 선언
            - let (변수명) 
            - var * 거의 사용 x
            - const * 상수 선언
            - 변수명 입력시 주로 camelCase 사용
                - camelCase
                    - ex) let myMoney
                - snake_case
                    - ex) my_money
        - 할당
            - 변수명 = 데이터
        - 선언 + 할당
            - let 변수명 = 데이터
    - 배열
        - 빈배열 []
        - 숫자 배열 [1,2,3]
        - 문자열배열 ["가", "나", "다"]
        - 자주 사용되는 기능(데이터 변환, 제어할 수 있게 해주는 것) => 명령어 뒤에 ()가 붙어 있는 것
            - array.length
            - array[인덱스]
            - array.push() -> 맨 뒤 값 추가
            - array.pop()  -> 맨 뒤 값 삭제
            - array.sort()
            - array.includes(값) -> 배열 데이터 확인
            - array.concat(array2) -> 배열 2개 연결
            - array.join() -> 배열을 문자로 만들기
            - array.slice() -> 배열 분리
            - array.filter() -> 배열에서 원하는 요소 뽑기
            - array.map() -> 배열의 모든 요소 변경
        
- chrome 개발자 도구
    - f12
    - 웹사이트를 전반적으로 분석하고 시험해 볼 수 있도록 도와주는 도구
    - 요소(elements)
        - HTML을 분석하고 수정해볼 수 있는 도구
    - 콘솔(console)
        - 현재 로딩된 페이지에서 자바스크립트를 시험하거나 로그/오류 메시지 등을 확인할 수 있는 도구
    - 소스(Resources)
        - 현재 로딩된 페이지에서 사용된 리소스를 열람할 수 있는 도구
    - 네트워크(Networks)
        - 서버와의 통신 내역을 보여주는 도구
    - 성능 (Audits)
        - 웹 어플리케이션의 성능을 향상시킬 방법을 컨설팅해주는 도구

- 회원가입 화면 만들어 보기 (12_signup)
    - css 연결 안하고 스타일 적용 안된다고 하고 있었음
    - link, rel 제대로 연결해주기

    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/signup2.jpg" width="600"/>

    [회원가입 화면]

### Day 05
- 객체
    - 중괄호 안에 데이터를 넣고 쉼표로 각 데이터를 구분함

        const profile = {
            name: "홍길동",
            age: 50,
            height: 164,
        }

    - key - value Pair
        - key = name, age, height
        - value(값) = 홍길동, 50, 164
        - 값은 비어있을 수 있음
    - 빈객체, 숫자값, 문자열 값을 넣은 객체를 생성할 수 있음
    - 객체에 담긴 값을 가져오는 방법
        - 변수명.key (주로사용)
        - 변수명["key"]
        
                const profile = {
                    name: "홍길동",
                    age : 49,
                    height: ,
                    school: "코드중학교",
                }
                profile.name => "홍길동"
                profile["school"] => "코드중학교"

- 배열안에 객체를 담을 수 있음

        let students=[
            {name:"길동", pet:"강아지", house:"구로구"},
            {name:"철수", pet:"고양이", house:"관악구"},
            {name:"다희", pet:"미어캣", house:"강서구"}
        ]

        students[0]
        => {name:"길동", pet:"강아지", house:"구로구"}

        students[0].name => "길동"

- 데이터타입과 연산자
    - 데이터타입
        - string : 영문, 한글 등 문자를 말함 " "
        - number : 숫자
        - boolean : 참, 거짓을 말함
        - object : { }
            - 배열 = 객체의 일부분으로 간주하고 있음
        - null : 아무것도 없음을 직접 입력함
        - undefined : 정의되지 않음을 의미함 (값이 없음을 컴퓨터가 알려주는 것)
    - 연산자
        - 산술연산자
            - '+' (숫자 더하기도 가능하지만 문자열 더하기도 가능)
                - 숫자 + 문자열 => 문자열
            - '-'
            - '*'
            - / : ex) 33 / 2 => 16
            - % : 나머지 ex) 33 % 2 => 1
        - 비교연산자
            - <
            - `>
            - <=
            - `>=
            - 엄격한 동치 연산자
                - ===
                - !==
                - 데이터 타입과 값까지 같아야 True
            - 느슨한 동치 연산자
                - ==
                - !=
                - 타입 비교 없이 값만 같으면 True
        - 논리연산자
            - && : and
            - || : or
            - ! : not -> boolean을 반전시킴

- 조건문
    - 특정 조건을 만족하면 실행
    - 핵심 : 시작점과 끝점이 존재
    - 조건문 : 컴퓨터가 조건에 맞는지 true / false로 판단하여 판단을 기반으로 각각 다른 명령을 실행할 수 있도록 하는 것
    - 비교 연산자와 함께 쓰임
    - 조건이 맞다면 A 실행(시작점), 아니라면 B 실행(끝점)

            if(조건){
                A실행
            }
            else{
                B실행
            }

    - 여러개의 조건 넣기도 가능

            if (A!==B){
                명령문 1
            } else if ((C===D) && (E === F)){
                명령문 2
            } else {
                명령문 3
            }

            => A!== B 라면 명령문1 실행 / 아닌 경우 else if 조건 검색
            A===B, (C===D) && (E === F) 인 경우 명령문 2실행 / 아닌경우 else 실행
        
- 반복문
    - 같은 행위를 반복하는 것
    - 핵심 : 몇 번 반복할 것인가
    
            for (초기식; 조건식; 증감문){
                반복해서 실행할 내용
            }

            for (let i = 0; i < 5; i + i +1;) {
                console.log("hello")
            }

            => 반복 (i를 0부터 시작; i가 5보다 작을때까지만; 한번 반복할 때마다 i에 1을 더함;){
                콘솔에 로그를 남김("안녕")
            }
    - 초기식 : 반복문의 시작점을 만들어 주는 것
        - let i = 0
        - i의 시작점 0 을 알려주는 것임
        - const 사용 불가 => i = i + 1이 불가능 하기 때문
    - 조건식 : 반복문의 끝점을 알려주는 것
        - i < 5
    - 증감문 : 카운트를 어떻게 할 것인가
        - i = i + 1 / i++(이렇게 써도 됨)
    - 변수명은 꼭 i가 아니어도 상관없음
    - 특정조건 만족 시
        - 조건식을 통한 정상종료 이전에도 종료(break)가능
        - 명령문을 실행하지 않고 다음 반복으로 건너뛰기(continue) 가능

- 수학객체
    - 자바스크립트의 수학 기능을 사용하는 명령어
    - 최대값 구하기 : Math.max()
    - 최소값 구하기 : Math.min()
    - 0 ~ 1 랜덤 수 생성 : Math.random()
    - 반올림 : Math.round()
    - 올림 : Math.ceil()
    - 버림 : Math.floor()

- DOM
    - Document Object Model 의 줄임말
    - html => tag로 구성 => tag : 약속된 명령어
    - 웹브라우저가 정적인 웹페이지를 변경하거나 조작하기 위해 HTML 파일을 자바스크립트 객체로 만들어줌
    - html과 javascript가 서로 상호작용하며 동적인 작동 가능하게 만듦

            document.getElementByld("tagID").InnerText

            => HTML 파일에서 "tgID"라는 id를 가진 태그를 선택해서 제어함


- 싸이월드 화면 만들어보기

    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/cyworld2.jpg" width="600"/>

    [싸이월드 화면]

    - iframe 태그 활용하여 다른 html과 css 연결시킴
    - iframe 태그를 이용하여 다른 화면을 띄울 수 있음

    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/cyworld3.jpg" width="600"/>

    [싸이월드 화면]

### Day 06
- 함수
    - 우리가 직접 만드는 기능
    
            function hello(){
                alert("안녕하세요")
            }
    - function 함수이름(매개변수) {함수를 호출했을 때 실행할 명령문}
    - 매개변수: Optional (함수안에서 사용해야함)
    - 데이터 반환 : return문
    - return문 
        - Optional
        - 결과값이 반환되어 나옴 (콘솔로그의 경우 결과값 반환되어 나오지 않음, 실제로 작동하는 것 x)
    
                function hello(name){
                    alert(name+"님 안녕하세요")
                }

    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/function1.jpg" width="600"/>

    [function hello(name)의 결과화면]

    - 함수 작성방법
        - 함수 선언식

                    function hello(name){
                        alert(name + "님 안녕하세요")
                    }

        - 함수 표현식
        
                    const hello = function(name){
                        alert(name + "님 안녕하세요")
                    }

        - 화살표 함수

                    const hello = (name) => {
                        alert(name + "님 안녕하세요")
                    }
        
        - 작성방법이 모두 다르지만 실행방법은 모두 동일함

- 내장함수
    - 자주 사용되는 함수를 자바스크립트에 내장하여 편리하게 이용할 수 있도록 한 것
    - 많이 사용되는 내장 함수
        - 시간 지연 함수 (시간 입력 시 ms 단위로 입력)

                setTmeout(func, time)

            <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/setTimeout.gif" width="400"/>

        - 시간 반복 함수 (시간 입력 시 ms 단위로 입력)

                setInterval(func, time)

            <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/setInternal.gif" width="400"/>
            
            [1초가 지났습니다가 계속 출력됨]

            <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/timer.gif" width="400"/>
            
            [조건문을 활용하여 10초에서 0초까지 출력되는 타이머 만들기]

- 싸이월드 만들기
    - 추억의 BGM 화면 만들기
    - 미완성

### Day 07
- 싸이월드 만들기
    - Day 06에서 미완성한 추억의 BGM 화면 만들기
    - 사진 다시 다운받은 후 이름, 가수 넣어줌
    - 테이블 만들기

    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/cyworld4.jpg" width="600"/>

    [싸이월드 화면]

### Day 08
- setInterval, clearInterval에 대한 공부가 조금 더 필요함
- 이벤트 감지
    - ex1) 회원가입 화면에서 이메일, 비밀번호, 비밀번호 확인을 다 입력해야 회원가입 버튼 활성화되는 것
    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/event1.gif" width="600"/>

    - ex2) 전화번호 입력 시 자동으로 다음 탭으로 넘어가지는 것
    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/event2.gif" width="600"/>

- 싸이월드 만들기 마무리
    - 그동안 만들었던 화면들 해당 버튼 클릭 시 이동할 수있도록 만듦

    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/cyworld5.gif" width="600"/>

### Day 09
- Final Project

    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/finalProject1.jpg" width="400"/>
   
    [디자인 화면]

### Day 10
- Final Project

    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/finalProject.gif" width="600"/>
   
    [구동 화면]

<hr>

## Class 02 CSS 기초

### Day 01
- 웹 브라우저란?
    - 인터넷 통신을 할 수 있는 프로그램
    - ex) 크롬, 파이어폭스, 사파리, 엣지 등등

- CSS란?
    - Cascading Style Sheet
    - 웹 페이지의 스타일 & 레이아웃을 담당하는 문서

- CSS 기본용법

        <div> DIV 입니다.</div>
        [HTML 소스]

        div{
            background: red;
        }
        [CSS소스]

    - 선택자 { 선언 = 속성(property) : 속성값(property value) }

- CSS 적용 방식 : 인라인 방식, style태그 이용, 분리된 css 파일 연결
    - 인라인(in-line)방식
        - 속성을 적용할 HTML 태그에 직접 CSS를 입력해주는 방식

                <div style="background-color: red;">DIV입니다.</div>
        - css가 길어질 수록 가독성이 떨어지고, 유지보수가 어렵다는 단점이 있음
        - 실무에서 거의 사용 x

    - style 태그 이용
        - html 문서 head 내에 style 태그를 사용함

                <!DOCTYPE html>
                <html lang="ko">

                <head>
                    <meta charset="UTF-8">
                    <meta http-equiv="X-UA-Compatible" content="IE-edge">
                    <title> 1일차 수업</title>
                    <style>
                        div{
                            background-color: red;
                        }
                    </style>
                </head>

                <body>
                    <div> DIV 입니다. </div>
                </body>
                </html>

    - 분리된 CSS파일 연결
        - HTML 파일, CSS파일 따로 만든뒤 link 태그를 이용해 연결해주는 방식

                <link rel="stylesheet" href="./index.css">

        - rel : 해당 태그로 연결시켜줄 파일과 어떤 관계인지 지정 (relation)
        - href: 연결할 파일의 경로를 지정
        - 확장자명에 .html, .css를 꼭 작성해줘야함
        - 실무에서 가장 많이 활용하는 방식
        - 유지보수가 편리하고 소스코드를 관리하기 좋음

- 선택자
    - 태그 선택자
    
            tag{
                property: value
            }

    [예시]
    
            <div>
                <h1>제목입니다.</h1>
                <p>내용입니다.</p>
            </div>

            div{
                background-color: #f9f9f9;
            }

            h1{
                font-size: 20px;
                color: red;
            }

            p{
                color: blue;
            }
    
    - id 선택자

            #id{
                property: value;
            }

    [예시]

            <body> 
                <div>
                    <h1 id="title">제목입니다</h1>
                    <p>내용입니다.</p>
                </div>
            </body>

            #title{
                font-size: 28px;
                color: red;
            }
        
    - class 선택자
        - 여러개의 요소에 중복 지정 가능

                .class{
                    property: value
                }

    [예시]

                <body>      
                    <div>
                        <h1 id="title">제목입니다.</h1>
                        <p class="contents">내용입니다.</p>
                    </div>
                </body>

                .contents{
                    color: blue;
                }

    - 자손 선택자

            <body>      
                <div>
                    <h1 id="title">제목입니다.</h1>
                    <p class="contents">내용입니다.</p>
                </div>
            </body>
        
        - div : 부모요소
        - h1, p : 자식요소1, 2

            .parent .child{
                property: value
            }
    
    [예시]

            <body>
                <h1 class="title">전체 제목입니다.</h1>
                <div class="box1">
                    <h1 class="title">제목입니다.</h1>
                    <p class="contents">내용입니다.</p>
                </div>
                <div class="box2">
                    <p class="text1">글 내용입니다. 1</p>
                    <p class="text2">글 내용입니다. 2</p>
                </div>
            </body>

            .box1 .title{
                color: yellow;
            }

            .box2 .text1{
                color: green
            }

    - 다중선택자
        - title 클래스와, headline아이디를 가진 경우

            .class#id{
                property: value;
            }

    [예시]

            <body>
                <h1 class="title">전체 제목입니다.</h1>
                <div class="box1">
                    <h1 class="title" id="headline">제목입니다.</h1>
                    <p class="contents">내용입니다.</p>
                </div>
                <div class="box2">
                    <p class="text1">글 내용입니다. 1</p>
                    <p class="text2">글 내용입니다. 2</p>
                </div>
            </body>

            .title#headline{
                color: violet
            }

### Day 02
- 에밋?
    - h1 태그 입력 방법
        - h1 입력 후 탭 선택 시 자동 완성 됨

                <h1> </h1>
    - title이라는 class, headline이라는 id를 가진 h1 태그를 생성하고 싶을 때
        - h1.title#headline 입력 후 탭 클릭 시 자동 완성 됨

                <h1 class="title" id="headline"></h1>
            

    - contents라는 class를 가진 p 태그 생성 시
        - p.contents 입력 후 탭 클릭 시 자동 완성 됨

                <p class="contents">내용입니다.</p>

- 폰트 기본 스타일
    - font 기본 속성
        - font-size : 글자 사이즈
        - font-weight : 글자 두께
        - font-style : 글자 기울임
        - text-decoration: 글자 꾸밈(밑줄, 취소선 등)
        - color: 글자 색

- 박스모델
    - 웹브라우저에서 HTML Element(요소)를 구성할 때 각각의 요소가 차지하는 박스 공간을 정의한 모델
    - 모든 HTML 요소는 박스 형태로 되어 있음 => 이러한 박스 형태 = 박스 모델임

- box-sizing 속성
    - content-box
        - content 영역을 기준으로 box의 size 적용
        - 기본값
    - border-box
        - border 영역을 기준으로 box의 size 적용

- inline 요소 vs Block 요소
    - block 요소
        - 블록요소를 여러개 연속해서 쌓을 경우, 자동으로 다음줄로 넘어감
        - 좌/우 양쪽으로 늘어나 부모 요소의 너비를 가득 채움
        - ex) div, p, u, dl, h1, h2, h3, 등등
    - inline 요소
        - 여러개의 요소를 연속해서 입력해도 자동으로 다음줄로 넘어가지 않음
        - 태그에 할당된 공간 만큼의 너비만 차지함
        - ex) span, a, img, strong, em, input, button, textarea, select, 등등

- 실습
    - 일기장 만들기
    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/mydiary1.jpg" width="600"/>



### Day 03
- 실습
    - 일기장 만들기 마무리
    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/mydiary2.jpg" width="600"/>


### Day 04
- 레이아웃
    - 사전적 정의 : 출판 광고 건축 분야 등에서 요소를 효과적으로 배치하는 것
    - css 레이아웃 : css를 이용하여 단순 문서 형태인 html을 보기 좋게 배치하고 재배열 하는 것, 관련기능, 완성된 배열 등을 포괄적으로 지칭함
    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/layout.jpg" width="600"/>

    [레이아웃]

- 선택자
    - 전체선택자
        - html에서의 모든 요소를 선택하는 것

                *{
                    property: value
                }
   
    - 그룹 선택자
        - 여러개의 선택자를 동시에 선택, 동시에 적용할 때 사용
        - 원하는 선택자를 ,를 이용하여 연결
        - 선택자의 갯수 상관 없이 계속 연결 가능

                .class1, .class2{
                    property: value
                }
    
    - 가상 클래스 선택자
        - 실제로 html 요소를 수정하지 않고 css 만으로 가상 요소를 추가해 선택할 수 있음

                    선택자:가상클래스{
                        property: value
                    }

        - first-child가상 클래스 선택자
            - 해당 요소들 중 첫번째 클래스를 선택한다는 의미

                    .class:first-child{
                        property: value
                    }

        - last-child 가상 클래스 선택자
            - 해당 요소들 중 마지막 클래스를 선택한다는 의미

                    .class:last-child{
                        property: value
                    }

        - nth-child(n) 가상 클래스 선택자
            - 원하는 순서에 있는 클래스를 선택한다는 의미
            - (n)에는 원하는 순서를 넣을 수도 있고, 2n과 같이 2의 배수를 표현하는 숫자도 넣을 수 있고, 연산자가 모두 사용 가능함
            
                    .class:nth-child(n){
                        property: value
                    }

        - hover(오버)
            - 요소 위에 마우스가 올라갔을 때 발생하는 전환효과 등을 말함

                    .class:hover{
                        property: value
                    }

                    ex)
                    .button1:hover{
                        background:red;
                        color:#ffffff;
                    }

- css 레이아웃 흐름
    - Float -> Flex -> Grid
    - Float 
        - 현재 거의 사용하지 않음
        - 반응형 웹에 적합하지 않기 때문
            - 반응형 웹 : 모바일, 태블릿, pc 등 접속하는 기기의 너비에 맞추어 레이아웃이 변하는 웹페이지
        - float를 사용한 코드도 읽을 수있기 위해 배워야 함
        - 레이아웃이 어떻게 변해왔는지 알면 flex를 더 효과적으로 사용할 수 있음
    - Flex와 Grid를 상황에 따라 혼용함

- Float 레이아웃
    - float
        - 기본값 : none

                float:none
        - left, right로 요소를 배치시킬 수 있음
        
        <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/float_left.jpg" width="600"/>
        
        [float:left]

        <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/float_right.jpg" width="600"/>
        
        [float:right]

                float:left
                float:right
    - clear
        - float가 적용된 요소, float가 적용된 요소에게 영향을 받고 있는 요소들에게 추가로 줄 수 있는 속성
        - 기본값 : none

                clear:none
        
        - left, right, both
        - both를 많이 사용함
        <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/float_right-clear_left.jpg" width="600"/>

        [float_right + clear_left]

        <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/float_right-clear_right.jpg" width="600"/>

        [float_right + clear_right]

- 실습
    - 다이어리 만들기
        - hover 선택자
        - float 정렬
        <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/mydiay.gif" width="600"/>

- Flex
    - css 레이아웃의 꽃
    - css 레이아웃 배치에 중점을 두고 고안되었기 때문에 기존의 float 방식보다 훨씬 수월하고 간단하게 레이아웃을 잡을 수 있음
    - 요소의 속성을 flex로 변경
    - flex-direction : row(행) / column(열)
    - flex-direction이 바뀌면 중심축의 방향이 바뀌기 때문에 justify-content, align-items의 정렬 방향도 바뀜
    - flex-direction의 기본값 : row ㅁㅁㅁㅁ
    - flex-direction: column : ㅁ
                               ㅁ
                               ㅁ
                               ㅁ
    - justify-content : 중심축 방향 정렬
        - flex-start : 기본값 => container 시작점에 정렬
        - flex-end : container 끝부분을 기준으로 정렬
        - center: 중앙정렬
        - space-between : 양끝에는 여백이 없고 container 안의 item들이 균일한 간격을 두고 정렬됨
        - space-around : 양끝에도 여백이 생기고 container 안의 item들이 균일한 간격을 두고 정렬됨
        - space-evenly : 양끝과 container 안의 item들의 모든 여백의 크기가 균일함
    - align-items : 중심축 반대 방향 정렬
        - stretch : 기본값 => item을 container 영역을 꽉 채움
        - flex-start : 시작점 기준으로 정렬
        - flex-end : container의 끝부분 기준으로 정렬
        - center : 중앙정렬
        - align-items는 flex-item이 한줄일 때 우선 적용하고 두줄 이상일 경우 align-content라는 다른 속성을 써줘야 함


                display : flex
                flex-direction : row / flex-direction : column
                justify-content : space-between
                align-items : center

### Day 05
- 선택자
    - 가상클래스 선택자

            :first-of-type
            :active
            :focus
            :visited

    - first-of-type
        - first-child와 비슷하지만 다름
        - first-child 
            - 형제 요소 중 첫번째 요소를 선택하는 가상 클래스
            - 같은 부모 안에 있는 형제 요소 중 첫 번째 요소 선택

                    <div class="container">
                        <h1>이렇게</h1>
                        <p>자식이 있다면?</p>
                    </div>

                    .container h1:first-child{
                        background:red;
                    }
                    => h1 background 색상이 red로 적용됨

                    .container p:first-child{
                        background:red;
                    }
                    => container의 첫번째 자식요소가 h1이기 때문에 p태그를 first-child로 인식하지 않아 적용되지 않음
        - first-of-type 
            - 형제 요소 중 첫번째 요소를 선택하는 가상 클래스
            - 해당되는 요소만 카운트한다는 점이 first-child와 다른점임

                    <div class="container">
                        <h1>제목입니다.</h1>
                        <p>첫번째 p 태그 입니다.</p>
                        <p>두번째 p 태그 입니다.</p>
                        <span>첫번째 span 태그 입니다.</span>
                        <p>세번째 p 태그 입니다.</p>

                    </div>

                    .container h1:first-child{
                        background:red;
                    }
                    => h1 background 색상이 red로 적용됨

                    .container p:first-of-type{
                        background:red;
                    }
                    => p태그들 중 첫번째 p 태그에 background 색상이 red로 적용됨

### Day 06
- 선택자
    - of-type
        <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/of-type-and-child.jpg" width="600"/>

    - active
        - 활성화된 요소를 선택하는 가상 클래스 선택자
        - 활성화된 요소 : 버튼 등을 클릭해서 요소의 동작이 활성화되어 있는 상태
            ex) 버튼을 클릭할 때 색이 변하는 것

    - focus
        - focus를 받고 있는 입력 창 등의 요소를 선택하는 가상 클래스 선택자
        - Tab키 등을 이용해서 입력창의 커서가 활성화되어 있는 상태

    - visited
        - 사용자가 방문한 적 있는 링크를 선택하는 가상 클래스 선택자
        - 방문한 적 있는 링크 : 링크를 눌러서 해당 경로를 방문한 기록이 브라우저상에 남아 있는 링크
            ex) 기본컬러 -> 보라색

        <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/active-focus-visited.gif" width="600"/>

- 가상 요소 선택자
    - 실제로 html요소를 수정하지 않고, css 만으로 가상 요소를 추가해 선택할 수 있음
    - before, after

        [html 소스]

            <div class="box1">
                나는 박스1입니다.
                <p class="text">나는 박스2입니다.</p>
            </div>
        

        [css 소스]

            .box1{
                    width : 200px;
                    height: 300px;
                    background-color: yellow;
                }
            .text{
                    background-color: blue;
                }
        


        [가상요소 선택자 사용시 html]

            <div class="box1">
                나는 박스1입니다.
            </div>


        [가상요소 선택자 사용시 css]

            .box1{
                width : 200px;
                height: 300px;
                background-color: yellow;
            }
            .box1:after{
                content:"나는 박스2입니다.";
                display: block;
                background-color: blue;
            }

        - 결과는 같음

- 형제요소 선택자
    - A와 같은 부모를 가지고 있는 형제 요소들 중 B를 선택함

            A~B{
                property : value
            }

### Day 07
- flex 추가
    - flex => css 레이아웃 배치에 중점을 두고 고안됨
    
            display: flex
            flex-direction : row | column => 중심축 설정
            justify-content :             => 중심축 기준으로 정렬 설정
            align-item :                  => 중심 반대축 방향의 정렬 설정

    - flex-wrap
        - flex-item이 여러개일 때 item 들의 줄바꿈을 허용할 것인지 말 것인지 결정
        - 기본값 : nowrap => 무조건 한줄 안에 들어가게 강제함
        - wrap : item의 규격에 맞춰 다음줄로 개행됨
        - 주의 : align-items는 flex-item이 한줄일 때 우선 적용됨, 두줄 이상일 때에는 align-content라는 다른 속성을 써줘야 함

    - align-content
        - 여러 줄이 된 flex-item의 중심 반대 축 정렬을 어떻게 할 지 결정
        - 기본값 : stretch
            - item의 실제 규격과 상관 없이 늘어난 형태
        - flex-start : container의 시작점을 기준으로 item 정렬
        - flex-end : container의 끝점을 기준으로 item 정렬
        - center : 중심을 기준으로 item 정렬
        - space-between : start-line과 end-line으로 벌어져 정렬됨
        - space-around : 축을 기준으로 위, 아래의 간격이 동일함 => 가운데는 start-line, end-line의 간격과 비교했을 때 2배 간격임
        - space-evenly : 위, 아래의 간격이 동일함

    - flex-flow
        - flex-direction과 flex-wrap을 합쳐놓은 단축 속성
        - 단축속성 : 유사한 성질을 가진 여러 공통의 속성들을 한번에 사용할 수 있도록 묶어놓은 속성
            ex) border

        [flex-direction, flex-wrap 속성 2개 사용]

                flex-direction: row;
                flex-wrap: wrap;

        [flex-flow 속성 1개 사용]

                flex-flow: column wrap

    - flex-item 속성들
        - order : item의 순서 지정
        - flex-basis : item의 기본 사이즈 지정
        - flex-shrink
        - flex-grow 

[display - flex 설정 x -> o -> x]
   
<img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/display-flex.gif" width="600"/>


[flex-wrap 설정]
    
<img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/flex-wrap.gif" width="600"/>

1. container안의 box들의 width 를 200px로 설정 => flex-wrap의 기본값이 stretch로 container 안에 꽉 채워져 200px로 나오지 않음
2. flex-wrap 설정 => wrap으로 변경하여 box들의 width로 설정된 200px로 나옴
            
### Day 08
- CSS 상속
    - 부모요소의 속성값을 자식요소에게 상속함

            <div class="container">
                바깥에 있는 박스입니다.
                <div class="inner-box">
                    <p> 안쪽에 있는 박스입니다. </p>
                </div>
            </div>

            .container{
                color: red;
            }

        - 바깥에 있는 박스입니다. 안쪽에 있는 박스입니다. 2개 모두 빨간색 적용됨
    - 모든 속성이 상속되지는 않음

            <div class="container">
                바깥에 있는 박스입니다.
                <div class="inner-box">
                    <p> 안쪽에 있는 박스입니다. </p>
                </div>
            </div>

            .container{
                color: red;
                border: 3px dashed blue
            }
        
        - border 속성은 container에만 적용됨
        - 상속되는 속성과 상속되지 않는 속성이 있기 때문
            - 상속되는 속성 : color, font-family, font-size 등등
            - 상속되지 않는 속성 : padding, margin, border 등등
    - 여러개의 상속 속성이 겹쳤을 때
        - Cascading이라는 룰이 우선순위를 결정함
    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/inherit.gif" width="600"/>

- 웹폰트
    - font-family : "폰트이름"
    
            font-family: arial, "맑은 고딕", sans-serif;

    - font-family에 2개 이상의 폰트 설정
        - 앞에서부터 우선순위 부여받음
        - 유저 컴퓨터에도 폰트 파일이 설치되어 있어야 글시체가 제대로 보임
    
    - 웹폰트 : 웹전용 폰트
        - 사용자가 로컬컴퓨터에 폰트를 직접 설치하지 않아도 특정 서버에 위치한 폰트를 다운받아 웹페이지에 표시해주는 것
        - 사용자들이 알지 못하는 폰트 다운로드가 진행되는 것임

    - 웹폰트 적용 방법
        - 폰트 파일을 직접 다운로드 받아서 적용하는 방법
            - @font-face이용
                1. 웹폰트 파일 준비 (확장자명 : woff / woff2 / ttf / eot)
                2. css문서에서 @font-face를 이용해 폰트 파일 불러옴
                3. 불러운 폰트 파일을 이용해 새로운 font-family를 만듦
                4. 만든 font-family 사용

        - 외부 서비스에서 제공하는 링크를 이용하는 방법
            - @import 혹은 link태그 이용
                1. 구글 폰트에 접속해서 원하는 폰트를 찾음
                2. 폰트를 상세페이지 접속 후, 원하는 굵기의 폰트 옆에 있는 Select this style 클릭
                3. Use on web 항목에서 import를 선택하고 해당 import 구문을 css 파일 내에 입력
                4. css rules to specify familes를 참고하여 font-family 작성

- 폰트
    - font-size : 텍스트의 크기를 지정함
    - font-weight : 텍스트의 두께를 지정함
    - text-decoration : 텍스트에 장식용 선을 추가함
    - color : 텍스트의 색 지정 
        - 색상 직접 지정
            ex) color : red;
        - Hex 코드 사용
            ex) color : #5145d8;
        - RGB 코드 사용
            ex) color : rgb(213,229,37)
    - line-height : 텍스트의 행간을 설정함
        ex) line-height : 1.8 => 해당 텍스트의 1.8배의 행간
        ex) line-height : 52px -> 52px 크기의 행간 => 다른 단위를 적을 때는 무조건 단위까지 적어줘야 함
    - letter-spacing : 텍스트의 자간을 설정함
        - 다양한 단위 부여 가능
        - 기본값 : normal
        - em, px
        - 양수, 음수 사용 가능
    - word-spacing : 텍스트의 단어간 간격 지정
        - 다양한 단위 부여 가능
        - 기본값 : normal
        - em, px
        - 양수, 음수 사용 가능
    - text-align : 블록요소나 표 안에서 텍스트의 가로 정렬 방식을 지정
        - left, right, center로 설정 가능
        - 좌측, 우측, 중앙 정렬
        - justify => 양측정렬
            - left와 비교했을 때 left 정렬은 우측이 울퉁불퉁한 경우가 있으나 justify의 경우 좌 우측 라인이 한줄로 이어져 있음
    - vertical-align : 인라인 요소나 표 안에서 텍스트의 세로 정렬 방식을 지정
        - top, middle, bottom 으로 설정 가능
        - 상단, 중앙, 하단 정렬
    - text-indent : 텍스트의 들여쓰기를 설정함
        - 다양한 단위 부여 가능
        - 기본값 : 0
        - px, em, rem
        - 양수, 음수 사용 가능
    - text-transform : 영문 텍스트의 대/소문자를 바꿀 수 있음
        ex) text-transform : capitalize
        - 기본값 : none
        - capitalize => 각각의 단어의 첫번째 글짜 대문자로 변환
        - uppercase => 모두 대문자로 변환
        - lowercase => 모두 소문자로 변환
    - word-break : 텍스트가 콘텐츠 박스 영역 밖으로 넘쳤을 때 어떻게 줄을 바꿀지 설정
        - keep-all : 띄어쓰기 기준 줄바꿈
        - break-all : 어절단위 줄바꿈 => 지정한 범위에 글이 꽉 참 but, 가독성은 조금 떨어짐
    - overflow-wrap : 단어가 콘텐츠 박스 영역 밖으로 넘쳤을 때 줄바꿈 여부를 설정
        - 좁은 영역 안에 긴 단어가 들어가 콘텐츠 박스 영역 밖으로 넘친 경우 -> 콘텐츠 영역 밖으로 나가게 됨 => overflow-wrap을 설정한 경우 다음줄로 넘어가게 설정 가능
            ex) This is a WATERMELON. A watermelon is delicious 라는 문장에서
                <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/overflow-wrap-vs-word-break.jpg" width="600"/>
        - normal
        - break-word
    - overflow : 콘텐츠가 커서 요소 안에서 내용을 다 보여주기 힘들 때, 어떤 방식으로 보여줄지 설정함
        - 기본값 : visible
        - hidden
        - scroll
        - auto
    - text-overflow : 줄바꿈을 하지 않을 때, 요소 밖으로 넘치는 text를 어떻게 표기할 것인지 설정함
        - text-overflow를 적용하고 싶은 요소에는 반드시 다음 선언들도 함께 적용되어야 함
        - text-overflow 선행 조건 
            - white-space : nowrap;
            - overflow : hidden;
        - 기본값 : clip
        - ellipsis

- 단위
    - 절대단위
        - 외부 요인에 영향을 받지 않고 절대적인 값을 지니는 단위
        - ex) cm, km 등등

        - px (pixel, 화소)
            - 화면을 구성하는 가장 기본이 되는 단위
            - 수많은 작은 네모들로 구성되어 있고 이 네모 한칸을 1px이라고 부름
        
        - pt (point, 포인트)
            - 인쇄를 위한 단위
            - 1pt == 1/72inch(인치)
            - 웹에서는 잘 사용하지 않음

    - 상대단위    
        - 외부 요인에 영향을 받아 유동적인 값을 지니는 단위
        - ex) %

        - %
            - 부모 요소의 해당 속성 값에 비례하여 지정한 비율의 값을 적용함

        - em
            - 스타일 지정 요소의 font-size 속성 값에 비례하여 값을 결정함
            - font-size : 16px인 경우
              1em => 16 * 1 = 16px
              0.8em => 16 * 0.8 = 12.8px
              3em => 16 * 3 = 48px
        
        - rem
            - <strong>최상위 html요소</strong>의 font-size 속성 값에 비례하여 값을 결정함

- 캐스케이딩(cascading)
    - css = cascading style sheet
    - cascading : 폭포, 위에서 아래로 흐르는 이라는 의미
    - 수많은 스타일 요소 중 어떤 스타일을 브라우저에 그릴지 결정해주는 css 우선순위 적용 원리
    - 기준
        - 중요도
            - css가 선언된 위치에 따라 우선순위가 결정됨
            - 브라우저 스타일 시트 < 사용자 스타일 시트 < 개발자 스타일 시트 순으로 중요도가 높음
            - 브라우저 스타일 시트
                - 아무런 css 설정하지 않은 html 문서로 기본적으로 저장되어 있는 스타일을 의미함
            - 사용자 스타일 시트
                - 사용자 폰트 지정
                - 고대비 모드 사용
            - 개발자 스타일 시트
                - 해당 웹페이지의 개발자가 만들어서 넣어놓은 스타일
                - link로 연결한 css 파일 < style 요소 안에 있는 css < 인라인  스타일 css
                <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/cascading.gif" width="600"/>
            - 인라인 스타일 css < style요소 안에 있는 css < link로 연결한 css 파일 < 사용자 스타일 시트 < 브라우저 스타일 시트 순

        - 구체성(명시도)
            - 선택할 대상을 구체적으로 특정할수록 명시도가 높아짐
            - 명시도가 높아지면 우선순위도 함께 높아짐
            - 부모에게 상속받은 속성 < 전체 선택자 < 태그 선택자 < 클래스 선택자 가상 선택자 < ID 선택자 순

            - 강제로 명시도 끌어올리기 : !important (가능한 사용 x)

        - 선언순서
            - 나중에 선언한 스타일이 우선 적용됨

### Day 09
- 배경
    - background-color : 요소의 배경에 색상 지정 가능
    - background-image
        - 요소의 배경 이미지를 한개 혹은 여러 개 지정함
            - background-image:url("이미지 경로")
        - 그라데이션도 지정이 가능함
            - background-image:linear-gradient(방향, 시작 색상, 종료 색상)
            - 방향 : to top, to left, to right, to bottom, 생략(to top)
            - background-image : radial-gradient
            - background-image : conic-gradient
        - 콤마(,)를 이용하여 여러가지 배경을 동시에 사용하기도 가능
        - 먼저 선언하는 것이 위에 올라오게 됨
    - background-position
        - 요소의 배경 이미지의 위치를 지정
        - bottom, top, left, right, center를 조합하여 위치 지정 가능
        - 직접적인 수치 지정 가능 (50px 150px) -> 첫번째 값 : x축
    - background-repeat
        - 요소의 배경 이미지의 반복 여부, 반복 방향 지정
        - 기본값 : repeat으로 끝없이 반복되는 형태임
        - no-repeat : 반복 없이 한개의 이미지만 원하는 위치에 들어가짐
        - repeat-x / repeat-y : 해당 축으로만 이미지가 반복됨
    - background-size
        - 요소의 배경 이미지의 크기 지정
        - 기본값 : auto -> 이미지가 가지고 있는 고유한 값으로 입력
        - cover : 많이 쓰이는 속성 중 하나, 이미지를 늘려서 요소 안에 빈틈 없고 찌그러지지 않도록 만듦
        - contain : 이미지 늘려서 요소 안에 채움 (이미지 전체 다 보이는것이 더 중요하기 때문에 빈틈이 있을 수 있음)
        - 직접적인 수치 지정 (50px 150px) -> 첫번째 값 : x축
    - background-attachment
        - 요소의 배경 이미지의 스크롤 여부 지정
        - 기본값 : scroll -> local과 비슷하지만 내부에서 스크롤 작동 x
        - fixed : 고정
        - local : 내부에서도 스크롤 작동
    - 단축속성
        - background-color / background-image / background-position / background-repeat / background-size

                background: color image repeat position/size attachment

                background: red url("../star.png") no-repeat center/cover fixed

    - object-fit
        - img, video 등 대체요소의 내용이 지정된 너비와 높이에 맞춰지는 방식을 지정함
        - 기본값 : fill -> 사이즈에 맞춰 찌그러지지만 꽉채움
        - cover : 백그라운드 사이즈에 cover를 준것과 같게 빈틈이 생기지 않는 범위에서 적절한 비율로 요소 꽉 채움
        - contain : 여백과 상관없이 이미지 전체가 보이도록 요소를 채움
        - none : 이미지 원본 비율대로 보여줌
        
    - object-position
        - img, video 등 대체요소의 콘텐츠 정렬 방식을 지정함
        - 직접적인 수치 지정
        - top, bottom, left, right, center를 조합하여 위치 지정 가능

- 색상
    - 색상 이름
        - 색의 이름을 표기하는 방식
        - 기본 16색 + 200색 => 총 216색(웹안전색상) 표기 가능
        - 웹안전색상 : 어떤 운영체제, 어떤 브라우저에서도 안전하게 그려지는 색
        - vs code에서 자동완성으로 제공됨
        - ex) red, blue 등
    - Hex 색상 코드
        - 16진수 여섯자리로 색상을 표기하는 방법
        - 실무에서 가장 많이 사용되는 방법
        - https://htmlcolorcodes.com/color-picker/ 
          -> VSCode 내장 색상 선택기
        - ex) #94FB11
    - rgb / rgba
        - red, green, blue값을 이용해 색상을 표기하는 방법
        - 0 ~ 255 사이의 숫자를 입력할 수 있음
        - rgba : 색상에 투명도도 적용할 수 있음
        - ex) rgb(251, 247, 17)
    - opacity
        - 요소의 불투명도를 설정할 수 있음
        - 0부터 1까지의 숫자를 지정할 수 있음

- 단위
    - 상대단위
        - vw / vh
            - 요소의 규격을 viewport의 너비값과 높이값에 비례하여 결정
            - viewport : 브라우저 안에서 실제로 화면이 그려지는 영역
            - vw : viewport width
            - vh : viewport height
            ex) viewport 1200px 920px인 경우
                10vw => 1200 * 0.1 = 120px
                50vh => 920 * 0.5 = 460px
                100vw => 1200 * 1 = 1200px

- 함수
    - 특정한 기능을 가지는 상자 같은 것
    - calc()
        - 괄호 안의 사칙연산을 수행한 결과를 속성값으로 사용함
        - 덧셈과 뺄셈의 경우 연산자 앞 뒤에 공백을 한칸씩 둬야 함
        - 곱셈, 나눗셈 상관 x

                width : calc(2*100px);
                width : calc(100% - 120px)


        [calc 기본 실습]

        <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/calc1.jpg" width="600"/>


        [사이드바, 컨텐츠부분 width 설정]

        <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/calc2.jpg" width="600"/>

- position
    - html 요소가 배치되는 방식을 결정하는 속성
    - 속성값
        - 기본값 : static
            - 요소를 문서상 원래 있어야 하는 위치에 배치함
            - top, bottom, left, right 적용 불가
        - relative
            - 원래 있던 자리를 기준으로 요소의 위치를 조정할 수 있음
            - top, bottom, left, right 적용 가능
        - absolute
            - 절대 좌표를 기준(absolute의 부모요소 중 relative가 적용된 요소를 기준)으로 요소의 위치 조정 가능
            - top, bottom, left, right 적용 가능
            <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/absolute.gif" width="600"/>

        - fixed
            - 스크롤과 무관하게 뷰포트를 기준으로 요소의 위치를 설정할 수 있음
        - sticky
            - 요소의 원래 위치에 있다가 스크롤이 내려가면 지정한 좌표에 고정됨
            - 기준 : 부모요소의 좌표
    - 해당 방향 기준으로 요소의 좌표값을 변경
        - tob, bottom, left, right
    - z-index
        - 여러개의 요소가 겹쳐져 있을 때 무엇이 앞으로 나올지 결정하는 속성
        - 기본값 : auto
        <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/z-index.gif" width="600"/>

### Day 10
- transition
    - transition-property
        - 어떠한 속성에 transition을 적용할 것인지 지정함
        
                transition-property : color, transform
    
    - transition-duration
        - transition에 걸리는 시간을 지정함

                transition-duration : 0.2s

    - transition-timing-function
        - transition의 속도 패턴을 지정함
        - 변화가 일정한 속도로 변할것인지, 느리게 시작해서 빠르게 끝낼것인지 등을 지정할 수 있음
        - linear : 일정한 속도로 변화
        - ease : 시작할때는 빨라지다 느려짐
        - ease-in : 천천히 시작했다가 속도를 높여 끝남
        - ease-out : 빠른속도로 시작했다가 천천히 끝남
        - ease-in-out : 천천히 시작 -> 정상속도 -> 빠르게 끝남

                transition-duration 0 :ease-in-out

    - transition-delay
        - transition 요청을 받은 후, 실제로 실행되기까지 기다려야 하는 시간의 양을 지정

                transition-delay : 2s

    - transition 단축 속성
        - 순서 : property duration timing-function delay 

                transition : color 0.4s ease-in-out 1s

### Day 11
- transform
    - 요소에 이동, 회전, 확대 축소, 비틀기 등의 변형 효과를 줄 수 있음
    - 속성값
        - translate(x,y)
            - 요소의 좌표를 움직일 수 있음
            - x축으로 x만큼, y축으로 y만큼 이동시킴
            - 양수 음수 모두 입력 가능
            - 두 값 중 하나만 입력된 경우 같은 값 만큼 이동
            - 요소의 x축 좌표를 n만큼 움직일 수 있음 => transform : translateX(20px)
            - 요소의 y축 좌표를 n만큼 움직일 수 있음 => transform : translateY(20px)

                    transform : translate(20px, 25%)
            
        - scale(x,y)
            - x축으로 x만큼, y축으로 y만큼 요소를 축소 혹은 확대함
            - 요소의 x축 좌표를 n만큼 축소 혹은 확대 할 수 있음 => transform : scaleX(20px)
            - 요소의 y축 좌표를 n만큼 축소 혹은 확대 할 수 있음 => transform : scaleY(20px)

                    transform : scale(0.75, 1.1)

        - skew(x-angel, y-angle)
            - x축으로 x도 만큼, y축으로 y도 만큼 요소를 기울임
            - 요소를 x축으로 x도 만큼 기울임 => transform : skewX(15deg)
            - 요소를 y축으로 y도 만큼 기울임 => transform : skewY(15deg)

                    transform : skew(15deg, 10deg)
                    
        - rotate(angel)
            - 요소를 n만큼 회전시킴
            - 시계방향으로 회전됨

                    transform : rotate(45deg)

### Day 12
- transform 중첩적용
    - transform 은 변환함수를 중첩 적용 시키는 것 가능
    - 요소를 75도 회전시키고 y축 방향으로 120px 이동

            transform : rotate(75deg) translateY(120px)
    
    - 요소를 x축 방향으로 30도, y축방향으로 10도 기울이고 45도 회전

            transform : skew(30deg, 10deg) rotate(45deg)

    - 요소를 y축 방향으로 0.75축소시키고 x축 방향으로 20도 기울임

            transform : scaleY(0/75) skewX(20deg)

- transform + transition
    - transform은 transition과 animation과 함께 사용하면 더 다채로운 애니메이션 효과를 만들 수 있음

- 쇼핑몰 화면 만들기
    - itemWrap
        - 사진이 나오는 전체적인 구조
        - display -> flex를 이용하여 정렬을 정의해줌
        - flex-wrap: wrap => 여러줄로 나올 수 있도록 설정
    - item
        - 이미지와 이름, 가격이 나올 수 있는 박스
        - overflow : hidden 을 이용하여 박스 사이즈보다 커진 부분에 대하여 보이지 않게 설정
        - position : relative 를 이용하여 이미지, 이름, 가격 박스를 합칠 수 있게 기준 설정
    - imgBox
        - item 박스의 가로 세로 사이즈에 맞추기 위하여 width와 height를 100%로 설정
        - 가장 앞에 나올 수 있도록 z-index : 1설정해줌 (z-index의 기본값은 auto로 꼭 설정 안해도 됨)
    - imgBox img
        - 이미지로 itmBox의 사이즈에 맞추기 위하여 width와 height를 100%로 설정
        - object-fit : cover를 통해 사진이 해당 사이즈에 맞추기 위해 찌그러지는 것을 방지
    - textBox
        - item 박스의 가로 세로 사이즈에 맞추기 위하여 width와 height를 100%로 설정
        - position: absolute, top:0, left:0 => imgBox와 겹치기 위해 설정
        - display : flex, flex-direction:column => 이름과 가격을 위아래로 배치 시키기 위해 설정
    - textBox__name
        - transform : translateY(50px) => y축 방향으로 50px 이동시키기 위해 설정
        - opacity : 0 => 투명도 0 => 마우스오버했을 때 투명도 1 만들어 안보이다가 보이게 설정하기 위함
    - textBox__price
        - transform : translateY(50px) => y축 방향으로 50px 이동시키기 위해 설정
        - opacity : 0 => 투명도 0 => 마우스오버했을 때 투명도 1 만들어 안보이다가 보이게 설정하기 위함
    - .item:after
        - 가상선택자로 content가 입력되어야 해서 content:""입력
        - display : block => 
        - position: absolute, top:0, left:0 => imgBox와 겹치기 위해 설정
    - hover
        - imgBox img
            - transform : scale(1.1) => 이미지를 1.1배 크게 만듦
            - filter : blur(3px) => 이미지 블러 처리
        - textBox__name, textBox__price
            - opacity : 1 => 투명도 0에서 1로 바꿔 글이 안보이다가 보이게 바뀜
            - transform : translateY(0) => y축을 0으로 바꿔 위에서 설정한 translateY(50)으로 변경되며 위로 올라가는 형식으로 보이게 만듦
    - transition
        - item:after, itemBox img, texBox__name, textBox__price
            - 설정해준 대로 자연스럽게 연결시킴
        - textBox__price
            - delay를 통해 다른 transition보다 조금 늦게 반응하도록 만듦

    [쇼핑몰 화면 - card]

    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/myshop-card.gif" width="600"/>
    
### Day 13
- animation 
    - animation : 연속되는 여러 이미지를 연결해서 자연스럽게 움직이는 것처럼 보이게 만드는 기법
    - css를 이용해서 animation을 만드는 방법
        - transition 속성 사용
        - animation 속성과 keyframe 활용
    - transition vs animation
        - transition 
            - 특정한 이벤트를 기점으로 작동
            - transition으로 만들 수 있는 것은 animation보다 transition 사용
            - hover, click 등
        - animation
            - 시작하기 위한 이벤트 필요 x
            - transition으로 만들 수 없는 경우에만 animation, keyframes 사용
            - 시작, 정지, 반복까지 제어 가능
    - animation 속성
        - @keyframes로 애니메이션을 정의하고, 정의한 애니메이션을 불러와서 제어해주어야 함
        - 하나의 동작을 만들기 위해 keyframe속성과 애니메이션의 속성을 제어해줘야 함

- @keyframes
    - CSS 애니메이션의 시작, 중간, 끝 등의 중간상태를 정의함
    
            @keyframes moveRight{
                from{
                    left: 0;
                }
                to{
                    left: 200px;
                }
            }
    - moveRight : 애니메이션 이름
    - from : 시작 시점의 css
    - to : 종료 시점의 css
    - from, to 대신 진행도 (%) 표기 가능
    - 진행도로 표기할 경우 0%, 50%, 100%로 중간지점 추가도 가능

- animation 속성들
    - animation-name
        - 어떤 keyframes를 요소에 적용할 것인지 지정

                animation-name : moveRight

    - animation-duration
        - 애니메이션을 한번 재생하는데 걸리는 시간 설정

                animation-duration: 2s

    - animation-direction
        - 애니메이션 재생 방향 정의(정방향/ 역방향)
        - 기본값 : normal => 정방향 재생
        - reverse : 역방향 재생
        - alternate: 정방향 재생 + 반복 시 정방향, 역방향 번갈아 재생
        - alternate-reverse : 역방향 재생 + 반복 시 역방향, 정방향 번갈아 재생

                animation-direction:alternate
    
    - animation-iteration-count
        - 애니메이션 재생 횟수 정의
        - 기본값 : 0
        - infinite => 무한반복
        - 원하는 횟수 숫자로 입력해주면 됨

                animation-iteration-count : infinite | 3
    
    - animation-timing-function
        - 애니메이션 재생 패선 정의
        - transition-timing-function과 유사함

                animation-timing-function : ease-in-out
    
    - animation-delay
        - 애니메이션 시작을 얼마나 지연할 지 설정

                animation-delay : 4s

    - animation 단축속성
        - name duration timing-function delay iteration-count direction 순서

                animation : moveRight 0.4s linear 1s infinite alternate

### Day 14
- grid 레이아웃
    - flex 레이아웃과 grid 레이아웃을 상황에 따라 혼용함
    - flex 
        - 1차원적 구조로 row 혹은 column 방향 중 택 1 해야 함
        - 여러 줄로 나눠야 할 경우 1차원적 구조로 만들어진 flex를 다단으로 중첩시켜 만들어야 함
    - grid
        - 2차원적 구조
        - 동시에 row, column 설정 가능

- grid 속성
    - 요소의 속성을 grid로 변경

            display : grid

    - grid-template-rows
        - grid의 행의 개수 및 크기를 지정할 수 있음
        - 행: 총 3개
        - 각 행은 1fr(분수), 2fr, 200px로 규정되어 있음

                grid-template-rows : 1fr 2fr 200px

    - grid-template-column
        - grid의 열의 개수 및 크기를 지정할 수 있음
        - 열: 총 3개
        - 각 열은 1fr(분수), 2fr, 1fr, 1fr로 규정되어 있음 => 1:2:1:1 비율로 나눔을 이야기함

                grid-template-rows : 1fr 2fr 1fr 1fr

    - repeat(a,b)
        - grid-template에서 사용할 수 있는 반복 함수
        - b 규격의 grid-template을 a개 생성함

            [예시 1번]
                grid-template-columns:repeat(4, 1fr)

            [예시 1번과 같은 내용]

                grid-template-columns : 1fr 1fr 1fr 1fr 

            [예시 2번]
                grid-template-columns:3fr repeat(2, 1fr 200px)

            [예시 2번과 같은 내용]

                grid-template-columns : 3fr 1fr 200px 1fr 200px
    
    - grid-column / grid-row
        - grid-item이 얼마만큼의 영역을 차지할 지 정의 함
        - grid-column : grid-line의 번호 기준으로 영역 할당
        - grid-row : grid-number의 번호 기준으로 영역 할당

                grid-column: 1/3

                => grid-line 1번에서 3번
    
    
    [grid layout column, row 설정]    
        <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/grid-layout.gif" width="600"/>


### Day 15
- flex 레이아웃을 이용하여 만들었던 쇼핑몰 카드 화면을 grid 레이아웃으로 바꿔보기

- flex와 grid의 차이점
    - flex
        - 비교적 작은 단위의 레이아웃 구성에 적합
        - 작업 유동성이 높기 때문에 디자인이나 기획이 확실하게 잡히지 않아 변경 가능성이 있는 경우에 적합
    - grid
        - 큰 규모의 레이아웃 구성에 적합
        - 레이아웃 구조가 확실하게 잡혀있는 경우, 효율적으로 반응형 디자인을 구현할 수 있음
        - 상대적으로 최신 기술이기 때문에 모든 브라우저에서 지원하지 않음
    
### Day 16
- 반응형 웹
    - 다양한 크기의 디바이스에 맞춰 보이는 화면이 달라지는 웹페이지를 의미함

- 미디어 쿼리
    - 뷰포트의 너비에 따라 웹 사이트의 스타일 시트를 수정할 수 있음
    - 뷰포트의 너비 이외에도 단말기의 종류, 해상도 등을 기준으로 설정할 수 있음

            @media screen and (max-width:500px) {
                // 스크린의 viewport 너비가 500px 이하일 경우
                // 적용시킬 스타일 시트
            }
        <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/media-query.gif" width="600"/>


- breakPoint
    - viewport : 실제로 웹페이지의 컨텐츠가 차지하는 영역
    - 반응형 웹사이트 작업의 기준이 되는 중단점을 말함
    - pc / 태블릿 / 모바일의 기준이 되는 규격 분기를 말함
        <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/breakpoint.jpg" width="400"/>
        <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/break-point.gif" width="600"/>
    
- 반응형 웹에 자주 쓰이는 속성
    - max-width / max-height
        - 요소의 최대 크기 지정하는 속성
    - max-width / max-height
        - 요소의 최소 크기 지정하는 속성
    - max()
        - 소괄호 안에 입력된 값 중 제일 높은 값을 속성값으로 출력하는 함수
        - 소괄호 안에는 여러 개의 콤마로 연결해 입력해 줄 수 있음
    - min()
        - 소괄호 안에 입력된 값 중 제일 낮은 값을 속성값으로 출력하는 함수
        - 소괄호 안에는 여러 개의 콤마로 연결해 입력해 줄 수 있음

<hr>

## Class 03 JavaScript
### Day 01
- JavaScript에서 많이 쓰이게 될 명령어
    - console.log()
        - ()안에 출력하고 싶은 내용을 입력해주면 됨 
        
                console.log(1) 
                =>1 출력됨

        - 기본적인 사칙연산 가능 
        
                console.log(10 + 20) 
                => 30 이 출력됨

- 변수
    - 데이터를 담아주는 상자
    - 변수 선언 키워드
        - var
            - 자주 사용하지 않음
        - let
            - let 변수명 ;

                    let box;
        - const
    - 변수명은 명시적이어야 함
    - 할당
        - 할당 연산자(=)를 이용하여 데이터를 변수에 할당해줌
        - box 변수에 할당해주기

                box = 123;
    - 선언과 할당은 동시에 할 수도 있음

            let box = 123;

### Day 02
- 재할당
    - 이미 데이터가 할당되어 있는 변수에 다시 할당하는 것

            let box;
            box = 1;
            console.log(box);
            box = 5;
            console.log(box);

            출력내용
            => 1
            => 5 

    - let 재할당 가능
    - const 재할당 불가능

- 재선언
    - 이미 선언되어 있는 변수명으로 다시 선언 시도하는 것

            let box;
            let box;

            출력 내용
            => Uncaught SyntaxError: Identifier 'box' has already been declared

    - let 재선언 불가능
    - const 재선언 불가능


### Day 03
- 예약어
    - 변수로 선언 불가능
        - 변수 선언 시 첫글자는 숫자 사용 불가능
    - 예약어 종류 아래 예시보다 더 많은 예약어들이 있음
        - new
        - else
        - do
        - if
        - break
        - case
        - finally
        - catch
        - this

- 데이터 타입(자료형)
    - string
        - 문자열
        - "", ''안에 입력된 데이터
        - 연산기호 '+' 사용 가능
    - int
        - 숫자형
        - 여러가지 연산이 가능한 산술 연산자의 사용 가능
    - 혼합연산
        - 문자타입과 숫자타입에서 공통으로 사용할 수 있는 산술 연산자 -> '+'

                "문자 타입" + 10

                => 문자 타입10
    - 이외의 데이터 타입
        - boolean
        - undefined
        - null
        - symbol
        - bigint
        - object

- 배열
    - 데이터를 담아두고 접근하는 '상자'로 변수, 상수 사용
    - 데이터들이 많을 경우 변수와 상수 여러개를 담을 '저장창고' 필요
    - 저장창고의 역할을 하는 것 = 배열
    - 배열 만들기
        - 대괄호 [] 사용

                let makeArr = ["a", "b", "c", "d"]
    - 인덱스
        - 배열의 요소에 순서를 부여하며 해당 요소에 접근이 가능하도록 해줌
        - 0부터 시작함

                makeArr[1] => b
                makeArr[3] => d
    - 배열의 길이
        - length
        - 배열 내 요소의 개수를 알려주는 역할
        - 인덱스와 다르게 1부터 count 됨

                makeArr.length => 4

- 배열의 메소드
    - 메서드 : 어떠한 기능을 가지고 있는 명령어로 배열의 메서드(메소드)는 배열에 내장되어 있는 기능임
        - 
        <a href="https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Array#%EC%A0%95%EC%A0%81_%EB%A9%94%EC%84%9C%EB%93%9C" target="_blank">메서드 확인할 수 있는 페이지</a>
    - push
        - 배열의 가장 뒤의 데이터를 추가
        
                makeArr.push(추가할 데이터)
    - pop
        - 배열의 가장 뒤의 데이터를 삭제
        - push와 다르게 괄호안에 데이터를 넣지 않아도 됨

                makeArr.pop()
    - includes
        - 특정 배열에 주어진 데이터가 포함되어 있는지 확인
        - 포함되어 있는지에 따라 boolean값을 반환함

                makeArr.includes("d")
                => true
    - indexOf
        - 특정 배열에서 지정된 요소를 찾을 수 있는 첫번째 인덱스를 반환
        - 찾을 수 없으면 -1을 반환함

                makeArr.indexOf("c")
                => 2

### Day 04
- 객체
    - 중괄호 이용({})하여 만듦

            let userData = {
                name:"김지현",
                age:28,
                hight:160,
                company:"abcCompany"
            }
    - key : value의 구성으로 되어 있고 하나의 key와 value를 property라고 함

- 객체 프로퍼티에 접근하기
    - 점표기법 (Dot notation)
        - key값에 접근시 점을 이용해서 접근하는 방법

                userData.name => "김지현"
    - 괄호 표기법 (Bracket notation)
        - key 값에 접근 시 괄호[]를 이용해서 접근하는 방법

                userData["name"] => "김지현"
        - 괄호표기법 사용시 "" 붙이지 않으면 key값이 아닌 변수로 인식되기 때문에 주의가 필요함

- 객체 Method
    - key
        - 객체의 key만 가져와 배열에 담아주는 메서드

                Object.keys(userData)
                => ["name", "age", "hight", "company"]
    - value
        - 객체의 value만 가져와 배열에 담아주는 메서드

                Object.values(userDate)
                => ["김지현", "28", "160", "abcCompany"]

### Day 05
- HTML의 기초
    - head/ body
    - div, span, input, button태그를 다시 한번 확인함
    - style 을 body에서 직접 태그에 사용하여 글자 색 변경
    - head 에서 script를 활용하여 콘솔 창에 원하는 문구 출력

### Day 06
- 함수 선언과 호출
    - 함수 선언

            const consoleTool = function (){
                console.log("함수를 실행했어요")
            }
    
    - 함수 호출
    
            consoleTool()

- document.querySelector()
    - 원하는 태그를 불러올 수 있음
    - 한 태그가 여러개 사용될 경우 #아이디와 .클래스를 이용하여 구분 할 수 있음
    - document.querySelector('#target-year-input') 사용 시 target-year-input 아이디를 사용하고 있는 태그 자체를 불러옴
        - 불러오는 결과값 : input id = "target-year-input" class="target-input
    - 해당 태그의 값(value)을 출력해야할 때
        - document.querySelector()뒤에 .value 입력해주면 됨
        
                document.querySelector().value
        - document.querySelector('#target-year-input').value
            - target-year-input 아이디를 사용하고 있는 태그에 입력된 값을 불러올 수 있음

- new Date()
    - 날짜 데이터를 일종의 객체로 관리하며 이 날짜 데이터를 가지고 올 수 있는 방법
    - new Date 사용 시 사용자의 컴퓨터 시간을 기준으로 현재 날짜, 시간을 모두 구해올 수 있음

- 함수의 반환
    - return
    - 결과값을 반환해줌
    - 함수 종료의 기능을 가지고 있기도 함

- 함수 선언의 종류
    - 표현식
        - 변수에 함수를 할당하는 것으로 표현
        - 호이스팅 영향 받지 않음 => 함수 선언 전 함수가 사용된 경우 error 발생 => 표현식을 사용하는 것이 좋음

                const 함수이름 = function(param1, param2, ...) {
                    // 
                    return 결과값
                }
    - 선언문
        - 선언 키워드 존재 x
        - 호이스팅의 영향을 받게 됨
        - 호이스팅 = 위로 끌어올려지는 것 => 함수 선언 전 함수가 사용된 경우 아래 선언된 함수를 예측하여 사용

                function 함수이름(param1, param2, ...) {
                    //
                    return 결과값
                }
    - 화살표 함수
        - 표현식과 비슷하게 생김
        - 표현식과 다르게 function이 없고 => 사용됨
        - 메서드에서 사용할 경우 많이 사용됨

                const sum = () => {
                    let result = 10 + 10;
                    return result;
                }

- local host
    - 사용자의 컴퓨터 자체를 가리키는 ip 주소의 도메인
    - local host = 도메인
    - 127.0.0.1 = ip 주소
    - local host === 127.0.0.1
    - DNS = Domain Name System 으로 아이피주소를 도메인으로 변경시켜주는 것
    - localhost:5500 -> :5500 = 포트번호로 live server가 사용하기 위해 설정해놓은 포트번호
    - 식당 위치를 말할 때 식당 이름을 이야기 하는 것 => 도메인으로 말하는 것
    - 식당 위치를 말할 때 식당 주소를 이야기 하는 것 => ip주소로 말하는 것
    - 5500이라는 식당 문을 live server가 열어놓은 것을 의미함

- 비교연산자
    - 자바스크립트의 데이터를 서로 비교
    - 느슨한 비교 연산자와 엄격한 비교 연산자가 있음
    - 실무에서는 엄격한 비교 연산자만을 사용함
    - 느슨한 비교 연산자
        - ==
        - 데이터 값은 비교하지만 타입은 비교하지 않음
        - 문자열 1과 숫자 1은 엄격히 구분되어야 하는데 느슨한 비교 연산자를 사용할 경우 같다는 결과가 나옴

                1 == '1'
                => true

    - 엄격한 비교 연산자
        - ===
        - 데이터 값과 타입 모두 비교함
        - 문자열 1과 숫자 1을 다른 것으로 인식함

                1 === '1'
                => false

### Day 07
- 배열과 객체의 비교
    - 원시타입
        - Primitive type
        - String, Number, Boolean, Bigint, undefined, Symbol, Null => 데이터타입
        - 불변성 => 데이터 변화하지 않음

    - 참조타입
        - Reference type
        - 원시타입 이외의 모든 것

                let arr = [1, 2, 3]

                arr === [1, 2, 3] => false
                주소값까지 비교하기 때문에 false가 나옴

- 조건문
    - 로직의 실행조건
    - if 문
        - 데이터가 특정조건에 해당하는 경우 작성한 코드 진행 해당하지 않을 경우 코드 진행하지 않음
        - if(조건식 입력) {조건이 성립(true를 return 하는 경우)하면 실행되는 코드}
        
                let name = "Jason"
                if(name === "Jason") {
                    console.log("Hi, Jason")
                }
    - else if 
        - if문에서 true에 해당하지 않은 경우

                const obj = {
                    name: "Peter",
                    age : 25
                }
                if(obj.name === "Jason") {
                    console.log("안녕, " + obj.name)
                }
                else if(obj.name === 'Peter'){
                    console.log('안녕, ' + obj.name)
                }
                else{
                    console.log('you are not a member!')
                }

- 논리 연산자
    - And 연산자
        - &&
        - 양쪽에 위치한 조건을 모두 만족하는 경우 true
    
    - Or 연산자
        - ||
        - 양쪽에 위치한 조건 중, 하나라도 만족하는 경우 true
    
    - NOT 연산자
        - !
        - boolean의 값을 반전시켜주는 논리 연산자
        - false(거짓)과 같은 것으로 치는 값
            - undefined
            - null
            - 0
            - ""
            - NaN

### Day 08
- 반복문
    - 반복적인 코드의 양을 획기적으로 압축
    - for문
        - 예시

                for(let i = 0; i< 10; i = i + 1) {
                    console.loe(i)
                }

                => 0~9까지 출력됨

        - 최초식
            - 반복문에서 반복의 기준이 됨
            - 반복문 안에서만 적용됨

                    let i = 0;

        - 조건식
            - 해당 조건인 경우 계속해서 로직을 반복 실행

                    i < 10;
        - 증감문
            - 반복해줄 로직을 끝날때 마다 증감문 반복됨
            - 로직이 끝날 때 i(0)가 증감문을 만나 i가 1로 재할당됨
            - i가 계속 재할당되다가 10보다 작지 않은 경우가 되면 반복문이 종료됨
            
                    i = i + 1

        - 11_D-day-Counter-repetition 코드 복습

                // 남은 시간을 계산한 날짜, 시간, 분, 초를 모아놓은 객체
                const remainingObj = {
                    remainingDate: Math.floor(remaining / 3600 / 24),
                    remainingHours: Math.floor(remaining / 3600) % 24,
                    remainingMin: Math.floor(remaining / 60) % 60,
                    remainingSec: Math.floor(remaining) % 60
                }
                -> 객체 사용 안할 경우 각각 변수로 설정해 줘야함

                // 해당 아이디값을 가지고 있는 태그들을 모아놓은 객체
                const documentObj = {
                    days : document.getElementById('days'),
                    hours : document.querySelector('#hours'),
                    min : document.querySelector('#min'),
                    sec : document.querySelector('#sec')
                }
                -> 객체 사용 안할 경우 각각 변수로 설정해 줘야함

                // 남은시간을 모아놓은 객체의 key값에 대한 변수 설정
                const timeKeys = Object.keys(remainingObj)

                // 태그를 모아놓은 객체의 key값에 대한 변수 설정
                const docKeys = Object.keys(documentObj)

                // 태그에 시간을 넣는 반복문
                for(let i = 0; i < timeKeys.length; i = i + 1){
                    documentObj[docKeys[i]].textContent = remainingObj[timeKeys[i]]
                }

                // 반복문 사용 안 할 경우 태그에 시간을 넣는 방법
                documentObj['days'].textContent = remainingObj.remainingDate;
                documentObj['hours'].textContent = remainingObj.remainingHours;
                documentObj['min'].textContent = remainingObj.remainingMin;
                documentObj['sec'].textContent = remainingObj.remainingSec;

    - while 문
        - 종료조건을 제대로 설정하지 않으면 무한 반복됨
        - 예시

                let i = 0;

                while (i<10){
                    console.log(i)
                    i = i + 1
                }

                => 0 ~ 10이 출력됨

                let i = 0;
                let status = true

                while(status === true){
                    console.log(i)

                    if (i>10){
                        status = false
                    }

                    i = i + 1
                }
        
        - 최초식
            - for문과 다르게 최초식이 while문 밖에 위치함

                    let i = 0
        
        - 조건식
            - 괄호 안에 위치함

                    i < 10

        - 증감문
            - 코드 안에 위치함

                    i = i + 1
    
    - for in
        - 객체에서 사용
        - 사용할 객체 안에 있는 키들을 변수명(key)으로 받아오겠다
        - for in 사용하기 전에는 객체를 하나하나 돌면서 key 값을 받아왔
        
                for (let key in 사용할 객체) {
                    console.log(key)
                }

- 시간반복
    - setTimeout()
        - for문을 활용하여 특정시간동안 반복되는 함수를 만들 수 있음

                for(let i = 0; i < 100; i++>){
                    setTimeout(() => {
                        counterMaker();
                    }, 1000*i)
                }
        - 1000 === 1000ms === 1s
        - 1000 * i 해주는 이유 : 1초씩 뒤에 해당 함수를 실행하기 위해서임
        - i가 100보다 작을때까지만 반복되는 문제점 발생

    - setInterval()
        - javaScript에 내장되어 있는 함수로 for문 없이 setTimeout처럼 시간간격을 두고 함수를 실행할 수 있도록 만듦
        
                setInterval(counterMaker, 1000);
        - 1초에 한번씩 해당 함수를 실행
        - 1초 뒤부터 해당 함수가 실행되기 때문에 countdown 할 때 0부터 나오는 문제가 발생함
            - 해당함수를 먼저 한번 실행하여 0부터 나오는 문제 해결

    - clearInterval()
        - 새로고침버튼을 눌러야 타이머가 종료됨
        - clearInterval 활용하여 타이머를 종료시킬 수 있음
        - 버튼을 누를때마다 숫자가 1에서부터 늘어나는 것을 확인함
            - intervalId 변수로 숫자를 확인해봄
        - 숫자가 계속 늘어나는데 숫자만큼 clearInterval을 실행해줘야 타이머가 멈추는 것도 확인함
            - intervalId를 넣을 배열이 필요함
            - intervalIdArr 변수를 이용하여 해당 숫자를 대입해줌(intervalId 만들어 내는 함수에서)
                - 문제발생
                    - clearInterval()함수에서 해당 배열을 가지고 오지 못함
                    - push를 이용하였지만 해당 배열에 값이 계속 1개만 추가됨을 확인함
                - 원인
                    - 지역변수로 intervalIdArr을 설정하였기 때문에 다른 함수인 clearInterval에서는 해당 배열의 존재를 알지 못함
                    - 버튼을 누를때마다 intervalIdArr을 새로 설정하였기 때문에 계속 reset이 되고 있었음
                - 해결
                    - 전역변수로 intervalIdArr을 설정해줌으로써 위 두개의 문제를 동시에 해결할 수 있음

## Day 09
- 전달인자, 매개변수
    - 함수의 외부에서 데이터를 전달받아 내부에서 활용하기 위한 수단
    
- 매개변수
    - parameter
    - 함수를 선언할 때 소괄호 안에 정의되는 변수

            const sum = function(a, b) {
                console.log(a)
                console.log(b)
            }

            sum() => undefined
                     undefined 출력

            const sum2 = function(a, b) {
                let result = a + b;
                return result;
            }

- 전달인자
    - arguments
    - 함수를 호출할 때, 함수 내부로 전달되는 데이터

            sum(10) => 10
                       undefined 출력
            
            sum(10, 20) => 10
                           20 출력

            sum2(10, 20) => 30
    
- Web Storage
    - 브라우저 내에 존재하는 데이터 저장소
    - Session Storage
        - key-value 형태 저장
        - 로컬 환경에 데이터 저장
        - 세션 단위로 구분되며 활용
            - 세션 : 사용자가 브라우저를 통해 웹페이지에 접속한 시점부터 해당 웹페이지 접속을 종료하는 시점까지 의미하는 단위
            - 세션 : 사용자의 웹페이지 접속 상태에 따른 단위
        - 브라우저, 탭을 종료하면 영구 삭제됨
    
    - Local Storage
        - key-value 형태 저장
        - 로컬 환경에 데이터 저장
        - 도메인 단위로 구분되며 활용
        - 브라우저 자체를 종료해도 존재함

- local storage 접근 방법
    - local storage에 데이터 저장 : localStorage.setItem('key', value)
    - local storage에 저장되어 있는 데이터 접근 : localStorage.getItem('key')
    - local storage에 저장되어 있는 데이터 삭제 : localStorage.removeItem('key')

    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/d-day-counter.gif" width="600"/>

- ul/ol/li 태그
    - ul 태그
        - unordered list
        - 순서가 없는 목록
        - 검은 점으로 항목들을 표현함
        - ul태그만을 작성하면 목록이 출력되지 않음 => li태그와 함께 사용해야함

                <ol>
                    <li>항목</li>
                    <li>항목</li>
                    <li>항목</li>
                </ol>
            
            <ol>
            <li>항목</li>
            <li>항목</li>
            <li>항목</li>
            </ol>

    - ol 태그
        - ordered list
        - 순서가 정해진 목록
        - 숫자에 항목들을 할당해서 나열
        - ol태그만을 작성하면 목록이 출력되지 않음 => li 태그와 함께 사용해야함

                <ol>
                    <li>1번 항목</li>
                    <li>2번 항목</li>
                    <li>3번 항목</li>
                </ol>
        
        <ol>
        <li>1번 항목</li>
        <li>2번 항목</li>
        <li>3번 항목</li>
        </ol>

- DOM
    - Document Object Model
    - 브라우저가 HTML 문서를 파싱(해석)하는 과정에서 생겨나는 객체
    - 트리구조를 가짐

            console.dir(document.childNodes[].childNodes)
            => 자식 노드의 자식노드 등으로 찾아 내려갈 수 있음

    <img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/dom.png" width="600"/>

### Day 10
<img src="https://raw.githubusercontent.com/kimjihyeon-angela/pp04_Study_html-css-java/main/image/Todo-List.gif" width="600"/>

### Day 11
- 스코프
    - 변수 참조의 유효범위
    - 전역 스코프
        - global scope
        - 전체

                let x = 0;
                let y = 1;
                const scopeTest = function () {
                    let z = 2;
                    console.log(x);
                    console.log(y);
                    console.log(z);
                    => x, y, z의 값 0, 1, 2가 다 출력됨
                }
                console.log(x);
                console.log(y);
                console.log(z);
                => x, y의 값 0, 1은 출력되지만 z는 undefined 에러 발생함


    - 지역 스코프
        - local scope
        - 함수 내, 특정 지역 내
        - 함수레벨 스코프
            - 함수를 실행할 때 생겨나는 지역 스코프

                    const sum = function () {
                        var x = 0;
                    }

                    console.log(x)

                    => undefined 출력됨

                    const sum2 = function() {
                        let x = 0;
                    }

                    console.log(x)

                    => undefined 에러 발생

        - 블록레벨 스코프
            - 코드 블록에 의해서 생성되는 스코프
            - if, for, while문 등 중괄호를 사용해서 코드 블록을 작성하는 환경에서 생성됨

                    if() {
                        var y = 0;
                    }

                    console.log(y)
                    
                    => 정상적으로 값(0)이 출력됨 => var사용 지양
                    
                    if() {
                        let y = 0;
                    }

                    console.log(y)
                    
                    => undefined 에러 발생

- 실행 컨텍스트
    - debugger 기능 사용시 각 함수에 의해 생성되는 변수, 변수의 호이스팅 등을 확인할 수 있는데 이때 해당 정보들을 담고 있는 것
    - 각 함수 실행될 때마다 고유한 실행 컨텍스트가 생성됨

- 호이스팅

        console.log(letKeyword)
        let letKeyword = 'let is safe'

        => letKeyword is not defined 에러 발생함

        console.log(varKeyword)
        var varKeyword = 'var is not safe'

        => undefined 출력됨

        fn1()

        function fn1() {
            console.log("hoisting occurred')
        }

        => hoisting occurred 출력됨

        fn2()
        const fn2 = function(){
            console.log("error occurred")
        }

        => fn2 is not defined 에러 발생함

    - 호이스팅 : 위로 끌어 올려지는 것처럼 동작하는 것
    - var 키워드의 경우 선언부가 위쪽으로 올라가서 해석이 됨 => 선언만하고 할당은 안되어 있기 때문에 undefined가 출력되는 것임
    - 변수만 호이스팅 발생하는 것 x => 함수도 호이스팅 발생함 (함수 선언식으로 정의된 경우)
    - 변수 선언 단계
        - 선언단계
            - 선언한 변수를 식별자가 담기는 객체에 할당하는 단계
        - 초기화 단계
            - 변수에 할당할 메모리 공간을 부여하는 단계
        - 할당 단계
            - 정의된 변수에 데이터가 할당되는 단계

### Day 12
- 호이스팅
    - let, const 는 선언단계, 초기화단계가 분리되어 실행됨
    - let, const가 호이스팅이 발생하지 않는 것은 아님
    - 선언 코드 만나기 전 참조 시도하면 에러 발생하는 이유
        - TDZ때문 
            - Temporal Dead Zone
            - 선언단계와 초기화 단계 사이에 존재
            - 초기화 단계를 거치기 전 TDZ공간에 머무르는 변수를 참조하려 시도하면 참조에러(Reference Error)발생
    - var 키워드의 경우 선언단계, 초기화단계가 함께 실행되기 때문에 TDZ존재하지 않음

- geoLocation
    - 현재 사용자의 위치값을 얻어올 수 있는 API
    - navigator.geolocation 객체를 통해 사용할 수 있음
    - 현재 위치 가져오는 방법 : getCurrentPosition()메서드 사용
    - position.coords 객체로 위도, 경도 등을 받아옴
    - 원하는 정보(위도, 경도)만 이용하기 위하여 새로운 객체를 이용하여 저장

- open Weather Map
    - open API 이용

- API
    - 어떠한 프로그램에서 제공하는 기능을 사용자가 활용할 수 있도록 만들어 둔 인터페이스

- http
    - Hyper Text Transfer Protocol
    - 서버와 클라이언트가 통신하기 위해 정의된 규약

### Day 13
- http
    - request Method
        - get : 서버의 데이터를 조회하는 Method (HTTP message에 요청 바디를 담아줄 수 없음)
        - post : 서버에 데이터를 등록하는 Method
        - put : 서버의 리소스를 Request body에 담긴 내용으로 수정하는 Method
        - patch : 서버 내 리소스의 일부를 수정하는 Method
        - delete : 서버 내 리소스를 삭제하는 Method
        - option : 서버에서 허용하는 Method의 목록을 알려주는 Method

    - 상태코드
        - http 통신을 통해 전달하는 상태 코드는 요청에 대한 응답의 결과를 세자리 번호로 나타내줌
        - 1XX : 요청을 정상적으로 받은 것을 응답, 계속해서 작업중임을 의미함
        - 2XX : 클라이언트의 요청을 수신, 승낙하였고, 정상적으로 요청이 수행될 것임을 의미함
        - 3XX : Redirection과 관련한 동작이 수행 되었을 때 돌려 받는 상태 코드
        - 4XX : 클라이언트가 보낸 요청이 잘못 되었음을 의미하는 상태 코드
        - 5XX : 서버에서 요청을 받아 로직을 수행하는 과정에서 문제가 생겻을 때 받게 되는 상태 코드

- 동기와 비동기
    - 동기 : 하나의 작업이 종료될 때까지 다음 동작은 기다리는 실행 방식

            1. 손님이 주문
            2. 앞선 손님의 주문에 대한 응답이 완료될 때까지 다음 손님은 아무런 동작을 할 수 없음
            3. 앞선 손님이 주문에 대한 응답을 받았다면 다음 손님이 주문 가능

    - 비동기 : 하나의 작업이 진행됨과 동시에 또 다른 작업도 함께 진행되는 것

            1. 손님이 주문
            2. 앞선 손님의 주문이 완료되는 동안 해당 손님은 옆 대기줄에서 본인의 주문이 완료될 때까지 대기
            3. 그와 동시에 다음 손님의 주문 진행
    
    - JavaScript의 경우 동기적으로 작동함
        - call stack, callback queue라는 영역으로 인해 비동기처럼 작동하기도 함

                console.log("1")

                setTimeout(() => {
                    console.log("2")
                }, 2000)

                console.log("3")

                => 코드 실행 시 1, 3이 먼저 출력된 후 2초 뒤 2가 출력됨을 볼 수 있음
        - 동기식으로 작동될 경우 1출력된 후 2초 후 2출력되고 3이 출력되어야 하는데 다르게 작동함

- 자료구조
    - 컴퓨터의 데이터를 효율적으로 관리하기 위해 만들어 놓은 데이터 관리 체계
    - stack
        - Last In First Out (LIFO)
        - 먼저 들어온 함수, 데이터가 가장 마지막에 처리되는 구조

    - queue
        - First In First Out (FIFO)
        - 먼저들어온 함수, 데이터가 가장 먼저 처리되는 구조

- call stack
    - 함수가 담겨지는 공간

            const func3 = function() {
                console.log("func3 call")
            }

            const func2 = function() {
                func3()
                console.log("func2 call")
            }

            const func1 = function() {
                func2()
                console.log("func1 call")
            }

            func1()

            => func3 call func2 call func1 call 순으로 출력됨

- callback queue
    - Web APIs(비동기 함수)
        - DOM
        - setTimeout()
        - setInterval()
    - 함수를 실행하는 도중에 콜백함수(Web APIs)가 호출된 경우
        - callback queue로 들어와서 call stack이 비워지기를 기다림
        - call stack에 들어있던 함수가 다 종료되면 callback queue에 있던 함수가 call stack으로 들어가짐

- Promise 객체
    - 비동기적으로 동작시켜줘야 함
    - 데이터를 현재 얻을 수 없지만 추후 작업이 완료되면 받아올 수 있는 데이터에 대한 접근 수단의 역할
    - 상태
        - pending(대기) : 비동기 처리가 아직 완료되지 않은 상태를 의미
        - fulfilled(이행) : 비동기 처리가 완료되어 결과값을 반환해준 상태
        - rejected(실패) : 비동기 처리가 실패 혹은 오류가 발생한 상태

- then, catch
    - then => 요청이 완료된 경우 익명함수 실행
    - then 뒤에 then을 이어서 사용하기 가능
    - catch => then이 실패한 경우 catch에서 작성한 익명함수 실행

### Day 14
- 구조분해할당
    - destructuring assignment
    - 구조화 되어 있는 배열, 객체와 같은 데이터를 destructuring(분해) 시켜 각각의 변수에 담는 것
    
            let arr = [1, 2, 3, 4, 5]

            let one = arr[0]
            let two = arr[1]

            console.log(one, two) => 1, 2

    - 배열 구조분해할당
        - 배열 선언
        - let [변수로 사용할 문자, 변수로 사용할 문자] = 배열

                let arr = [1, 2, 3]
                let [one, two] = arr

                console.log(one, two) => 1, 2
                console.log(arr) => [1, 2, 3]

    - 객체 구조분해할당
        - 객체 선언
        - let {변수로 사용할 문자, 변수로 사용할 문자} = 객체

                let obj = {
                    name:"otter",
                    gender:"male"
                }

                let {name, gender} = obj

                console.log(name, gender) => otter, male

- spread 연산자
    - 하나로 뭉쳐있는 값들의 집합을 전개해주는 연산자
    
            let arr = [1, 2, 3, 4, 5]

            console.log(arr) => [1, 2, 3, 4, 5]
            console.log(...arr) => 1, 2, 3, 4, 5
    
    - 문자열에서도 사용 가능

            let str = "Hello"
            
            console.log(...str) => "H""e""l""l""o"
    
### Day 15
- 얕은 복사
    - 주소값까지만 복사
    - 스프레드 연산자 활용하여 복사
    - 객체 안에 객체가 존재할 경우 제대로 복사되지 않는 문제점 발생

            let origin = {
                name : "otter",
                age : 25
            }

            let copy = origin
            origin.name => otter

            copy.name = "rabbit"

            origin.name => rabbit

- 깊은 복사
    - 실제 데이터까지 복사
    - JSON.stringify를 활용하여 JSON 형태(string으로 이루어져 있음)로 복사
    - 그 후 JSON.parse를 활용하여 원래 형태로 변환시켜 깊은 복사가 이루어짐
    

## Day 15
- rest parameter
    - 사용하지 않는 데이터를 제외하고 필요한 데이터만 변수에 담아서 사용할 수 있도록 만들어 줌
    - ...rest는 마지막에 사용해야 함
    - 무조건 ...rest일 필요는 없음 => 변수처럼 사용되기 때문에 다른 이름으로 해도 상관 없음
        - ...any와 같이 다른 이름으로 작성해도 상관 없음