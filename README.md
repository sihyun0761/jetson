# Jetson Nano
***

**Jetson Nano Setting 준비물**

```
 - jetson nano 4gb
![스크린샷 2024-09-06 160330](https://github.com/user-attachments/assets/cf3fd8e0-7d34-406e-83d0-15009c4d8f01)

 - c type power adapter
![download](https://github.com/user-attachments/assets/633b5186-e925-40a0-9d94-effa8aa1e32c)

 - 와이파이 동글
![download](https://github.com/user-attachments/assets/64725752-622d-4c50-a9dc-3d2bb5b0ac12)

 - 웹캠(USB Camera), 또는 CSI Camera (라즈베리파이 V2)
![download](https://github.com/user-attachments/assets/bab07b07-4cfa-40df-8c01-ca99b5d97904)

 - 64기가 이상 마이크로sd카드
![download](https://github.com/user-attachments/assets/1e9b401b-f35d-4f12-a0f8-a7ab7f46a398)

 - 그외 쿨링펜, lcd, 또는 모니터. hdmi
```
 



이미지  굽기 위해 필요한 것들
```
sd card formatter  download
balenaetcher download --->  이미지 굽기
제슨나노에 sd넣고 우분투 설치
```  

### 온도 확인과 쿨링팬
***
jtop : system monitoring tool
terminal 열기
```
sudo apt install python3-pip
sudo -H pip3 install -U jetson-stats
```
만약 에러가 뜨면 sudo apt-get upgrade, sudo apt-get update해준다.
jetson-stats-4.2.3 가 써진 걸 확인.
이제 온도를 확인하자
```
reboot
jtop
```
이제 쿨링팬을 돌려보자
```
sudo sh -c 'echo 128 > /sys/devices/pwm-fan/target_pwm'
```
다시 온도를 확인해보자. 온도가 많이 떨어진다.

### 카메라
***
카메라를 인식하고 실행하자.
```
~$  ls /dev/vi*
~$ git clone https://github.com/jetsonhacks/USB-Camera.git
~$ cd USB-Camera
python3 usb-camera-gst.py
```





























