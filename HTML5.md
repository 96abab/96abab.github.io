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

    HTTPclient
    -HTML을 다운받아 출력하고 제어하는 역할을 한다