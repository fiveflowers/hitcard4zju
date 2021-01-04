<h1 align="center">
“健康打卡”定时自动执行脚本 
</h1>
<p align="center">
<img src="https://img.shields.io/badge/Python-3-blueviolet?logo=python">
<img src="https://img.shields.io/badge/%E5%BE%AE%E4%BF%A1%E6%8E%A8%E9%80%81-%E2%9C%85-9cf?logo=wechat">
<br/>


> 项目来源于 [ZJU-nCov-Hitcarder](https://github.com/Tishacy/ZJU-nCov-Hitcarder)，该仓库在源 `repo` 的基础上增加了微信推送的功能，并对部分 `emoji` 进行调整

> 项目用于学习交流，如有身体不适等情况还请 **及时如实上报** ！

# 脚本简介
- 自动填写：脚本读取用户上次的打卡的表单信息，并按照相同内容自动打卡
- 自定义打卡时间：脚本的每日自动打卡时间可由用户指定
- 微信推送：打卡成功或者程序报错将会微信推送，意外终止也不要慌，学院/辅导员会钉你的～
- 代码开源：无后门

# 安装
## 1. `clone` 该项目到机器上（服务器最好啦，毕竟不关机
```bash
$ git clone https://github.com/fiveflowers/hitcard4zju.git
```
## 2. 安装依赖
```bash 
$ cd hitcard4zju
$ pip3 install -r requirements.txt
```
## 3. 注册 Server 酱服务，用于配置微信推送（可选）
- 官网：[Server酱](http://sc.ftqq.com/3.version)
- 注册，关注公众号（用于给用户推送消息），拿到 `SCKEY`

## 4. 将 `config.json.template` 模板文件重命名为 `config.json` 文件，并修改 `config.json` 中的配置
```json
{
    "username": "你的浙大统一认证平台用户名",
    "password": "你的浙大统一认证平台密码",
    "schedule": {
        "hour": "0",    # 小时
        "minute": "5"   # 分钟
    },
    "sckey": "Server酱的密钥"   # 如果没有就留空白
}
```
## 5. 启动脚本
> 只有进程在，才会自动打卡，脚本退出就没了，安全放心
```bash
python3 hitcard.py
```

# Tips
- 自定义打卡定位，参考源 `repo` 的 [8#issue-565719250](https://github.com/Tishacy/ZJU-nCov-Hitcarder/issues/8#issue-565719250)

