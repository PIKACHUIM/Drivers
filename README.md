# Windows 专用 / 特殊 / 自签名驱动文件存档

# Windows Exclusive/ Special/ Self-signed Drivers Archives

## 使用前提 / Precondition

1. ### 下载证书信任文件：[点击下载 Import.zip](https://github.com/PIKACHUIM/Drivers/raw/main/Import.zip)

2. ### 点击`Import.zip/Import.exe`安装证书

## 驱动列表 / Drivers List 

- ### [CFaDisk](https://github.com/PIKACHUIM/Drivers/tree/main/CFaDisk)

  > #### CFaDisk - 把SD卡 / 读卡器 / 内存卡识别为本地硬盘
  >
  > CFaDisk - Identify SD card/ Reader / Memory Card as Local Hard Drive
  >
  > ##### 自建CA下载：[CFaDisk - 自建系统CA系统签名驱动](https://github.com/PIKACHUIM/Drivers/raw/main/CFaDisk/Drvier-Pika.zip)     
  >
  > ##### 伪造时间戳：[CFaDisk - 伪造时间CA证书签名驱动]()
  >
  > 选择一个下载就行，两者区别：
  >
  > - **自建CA是自己信任的证书签名，Win10开启了Secure Boot无法使用，但是信任了不会被黑名单**
  > - **伪造时间戳是利用泄漏EV代码证书和自建CA签发的时间戳，可以过Secure Boot但可能被黑名单**

- 

