### 方案一
#### 服务器保持连接
登录服务器修改/etc/ssh/ssh_config，添加如下两句
`
ClientAliveInterval 120
ClientAliveCountMax 720
`
然后重启sshd服务`sudo systemctl restart sshd`

### 方案二
#### 客户端保持连接
修改`/etc/ssh/ssh_config`添加`ServerAliveInterval 120 `，完整如下
`
Host server
    HostName xxx.domain.local
    ServerAliveInterval 120
    User root
`
