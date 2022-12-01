# OrangeKVM
An IPKVM board for OrangePi Zero.  
以香橙派zero为核心的IPKVM模块，可固定于PCIE插槽.  
https://oshwhub.com/blue_beaker/orangepi-ipkvm
  
  
### Features:  
- PCIE mount  
- Power/Reset Buttons and Power/HDD LEDs connected to GPIO via optocouplers.  
- Exports UART0,UART2,USB2,USB3 ports.  
- Emulates keyboard and mouse with CH9329 chip.  
- Emulates USB devices like Mass Storage and Ethernet with OrangePi Zero USB Gadget mode.

### 特性:
- 可固定于PCIE插槽.  
- 已将电源和重启按钮、电源和硬盘灯通过光耦连接到GPIO：
- 引出UART0、UART2、USB2、USB3接口，便于调试和扩展。 
- 模拟键盘鼠标：基于CH9329  
- 模拟存储、网卡等USB设备：使用OrangePi Zero的USB Gadget功能.  


### Requirements  
- An OrangePi Zero
- A USB video capturer with UVC protocol  
- A TF Card for the OrangePi Zero  

### 需求  
- OrangePi Zero  
- USB视频采集卡（UVC协议）  
- 一张TF卡, 用于OrangePi Zero  

### GPIO定义/GPIO Specifications

```Power Button-PA11  
Reset Button-PA12  
Power LED-PA13  
HDD LED-PA2  
```

```电源按钮-PA11  
重启按钮-PA12  
电源灯-PA13  
硬盘灯-PA2  
```
 

### Getting Started
There isn't a prebuilt image yet, you can install armbian and use the following programs for building your IPKVM:
- ustreamer for streaming video from the capturer   
- [This](https://github.com/Blue-Beaker/9329KeyboardRemote) for CH9329 emulated mouse and keyboard; you will also need a program to tunnel the uart for CH9329 to TCP.
- You can emulate usb mass storage with [this](https://linux-sunxi.org/USB_Gadget/Mass_storage).  



### 开始使用
目前没有开箱即用的预构建镜像，可以先使用armbian系统，安装软件来实现ipkvm功能:
- ustreamer 串流捕获到的采集卡画面  
- [此工具](https://github.com/Blue-Beaker/9329KeyboardRemote)通过CH9329模拟键盘鼠标; 还需要使用其他程序将CH9329使用的串口隧道到TCP.
- 可以用此方法模拟usb存储设备：[USB Gadget/Mass storage](https://linux-sunxi.org/USB_Gadget/Mass_storage).

