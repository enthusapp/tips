### tag 관리
http://minsone.github.io/git/git-addtion-and-modified-delete-tag

### 특정 파일 checkout
```
git checkout <branch> filePath
```

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
#### 처음 더하기
```
$ git submodule add <repository> [path]
```
#### 최신 버젼으로 받기
서브 모듈의 path 로 들어가 `git pull`

#### clone 이후 첫 pull
```
git submodule init
git submodule update
```
#### submoudle 지우기
```
// 먼저 git submodule deinit -f 명령어를 통해서 해당 모듈을 deinit 해줍니다.
git submodule deinit -f test_app

// 그 다음 .git/modules 폴더에 들어가서 해당 폴더를 삭제합니다.
rm -rf .git/modules/test_app

// 마지막으로 git에서 해당 폴더를 제거해주면 됩니다.
git rm -f test_app
```

#### Reference
* https://ohgyun.com/711
* https://feel5ny.github.io/2019/01/27/Git_01/
* http://snowdeer.github.io/git/2018/08/01/how-to-remove-git-submodule/

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
