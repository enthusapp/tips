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
