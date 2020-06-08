# Ubuntu-Starter
Ubuntu에서 웹 개발에 필요한 환경 잡기 및 지식 정리

## VMWare(가상머신)으로 Ubuntu 사용 시에 vmware-tools 설치하기
* 설치 : `sudo apt-get install -y open-vm-tools-desktop`
* 참고 사이트 : [링크](https://kkn1220.tistory.com/109)

## Native Ubuntu 사용 시에 apt-get 안되는 문제
이미 떠 있는 apt 프로세스를 모두 종료시킨다.
* 프로세스 확인 : `ps aux | grep -i apt`
* 

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

### Docker
* 설치 : `sudo apt-get install -y docker`

### ADB
* 설명 : android platform tools
* 설치 : `sudo apt-get install -y android-tools-adb android-tools-fastboot`
* 참고 사이트 : [링크](https://linuxtechlab.com/install-adb-fastboot-ubuntu/)

### htop
* 설명 : 기본 탑재된 top 보다 좀 더 Visual 한 버전의 프로세스 보기
* 설치 : `apt-get install -y htop`

### net-tools
* 설명 : ifconfig
* 설치 : `apt-get install -y net-tools`

### traceroute
* 설명 : 서버 접속 가능 및 경로 파악
* 설치 : `sudo apt-get install -y traceroute`
* 사용법 : `traceroute -p [포트] [서버 IP] -T`

### tomcat
* 설치 : `apt-get install -y tomcat9`

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
