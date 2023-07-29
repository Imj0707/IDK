# IDK (I Don't know 몰라요) 🤣
2023.7.29 NVIDA Jetson 사용 👍 (with Greendangdang 😎)

프로젝트를 만든 사람도 이 프로젝트가 뭔지 몰라요. ^_____^

# Ubuntu 설치
<hl>
  
  1. https://developer.nvidia.com/embedded/learn/getting-started-jetson 에서 JetSon nano 2GB용 ubuntu 이미지 다운로드
  
  2. 64GB sd카드 포맷
  3. balenEtcher로 sd카드에 flash ⚡

<img src="./jetson-ubuntu.png">


# Jetson 조립하기 🛠
1. 쿨링팬 설치 
2. 키보드와 마우스 연결하기
3. 카메라 설치 및 연결

<img src="./jetson.png">

# Jetson 쿨링팬 돌리기 🔧
: Jetson의 발열이 너무 심해서 쿨링팬이 필요함.

<hl>

cd Download ✏ Download 폴더로 이동

git clone  https://github.com/jetsonworld/jetson-fan-ctl.git ✏ Git 프로젝트 복제

cd jetson-fan-ctl ✏ 복제한 프로젝트 폴더로 이동

sudo sh install.sh ✏ 설치 시작

# Jetson 상태, 메모리 체크를 위한 Python Package 설치 ⚙

sudo apt-get upgrade && update ✏ Ubuntu Package 업데이트 & 업그레이드 

sudo apt-get install python3-pip ✏ pip3 설치

sudo -H pip3 install -U jetson-stats ✏ jtop Package 설치

pip3 list | grep jetson ✏ Package가 설치 되어있는지 확인

<h1>재부팅</h1>

jtop ✏ jtop 실행

<img src="./jtop.png">


# 카메라 체크 📸
git clone https://github.com/jetsonhacks/USB-Camera.git ✏ Camera 복제

cd USB-Camera ✏ USB-Camera 폴더로 이동

python3 usb-camera-gst.py ✏ usb-camera-gst.py 실행

또는

python3 usb-camera-simple.py ✏ usb-camera-simple.py 실행

<img src="./jetson_camera.png">

# Headless Mode 사용하기 ⛓

GUI가 아니라 CUI로 모니터없이 ssh로 연결해서 Jetson사용하기


<hl>
    1. Powershell을 관리자 권한으로 실행 😎
    2. 최상위 폴더로 이동
    3. ssh를 사용하여 연결
</hl>

# 실행 결과

(NVIDA의 전용 서버 ip : dli@192.168.55.1) 

첫번째 실행 : Connection timed out 에러 발생 😶

두번째 실행 : 똑같은 에러 발생 (재부팅 후) 🙄
