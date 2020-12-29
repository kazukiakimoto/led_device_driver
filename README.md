# led_device_driver
![Alt] 
(https://github.com/kazukiakimoto/led_device_driver/blob/master/image/IMG_6012.PNG)

# 概要
RaspberryPi3ModelB上でLED三個を光らせるプログラム

# 説明
このデバイスドライバはキーボードのrで赤色のLED、bで青色のLED、yで黄色のLEDを点灯させることが出来、dで全消灯します。

# デモ
　URL:
 
# スペック
- PC:Raspberry Pi 3 Model B  
- OS:Ubuntu 20.04.1 LTS  
- Parts:
  - LED  
    - red http://akizukidenshi.com/catalog/g/gI-06245/ 
    - blue https://akizukidenshi.com/catalog/g/gI-06247/  
    - yellow https://akizukidenshi.com/catalog/g/gI-06248/  
  - Bread Board http://akizukidenshi.com/catalog/g/gP-05294/  
  - jumper wire 
    - male-male http://akizukidenshi.com/catalog/g/gC-05371/  
    - male-female http://akizukidenshi.com/catalog/g/gC-08933/  
 
# インストール
~~~
$ git clone https://github.com/kazukiakimoto/led_device_driver
~~~

# 使い方
~~~
$ make
$ sudo insmod myled.ko  
$ sudo chmod 666 /dev/myled0 
ex)赤色のLEDを光らせる
$ echo r > /dev/myled0
ex)青色のLEDを光らせる
$ echo b > /dev/myled0
ex)黄色のLEDを光らせる
$ echo y > /dev/myled0
ex)全消灯
$ echo d > /dev/myled0
~~~


# LICENSE
GNU General Public License v3.0
https://www.gnu.org/licenses/gpl-3.0.ja.html
