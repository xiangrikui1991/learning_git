## 1. Failed to connect to github.com port 443: Timed out
```git
#问题：Failed to connect to github.com port 443: Timed out
harveyhwliu@harveyhwliu-PC0 MINGW64 /i/codeRepo/Machine_Learning_Repository (master)
$ git pull origin master
fatal: unable to access 'https://github.com/harveyhwliu/Machine_Learning_Repository/': Failed to connect to github.com port 443: Timed out

#解决方案：设置http访问代理
harveyhwliu@harveyhwliu-PC0 MINGW64 /i/codeRepo/Machine_Learning_Repository (master)
$ git config --global http.proxy web-proxy.tencent.com:8080

#验证：
harveyhwliu@harveyhwliu-PC0 MINGW64 /i/codeRepo/Machine_Learning_Repository (master|MERGING)
$ git config --get http.proxy
web-proxy.tencent.com:8080

#业务再次访问，正常

```

## 2. git 删除远程仓库中的内容
&emsp;&emsp;在github上只能删除仓库,却无法删除文件夹或文件, 所以只能通过命令来解决
```git
git pull origin master
git rm 002配置解析模块_toml笔记.md
git rm -rf 002类型/
git add *
git commit -m "update golang repository"
git push -u origin master

```
