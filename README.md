# summary
个人总结和经验
参考链接：https://github.com/mzlogin/awesome-adb

查看版本： adb version
安装apk: adb install demo.apk
保留数据和缓存文件重新安装： adb install –r demo.apk
安装到sd卡： adb install –s demo.apk
卸载apk: adb uninstall <packagename>
卸载apk，但是保存数据和缓存文件： adb uninstall –k <packagename>
显示已连接设备： adb devices  

启动和关闭adb服务：
	adb start-server      adb kill-serve

列出手机安装的所有包名：
	adb shell pm list packages
列出手机所有系统应用包名：
	adb shell pm list packages –s
列出手机所有第三方应用包名：
	adb shell pm list packages -3

清除应用数据和缓存：
	adb shell pm clear <packagename>
启动应用：
	adb shell am start –n <packagename>/<appActivity>
强制关闭应用：
	adb shell am force-stop <packagename>

查看日志： adb logcat
重启： adb reboot
获取序列号： adb get-serialno  
获得MAC地址：adb shell cat /sys/class/net/wlan0/address
查看设备型号： adb shell getprop ro.product.model
查看系统版本： adb shell getprop ro.build.version.release
查看屏幕分辨率： adb shell wm size
查看屏幕密度： adb shell wm density

屏幕截图：
	adb shell screencap –p /sdcard/sc.png 
发送手机截图到电脑指定路径：
	adb pull /sdcard/sc.png  C:\Users\MaiBenBen\Desktop\image\
屏幕录制：
	adb shell screenrecord /sdcard/demo.mp4
发送手机视频到电脑指定路径：
	adb pull /sdcard/demo.mp4 C:\Users\MaiBenBen\Desktop\image\ 
