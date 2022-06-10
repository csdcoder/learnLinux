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

6. 安装中文输入法https://juejin.cn/post/7030337513407381541

   ```bash
   sudo apt-get install fcitx
   sudo dpkg -i sogoupinyin_版本号_amd64.deb
   # 如果安装过程中提示缺少相关依赖，则执行如下命令解决：
   sudo apt -f install
   #卸载系统ibus输入法框架
   sudo apt purge ibus
   ```

   

6. 安装typorahttps://download.typora.io/linux/typora_0.11.18_amd64.deb

8. 安装clash for windows

   从 [GitHub - Fndroid/clash_for_windows_pkg](https://github.com/Fndroid/clash_for_windows_pkg) 下载 CFW，注意下载 `Clash.for.Windows-x.xx.x-x64-linux.tar.gz`

   将其解压到 `/usr/local/cfw`

   ```bash
   tar zxvf Clash.for.Windows-0.19.5-x64-linux.tar.gz -C cfw --strip-components 1
   ```

   创建 `~/.local/share/applications/cfw.desktop` 用于显示桌面图标

   ```bash
   touch ~/.local/share/applications/cfw.desktop
   tee ~/.local/share/applications/cfw.desktop <<-'EOF'
   [Desktop Entry]
   Version=1.0
   Name=Clash For Windows
   GenericName=Clash For Windows
   Comment=Clash For Windows for Linux
   Exec=/usr/local/cfw/cfw
   Terminal=false
   Type=Application
   Icon=clash
   Categories=Network
   EOF
   ```

7. 安装有道英文词典

10. Nvida

   ```shell
   # Install tool for hardware detection
   sudo apt install nvidia-detect
   
   # Perform the scan
   sudo nvidia-detect
   
   # Install recommended driver. It is nvidia-driver for me. Yours could be different.
   sudo apt install nvidia-driver
   ```