# rock64-openwrt
rock64 v2 （1G DDR）开发板的openwrt固件

# 修改SD rootfs移植版
* 使用mrfixit2001/debian的固件引导 https://github.com/mrfixit2001/debian_builds/releases/download/190531/rock64-debian-mrfixit-190531.img.xz
* 使用openwrt官网的 armvirt64 根文件系统 https://downloads.openwrt.org/releases/22.03.3/targets/armvirt/64/openwrt-22.03.3-armvirt-64-rootfs-ext4.img.gz
* 拷贝mrfixit固件根目录的 /lib/modules 和/lib/firmware 到 openwrt的根文件系统
* 修改 openwrt 根文件系统的 /etc/inittab 文件，添加一行 “ttyS2::askfirst:/usr/libexec/login.sh”
* 使用修改后的openwrt根文件系统引导系统
