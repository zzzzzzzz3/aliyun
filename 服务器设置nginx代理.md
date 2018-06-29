### 添加秘钥登录服务器
使用`ssh-keygen`生成公私钥，将本地的用户的.ssh目录下的id_rsa.pub公钥拷贝到服务器端的authorized_keys文件中

### 下载nginx
`sudo apt-get update`
`apt-get install nginx`

### 启动nginx
`sudo /etc/init.d/nginx start`

### 修改nginx配置
`vim /etc/nginx/nginx.conf`在`http{...}`里添加`server{listen 80; server_name localhost;}`，然后重新加载`sudo systemctl reload nginx`

### 修改aliyun服务器的安全组
如果无法通过访问到服务器可以修改服务器的安全组规则，添加80端口的访问权限
