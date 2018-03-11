### <h3>SSHAutoLogin</h3>
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
