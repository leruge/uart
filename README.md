# 树莓派创建BLE GATT服务器

## 安装流程
1. `sudo apt-get update` 更新软件列表
2. `sudo apt-get upgrade` 更新本地软件
3. `sudo apt-get install libdbus-1-dev libglib2.0-dev libudev-dev libical-dev libreadline-dev python3 python3-pip python3-docutils libcairo2-dev libxt-dev libgirepository1.0-dev -y` 安装依赖
4. `wget www.kernel.org/pub/linux/bluetooth/bluez-5.64.tar.xz` 下载bluez
5. `tar xvf bluez-5.64.tar.xz && cd bluez-5.64` 解压
6. `./configure --prefix=/usr --mandir=/usr/share/man --sysconfdir=/etc --localstatedir=/var --enable-experimental` 配置
7. `make -j4 && sudo make install` 编译安装
8. `pip install dbus-python` dbus
8. `pip install pycairo` gi依赖
9. `pip install PyGObject` gi依赖
10. 下载代码
10. `python uart_peripheral.py` 启动