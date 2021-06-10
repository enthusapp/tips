# 리눅스 Tips

## GITHUB 사용법

### 윈도우즈 github 에서 gitignore 적용방법
```
git rm -r --cached . 
git add . 
git commit -m "fixed untracked files"
```

### git 사용법
https://rogerdudler.github.io/git-guide/index.ko.html

### Git 작업 방법
git init --bare 서버이름
작업 폴더로 이동
git clone 서버경로
작업, 수정
git add -i
git commit -m “수정내용”
git push origin master

## invalid module format 에러 해결
http://mintnlatte.tistory.com/316

## 리눅스 드라이버 만들기
http://www.joinc.co.kr/modules/moniwiki/wiki.php/Site/Embedded/Documents/WritingDeviceDriversInLinux

## Xming 에서 windows 로 복사하는 방법
To copy selected text within a command-line window in xming:
to copy the text, use Alt + Shift + C
to paste into windows, use the normal Ctrl + V

## Font 수정
http://ospace.tistory.com/242
https://awesome.naquadah.org/wiki/Customizing_GTK_Apps

## 개행문자 제거
http://myje.tistory.com/226
출처 - http://revf.tistory.com/146

쉘스크립트 실행 시 유닉스 개행문자와 도스 개행문자가 섞여 있는 경우
 ^M 문자를 제거 하는 방법

1. vi -b 파일명 ( vi를 binary 편집 모드로 실행 )
2. vi 명령 줄에 %s/^M//g 와 같이 입력 후 엔터
3. 저장 후 vi 종료
^ : ctrl + v
M : ctrl + M

## 자바문법
http://hyeonstorage.tistory.com/177

## Git 와 Eclipse 연동
http://itmir.tistory.com/461

## Git 특정 폴더만 checkout 하기
http://stackoverflow.com/questions/600079/is-there-any-way-to-clone-a-git-repositorys-sub-directory-only
한 뒤 git checkout

## vim 사용하기
e#: 이전 편집하던 파일로 이동
e!: 수정전 상태로
ctrl+r: window editor의 ctrl+y
http://qaos.com/sections.php?op=viewarticle&artid=108

http://blog.outsider.ne.kr/518

set ai
set ts=4
set sw=4
set cindent
set ruler
set bs=indent,eol,start
set hlsearch
set nu
syntax on
set incsearch “searching 글자를 치는 도중 커서가 해당 글자로 자동으로 이동
set guifont=Courier\ 10\ Pitch\ 12
colorscheme koehler

http://vim.wikia.com/wiki/Change_font


http://gypark.pe.kr/wiki/Vi%EB%A1%9C%EB%AC%B8%EC%9E%90%EC%97%B4%EC%B9%98%ED%99%98%ED%95%98%EA%B8%B0


:5,10s/a/b/     - 5번째 줄부터 10번째 줄까지 각 줄의 첫번째 "a" 를 "b" 로 바꾼다.
:.,.+10s/a/b/g  - 현재 줄부터 (현재 행번호+10)번째 줄까지 모든 "a" 를 "b" 로 바꾼다.
:1,$s/a/b/c     - 첫번째 줄부터 마지막 줄까지 (즉 문서 전체) 각 줄의 "a" 를 "b" 로 바꾸되, 사용자에게 확인을 받는다.
:%s/a/b/gi      - 역시 문서 전체에서 "a" 와 "A" 를 "b" 로 바꾼다.
:%s/Hello/Good Morning/g - 당연히... 두 글자 이상의 문자열도 검색 및 치환이 가능하다.


## ctags 사용하기
http://www.viper.pe.kr/cgi-bin/moin.cgi/ctags_%EC%99%80_vi_%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0

http://home.postech.ac.kr/~kypark/linux-apps/vimctags.html


## grep 사용하기
```
alias gr='grep --color -R -n --exclude=.*.swp,tags' 
```

bashrc
alias ll='ls -l'

## IP 설정보기
ifconfig

## gitweb 설치
ubuntu 12.04
http://forum.falinux.com/zbxe/index.php?document_srl=786190&mid=lecture_tip
ubuntu 14.04
http://blog.daum.net/junek69/37

### cgi 설치
http://askubuntu.com/questions/403067/cgi-bin-not-working

### gerrit 설치
https://code.google.com/p/gerrit/
http://pseg.or.kr/pseg/infoinstall/1780

## Find 명령어
find -name '*.pl’
find -name '*.pl’ | grep xxx

## Samba 서버설치
http://egloos.zum.com/entireboy/v/4758471

## 우분투 한글키 동작
http://egloos.zum.com/nemonein/v/5227053

## 우분투 Android SDK 설치
https://www.davidlab.net/ko/tech/how-to-setup-android-dev-env-on-ubuntu-part1/

## 우분투 Android Eclipse 설치
http://thrillfighter.tistory.com/157
http://hyeonstorage.tistory.com/129

## deb 파일 설치
sudo dpkg -i askubuntu_2.0.deb

## INTEL graphic library 설치(GLX 관련)
https://01.org/linuxgraphics/downloads/2015/2015q1-intel-graphics-stack-release


http://www.linuxfromscratch.org/blfs/view/svn/general/pixman.html
```
sudo apt-get install libdrm-intel1
```

http://askubuntu.com/questions/213678/how-to-install-x11-xorg
```
sudo apt-get install libx11-dev
sudo apt-get install x11proto-gl-dev
sudo apt-get install freeglut3-dev
sudo apt-get install libgcrypt11-dev
```
### fixesproto 
```
No package 'xcmiscproto' found
Requested 'xtrans >= 1.3.5' but version of XTrans is 1.3.4
No package 'bigreqsproto' found
No package 'randrproto' found
No package 'renderproto' found
No package 'fontsproto' found
No package 'videoproto' found
No package 'compositeproto' found
No package 'recordproto' found
No package 'scrnsaverproto' found
No package 'resourceproto' found
No package 'xf86driproto' found
No package 'presentproto' found
No package 'xineramaproto' found
No package 'xkbfile' found
No package 'xfont' found
```
```
sudo apt-get install libxfont-dev
sudo apt-get install libxkbfile-dev
sudo apt-get install libxcb-keysyms1-dev
```
Could not create SDL2 window: Couldn't find matching GLX visual


Linux 에서 삼성 android USB 잡기
http://egloos.zum.com/jaehwa/v/1014020
http://developer.android.com/tools/device.html


