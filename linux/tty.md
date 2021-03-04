# tty 에서 수정 방법
## 자료
* https://superuser.com/questions/431843/configure-permissions-for-dev-ttyusb0
* https://github.com/esp8266/source-code-examples/issues/26

## udev rules 추가
`/etc/udev/rules.d/60-extra-acl.rules` 파일 생성
```
KERNEL=="ttyUSB[0-9]*", TAG+="udev-acl", TAG+="uaccess"
```

### 그룹 추가
```bash
sudo gpasswd -a YourUsername dialout
```
