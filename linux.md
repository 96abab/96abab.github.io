# 리눅스 명령어
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
1. 파일 시스템 탐색 기본 명령어
<br>


<br>

    $ pwd   : 작업 디렉토리 위치를 확인한다

        /home/vagrant/git

<br>
<br>

    $ cd  (디렉토리명) : 현재 작업하는 디렉토리의 위치를 이동 시킨다 

        [vagrant@host1 git]$ cd bitcamp-ncp

        [vagrant@host1 bitcamp-ncp]$

<br>
<br>
      
    $ ls  : 현재 위치한 디렉토리에 있는 디렉토리와 파일들의 리스트를 출력한다

        b.txt    x.txt    README.md 

<br>
<br>

$ file (파일명):  지정한 파일의 타입을 확인한다

        [vagrant@host1 bitcamp-ncp]$ file README.md

        README.md: ASCII text, with no line terminators



$ less  (파일명): 텍스트형식의 파일의 내용을 1페이지씩 보여준다 pageup과 pagedown으로 이동가능하고 화살표 커맨드와 스페이스바로도 이동이 가능하다 그리고 q를 누르면 출력모드가 종료된다

        1111

        2222

        3333

        4444

        5555

        6666

        b.txt (END)



 

2. 파일과 디렉토리 조작 명령어

$ cp (복사할파일) (붙여넣을 파일) : 지정파일 내용을 붙여넣을 파일에 복사하여 넣는다 만약 붙여넣을 파일이 없다면 생성하여 붙여넣는다 

<br>

    [vagrant@host1 bitcamp-ncp]$ cp b.txt bb.txt <- 해당 파일이 없을경우 만들어서 붙여넣는다 (파일생성가능)

<br>
<br>

$ mv (파일의 현재 경로/파일 이름)(이동시킬 경로) : 파일의 경로를 이동시킬때 사용한다  *주의점 : pwd등을 이용하여 home/경로부터 지정해줘야 이동한다



        [vagrant@host1 bitcamp-ncp]$ ls

        bb.txt  b.txt

        [vagrant@host1 bitcamp-ncp]$ mv b.txt /home/vagrant/git/bitcamp-ncp/xxx

        [vagrant@host1 bitcamp-ncp]$ ls

        bb.txt

        [vagrant@host1 bitcamp-ncp]$ cd xxx

        [vagrant@host1 xxx]$ ls

        b.txt

<br>
<br>


$ mkdir (디렉토리명):  디렉토리를 생성한다



        [vagrant@host1 xxx]$ ls

        b.txt

        [vagrant@host1 xxx]$ mkdir ccc

        [vagrant@host1 xxx]$ ls

        b.txt  ccc


<br>
<br>

3. 명령어를 다루는 명령어

<br>


$type : 지정한 리눅스 명령어를 내장된 명령어 외부명령어인지 확인해준다



 [vagrant@host1 xxx]$ type ls

ls is aliased to `ls --color=auto'



 $which : 명령어 위치를 찾는다



[vagrant@host1 xxx]$ which ls

alias ls='ls --color=auto'

        /usr/bin/ls

$ man (명령어): 설명페이지를 볼 수 있다




    LS(1)                                               User Commands                                               LS(1)



    NAME

        ls - list directory contents



    SYNOPSIS

        ls [OPTION]... [FILE]...



    DESCRIPTION

        List  information  about the FILEs (the current directory by default).  Sort entries alphabetically if none of

        -cftuvSUX nor --sort is specified.



        Mandatory arguments to long options are mandatory for short options too.



        -a, --all

                do not ignore entries starting with .



        -A, --almost-all

                do not list implied . and ..



        --author

                with -l, print the author of each file



        -b, --escape

                print C-style escapes for nongraphic characters



        --block-size=SIZE

                scale sizes by SIZE before printing them; e.g., '--block-size=M' prints sizes  in  units  of  1,048,576



$apropos (명령어): 해당 명령어와 관련있는 명령어를 설명과 같이 보여준다



        _llseek (2)          - reposition read/write file offset

        afs_syscall (2)      - unimplemented system calls

        assert (3)           - abort the program if assertion is false

        auth_destroy (3)     - library routines for remote procedure calls


<br>
<br>


$ info : 명령어를 하이퍼텍스트 형식으로 관련정보를 알려준다



        File: coreutils.info,  Node: ls invocation,  Next: dir invocation,  Up: Directory listing



        10.1 'ls': List directory contents

        ==================================



        The 'ls' program lists information about files (of any type, including

        directories).  Options and file arguments can be intermixed arbitrarily,

        as usual.




$ whatis : 해당명령어의 간단한 설명


        [vagrant@host1 xxx]$ whatis ls

        ls (1)               - list directory contents

        ls (1p)              - list directory contents



$ alias : 사용 가능한 단축 명령어를 확인 할 수 있다



        alias

        alias egrep='egrep --color=auto'

        alias fgrep='fgrep --color=auto'

        alias grep='grep --color=auto'

        alias l.='ls -d .* --color=auto'

        alias ll='ls -l --color=auto'

        alias ls='ls --color=auto'

        alias which='alias | /usr/bin/which --tty-only --read-alias --show-dot --show-tilde'









 