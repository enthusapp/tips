### submodule
##### 처음 더하기
```
$ git submodule add <repository> [path]
```
##### 최신 버젼으로 받기
서브 모듈의 path 로 들어가 `git pull`

https://ohgyun.com/711

https://feel5ny.github.io/2019/01/27/Git_01/

### windows 에서 eol lf 설정
##### git
```
git config --global core.eol lf
git config --global core.autocrlf input
```
##### Visual Studio Code
```
"files.eol": "\n"
```
