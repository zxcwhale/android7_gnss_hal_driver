# 卫星定位接收机HAL驱动

适用于Android7或Android8
对于Android4, Android5, Android6, 请使用项目[android_hal_gpsbds](https://git    hub.com/zxcwhale/android_hal_gpsbds).
对于Android9或Android10, 请使用项目[android9_gnss_hal_driver](https://github.    com/zxcwhale/android9_gnss_hal_driver).
## 使用方法

1. 修改gps_zkw.c文件中的`GPS_CHANNEL_NAME`为接收机的TTY号.
2. 修改gps_zkw.c文件中的`TTY_BAUD`为接收机实际的波特率, 默认为`B9600`.
3. 在Android开发环境下编译.
4. 将编译结果gps.XXXX.so文件用adb push到Android设备的/system/lib/hw目录下. 如果是64位Android, 则push到/system/lib64/hw目录.

## 可能的问题

1. 如果编译出现找不到`ALOGD`, `ALOGE`的报错, 可以尝试将`ALOGD`改为`LOGD`, `ALOGE`改为`LOGE`.
