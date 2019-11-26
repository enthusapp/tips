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
