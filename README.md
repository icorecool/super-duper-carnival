# super-duper-carnival
Some small projects based on arduino uno
本项目是基于 arduino uno开发的一款智能开关门系统
实现用指定ic卡来控制开关门，蓝牙app控制舵机实现开关门，和开门后的灯带驱动。

项目硬件包括 arduino uno、0.96寸OLED、9g舵机、rc-522射频模块、hc-05蓝牙模块、ws2812彩色灯带
其中ws2812采用cpldcpu编写的light_ws2812 V2.4驱动来驱动。

常见问题：
如果ws2812出现LED闪烁或者没有显示预期的颜色，请查看如下说明：
这通常是电源供电不足的问题。
是否按照数据表中的指示为每个LED使用旁路电容？不使用旁路电容可能会出现该问题。
您的电源能否提供所需的电流水平？如果在最大亮度下设置为白色，则每个LED将消耗60mA电流，一个USB端口几乎不能提供10个LED。
LED仅显示白色：如果您的MCU的实际时钟频率低于代码中F_CPU给出的频率，则可能发生这种情况。

如果oled不正常显示，请查看如下说明：
	如果使用默认的I2C引脚D4 / D5，则将OLED_RESET更改为其他引脚。
 如果缺少相应库函数导致无法编译，请移步可以在Arduino库管理器中找到。
 如果屏幕闪烁请检查接线问题，源程序中已经写好接线。

下载整个压缩包直接用arduino ide打开.ino结尾的程序即可。
要把ic验证部分更改为自己所持有卡的信息。
