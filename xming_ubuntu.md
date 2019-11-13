
### sshd_config
```
$ sudo vim /etc/ssh/sshd_config

Port 22

HostKey /etc/ssh/ssh_host_rsa_key
HostKey /etc/ssh/ssh_host_ecdsa_key
HostKey /etc/ssh/ssh_host_ed25519_key

PubkeyAuthentication yes
HostbasedAuthentication no
PermitEmptyPasswords no
ChallengeResponseAuthentication no
UsePAM yes
X11Forwarding yes
X11DisplayOffset 10
X11UseLocalhost yes

PrintMotd no
PrintLastLog yes
TCPKeepAlive yes

AcceptEnv LANG LC_*
Subsystem       sftp    /usr/lib/openssh/sftp-server

```


### Putty 설정
* Enable X11 Forwarding
* X display location: localhost:0

### Links
* https://blog.naver.com/PostView.nhn?blogId=n_cloudplatform&logNo=221451046295&categoryNo=0&parentCategoryNo=0&viewDate=&currentPage=1&postListTopCurrentPage=1&from=postView
