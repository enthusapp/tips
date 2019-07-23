### 찾기
* :5,10s/a/b/     - 5번째 줄부터 10번째 줄까지 각 줄의 첫번째 "a" 를 "b" 로 바꾼다.
* :.,.+10s/a/b/g  - 현재 줄부터 (현재 행번호+10)번째 줄까지 모든 "a" 를 "b" 로 바꾼다.
* :1,$s/a/b/c     - 첫번째 줄부터 마지막 줄까지 (즉 문서 전체) 각 줄의 "a" 를 "b" 로 바꾸되, 사용자에게 확인을 받는다.
* :%s/a/b/gi      - 역시 문서 전체에서 "a" 와 "A" 를 "b" 로 바꾼다.
* :%s/Hello/Good Morning/g - 당연히... 두 글자 이상의 문자열도 검색 및 치환이 가능하다.
* :%s/\\<foo\\>/bar - 정확하게 foo에 일치될 때만
* :.,$s/a/b/c     - 현재 줄부터 마지막 줄까지 각 줄의 "a" 를 "b" 로 바꾸되, 사용자에게 확인을 받는다.

### ^M 문자를 제거 하는 방법
1. vi -b 파일명 ( vi를 binary 편집 모드로 실행 )
1. vi 명령 줄에 %s/^M//g 와 같이 입력 후 엔터
1. 저장 후 vi 종료
* 참조
  * ^ : ctrl + v
  * M : ctrl + M

### vim 명령어
* e#: 이전 편집하던 파일로 이동
* e!: 수정전 상태로
* ctrl+r: window editor의 ctrl+y
* http://qaos.com/sections.php?op=viewarticle&artid=108
* http://blog.outsider.ne.kr/518
* set incsearch “searching 글자를 치는 도중 커서가 해당 글자로 자동으로 이동
* set guifont=Courier\ 10\ Pitch\ 12
* colorscheme koehler 
* http://vim.wikia.com/wiki/Change_font
* http://gypark.pe.kr/wiki/Vi%EB%A1%9C%EB%AC%B8%EC%9E%90%EC%97%B4%EC%B9%98%ED%99%98%ED%95%98%EA%B8%B0

### .vimrc 설정
```
set ai
set ts=4
set sw=4
set cindent
set ruler
set bs=indent,eol,start
set hlsearch
set nu
syntax on
```
