# Linux-Server-Environment
리눅스 설치 및 환경 구현 
  
## Install Linux

## 1. Booting USB 만들기
#### 1) 준비

우분투 사이트 : <https://ubuntu.com/download/desktop>  : iso 파일 다운로드

#### 2) USB 준비
* 2GB 이상 빈 USB 준비

### 1.1 Mac 
#### 1) iso 파일 -> img 파일로 변경
  1. USB 꽂지 않은 상태에서 다운받은 iso 파일 경로 확인   
  ```
  ex) ~/Downloads/ubuntu-18.04.2-desktop-amd64.iso
  ```
  
  2. 맥이 취급 할 수 있도록 img 파일로 변경
  터미널 열고 아래 명령어 입력
  ```
  hdiutil convert -format UDRW -o ~/Downloads/ubuntu.img ~/Download/ubuntu-18.04.2-desktop-amd64.iso
  ```
 
