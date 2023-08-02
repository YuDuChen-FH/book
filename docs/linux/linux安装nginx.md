#### linux安装nginx

1. 安装gcc

   ```shell
    yum install gcc-c++  
   ```

2. *安装PCRE pcre-devel* 

   ```shell
   yum install -y pcre pcre-devel  
   ```

3. *安装zlib* 

   ```shell
   yum install -y zlib zlib-devel 
   ```

4. *安装Open SSL* 

   ```shell
   yum install -y openssl openssl-devel
   ```

5. 去官网下载需要的版本

6. 解压文件

   ```shell
   tar -zxvf xxx.tar.gz
   ```

7. 进入文件夹

8. 安装nginx

   ```shell
   #编译 执行命令 考虑到后续安装ssl证书 添加两个模块  如不需要直接执行./configure即可
   ./configure --with-http_stub_status_module --with-http_ssl_module
   #执行make命令(要是执行不成功请检查最开始安装的四个依赖有没有安装成功)
   make
   #执行make install命令
   make install
   ```

9. 启动nginx

   ```shell
   cd /usr/local/nginx/sbin
   # 默认配置文件启动
   ./nginx
   
   # 指定配置文件启动
   ./nginx -c  /安装nginx的路径/conf/nginx.conf
   ```

10. 停止或启动nginx

    ```shell
    cd /usr/local/nginx/sbin
    # 停止指令
    ./nginx -s stop
    # 或
    ./nginx -s quit
    
    # 重启命令
    ./nginx -s reload
    
    # 查看nginx进程
    ps -ef|grep nginx
    ```

11. 设置开机自启

    ```shell
    #编辑
    vim /etc/rc.local
     
    #最底部增加这一行
    /usr/local/nginx/sbin/nginx
    ```

    