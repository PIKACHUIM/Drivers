#### Xilinx - 赛灵思

## 下载地址

### 伪造时间戳（推荐，支持Win10安全启动）：[Xilinx-XDMA- 伪造时间CA证书签名驱动](https://github.com/PIKACHUIM/Drivers/raw/main/Xilinx/XDMA-Fake.zip)

### 自建CA下载（备用，兼容Win7 XP等系统）：[Xilinx-XDMA- 自建系统CA系统签名驱动](https://github.com/PIKACHUIM/Drivers/raw/main/Xilinx/XDMA-Pika.zip)

选择一个下载就行，两者区别：

- **自建CA是自己信任的证书签名，Win10开启了Secure Boot无法使用，但是信任了不会被黑名单**
- **伪造时间戳是利用泄漏EV代码证书和自建CA签发的时间戳，可以过Secure Boot但可能被黑名单**

## 使用教程

1. 下载[点击下载 Import.zip](https://github.com/PIKACHUIM/Drivers/raw/main/Import.zip)双击`Import.zip/Import.exe`安装证书

2. 右键Windows菜单，选择`Powershell（管理员）` / `终端（管理员）`，并执行：

   ```
   bcdedit /enum all
   bcdedit /set {default} testsigning on
   bcdedit /set nointegritychecks on
   bcdedit /set testsigning on
   bcdedit /debug ON
   bcdedit /bootdebug ON
   ```

   （**如果使用了伪造时间戳签名，则不需要此步骤**）

3. 进入对应架构文件夹，`右键`**inf文件**，然后点击`安装`

## 其他说明

自建PKI根证书为`Pikachu Fake CA RSA`

本驱动签名的自建时间戳服务器的证书由此颁发

该证书系统专用于虚拟签名，请问用于生产环境

更多信息请访问`https://cert.pika.net.cn/`
