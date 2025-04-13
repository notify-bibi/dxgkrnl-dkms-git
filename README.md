## dxgkrnl-dkms
这是一个为 Arch Linux 打包的 dxgkrnl 内核模块。dxgkrnl 是集成到 WSL2 Linux 内核中的 DirectX 驱动程序。



本项目基于 staralt/dxgkrnl-dkms ，并应用了两个补丁以解决编译和运行时的问题。通过将这些步骤打包成一个 AUR 包，简化了在 Arch Linux 上安装和维护该模块的过程。

### 安装方法


前往：https://github.com/notify-bibi/hyperv-vgpu-linux 有我实验好的一套脚本

在 archlinux 6.14.2-arch1-1 上成功




手动克隆并构建：
https://github.com/notify-bibi/hyperv-vgpu-linux/blob/master/install-dxgkrnl.sh

or

```bash
git clone https://github.com/ssxwcz/dxgkrnl-dkms.git
cd dxgkrnl-dkms
# 如果和你的linux kernal版本不匹配，需要编辑PKGBUILD，修改两处 wsl-6.14-rolling 的版本为对应您机器的内核版本，查看： uname -r 
# 确认后开始安装
makepkg -si OPTIONS=-debug
sudo modprobe dxgkrnl

# modinfo 成功执行则安装成功
modinfo dxgkrnl

```


### 测试

```bash
test_gpu.sh
但是搞笑的是d3d12 & 7900xtxt 才500+fps. llvmpipe 1100 fps
```


### 参考

-  [staralt/dxgkrnl-dkms](https://github.com/staralt/dxgkrnl-dkms)。
-  [ssxwcz/dxgkrnl-dkms-git](https://github.com/ssxwcz/dxgkrnl-dkms-git) 致谢！