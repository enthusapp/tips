### 실행 명령어
xeyes, gnome-calculator 는 되지만 gnome-terminal 만 안될때

```
gnome-terminal --disable-factory
```

### .bashrc
```
LC_ALL=$LANG
export LC_ALL
export XAUTHORITY=/home/enthus/.Xauthority
```

### sshd_config
```
$ sudo vim /etc/ssh/sshd_config

X11Forwarding yes
X11DisplayOffset 10
X11UseLocalhost yes

```

### Putty 설정
* Enable X11 Forwarding
* X display location: localhost:0

### Links
* https://blog.naver.com/PostView.nhn?blogId=n_cloudplatform&logNo=221451046295&categoryNo=0&parentCategoryNo=0&viewDate=&currentPage=1&postListTopCurrentPage=1&from=postView
