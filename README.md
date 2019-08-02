# Linux-Server-Environment
리눅스 설치 및 환경 구현 
  
## Install Linux

## Booting USB 만들기
#### 1) 준비

우분투 사이트 : <https://ubuntu.com/download/desktop>  : iso 파일 다운로드

#### 2) USB 준비
* 2GB 이상 빈 USB 준비

### 1 Mac 
#### 1) iso 파일 -> img 파일로 변경
  * USB 꽂지 않은 상태에서 다운받은 iso 파일 경로 확인   
  ```
  ex) ~/Downloads/ubuntu-18.04.2-desktop-amd64.iso
  ```
  
  * 맥이 취급 할 수 있도록 img 파일로 변경
    - 터미널 열고 아래 명령어 입력  
    - 명령어 이후 ubuntu.img.dmg 파일명을 ubuntu.img로 변경
  ```
  hdiutil convert -format UDRW -o ~/Downloads/ubuntu.img ~/Download/ubuntu-18.04.2-desktop-amd64.iso
  ```
  
  * 부팅용 USB 연결
    - 아래 명령어를 실행하여 USB의 장치 번호를 확인
  ```
  diskutil list
  
  (example) >>> /dev/disk2 
  ```
  
  * 만약 장치 번호가 disk2이며, ubuntu.img 위치가 Downloads일 경우 아래와 같이 명령어 실행 
    (약 10분 정도 시간 걸림)
  
  ```
  1. diskutil unmountDisk /dev/disk2
  2. sudo dd if=~/Downloads/ubuntu.img of=/dev/disk2 bs=1m
  ```
  
  * USB 장치 제거
  ```
  diskutil eject /dev/disk2
  ```
