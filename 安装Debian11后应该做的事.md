# 安装Debian11后应该做的事

1. 更改安装源

1. 安装typorahttps://download.typora.io/linux/typora_0.11.18_amd64.deb

1. 添加用户到sudo组

   ```bash
   su ~
   usermod -aG sudo andy
   ```

2. 更改软件源

3. Nvida

   ```shell
   # Install tool for hardware detection
   sudo apt install nvidia-detect
   
   # Perform the scan
   sudo nvidia-detect
   
   # Install recommended driver. It is nvidia-driver for me. Yours could be different.
   sudo apt install nvidia-driver
   ```

4. 安装中文输入法

   https://juejin.cn/post/7030337513407381541

5. 安装edge浏览器

6. 