# Ubuntu-Starter
Ubuntu에서 웹 개발에 필요한 환경 잡기 및 지식 정리

## 추가 하드디스크 마운트
* 참고 사이트 : [링크](https://psychoria.tistory.com/521)

## VMWare(가상머신)으로 Ubuntu 사용 시에 vmware-tools 설치하기
* 설치 : `sudo apt-get install -y open-vm-tools-desktop`
* 참고 사이트 : [링크](https://kkn1220.tistory.com/109)

## Native Ubuntu 사용 시에 apt-get 안되는 문제
이미 떠 있는 apt 프로세스를 모두 종료시킨다.
* 프로세스 확인 : `ps aux | grep -i apt`

### 참조 사이트
[How to Fix ‘E: Could not get lock /var/lib/dpkg/lock’ Error in Ubuntu Linux](https://itsfoss.com/could-not-get-lock-error/)

## 폴더명 한글 -> 영문 변경
* `export LANG=C`
* `xdg-user-dirs-gtk-update`
* Update Names 버튼 클릭
* 참고 사이트 : [링크](http://blog.naver.com/PostView.nhn?blogId=ijuju88&logNo=220961426979)

## apt
* apt : Ubuntu 전용 패키지(응용 프로그램) 설치 관리자

### apt 사용법
* 패키지(응용프로그램) 찾기 : `apt-cache search [찾을 패키지 명]`
* 패키지 설치 
  - 기본 : `sudo apt-get install [패키지 명]`
  - 자동 Yes으로 설치 : `sudo apt-get install -y [패키지 명]`
* 패키지 재설치 : `apt-get --reinstall install [패키지 명]`
* 패키지 삭제 
  - 패키지만 삭제(설정파일은 안지움) : `sudo apt-get remove [패키지 명]`
  - 설정 파일까지 삭제 : `sudo apt-get --purge remove [패키지 명]`
* 설치된 패키지 목록보기 : `apt list`

### ssh
* 설명 : 쉘 접속기
* 설치 : `sudo apt-get install -y ssh`
* `mkdir ~/.ssh`

### net-tools
* 설명 : ifconfig
* 설치 : `sudo apt-get install -y net-tools`

### ping
* 설명 : ping
* 설치: `sudo apt-get install -y iputils-ping`

### telnet
* 설명: telnet
* 설치: `sudo apt-get install -y telnet`

### traceroute
* 설명 : 서버 접속 가능 및 경로 파악
* 설치 : `sudo apt-get install -y traceroute`
* 사용법 : `traceroute -p [포트] [서버 IP] -T`

### htop
* 설명 : 기본 탑재된 top 보다 좀 더 Visual 한 버전의 프로세스 보기
* 설치 : `sudo apt-get install -y htop`

### Git
* 설명 : 버전 관리
* 설치 : `sudo apt-get install -y git`

### zsh
* 설치 : `sudo apt-get install -y zsh`
* 참고 사이트 : [링크](https://the-illusionist.me/47)

### oh-my-zsh
* 설치 : `sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"`
* 참고 사이트 : [링크](https://the-illusionist.me/47)

### Chrome
* wget 을 이용한 설치 
  - `wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -`
  - `sudo sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'`
  - `sudo apt-get update; sudo apt-get install -y google-chrome-stable`
* 참고 사이트 : [링크](https://snowdeer.github.io/linux/2018/02/02/ubuntu-16p04-install-chrome/)

### OpenJDK 
* OpenJDK 8 버전으로 설치 : `sudo apt-get install -y openjdk-8-jdk`

### Docker Desktop
설치 
* [우분투 18.04 Docker & Docker-Compose 설치](https://velog.io/@kys6879/%EC%9A%B0%EB%B6%84%ED%88%AC-18.04-Docker-Docker-Compose-%EC%84%A4%EC%B9%98)
* [Official - Install Docker Engine on Ubuntu](https://docs.docker.com/engine/install/ubuntu/)

### ADB
* 설명 : android platform tools
* 설치 : `sudo apt-get install -y android-tools-adb android-tools-fastboot`
* 참고 사이트 : [링크](https://linuxtechlab.com/install-adb-fastboot-ubuntu/)

### tomcat
* 설치 : `sudo apt-get install -y tomcat9`

## snap(Ubuntu 18.04 에서 선탑재됨)
* 설명 : GUI 패키지 설치 관리자
* 설치 : `sudo apt-get install -y snapd`

### snap 사용법
* 패키지(응용프로그램) 찾기 
  - `snap search [찾을 패키지 명]`
  - `snap find "키워드"`
* 패키지 설치 : `snap install [패키지 명]`
* 패키지 삭제 : `snap remove [패키지 명]`
* 설치된 패키지 목록보기 : `snap list`
* 패키지 업데이트 
  - 특정 패키지 `snap refresh [패키지 명]`
  - 모두 : `snap refresh` 

### JetBrain
* Intellij IDEA
  - Community : `snap install intellij-idea-community --classic`
  - Ultimate : `snap install intellij-idea-ultimate --classic`
* datagrip : `snap install datagrip --classic`
* clion : `snap install clion --classic`
* webstorm : `snap install webstorm --classic`

### Visual Studio Code
* 설치 : `snap install code --classic`

### ngrok
* 설명 : 외부망에서 tcp 접속할 수 있도록 지정 포트를 ngrok에서 제공해주는 도메인 및 포트에 바인딩해준다.
* 공식 사이트 : [링크](https://ngrok.com)
* 주의 : 회원가입 필요(무료)
* 설치 : `snap install ngrok`
* 사용법 : `ngrok tcp [지정 포트]`
* 예시 : `ngrok tcp 4321`

### GitHub Desktop 
* 설명 : 앱으로 Github 관리 
* 설치 : `snap install github-desktop --beta --classic`

### Slack
* 설명 : 사내 메신져
* 설치 : `snap install slack`

### 방화벽 설정
* 방화벽 로그 경로 : `/var/log/ufw.log`  
* 방화벽 설정 : `sudo ufw enable`  
* 방화벽 로그 설정 : `sudo ufw logging on`  
* 방화벽 정보 보기 : `sudo ufw status`  
* 참조사이트 : [링크](https://webdir.tistory.com/206)

## wifi 고정 아이피 설정
### 연결 가능 wifi 확인
설치(아래 확인 먼저 해보고 명령어가 없으면 설치)
``` bash
sudo apt-get install -y network-manager
systemctl start NetworkManager
```

확인
``` bash
nmcli dev wifi
```

연결
``` bash
nmcli dev wifi connect wifi이름 password 'wifi패스워드'
```

### 네트워크 인터페이스 확인
``` bash
$ ifconfig
...
wlan0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.0.32  netmask 255.255.255.255  broadcast 0.0.0.0
        inet6 abcd::ef01:0203:0405:0607  prefixlen 64  scopeid 0x20<link>
        ether ab:cd:ef:12:34:56  txqueuelen 1000  (Ethernet)
        RX packets 76464341  bytes 5643758780 (5.6 GB)
        RX errors 0  dropped 2556177  overruns 0  frame 0
        TX packets 366823  bytes 64157759 (64.1 MB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
```

### 고정 아이피 설정된 wifi 생성
yaml 파일 수정
``` bash
cd /etc/netplan/
sudo vi 01-network-manager-all.yaml
# Let NetworkManager manage all devices on this system
network:
  version: 2
  renderer: NetworkManager
  wifis:
          wlan0:        # ifconfig에서 확인한 네트워크 인터페이스
                  dhcp4: yes
                  dhcp6: no
                  addresses:
                        - 192.168.0.32/32       # 고정할 아이피
                  gateway4: 192.168.0.1
                  nameservers:
                        addresses: [168.126.63.1, 168.126.63.2]
                  access-points:
                        "wifi이름":
                                password: "wifi패스워드"
:wq
```

네트워크 적용
``` bash
sudo netplan apply
```

### 생성된 wifi 연결
``` bash
# 확인
nmcli dev wifi
# 연결
nmcli dev wifi connect netplan-wlan0-wifi이름 password '패스워드'
```

## 참고사이트
* [[우분투 서버 18.04 NET] 1.2무선(wifi) IP 주소 설정](https://m.blog.naver.com/PostView.nhn?blogId=sunguru&logNo=221519708161&proxyReferer=https:%2F%2Fwww.google.com%2F)
