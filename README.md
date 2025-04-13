## dxgkrnl-dkms
这是一个为 Arch Linux 打包的 dxgkrnl 内核模块。dxgkrnl 是集成到 WSL2 Linux 内核中的 DirectX 驱动程序。



本项目基于 staralt/dxgkrnl-dkms ，并应用了两个补丁以解决编译和运行时的问题。通过将这些步骤打包成一个 AUR 包，简化了在 Arch Linux 上安装和维护该模块的过程。

### 安装方法


前往：https://github.com/notify-bibi/dxgkrnl-dkms-git



手动克隆并构建：
```bash
git clone https://github.com/ssxwcz/dxgkrnl-dkms.git
cd dxgkrnl-dkms
makepkg -si


test_gpu.sh
但是搞笑的是d3d12 & 7900xtxt 才500+fps. llvmpipe 1100 fps

```

### 参考

-  [staralt/dxgkrnl-dkms](https://github.com/staralt/dxgkrnl-dkms)。
-  [ssxwcz/dxgkrnl-dkms-git](https://github.com/ssxwcz/dxgkrnl-dkms-git) 致谢！