# github 를 이용한 gitbook 만들기

## 초기 설정
https://github.com/GitbookIO/gitbook/blob/master/docs/setup.md#local-installation 참조
```
npm install gitbook-cli -g // 한번도 설치한적이 없다면

// repository 로 이동한 뒤에
gitbook install // 처음 실행
```

## 그림 올리기
그림 파일을 프로젝트 폴더에 복사하고 문서에 경로 링크를 추가
```
![그림 설명](그림파일 상대경로)
```

### 예시
`img` 폴더에 `test.png` 파일이 있을 경우,
```
![테스트 이미지](img/test.png)
```

## PDF 제작
* https://calibre-ebook.com 설치
* 명령어 `gitbook pdf` 실행
* pdf 파일 경로 문서에 추가, target 을 설정하지 않으면 제대로 이동하지 않음
```
<a href="seoulExternalLight_v1.0.pdf" target="_blank" >PDF 다운로드</a>
```

## 편집
[SUMMARY.md](SUMMARY.md) 에 새로 생성한 문서에 대한 경로를 추가합니다.

### 예시
```markdown
# Summary

* [소개](README.md)
* [투광등](flood/README.md)
  * [LFR](flood/lfr/README.md)
    * [LFR0655](flood/lfr/lfr0655/README.md)
      * [LFR0655-120FWC](flood/lfr/lfr0655/lfr0655-120fwc.md)
  * [LFC](flood/lfc/README.md)
    * [LFC0165](flood/lfc/lfc0165/README.md)
      * [LFC0165-48FWC](flood/lfc/lfc0165/lfc0165-48fwc.md)
```

## local Test
```
gitbook serve
```

## publish
편집 완료 후 사이트로 배포합니다.

1. markdown 변경 사항은 VSCode 를 통해 `main branch` 에 commit 및 push 합니다.
1. 아래 명령을 차례로 입력하여 gitbook 빌드 결과를 gh-pages branch 에 업로드 합니다.

> github 정책에 의해 `master` → `main` 으로 기본 branch 이름이 변경되었습니다. branch 이름 입력에 주의해야 합니다.

```
gitbook build
git checkout gh-pages
git pull origin gh-pages
xcopy .\_book\* . /y /s /e // windows cmd 는 xcopy .\_book\* %cd% /y /s /e
git clean -fx _book
git add .
git commit -sm "upload gh-pages"
git push origin gh-pages
git checkout main
```

## Troubleshooting
### gitbook install graceful-fs errror
* https://stackoverflow.com/questions/64211386/gitbook-cli-install-error-typeerror-cb-apply-is-not-a-function-inside-graceful
```
cd /usr/lib/node_modules/gitbook-cli/node_modules/npm/node_modules/
npm install graceful-fs@4.2.0 --save
```

## Links
* 접히는 summary 만들기: https://www.npmjs.com/package/gitbook-plugin-expandable-chapters
* https://blog.chulgil.me/how-to-make-blog-using-github-5/
* https://github.com/GitbookIO/gitbook
* https://jangbi882.gitbooks.io/gitbook-guide/content/program_account.html
* https://github.com/GitbookIO/gitbook-pdf
