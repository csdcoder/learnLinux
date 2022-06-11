# 安装Debian11后应该做的事

1. 添加用户到sudo组

   ```bash
   su ~
   usermod -aG sudo andy
   ```

2. 更改安装源

2. 安装git

4. 安装edge浏览器

   (1). Download the package from [Edge Web browser](https://www.microsoft.com/zh-cn/edge)

   (2). Run commands

   ```bash
   sudo dpkg -i microsoft-edge-stable_xxxx_xxxx_amd64.deb
   sudo apt -f install
   # run the first command again
   ```
   
5. 安装chromium

   ```bash
   sudo apt install chromium
   ```

6. 安装中文输入法

   ```bash
   sudo apt-get install fcitx
   # 提前在官网下载好deb安装包
   sudo dpkg -i sogoupinyin_版本号_amd64.deb
   # 如果安装过程中提示缺少相关依赖，则执行如下命令解决：
   sudo apt -f install
   #卸载系统ibus输入法框架
   sudo apt purge ibus
   ```

7. 安装 [typora](https://download.typora.io/linux/typora_0.11.18_amd64.deb)

7. 安装neovim

9. 安装vscode

   在 vscode 的设置中 enable vimrc配置方式，并填写 vimrc 文件地址

10. 安装gnome-tweaks工具

    ```bash
    sudo apt-get install gnome-tweaks
    ```

    安装完之后，直接在终端输入 `gnome-tweaks` 即可运行该工具。然后调整字体缩放比例

11. 安装有道英文词典，过程中需要安装依赖

12. 安装clash for windows

    1. 从 [GitHub - Fndroid/clash_for_windows_pkg](https://github.com/Fndroid/clash_for_windows_pkg) 下载 CFW，注意下载 `Clash.for.Windows-x.xx.x-x64-linux.tar.gz`

    2. 下载解压后运行**cfw**

       ```bash
       tar xzvf Clash.for.Windows-0.19.12-x64-linux.tar.gz  
       ./cfw
       ```
       
    3. 点击Profiles，输入在”机场“获取的配置文件链接，下载配置文件（或者从windows复制）
    
    4. 修改网络代理为手动：Proxy 127.0.0.1 7890
    
    5. 选择全局端口 Global
    
    6. 连接成功
    
    7. 有时需要临时在终端启用代理时，可以使用如下命令(不好使)
    
       ```bash
       export http_proxy=http://127.0.0.1:7890
       export https_proxy=http://127.0.0.1:7890
       ```
    
    > 参考出处：
    >
    > https://zhuanlan.zhihu.com/p/481794459
    >
    > https://bestoko.cc/p/linux-clash-for-windows/
    
13. 安装网易云

    解决 Linux 下的网易云音乐字体过小问题

    使用编辑器修改 `/opt/netease/netease-cloud-music/netease-cloud-music.bash` 的内容，在最后一行中添加 `--force-device-scale-factor=xxx`。 xxx 是字体放大的倍数

    ```bash
    #!/bin/sh
    HERE="$(dirname "$(readlink -f "${0}")")"
    export LD_LIBRARY_PATH="${HERE}"/libs
    export QT_PLUGIN_PATH="${HERE}"/plugins
    export QT_QPA_PLATFORM_PLUGIN_PATH="${HERE}"/plugins/platforms
    exec "${HERE}"/netease-cloud-music --force-device-scale-factor=1.25 $@
    ```

14. 安装vlc

15. 可选：修改系统语言

    ```bash
    sudo dpkg-reconfigure locales
    ```
    
16. Linux 下将 CapsLock 转换成 Esc（在gnome-tweaks-tool里可以改键盘映射）

17. 安装Flameshot，Flameshot 的键盘快捷键命令

    ```bash
    /usr/bin/flameshot gui
    ```







> 参考信息：
>
> [debian系统 设置常用工具的键盘快捷键](https://blog.csdn.net/weixin_43274002/article/details/118229442)
>
> 在终端上输入 **dpkg -l | grep xxxx**即可获取对应工具的 command命令
