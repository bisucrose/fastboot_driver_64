# Fastboot 驱动无法识别如何强制安装

在手机刷机的时候，经常会出现fastboot的驱动无法安装的情况。因为当下流行的驱动实际上是当年乐视手机的通用驱动，有一些签名已经不对了，所以Windows不会为设备安装LeMobile的驱动程序，具体现象如下图所示：

<img src="C:\Users\bi\Desktop\SurfaceDuo\fastboot_driver_64\Readme\image-20251206171447496.png" alt="设备管理器中可以看到Android设备的Fastboot驱动程式未安装，设备无法识别" style="zoom: 50%;" /><img src="C:\Users\bi\Desktop\SurfaceDuo\fastboot_driver_64\Readme\image-20251206171603584.png" alt="终端中可以看到Fastboot命令一直在等待设备" style="zoom: 50%;" />



## 方案一：双击文件中的DPInst64.exe安装驱动

所需的文件可以从以下仓库中下载：[bisucrose/fastboot_driver_64](https://github.com/bisucrose/fastboot_driver_64)

双击DPInst64.exe安装驱动，打开设备管理器查看感叹号还在不在。正常的设备应该可以安装好驱动，安装好长这个样子：

<img src="C:\Users\bi\Desktop\SurfaceDuo\fastboot_driver_64\Readme\image-20251206172040401.png" alt="安装成功" style="zoom:50%;" />

## 方案二：进入设备管理器安装驱动

如果上述方法安装失败，可能是你的设备太新，这时候进入设备管理器打开硬件，选择更新驱动程序，点击**浏览我的电脑以查找驱动程序**，选择刚刚的驱动文件夹，安装驱动

![手动安装](C:\Users\bi\Desktop\SurfaceDuo\fastboot_driver_64\Readme\image-20251206172410731.png)

![image-20251206172552344](C:\Users\bi\Desktop\SurfaceDuo\fastboot_driver_64\Readme\image-20251206172552344.png)

![image-20251206172624451](C:\Users\bi\Desktop\SurfaceDuo\fastboot_driver_64\Readme\image-20251206172624451.png)

这样就安装上了。



## 方案三：强行安装

如果前两种方法都不奏效，比如我的SurfaceDuo就不认这个驱动，那么你在保证驱动可用的前提下，可以强行安装驱动，具体方法如下：

- 跟随方案二到达下图，点击下面的**让我从计算机上的可用驱动程序列表中选取**：

  ![image-20251206172552344](C:\Users\bi\Desktop\SurfaceDuo\fastboot_driver_64\Readme\image-20251206172552344.png)

- 点击显示所有设备：![image-20251206173037921](C:\Users\bi\Desktop\SurfaceDuo\fastboot_driver_64\Readme\image-20251206173037921.png)

- 点击从磁盘安装，选择fastboot驱动文件夹，再选择`android_winusb.inf`，从下面的列表里面选择 Android BootLoader Interface ![image-20251206173259416](C:\Users\bi\Desktop\SurfaceDuo\fastboot_driver_64\Readme\image-20251206173259416.png)

  点击安装即可

  **千万不要选错设备！另外确保这个驱动真的适用于你的设备，否则在刷机时有变砖的可能！**





