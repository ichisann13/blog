**WSL2提供的Archlinux默认是没有AUR和32位库的，需要手动开启**

# 添加archlinuxcn源和开启32位库
```
sudo vim /etc/pacman.conf

# 添加如下内容
[archlinuxcn]
Server = https://mirrors.ustc.edu.cn/archlinuxcn/$arch

[multilib]
Include = /etc/pacman.d/mirrorlist
```

# 更新数据库，安装archlinuxcn的keyring
```
# 更新数据库，安装keyring
sudo pacman -Syy && sudo pacman -S archlinuxcn-keyring

# 安装paru，也可以换成yay
sudo pacman -S paru
```

# 开滚
```
sudo pacman -Syu && paru
```

之后就可以用AUR了

