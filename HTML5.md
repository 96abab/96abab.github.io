# HTML5 수업
=====================
<details>
<summary>click</summary>
<div markdown="1">


  1. [리눅스 명령어 정리](linux.md)

  2. [HTML수업](HTML5.md)

  3. [CSS수업](CSS.md)

</div>
</details>

<hr/>


# 2022-11-23
<br>
##http 등장 전 
<br>
논문을 text로 FTP server로 업로드하면 FTP client는 통신(protocol) 규칙에 따라 data를 송수신한다  
<br>
  
        단점
        - 논문이 참조하는 다른 논문을 다운로드 받기 번거롭다
        - 논문안에 다른 논문이 업로드된 서버 주소가 없다

##HTTP,HTML<br>
다른논문의 위치정보와 텍스트의 포맷을 지정 하고 그림,음성,동영상등을 삽입 

        <a href="">제목</a>   제목은 데이터고 명령어는 데이터를 설명하는 데이터 
        <img grc="a.gif">     

<br>

        {\rtf1\ansi\ansicpg949\deff0\nouicompat\deflang1033\deflangfe1042{\fonttbl{\f0\fnil\fcharset129 \'b8\'bc\'c0\'ba \'b0\'ed\'b5\'f1;}}
        {\colortbl ;\red255\green0\blue0;}
        {\*\generator Riched20 10.0.19041}\viewkind4\uc1 
        \pard\sa200\sl276\slmult1\b\f0\fs44\lang1042 ABC\'ba\'f1\'c6\'ae\'c4\'b7\'c7\'c1\b0\fs20\par  <-내용
        \par
        \cf1\i\'b3\'d7\'c0\'cc\'b9\'f6 \cf0\'c5\'ac\'b6\'f3\'bf\'ec\'b5\'e5sdfs\par
        \par
        \i0\lang18\par
        }    

<br>
##HTTP
<br>
HTML 문서를 원활하게 송수신하고 찾아가기 쉽게 만든 통신 프로토콜

        HTTPclient(web browser)
        -
        예)크롬,파이어폭스,엣지
        
        HTTPserver(web server)
        -
        예)NginX,apache

###HTTPS
-HTTP+보안

<hr>
<hr>

##과제 목표<br>
웹 기술의 등장 과정을 조사하여 설명하시오.
<br>
1) 어느 단체의 누가 어떤 목적으로 웹 기술을 만들었는지?
<br>
        WWW 은 유럽입자물리연구소라는 곳에서 여러 대학과 연구기관에서 일하는 물리학자들 사이에서 효율적이고 신속한 자료를 공유받기 위한 목적이었는데 1989년에 "팀 버너스리"에 의해 시작된 프로젝트였습니다.
<br>

2) 웹 기술의 처음 목적과 지금 활용되는 상황이 어떻게 다른지?
웹기술의 처음 목적 지금 적용된 상황 어떻게 다른지 설명 
<br>
        최초의 브라우저인 "월드와이드웹"은 웹 탐색(Browser)의 역할과 편집(Edit)의 역할을 같이 했으며 NeXTSTEP이라는(애플의 공동설립자인 스티브 잡스가 설립한 넥스트 사에서 개발한 객체지향형 운영체제) 플랫폼 위에서 동작한다고 합니다.

        웹브라우저는 위키처럼 다중 작성자의 환경(소셜 웹)을 뜻했는데 이후에 나오는 브라우저들은 편집의 역할을 빼고 탐색 기능만 제공하게 되어 본래 의도와 다르게 제공 되었다
        
        -웹 1.0이 인터넷을 통해 일방적으로 정보를 보여주었다
        
        -웹 2.0(Web 2.0)이란 개방, 참여, 공유의 정신을 바탕으로    사용자가 직접 정보를 생산하여 쌍방향으로 소통하는 웹 기술이다 또한
        웹 2.0이 데스크톱 컴퓨터의 응용 프로그램을 대체할 것으로 예견하고 있다
        최근에는 프로그래밍 단계의 웹 서비스뿐만이 아닌 UI를 통째로 사용할 수 있는 스크린 스크래핑 형태로도 웹 서비스를 사용한다

<br>
##web 기술의 활용 
<br>
        
        1세대
        -논문공유

        2세대 (webserver)
        -회사소개,제품소개,그림

        3세대 
        -방명록

        4세대
        -쇼핑몰+ MS ASP 프로그램,php

        5세대
        -단순 프로그램 -> 전문적인 app로 변화 -> app 관리 기능 강화 
        
        인사관리시스템,결제시스템 물류관리시스템,웹메일등

        -초창기 논문개시 현재 app개시
        
        ##CGI
        web server와 프로그램 사이에 데이터를 주고 받는 규칙 
<br>

web app 제작기술 
<br>

        -화면 만드는 기술 (front-end)
        html(콘텐트구성) + css(출력제어) + javascript(사용자의 액션에 응답,콘텐트를 제어)

        -데이터를 만드는 기술 (back-end)
        java,php,javascript,SQL

        -화면과 데이터를 둘다 만드는 기술 (full stack)
        
        SM(유지보수)/SI(시스템통합)

#HTML 기본구조
<br>

    <!DOCTYPE html> <- root엘리먼트

    엘리먼트(
    <html lang="en">  <-시작태그
    콘텐트(
        <head>  <- html의 자식 엘리먼트
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <meta http-equiv="X-UA-Compatible" content="ie=edge">
            <title>Document</title>
        </head>
    <body>

    </body>)
    </html>)

        시작태그와 끝태그를 사용
        <a></a>
        <P></P>
        <br><br>
        
        끝태그를 안써도 가능
        <br>
        <meta>

##HTML4 의 doctype

        <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
        "http://www.w3.org/TR/html4/strict.dtd">
        
        -위 해석
        루트엘리먼트 
        HTML
        
        문서의 규칙의 공개여부 
        PUBLIC
       
        공인시설 
        +-
        
        규칙을 만든 조직의 이름
        w3
        
        문서규칙 식별자 
        DTD
        
        문서규칙의 이름 
        HTML
        
        규칙의 언어 
        EN
        
        문서규칙을 정의한 DTD파일의URL  
        http://www.w3.org/TR/html4/strict.dtd
        
        DTD 는 old
        schema new


<br>
##XHTML은 끝태그 필수
<br>
<br>
##웹 퍼블리셔<br>
HTML,CSS,JAVAscript 을 활용한 단순 웹화면구성 
<br>
##FRONT-END<br>
HTML,CSS,JAVAscript  framework(vue.js)
<br>
##HTML 공부법
<br>

1. 예제 실행 따라해서 
2. 결과화면 확인
3. 태그 기능이해
4. 태그 경험해보기  

<br>
##알아보기<br>
meta name="viewport" content="width=device-width, initial-scale=1.0"

        meta ivewport태그
        
        -애플,아이폰,아이패드등 모바일 브라우저의 뷰포트를 크기 조절하기 위한 태그 w3c에
        표준이 아니지만 IOS장치가 널리 사용되면서 사실상 표준처럼 사용되고있다 

<br>
<br>
##data 와 메모리<br>
<br> 
bit에는 전기를 데이터로 바꿔 저장한다 이것을 사람은 0과1로 표현한다.
<br>
<br>
#data 저장
<br>
양수: 10진수->2진수 규칙을 그대로 적용 
        
    메모리 상태와 2진수 , 10진수 ,16진수

10진수를 2진수로 바꾸려면 힘들다 그래서 16진수로 표현하면 쉽다 
<br>
메모리상태를 직접적으로 보고싶다면 2진수<br>
문서의 간략히 적고 싶다면 16진수 
<br>
##UTF-8<br>
문자를 2진수로 표현하는 방식 중 하나

<hr>
<hr>

# 2022-11-24

##메모리 상태의 표기
<br>
        비트의 전기 상태를 2진수 표기법으로 표현하면 적합하다 (1은 전기가 있는상태 0은 전기가 없는 상태)
        
        -> 특정 비트들의 정확한 상태를 전달하고자 할때 사용한다 하지만 큰수를 표기하기에는 복잡하다 

        -16진수로 표현하면 표기를 단순화할 수 있다
<br>

##data를 메모리에 저장
<br>
        
        data를 2진수로 변환할 수 있다면 메모리에 저장할 수 있다
        -> 하지만 변환하려면 규칙이 있어야 한다 각 사람마다 정하는 규칙이 다르다면 서로 소통이 어려울수 있다

        -data (정수,실수,문자,그림,동영상,소리,빛,*냄새는아직 변환법이 없다)

<br>
##data 2진수 변환 규칙
<br>
<br>
###정수 
        
        1. sign-magnitude (*부동소수점의 가수부를 표현할때 사용)

        양수와 음수를 부호만 다르고 값은 같다 

                +24 -> 0001 1000
                -24 -> 1001 1000
        *문제점
        빼기 연산 결과가 일반적이지 않다 

        
        2. 1's complement

        ()의 보수란 
        ()로 만들기위한 수
        
        예) 9의보수
            8->1  옆에 1이 9의 보수
            5->4   // 4가 9의 보수
        
        현대의 컴퓨터는 음수를 표현할때 2의 보수를 사용한다

        
        4. Excess-k (k초과)
        부동소수점의  지수부를 표현할 때 사용

        정수 + K값 = 2진수
              (bias값)
               ㄴ> 메모리 비트수 -1 
                예) 8bit 2^(8-1) -1 = 128 -1 =127

###문자 

        1. ASCII (7bit) : 영어 알파벳 대.소 문자.숫자, 특수문자

        -7bit로 95자에대해 7bit 2진수 규칙을정함


        2.ISO-8859-1~n(국제표준) : ASCII + 유럽문자 + 남미문자

        - 8bit 사용
        - 한글 windows 기본 문자들 

        3. EUC-KR: 16bit로 한글문자 정의 
        
        ISO-8859-1(1byte) + 한글(2byte)

        똠,똡,똣은 정의되어 있지 않다 이러한 이유로 
        사용하기 불편하여 

        4. 조합형 한글 코드 (2byte)

        처음 컴퓨터가 한국에 보편적으로 도입되던 시기에 개발

         -모든 한글 표현 가능

                0=영어, 1= 한글(1bit) [1=한글]
                초성(5bit)            [01111=ㅉ]
                중성(5bit)            [00011=ㅏ]
                종성(5bit)            [10111=ㅇ]

        예) 1 01111 00011 10111  = 짱
        
        
        5.MS-949(CP949) 16bit
            ㄴ> EUC-KR + a 11172자
        
         -한글windowOS의 기본 규칙 
         
         -문자에 대해 2진수를 매칭한 규칙 
         "characterset" 문자 집합

          똥(문자) - B6CB(문자의 대해 정의된 2진수 규칙)

          *한글의 문자코드가 정렬되지 않은 단어가 있어 연속되지 않다

        7.unicode (2byte) 국제표준

         - 모든문자를 2byte로 정의한다 

           A-> 0041
           1-> 0031
           
           -영문자도 2byte로 메모리가 낭비되고 
           기존편집기에 사용 불가
           
           가-> AC00      한글을 EUC-KR 

         -한글의 모든 문자코드가 정렬되었다
         

        8. UTF-8 국제표준

         - 기존의 편집기에서도 영어를 읽고 쓸수 있도록 만들었다

         - 7bit로 정의해서 쓰던 문자를 그대로 계속 8bit 사용
         예)ASCII 문자코드

         -그 외 문자는 규칙에 따라 2~4byte로 변환
         예) 한글 2byte -> 3byte 변환 되었다 한글은 오히려 손해

                '가' 변환

                unicode2(utf-16) AC00 -> 1010 1100 0000 0000
                
                utf-8  EAB080 -> 1110 1010 1011 0000 1000 0000
         

         -Universal Coded Character Set + Transformation Format – 8-bit 

##색상


        R(bit)          G(8bit)           B(8bit)
        
        00                //                 // 
        ~                 //                 //
        ff                //                 //

        -빛의 밝기

##encoding

-문자를 문자코드로 2진수를 이용해 변환 하는것을 encoding(코드화 하다)이라고 한다 

-코드를 다른형식으로 변환 하는것도 encoding (예) 압축,암호화) 이라 부른다 
이를 되돌리는것을 decoding (예) 압축풀기 , 복호화)

        -URL encoding /decoding  =  percent encoding /decoding
        url에서 특수 목적(예약어)으로 사용하는 문자 를 reserved keyword 라고한다 
        데이터를 표현하는 용도로 사용할 수 없다 특정 형식에 맞게 변환해야한다


        예약어 와 비예약어
        -예약어는 변환해야하는 문자 비예약어는 변화할 필요가 없는 문자 

        encoding 예) 
                  (!) -> (%21) 
         16진수로  (21)    (25 32 31)
                
                (+) -> (%2B)
                (2B)     (25 33 46)

                (space) -> (+)
                (20)       (2B)

                '가' -> % EA % BO % 80
                (EA 30 30)    (25 45 41 25 42 45 25 38 30)
        
        숫자2는 2 의 보수  -> 0000 0010
        문자 "2" 는 ISO-8859-1 -> 0011 0010

        urldecoding 

        데이터를 입력하면 webbrowser가 자동으로 urlencoding을 수행 하여 webserver에서 자동으로 urldecoding 수행

##영상 data와 인코딩/디코딩

        인코딩

        -영상 데이터가 너무 커서 특별한 수학공식 알고리즘을 통해 압축하여 mp3.mp4.avi로 만든다 

        디코딩

        -mp3,avi등을 소리와 영상으로 되돌리는 것 


        영상을 주고 받을때 인코딩 기능과 디코딩 기능이 있어야한다

#web 기술
 - html 사용

        <title>
        <h1>
        <p>
        <style>
        <hr>  수평선
        <br>  
        <b>
        <i>
        <small>
        <sub>
        <sup>
        <ins>
        <img src="Penguins.jpg" alt="펭귄" width="300" />
        <img src="" alt="그림이 존재하지 않습니다." width="300" />
        src= 파일이 내부에 있을때 파일명만, alt= 시각장애인을 위한 기능 
        <ruby>
        <span>大韓民國</span>
        <rt>대한민국</rt>
        </ruby>
        <audio>
        <video poster>
        <oi>
        <li>
        <ul>
        <dt>
        <dd>
        <dl>
        <th>
        <colgroup>
        <caption>
        <table>
        <th>
        <tr>
        <td>
        <input type="text" name="search" />
        <input type="radio" name="cf" />짜장면<br /> 여러가지 사용시 이름을 통일시켜 하나만 선택할수 있게 한다 기본 선택으로 하고싶다면 checkde를 넣어주면 가능하다
        <label for="username">이름</label>
        <input type="text" id="title"/>
        <input type="text" id="username" />
        <input type="color" /><br />
        <input type="date" /><br />
        <input type="datetime" /><br />
        <input type="datetime-local" /><br />
        <input type="email" /><br />
        <input type="month" /><br />
        <input type="number" /><br />
        <input type="range" /><br />
        <input type="search" /><br />
        <input type="tel" /><br />
        <input type="time" /><br />
        <input type="url" /><br />
        <input type="week" />
        <input type="submit">
        <input type="text" value="coco">
        <textarea>............</textarea>
        <select multiple size="5">
        <option>김밥</option>
        <option>떡볶이</option>
        <option>순대</option>
        <option>오뎅</option>
        </select>
        <optgroup label="CSS3">
        <option>Animation</option>
        <option>3D Transform</option>



        https://via.placeholder.com/300x200  더미 이미지 

        controls,selected,checked,readonly
        -속성중 값에 상관없이 존재 유무로 기능을 수행하는 속성이 있다

##CR/LF -> line feed

carrage return
-예전에 타자기에서 줄 바꾸는 것을 모방하여 만든 코드 값

        CR->0x0D
        LF->0c0A

        windowsOS-> 줄바꿈을 표시할때 CRLE 2byte 를 붙인다
        linux ->                      LF 1byte만 사용한다


##tag 와 attribute

  <a href=""> </a>
     

##CSS

        1. <style> 태그  

        <style>
        .
        .
        .
        </style>

        2. inline 스타일

        <tfoot style="CSS코드넣기">..<tfoot>
                ㄴ(inline style)

        
        3. 외부 css파일 

        외부html 파일에서 css내용 공유

##MIME TYPE

        multi-purpose
        internet
        mail
        Extensions

        메일에 첨부한 콘텐트가 어떤 형식인지 상대편에게 알려주는 용도
        -> 현재는 메일뿐 아니라 웹등 여러 곳에서 사용

<hr>

#시맨틱 태그의 목적과 주요 시맨틱 태그의 용도를 기술하시오.
과제 목표

        1. 시맨틱 태그의 목적?

                -HTML5 이전에는 구조를 구분하기 위하여 div태그에 id 또는 클래스 등으로 구분하며 구조를 설계했으나
                인터넷이 발전하면서 웹문서의 양이 많아지고 각자 생성 양식이 달라 원하는 문서를 찾기 점점 힘들어지게 되었다
                
                div 태그와 같이 block element이면서 사이트의 구조를 설계하고 태그에 의미를 부여 하여 사이트의 구조를 파악하
                기 편하게 만들어주어 좀더 명시적이고 직관적으로 설계할 수 있다 
        
        
        - SEO 최적화에 유리 (SEO: Search Engine Optimization)

                검색 엔진이 태그 목적에 알맞게 설계되어있는 구조의 사이트에서 더욱 빠르고 효율적으로 정보를 파악할 수 있고 검색결과가 
                검색 엔진이 태그의 목적에 부합하게 설계되어있는 구조의 사이트에서 더욱 빨리 효율적으로 정보를 파악할 수 있어
                검색 결과의 노출에 유리할 수 있게 해준다.

        - 웹 접근성에 효율적

                일반적인 브라우저에서는 차이가 없지만 스크린리더 시각장애인을 위한 웹 서핑
                프로그램 과 같은 환경에서는 웹 접근성과 사용성을 향상시켜준다.

        
        - 유지보수의 용이성

                많은 수의 div사용으로 관리가 어려워지는 문제점에서 벗어나 태그의 이름만 보고도 어떤 영역인지 바로 확인이 가능하고 해당 태그 영역의 특성에 맞는 작업을 구분하여 진행하기에 용이하다.
        

        2. 시맨틱 태그의 용도를 간단히 기술하시오?

                header 
                -머리글,제목,헤더
                
                main
                -이름처럼 문서 body의 중심 주제,주요 내용 또는 응용 프로그램의 중심 기능과 관련되어나 확장되는 콘텐츠를 나타낸다
                
                footer
                -바닥글,문서 하단에 들어가는 정보 구분 공간을 표현하는 태그
                
                nav 
                -네이게이션,목차,리스트 등 다른 페이지로의 이동을 위한 링크 공간을 위주로 표현
                
                section
                - 주제,카테고리 별로 섹션을 구분하는 용도의 태그로 주로 사용 같은 테마를 가진 여러개의 콘텐츠의 그룹화
                
                article
                - 기사,블로그 등 텍스트 위주의 페이지를 구성할때 주로 사용
                
                aside
                -좌측과 우측 사이드 위치의 공간을 의미하며,본문 외에 부수적인 내용을 주로 표현하는 태그이다

<hr>

# 2022-11-25

##HTTP

webbrowser 가   webserver에 요청 

request line GET(method) / -(url)/a.html HTTP(protocol)/1.1

        | "GET"                    ; Section 9.3
        | "HEAD"                   ; Section 9.4
        | "POST"                   ; Section 9.5
        | "PUT"                    ; Section 9.6
        | "DELETE"                 ; Section 9.7

URI (uniform resource identifier)

        -URL(Uniform Resource Locator)
        http://img.naver.net/static/www/dl_qr_naver.png
        
        -URN(uniform resource name)
        urn:ietf:rfc:2141 - 'RFC 2141' 문서

##네트워킹  

        1. concection- oritented (연결지향) 연결후 통신 
        예)전화
        
        - TCP : 연결확인 과정중 3번의 연결을 과정을 통해 데이터 전송 신뢰성 확보 단점은 그 과정에서 지연시간이 발생
           HTTP1,2

                1)stateful -> client와 server가 연결과 요청 응답을 연결 끊길때까지 반복한다 
                
                - 한번연결후 끊을때까지 여러번 통신
                - 적은 수의 client 대응
                - 쓰레드 방식으로 여러 client를 대응할 수 있다
                - SSH,FTP,채팅,구글미트

                2)stateless -> client와 server가 연결과 요청 응답을 하고 연결을 끊는다 
                
                - 매번연결
                - 많은 수의 client와 대응 가능
                - HTTP 

        2. concectionless (비연결) 연결없이 데이터 전송 
        예)편지,방송
        편지는 특정 주소에
        방송은 특정 그룹에  
        - UDP :  데이터 전송 신뢰성 없다 -> 별도 처리 필요
          HTTP3

        *추천 참고 도서 : 모두의 네트워크


##proxy 서버
client와 server 중간에서 통신을 중재

-요청을 server에 보내면 proxy cache에 응답 데이터를 임시저장시켜 같은 자원을 요청할때 보관된 데이터를 즉시 전달하여 네트워크 오버헤드를 줄이고 응답속도를 개선한다 

-모니터링을통해 요청/응답내용을 감시하여 보안강화 
http 통신을 살펴볼 수 있다

exam-01에서 서버요청과 응답을 확인할 수 있는 charles 라는 프로그램을 다운로드 받고 CMD에서 ipconfig로 아이피 확인 후 입력하여 charles로 확인 가능

** charles에 내용이 나오지 않을 경우 proxy서버를 수동으로 끄고 켜서 설정해야 한다

        서버

        GET /git/bitcamp-nap/form/exam-01.html HTTP/1.1
        Host: 192.168.0.10:5500
        Upgrade-Insecure-Requests: 1
        User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/107.0.0.0 Safari/537.36
        Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
        Accept-Encoding: gzip, deflate
        Accept-Language: ko-KR,ko;q=0.9,en-US;q=0.8,en;q=0.7      *요청언어를 설정
        Connection: keep-alive

        
        클라이언트

        HTTP/1.1 200 OK
        Vary: Origin
        Access-Control-Allow-Credentials: true
        Accept-Ranges: bytes
        Cache-Control: public, max-age=0
        Last-Modified: Fri, 18 Nov 2022 07:21:33 GMT
        ETag: W/"2ed-184899d3929"
        Content-Type: text/html; charset=UTF-8             *mainprotocol type
        Content-Length: 2242
        Date: Fri, 25 Nov 2022 02:51:45 GMT
        Keep-Alive: timeout=5
        Proxy-Connection: keep-alive


        get 요청

         ET /html/form/exam02?name=&age=111 HTTP/1.1
                              ㄴ>쿼리스트링 (name=-- & age=111)
                                name : 파라미터명
                                -- : 파라미터값
                                & : 파라미터 구분자
                                data를 url에 붙여서 보낸다 서버에 보내는 데이터

                                한계

                                1. 바이너리 데이터를 보낼 수 없다(text이기 때문이다)
                                        -text 일반 텍스트 편집기로 편집가능한 포맷
                                        예) txt.rtf,html,cdd,js,xhtml.. ..
                                2. binary
                                -byte단위로 포맷 
                                -일반텍스트로 편집 불가        -> base64 
                                -전용 app 사용                    binary 데이터를 텍스트로변경가능
                                예) jpg,mp3,mp4 포맷이 깨진다 

                                즉 저장된 형식에 맞춰 읽어야한다 

                                3. URI 크기의 제한 떄문에 대용량 데이터를 보낼 수 없다 보통 64k apache는 8k

                                4. URL은 브라우저 캐시에 보관 되어 보안에 취약하다 
        

        post 요청


        POST /html/form/exam02 HTTP/1.1     <- request line      post부터 Connection까지 구역이 header   
        Host: 192.168.0.10:5500                     
        Content-Length: 18          <-   이것과 Content-Type 는 post방식에만 있는 header
        Cache-Control: max-age=0
        Upgrade-Insecure-Requests: 1
        Origin: http://192.168.0.10:5500
        Content-Type: application/x-www-form-urlencoded
        User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/107.0.0.0 Safari/537.36
        Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
        Referer: http://192.168.0.10:5500/git/bitcamp-nap/form/exam-02.html
        Accept-Encoding: gzip, deflate
        Accept-Language: ko-KR,ko;q=0.9,en-US;q=0.8,en;q=0.7
        Connection: keep-alive  

        name=asdfsadf&age=                <-    message-body

        
        
        post 요청 특징
        
        1. binary 데이터 전송가능
        2. URL에 노출안됨     -> URL 데이터에 포함해야하는 방식에 적합하지 않음 예)검색URL,게시글 조회 URL
        3. 여러개의 파일 첨부가능
        4. 용량제한없다 (서버에서 제한 하지 않는한)


##post와get방식은 input안에 name을 지정하지 않으면 
데이터를 서버에 보내지 않는다. 

enctype="multipart/form-data" 으로 하면 이름과 데이터                         

사진: input type="file" name="photo" multiple
여러 사진을 넣고싶다면 multiple을 추가해준다 

#주말동안

9-1
9-2
9-3은 빼고
10-1
깃허브에 html로 정리 와 css 테마 조정하기 index.html로 md옮겨서




        