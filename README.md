# linuxhacker
## 使用方法
```
  _ _                  _                _             
 | (_)_ __  _   ___  _| |__   __ _  ___| | _____ _ __ 
 | | | '_ \| | | \ \/ / '_ \ / _` |/ __| |/ / _ \ '__|
 | | | | | | |_| |>  <| | | | (_| | (__|   <  __/ |   
 |_|_|_| |_|\__,_/_/\_\_| |_|\__,_|\___|_|\_\___|_|
    				version: 1.0.0

Usage: golang -p [plugin] -c [choice]
Options:
-p	choose the plugin
-c	choose the choice for the corresponding plugin
```
插件:
- env_check  选项: docker(检查是否处于docker环境),vm(检查是否处于虚拟机中)
- privilege_check 选项: suid,sudo,cap,kernel
- maintance 选项: ssh_soft_link/ssh1,ssh_public_key/ssh2,ssh_key_logger/ssh3,ssh_stealth_login/ssh4,cron,file
- ssh_soft_link/ssh1 ssh软链接权限维持
- ssh_public_key/ssh2 ssh写公钥提权
- ssh_key_logger/ssh3 ssh key logger可以记录下别人ssh登录的密码
- ssh_stealth_login/ssh4 ssh隐身登录,w,last等命令查找不到
- cron 计划任务提权
- file 更改文件的atime,mtiem,实现webshell和一些恶意代码的权限维持
## 开发日志
### 2023 11.12 v1.0.0
- 可探测当前linux系统所处环境(是否是docker,vm等)
- 可探测当前linux系统的各种提权方法(suid,sudo等)
- 自带一些权限维持的模块
