## arch Linux 在 x86 机器上的安装

### 下载并制作镜像盘（我的基于2020-04-01版本）

### 键盘布局

1. 查看支持的键盘布局

   ```shell
   ls  /usr/share/kbd/keymaps/*/*/*.map.gz
   ```

2. 设置键盘布局

   ```shell
   loadkeys xxx   # 完整路径，默认us键盘布局
   ```

### 连接网络

1. 确保启用了网络接口

   ```shell
   ip  link
   ```

2. 连接到网络（无线网）

   1. 检查网卡是否被装载：`lspci -k` 或 `lsusb -v` 取决于网卡是在 `pci(e)`或`usb`总线上连接。
   2. 获取interface名字：`ifconfig`
   3. 检查无线网络接口是否被创建：`ip  link  set  enp0s31f6`  up
   4. 确定无线接口已运行：`ip  link  show  enp0s31f6`
   5. 打开网络接口：`ifconfig  enp0s31f6  up`
   6. 

