# mount 挂载移动硬盘

```bash
# 列印所有盘
sudo fsblk
# 检查文件系统类型
sudo fdisk -l /dev/sdb
# 如果文件系统是 NTFS，则需要安装 ntfs-3g
sudo pacman -S ntfs-3g
# 创建挂载点：
sudo mkdir -p /mnt/mydrive
# 使用 mount 命令挂载设备
sudo mount -t ntfs /dev/sdb1 /mnt/mydrive
# 检查和修复：  NTFS 文件系统
sudo ntfsfix /dev/sdb1
```