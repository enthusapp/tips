### BLE Scan
##### PC 에서 보유한 hci 기기 찾기
```
$ hcitool dev
Devices:
        hci0    A4:FC:77:17:B7:C2
```

##### Scan
```
$ sudo hcitool -i hci0 lescan
LE Scan ...
BC:6A:29:AC:2E:B4 (unknown)
BC:6A:29:AC:2E:B4 SensorTag
```

### Linux 기본 프로그램으로 BLE 테스트가 가능
* http://joost.damad.be/2013/08/experiments-with-bluetooth-low-energy.html

##### connect 에러 발생
* rfkill 사용: https://github.com/ev3dev/ev3dev/issues/171
* driver 업그레이드: https://askubuntu.com/questions/1071299/how-to-install-wi-fi-driver-for-realtek-rtl8821ce-on-ubuntu-18-04
* random option 사용: https://stackoverflow.com/questions/32947807/cannot-connect-to-ble-device-on-raspberry-pi
* 스마트폰으로 1 회 연결 후 다시 connect &rarr; **connection success**

##### notify 데이터 수신
* https://gist.github.com/fphammerle/d758ecf1968c0708eca66b5e9e5347d1
* https://stackoverflow.com/questions/15657007/bluetooth-low-energy-listening-for-notifications-indications-in-linux

* https://github.com/pcborenstein/bluezDoc/wiki/hcitool-and-gatttool-example
