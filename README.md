# Actions
用于自动化处理白嫖EPIC免费游戏

## 使用过程
1. 下载[DeviceAuthGenerator](https://github.com/xMistt/DeviceAuthGenerator/releases/)
2. 运行程序,在出现的页面里登录Epic账户,然后授权。完成后会出现一个 `device_auths.json`文件
3. Fork或者手动导入这个Repo,看你喜好(防止被Github一锅端)
4. 启用Actions,新建一个叫做`AUTH_JSON`的Secret,并将之前的`device_auths.json`文件内容粘贴进去。
5. 修改.github/workflows/claim.yml文件,改改自动领取时间什么的。
    ```  
schedule:
    - cron:  '51 16 * * 4'    #修改成其他时间（4改成*就是每天执行一次的意思）
    ```

## 多账户
最后获得的json大概长这样

```
{
    "mcseekeri": {
        "device_id": "114514",
        "account_id": "1919810",
        "secret": "893",
        "user_agent": "DeviceAuthGenerator/1.1.0 Windows/10.0.19041",
        "created": {
            "location": "Neverland",
            "ip_address": "114.51.45.14",
            "datetime": "1970-01-01T00:00:00.000Z"
        }
    }
}
```

如果要多账户签到,那么需要修改成这样。

```
{
    "mcseekeri": {
        "device_id": "114514",
        "account_id": "1919810",
        "secret": "893",
        "user_agent": "DeviceAuthGenerator/1.1.0 Windows/10.0.19041",
        "created": {
            "location": "Neverland",
            "ip_address": "114.51.45.14",
            "datetime": "1970-01-01T00:00:00.000Z"
        }
    },
    "mcseekeri2333": {
        "device_id": "114514",
        "account_id": "1919810",
        "secret": "893",
        "user_agent": "DeviceAuthGenerator/1.1.0 Windows/10.0.19041",
        "created": {
            "location": "Neverland",
            "ip_address": "114.51.45.14",
            "datetime": "1970-01-01T00:00:00.000Z"
        }
    }
}
```
