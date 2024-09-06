# Jetson Nano
***
```
 1. Jetson Nano Setting 준비물


        - jetson nano 4gb

        - c type power adapter
  
        - 와이파이 동글
  
        - 웹캠(USB Camera), 또는 CSI Camera (라즈베리파이 V2)
  
        - 64기가 이상 마이크로sd카드
  
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
제슨나노가 카메라를 인식하는 명령어
    ~$  ls /dev/vi*






























