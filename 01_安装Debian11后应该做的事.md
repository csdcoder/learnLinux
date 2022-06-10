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

7. 安装vscode

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
    
    7. 有时执行wget或curl来下载国外的东西，需要临时在终端启用代理时，可以使用如下命令
    
       ```bash
       export http_proxy=http://127.0.0.1:7890
       export https_proxy=http://127.0.0.1:7890
       ```
    
    > 参考出处：
    >
    > https://zhuanlan.zhihu.com/p/481794459
    >
    > https://bestoko.cc/p/linux-clash-for-windows/
    
    
