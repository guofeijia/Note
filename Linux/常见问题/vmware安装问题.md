*  启动时提示：smbus host controller not enabled

  使用vi或者vim进入 /etc/modprobe.d/blacklist.conf文件  在末尾加入  blacklist i2c-piix4  保存退出 然后 reboot重启

*  使用ip addr 或者ifconfig 都无法正确查看虚拟机的IP地址

  原因：centOS默认不开启ens33网卡，解决方法：vi /etc/sysconfig/network-scripts/ifcfg-ens33

  将ONBOOT=no  修改为 yes  保存退出并重启网络服务  sudo service network restart  再次输入ip a  查看IP地址



