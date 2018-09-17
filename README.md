### <h3>SSHAutoLogin</h3>
一般情况下，公司为了从安全角度考虑，所有的服务器都在内网，公网访问、管理服务器都要先通过一台跳板机，然后再由跳板机登录到相应的服务器进行操作，跳板机与服务器的连接都是内网地址。
![痛点](https://user-images.githubusercontent.com/24430878/45608187-0826a580-ba84-11e8-897a-1759327dc6cf.jpg)
由于每次都需要手动输入一些选项，浪费时间，故编写此expect自动交互脚本，方便用户登录跳板机。
### <h3>使用方式</h3>
- 给jump脚本文件添加可执行权限，并执行
```
chmod +x jump
./jump
```
- 可以将jump脚本文件软链接到/usr/local/bin下，这样便可以在终端中全局使用jump
```
ln -s $PWD/jump /usr/local/bin/
jump
```
### 提示
使用脚本前注意以下几点：
- 修改适合自己的*jumpserver*与*host*地址
- 使用脚本前，确保安装expect  
```
Linux下：yum install expect 
Mac下：brew install expect
```

#### 用户反馈:
1. In my case, when I use expect login my remote machine, rz/sz failed. But login without expect, rz/sz succeed.
