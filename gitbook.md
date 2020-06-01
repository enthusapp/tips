# github 를 이용한 gitbook 만들기

### 초기 설정
https://github.com/GitbookIO/gitbook/blob/master/docs/setup.md#local-installation 참조
```
npm install gitbook-cli -g // 한번도 설치한적이 없다면

// repository 로 이동한 뒤에
gitbook init // 처음 실행
gitbook serve // local 에서 gitbook 테스트
```


### 그림 올리기
그림 파일을 프로젝트 폴더에 복사하고 문서에 경로 링크를 추가
```
![그림 설명](그림파일 상대경로)
```

##### 예시
`img` 폴더에 `test.png` 파일이 있을 경우,
```
![테스트 이미지](img/test.png)
```

### PDF 제작
* https://calibre-ebook.com 설치
* 명령어 `gitbook pdf` 실행
* pdf 파일 경로 문서에 추가, target 을 설정하지 않으면 제대로 이동하지 않음
```
<a href="seoulExternalLight_v1.0.pdf" target="_blank" >PDF 다운로드</a>
```

### publish
```
$ gitbook build // 작업 완료 후 gitbook 페이지 생성
$ git checkout gh-pages // gh-pages branch 가 없을 경우 git checkout -b gh-pages
$ copy .\_book\* %cd% /y // Windows 환경, Linux 에서는 "cp -R ../_book/* ."
$ git clean -fx _book
$ git add .
$ git commit -sm "upload gh-pages"
$ git push origin gh-pages
$ git checkout master
```

### Links
* https://blog.chulgil.me/how-to-make-blog-using-github-5/
* https://github.com/GitbookIO/gitbook
* https://jangbi882.gitbooks.io/gitbook-guide/content/program_account.html
* https://github.com/GitbookIO/gitbook-pdf
