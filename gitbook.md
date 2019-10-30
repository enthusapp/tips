# github 를 이용한 gitbook 만들기

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
* pdf 파일 경로 문서에 추가

### publish
```
$ git checkout -b gh-pages // branch 가 이미 있으면 git checkout gh-pages
$ cp -R ../_book/* .
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
