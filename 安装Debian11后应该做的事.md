# 安装Debian11后应该做的事

1. 添加用户到sudo组

   ```bash
   su ~
   usermod -aG sudo andy
   ```

2. 更改安装源

3. 安装edge浏览器

4. 安装中文输入法https://juejin.cn/post/7030337513407381541

5. 安装typorahttps://download.typora.io/linux/typora_0.11.18_amd64.deb

6. 安装git

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