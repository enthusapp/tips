공개키 에러로 apt-get update 가 안될때는 수동으로 dirmngr package 를 다운로드 받아 설치하고, 공개키를 설정하면 된다.

```bash
curl -O http://ftp.kr.debian.org/debian/pool/main/g/gnupg2/dirmngr_2.1.18-8~deb9u4_armhf.deb  // arch 에 따라 다른 경로 선택
sudo dpkg -i dirmngr_2.1.18-8~deb9u4_armhf.deb
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 9165938D90FDDD2E // 같은 방식으로 공개키 입력
```
