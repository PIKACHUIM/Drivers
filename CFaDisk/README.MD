# CFaDisk驱动

## 软件说明

**cfadisk.inf驱动**能够**将内置SD卡读卡器变成本地磁盘**，解决一些软件不能安装在SD卡/U盘/移动硬盘等设备上的问题。

## 使用教程

1. 下载[Import.zip]()双击`Import.zip/Import.exe`安装证书

2. 右键Windows菜单，选择`Powershell（管理员）` / `终端（管理员）`，并执行：

   ```
   bcdedit /enum all
   bcdedit /set {default} testsigning on
   bcdedit /set nointegritychecks on
   bcdedit /set testsigning on
   bcdedit /debug ON
   bcdedit /bootdebug ON
   ```

3. 进入对应架构文件夹，`右键`**inf文件**，然后点击`安装`

## 其他说明

自建PKI根证书为`Pikachu Fake CA RSA`

本驱动签名的自建时间戳服务器的证书由此颁发

该证书系统专用于虚拟签名，请问用于生产环境

更多信息请访问`https://cert.pika.net.cn/`
