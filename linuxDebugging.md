### 가장큰 용량 파일 찾기
* ref: https://rerethink.tistory.com/entry/%EB%A6%AC%EB%88%85%EC%8A%A4-%EA%B0%80%EC%9E%A5%ED%81%B0-%EC%9A%A9%EB%9F%89-%ED%8C%8C%EC%9D%BC-%EC%B0%BE%EA%B8%B0-%EB%94%94%EB%A0%89%ED%84%B0%EB%A6%AC

```
find /usr -size +20000 -print 
```

### 점유율 높은 process 확인
* ref: https://askubuntu.com/questions/33640/kworker-what-is-it-and-why-is-it-hogging-so-much-cpu
1. Install `perf`:
  
```sudo apt-get install linux-tools-common linux-tools-3.11.0-15-generic // install as liux kernel version```
  
2. Record some 10 seconds of backtraces on all your CPUs:
  
```sudo perf record -g -a sleep 10```
  
3. Analyse your recording:
  
```sudo perf report```

### Ubuntu kernel upgrade
* https://wiki.ubuntu.com/Kernel/LTSEnablementStack
```
sudo apt-get install --install-recommends linux-generic-hwe-18.04 xserver-xorg-hwe-18.04 
```
### repository 
https://twpower.github.io/99-change-apt-get-source-server

### Ubuntu 에서 sudo 로 허가 거부되는 access 실행하는 방법
sudo bash -c 'echo 0x8400082 > /sys/module/acpi/parameters/debug_layer'
