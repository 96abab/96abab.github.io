# HTML5 수업


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
        \pard\sa200\sl276\slmult1\b\f0\fs44\lang1042 ABC\'ba\'f1\'c6\'ae\'c4\'b7\'c7\'c1\b0\fs20\par     <-  
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
        
        -애플,아이폰,아이패드등 모바일 브라우저의 뷰포트를 크기 조절하기 위한 태그 w3c에 표준이 아니지만 IOS장치가 널리 사용되면서 사실상 표준처럼 사용되고있다 
<br>
<br>
##data 와 메모리
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