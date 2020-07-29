# namespace 学习

参考文档：

* [https://coolshell.cn/articles/17010.html](https://coolshell.cn/articles/17010.html)
* [https://coolshell.cn/articles/17029.html](https://coolshell.cn/articles/17029.html)
* [https://man7.org/linux/man-pages/man7/namespaces.7.html](https://man7.org/linux/man-pages/man7/namespaces.7.html)

## 系统调用

* `clone()` 用来创建一个新的进程
* `unshare()` 使某进程脱离某个namespace
* `setns()` 把某进程加入到某个namespace

## 分类

* Mount
* UTS : hostname & NIS domain name
* IPC
* PID
* Network
* User


## IPC 相关命令

```shell
ipcmk # 创建ipc资源
ipcrm # 移除ipc资源

ipcs -a # 显示所有的IPC设施
ipcs -q # 显示消息队列
ipcs -s # 显示信号量
ipcs -m # 显示共享内存
ipcs -q/s/m -i <id> # 查看详情
ipcs -q/s/m -l # 显示限制
ipcs -q/sm -c # 显示 creators/owners
ipcs -p # 显示最近访问过IPC设施的进程ID
ipcs -t # 显示IPC设施的最后操作时间
ipcs -u #显示状态
```

# 其他相关知识点

* chroot
* rootfs