---
lang: zh-CN
title: 清理 Manjaro 系统空间
description: 清理 Manjaro 系统空间
time: 2021-03
---

## 清理 Manjaro 系统空间

- ``sudo du -h --max-depth=1``查询当前目录下各文件夹和文件空间占用情况
- ``sudo pacman -Sc`` 清除未安装的软件包的缓存
- ``sudo pacman -Scc`` 清除全部软件包的缓存
- ``sudo pacman -R $(pacman -Qdtq)`` 清除无用的包文件
- ``journalctl --disk-usage`` 查看日志文件着那用了多少空间
- ``journalctl --vacuum-time=1w`` 只保留最近一周的日志

```shell
# 进入系统根目录
/
# 执行以下命令查看各目录大小
sudo du -h --max-depth=1
```

一般情况就是

- /home
- /var
- /opt
- /usr

空间占用可能是最多的

----