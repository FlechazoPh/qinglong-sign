<h1 align="center">qinglong-sign</h1>

<div align="center">
    基于青龙面板的脚本库
</div>

## ✨ 特性

- 网易云音乐合伙人自动评分 ✔
- 九号出行APP自动签到 ✔

## 🔨 使用


#### 1.进入容器
```
docker exec -it ql bash
```
修改`ql`为你的青龙容器名字

#### 2.拉取仓库
```
ql repo https://github.com/KotoriMinami/qinglong-sign.git "sign_" "" "utils"
```
#### 3.配置脚本数据
- 方式1 （使用json文件）

复制配置文件到青龙config目录下
```
cp /ql/repo/KotoriMinami_qinglong-sign/sg_config.json /ql/data/config/sg_check.json
```

在青龙面板的配置目录（`/ql/data/config`）下找到 `sg_check.json` 文件 或 前往web端的`控制面板 / 配置文件` 下拉选择`sg_check.json`，
然后根据配置说明进行抓包配置即可。

## ⚙ 配置说明

| 配置名称            | 参数说明                                                                                                                                | 获取位置                                    |
|:----------------|:------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------|
| MUSIC_COPARTNER | "cookie"：网易云音乐cookie；<br/>"extra_count"（int类型）： 额外评定歌曲数，无此参数默认为`7`；<br/>"commit"（bool类型）：评定歌曲同时是否留言，如开启会从一言api随机获取一句内容进行评论，无此参数默认为`false` | [网易云音乐](https://music.163.com/)         |
| NINEBOT         | "deviceId": "app中抓包/portal/api/user-sign/v1/sign接口，从请求参数中获取"<br/>"authorization": "抓包接口同上，从请求头中获取"                                                                                                                               | [九号出行APP](https://www.ninebot.com/app/) |

- 方式2（配置环境变量）

前往web端的`控制面板 / 环境变量` 点击创建变量，
然后根据配置说明进行抓包配置即可。

## ⚙ 配置说明

| 配置名称                | 格式                        | 说明                                                                                                                                                  | 获取位置                                    |
|:--------------------|:--------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------|
| MUSIC_COPARTNER_ENV | cookie#extra_count#commit | `cookie`、`extra_count`同上，`commit`为非0的值表示启用，默认不启用。<br/>其中`extra_count、commit`可不填写，如填写需同时填写。<br/>多个账号`&`分隔。<br/>例：`cookie1&cookie2#7#1&cookie3#8#0 ` | [网易云音乐](https://music.163.com/)         |
| NINEBOT_ENV         | deviceId#authorization    | 同上，多个账号`&` 分隔。<br/>例：`xxxxx#xxxx&xxxx#xxxxx`                                                                                                        | [九号出行APP](https://www.ninebot.com/app/) |

#### 4.安装下面两个依赖
`PyExecJS`
`pycryptodome`

不会的可以直接去 web端的`控制面板 / 依赖管理 / Python3` 处添加依赖



## 🔈 特别声明

- 本仓库发布的脚本及其中涉及的任何解锁和解密分析脚本，仅用于测试和学习研究，禁止用于商业用途，不能保证其合法性，准确性，完整性和有效性，请根据情况自行判断。

- 本项目内所有资源文件，禁止任何公众号、自媒体进行任何形式的转载、发布。

- 本人对任何脚本问题概不负责，包括但不限于由任何脚本错误导致的任何损失或损害。

- 间接使用脚本的任何用户，包括但不限于建立VPS或在某些行为违反国家/地区法律或相关法规的情况下进行传播, 本人对于由此引起的任何隐私泄漏或其他后果概不负责。

- 请勿将本仓库的任何内容用于商业或非法目的，否则后果自负。

- 如果任何单位或个人认为该项目的脚本可能涉嫌侵犯其权利，则应及时通知并提供身份证明，所有权证明，我们将在收到认证文件后删除相关脚本。

- 任何以任何方式查看此项目的人或直接或间接使用该项目的任何脚本的使用者都应仔细阅读此声明。本人保留随时更改或补充此免责声明的权利。一旦使用并复制了任何相关脚本或Script项目的规则，则视为您已接受此免责声明。

**您必须在下载后的24小时内从计算机或手机中完全删除以上内容**

> ***您使用或者复制了本仓库且本人制作的任何脚本，则视为 `已接受` 此声明，请仔细阅读***


#### Tip: 刚学习玩这个, 大佬轻喷,后期可能不定期增加其它脚本

## 致谢

[@Sitoi](https://github.com/Sitoi)

[@yuxian158](https://github.com/yuxian158/)

[@weixin_44530979](https://blog.csdn.net/weixin_44530979)
