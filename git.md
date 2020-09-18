### create branch
```
git branch newbranch
git checkout newbranch
git push origin newbranch
```

### delete branch
```
git branch -d newbranch
```

### branch merge
```
git checkout branchname
git checkout master
git merge branchname

// fix conficts
```

### delete branch
```
git branch --delete branchname
git branch -D branchname  // 오류 발생할 경우 강제 삭제
git push origin :branchname   // 삭제된 branch server 에 반영
```

### 이전 commit 으로 돌아가기
```
git reset HEAD~1 // 1 commit 돌아가기
```

### submodule
##### 처음 더하기
```
$ git submodule add <repository> [path]
```
##### 최신 버젼으로 받기
서브 모듈의 path 로 들어가 `git pull`

##### Reference
* https://ohgyun.com/711
* https://feel5ny.github.io/2019/01/27/Git_01/

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
