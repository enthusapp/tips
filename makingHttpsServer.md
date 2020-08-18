# Raspberry Pi 에 HTTPS Server 만들기
## TODO
* [ ] sdcard 복사 후 동일 동작
* [x] PC 브라우저에서 HTTPS 프로토콜로 Raspberry Pi server 접속
* [x] Android 브라우저에서 HTTPS 프로토콜로 Raspberry Pi server 접속
* [x] iOS 브라우저에서 HTTPS 프로토콜로 Raspberry Pi server 접속
## HTTPS Server 가 필요한 이유
### Mixed contents error & Serverless
Android, iOS 앱에서 http 로의 접속이 제한되고 있다.
IoT https 서버를 사용하는 데에는 사용 비용과 구현에 대한 시간 및 노력이 필요하다.
## Custom Certification Authority 만들기
### Custom Certification Authority 설치
#### Android
https://support.google.com/pixelphone/answer/2844832?hl=en
#### iOS
https://medium.com/collaborne-engineering/self-signed-certificates-in-ios-apps-ff489bf8b96e
#### PC
https://stackoverflow.com/questions/7580508/getting-chrome-to-accept-self-signed-localhost-certificate
