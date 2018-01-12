# 这个文件用于记录一些Android+DVB-T2 S905D项目的一些开发资料

## 控制tuner 5V输出
>>>
 * 此驱动用于接口控制tuner 5V的输出接口
 * 此接口在/sys/class/dvbtgpio/control
 * echo 1 > /sys/class/dvbtgpio/control 可以使得tuner 输出5V电压
 * echo 0 > /sys/class/dvbtgpio/control 可以使得tuner 输出5V电压为0V
>>>

---

## 设置数码管显示频道等信息

修改log
```
xcf@reako-ubuntu-14:~/S905D/xinke/s905d_svn/S905D/amlogic_905d/external/fd650_svr$ svn commit -m "DEV: Changed the fd650 display channel on property sys.dvb.active set 1"
Sending        Android.mk
Sending        src/fd650_svr.c
Transmitting file data ..
Committed revision 48.
```
>
> 修改后，进入dvb应用，请设置property sys.dvb.active 为1，退出dvb应用时，还原为0.
> 当sys.dvb.active设置为1后，数码管显示不由fd650_svr这个线程控制
> 开发者可以通过/dev/fd650_dev这个驱动接口进行操作。

> 比如需要显示0001这个频道

> 可以： echo 0001 > /dev/fd650_dev.
>

---

## 开机广告应用代码仓库
```
git clone xcf@192.168.1.18:/home/xcf/git/code_repository/boot_ad.git

password: XCF@mele100

```
---

## 应用启动广告代码仓库
```
git clone xcf@192.168.1.18:/home/xcf/git/code_repository/app_start_ad.git

password: XCF@mele100

```
