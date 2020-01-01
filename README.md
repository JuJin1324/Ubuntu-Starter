# Ubuntu-Starter
Ubuntu에서 웹 개발에 필요한 환경 잡기 및 지식 정리

## VMWare(가상머신)으로 Ubuntu 사용 시에 vmware-tools 설치하기
* 설치 : `sudo apt-get install -y open-vm-tools-desktop`
* 참고 사이트 : [링크](https://kkn1220.tistory.com/109)

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
  - `wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add - 
  - `sudo sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'`
  - `sudo apt-get update; sudo apt-get install -y google-chrome-stable`
* 참고 사이트 : [링크](https://snowdeer.github.io/linux/2018/02/02/ubuntu-16p04-install-chrome/)

### OpenJDK 
* OpenJDK 8 버전으로 설치 : `sudo apt-get install -y openjdk-8-jdk`

### JetBrain 
* 설치 : `sudo apt-get install -y jetbrains-toolbox`

### Docker
* 설치 : `apt-get install -y docker`

### Visual Studio Code
* wget을 이용한 설치 
  - `wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -`
  - `sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"`
  - `sudo apt-get update; sudo apt-get install -y code`
* 참고 사이트 : [링크](https://linuxize.com/post/how-to-install-visual-studio-code-on-ubuntu-18-04/)

### GitHub Desktop 
* 설명 : 앱으로 Github 관리 
* 설치 : `scoop install github`

### Slack
* 설명 : 사내 메신져
* 설치 : `scoop install slack`

### ADB
* 설명 : android platform tools
* 설치 : `scoop install adb`

### tomcat
* 설치 : `scoop install tomcat`

### telnet
* 설치 : `scoop install telnet`

### KaKaoTalk
* 설치 : `scoop install kakaotalk`
