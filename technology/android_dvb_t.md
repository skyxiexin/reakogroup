# 这个文件用于记录一些Android+DVB-T2 S905D项目的一些开发资料

## 控制tuner 5V输出
>>>
 * 此驱动用于接口控制tuner 5V的输出接口
 * 此接口在/sys/class/dvbtgpio/control
 * echo 1 > /sys/class/dvbtgpio/control 可以使得tuner 输出5V电压
 * echo 0 > /sys/class/dvbtgpio/control 可以使得tuner 输出5V电压为0V
>>>
