#### 开放端口

1. 开放端口号

   ```shell
   firewall-cmd --zone=public --add-port=xxxx/tcp --permanent
   ```

2. 刷新防火墙

   ```shell
   firewall-cmd --reload
   ```

3. 检查端口号是否放开

   ```shell
   firewall-cmd --query-port=5011/tcp
   ```

   