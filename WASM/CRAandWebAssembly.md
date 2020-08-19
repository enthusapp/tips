# CRA 에 WASM 으로 C 코드 동작시키기
CRA(Create React App) 에 wasm 으로 c 코드를 사용하는 방법을 간단하게 정리하고자 한다.

## CRA
CRA 생성

```bash
$ yarn create react-app wasm
```

## CRA 의 MIME type 에 wasm 을 추가
서버의 MIME type 에 application/wasm 을 추가해야 에러 발생하지 않음

webpack5 에서 wasm 의 MIME type 지원이 `experimental` 로 구분되어 있기 때문에 CRA 에 기본설정으로 추가되어 있지 않음

CRA 에 MIME type 을 추가하려면 `npm eject` 를 한뒤에 webpack.config 를 수정해야 한다.

ejce

## Emscripten 을 이용하여 C → WASM 만들기
Emscripten 은 C/C++ 을 WASM 으로 빌드하는 툴

### Emscripten 설치
### Emscripten C 빌드
#### 데이터 입출력 함수 만들기
#### wasm 파일을 public 폴더로 이동시키기
#### binding js 파일 수정하기

## Reference
* [전체 소스](https://github.com/mallamhando/CRA_C_WebAssembly)
* [CRA 에서 wasm 적용하기](https://medium.com/@marvinirwin/webassembly-react-and-create-react-app-8b73346c9b65)
* [CRA Webpack 설정 바꾸기](https://medium.com/@jsh901220/create-react-app%EC%97%90%EC%84%9C-eject%EC%82%AC%EC%9A%A9%EC%95%88%ED%95%98%EA%B8%B0-customize-cra-react-app-rewired-10a83522ace0)
* [C WASM 과 Javascript 사이에서 데이터 주고 받기](https://github.com/3dgen/cppwasm-book/blob/master/en/ch2-c-js/ch2-04-data-exchange.md)
* [CRA 에 wasm type 을 추가하지 않는 이유](https://github.com/facebook/create-react-app/pull/7911)

## Tags
CRA, React, Emscripten, WASM
