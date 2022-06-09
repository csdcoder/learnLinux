# 安装Debian11后应该做的事

1. 添加用户到sudo组

   ```bash
   su ~
   usermod -aG sudo andy
   ```

2. 更改安装源

2. 安装git

4. 安装edge浏览器

   https://www.microsoft.com/zh-cn/edge

   https://www.linuxcapable.com/zh-CN/%E5%A6%82%E4%BD%95%E5%9C%A8-debian-11-%E4%B8%8A%E5%AE%89%E8%A3%85-Microsoft-Edge/

   ```
   dpkg -i microsoft-edge-stable_102.0.1245.33-1_amd64.deb
   sudo apt install microsoft-edge-stable -y
   ```

5. 安装Chrome或chromium

   https://www.linuxcapable.com/zh-CN/%E5%A6%82%E4%BD%95%E5%9C%A8-debian-11-%E4%B8%8A%E5%AE%89%E8%A3%85%E8%B0%B7%E6%AD%8C%E6%B5%8F%E8%A7%88%E5%99%A8/

   https://bynss.com/linux/537554.html

4. 安装中文输入法https://juejin.cn/post/7030337513407381541

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

8. Nvida

   ```shell
   # Install tool for hardware detection
   sudo apt install nvidia-detect
   
   # Perform the scan
   sudo nvidia-detect
   
   # Install recommended driver. It is nvidia-driver for me. Yours could be different.
   sudo apt install nvidia-driver
   ```

6. 