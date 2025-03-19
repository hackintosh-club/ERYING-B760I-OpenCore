## 尔英 PHANTOM WING B760-I DDR4 黑苹果 OpenCore EFI

![image](ScreenShot/ERYINGB760I.png)

### [ENGLISH](README.EN.md)

[OpenCore 1.0.4](https://github.com/acidanthera/OpenCorePkg)

### macOS

- macOS Monterey 12.x
- macOS Ventura    13.x 
- macOS Sonoma   14.x
- macOS Sonoma    15.x

### 硬件

- 芯片组: B760
- Bios 版本: RAP23006（2023-11-03）
- 处理器: 英特尔12代 i5-12400
- 内   存: 金百达银爵系列C18  32G（16G*2套条）DDR4 3600MHz
- 硬   盘: 京造鲲鹏 2T Windows + MacOS
- 核   显: 英特尔超核心显卡770 (仅在Windows中可以使用)
- 独   显: 蓝宝石 RX580 2304流处理器
- 声   卡: 瑞昱 ALC897
- 有线网卡: 瑞昱 RTL8125B 2.5GB
- 无线网卡: 英特尔 AX211
- 机   箱: 笨牛 U35 9升
- 电源: 全汉 MS500 经典版 80铜牌

### BIOS设置

```
Advanced
  |-- Super IO Configuraion
     |-- Serial Port 1 Configuration : Disabled
  
  |-- PowerManagement Configuration
     |-- Wake on LAN : Disabled
  
  |-- CSM Configuration
	      |-- Video：UEFI  ( need reboot )
	      |-- CSM Auto Switch : Disabled 
	      |-- CSM Support : Disabled
 
Chipset
  |-- Primary Display : Auto
  |-- VT-d : Enabled

Boot
  |-- Fast Boot : Disabled

Security
  |-- Secure Boot Mode  : Disabled

```

### 注意事项

 - 安装成功后必须使用 [OpenCore Configurator](https://mackie100projects.altervista.org/opencore-configurator/) 或者 [OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools) 生成你自己的 SMBIOS
 - 此EFI中的英特尔无线网卡驱动[AirportItlwm.kext](https://github.com/OpenIntelWireless/itlwm/releases)仅适用于 MacOS 15 Sequoia ,安装其它版本请自行下载替换此驱动
 - **WiFi 需使用 [OCLP-Mod by laobamac](https://github.com/hackintosh-club/intel-nuc10/releases/tag/oclp) 打入驱动补丁**
 - 如需使用带有小核心的CPU，必须勾选配置文件中Kernel--ProvideCurrentCpuinfo选项

### 参考内容

[1.黑苹果安装过程演示](https://hackintosh.club/d/10000060)

[2.英特尔无线网卡WiFi驱动](https://hackintosh.club/d/10000015)

[3.英特尔无线网卡蓝牙驱动](https://hackintosh.club/d/10000017)

[4.我的B站黑苹果教程](https://space.bilibili.com/244390800/video)

[6.黑果之家](https://hackintosh.club/)

### 联系我们

QQ群: 23304408

![image](ScreenShot/QRCode.png)



### 常用工具

- [Hackintool](https://github.com/headkaze/Hackintool) 
- [OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools) AKA `OCAT`.
- [OpenCore Configurator](https://mackie100projects.altervista.org/opencore-configurator/) AKA `OCC`.
- [gibMacOS](https://github.com/corpnewt/gibMacOS) Build your own MacOS image.
- [ProperTree](https://github.com/corpnewt/ProperTree) Plist editor.