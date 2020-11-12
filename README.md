# MatrixClock
- 一个使用ESP8266和LED点阵制作的高精度时钟

## 视频演示
- 哔哩哔哩 <https://www.bilibili.com/video/BV11a4y1s7Tq/>  

## 源码来源
- <https://github.com/schreibfaul1/ESP8266-LED-Matrix-Clock>
  
## 修改了什么
- 将原作者使用的共阴极LED模块改为了共阳极LED模块（手头现有的）
- 将数字字体稍作修改，改的更丑了（手动滑稽）
- 添加了中文星期显示，可自行修改星期七或者星期天（自制？）
- 将显示模式改为了更符合中国人的阅读习惯（不知道你习不习惯，反正我是这样比较习惯）
- 将固定时间滚动改为了随机时间滚动
  
## 如何制作
1. 下载[Gerber_共阳极PCB.zip](https://github.com/myseil/MatrixClock/raw/main/Gerber_%E5%85%B1%E9%98%B3%E6%9E%81PCB.zip)，然后到嘉立创5元打板。
2. 将打样回来的PCB用美工刀分开，分成两张PCB。
3. 根据[`Bom.html`]文件进行焊接，注意CH340E和TPYE-C母口的焊接，不要连锡，不然容易烧板子。
4. 焊接完成后，通过Type-C数据线连接电脑和板子，检查电脑是否正确识别。
5. 下载[Arduino](https://www.arduino.cc/en/software)，安装完成后用Arduino打开[`MatrixClock.ino`]，会提示是否创建文件夹，同意即可
6. 点击Arduion的上传按钮编译[`MatrixClock.ino`]文件，编译的同时按下PCB上面的<font color=red>[`重启`]</font>和[`下载`]按键，然后松开[`重启`]按键，等待程序刷入即可。
7. 当Arduion提示完成后，按下PCB上面的[`重启`]按键，即可通过LED点阵看到效果。

>注意：第一次会提示[`Setup`]，用手机通过[`Esptouch`]APP进行WIFI配网即可。


## 鸣谢
- [立创EDA](https://lceda.cn/) - 超级简单易用易学的国产EDA
- [嘉立创](https://www.jlc.com/) - 5元10x10cm打样，顺丰包邮。真香警告！
- [立创商城](https://www.szlcsc.com/) - 元件齐全，有活动可以白嫖！ 

## 硬件开源地址
- [OSHWHub硬件开源平台](https://oshwhub.com/myseil/gao-jing-duled-dian-zhen-shi-zhong)
