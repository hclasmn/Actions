# Actions
用于自动化处理白嫖EPIC免费游戏

## 使用过程
下载DeviceAuthGenerator
运行程序,在出现的页面里登录Epic账户,然后授权。完成后会出现一个 device_auths.json文件
Fork或者手动导入这个Repo,看你喜好(防止被Github一锅端)
启用Actions,新建一个叫做AUTH_JSON的Secret,并将之前的device_auths.json文件内容粘贴进去。
修改.github/workflows/claim.yml文件,改改自动领取时间什么的。

