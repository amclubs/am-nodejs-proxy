# [am-nodejs-proxy](https://github.com/amclubs/am-nodejs-proxy)
基于 Node.js 的 vless 实现包。它在各种 Node.js 环境中都能运行，包括但不限于：Windows、Linux、MacOS、Android、iOS、树莓派等。同时，它也适用于各种 PaaS 平台，如：replit、heroku 等。

#
▶️ **新人[YouTube](https://youtube.com/@am_clubs?sub_confirmation=1)** 需要您的支持，请务必帮我**点赞**、**关注**、**打开小铃铛**，***十分感谢！！！*** ✅
</br>🎁请 **follow** 我的[GitHub](https://github.com/amclubs)、给我所有项目一个 **Star** 星星（拜托了）！你的支持是我不断前进的动力！ 💖
</br>✅**解锁更多技能** [加入TG群【am_clubs】](https://t.me/am_clubs)、[YouTube频道【@am_clubs】](https://youtube.com/@am_clubs?sub_confirmation=1)、[【博客(国内)】](https://amclubss.com)、[【博客(国际)】](https://amclubs.blogspot.com) 
</br>✅点击观看教程[CLoudflare免费节点](https://www.youtube.com/playlist?list=PLGVQi7TjHKXbrY0Pk8gm3T7m8MZ-InquF) | [VPS搭建节点](https://www.youtube.com/playlist?list=PLGVQi7TjHKXaVlrHP9Du61CaEThYCQaiY) | [获取免费域名](https://www.youtube.com/playlist?list=PLGVQi7TjHKXZGODTvB8DEervrmHANQ1AR) | [免费VPN](https://www.youtube.com/playlist?list=PLGVQi7TjHKXY7V2JF-ShRSVwGANlZULdk) | [IPTV源](https://www.youtube.com/playlist?list=PLGVQi7TjHKXbkozDYVsDRJhbnNaEOC76w) | [Mac和Win工具](https://www.youtube.com/playlist?list=PLGVQi7TjHKXYBWu65yP8E08HxAu9LbCWm) | [AI分享](https://www.youtube.com/playlist?list=PLGVQi7TjHKXaodkM-mS-2Nwggwc5wRjqY)

- [中文文档](./README_CN.md) 
- [视频教程](https://youtu.be/tj9uD575R80)

本自述文件解释了如何设置和使用“start.sh”脚本来管理项目组件。

## 初始设置

1. 使用 SSH 连接到您的主机：

```
ssh <username>@<panel>.serv00.com
```

使用 serv00 通过电子邮件发送给您的信息,上面的username、panel换成你接收的信息。

2. 启用管理权限：

```
devil binexec on
```

***完成此步骤后，退出 SSH 并再次登录。***

3. 克隆仓库代码：

```
cd domains/${USER}.serv00.net
```
```
git clone https://github.com/amclubs/am-nodejs-proxy.git
```
```
cd am-nodejs-proxy
```

## 使用

要使用该脚本，请运行：

```
./start.sh <action> <sub-action>
```

| Action |  Sub-Action   |         Command         |                  Description                   |
| :----: | :-----------: | :---------------------: | :--------------------------------------------: |
| setup  |   node/xray/cf   | `./start.sh setup node` |      通过单个命令设置服务       |
| check  |   node/xray/cf   | `./start.sh check node` |    检查 Cloudflared 和其他服务      |
|  show  | node/xray/all | `./start.sh show node`  | 显示来自 node/.env 的 VLESS 连接链接 |

查看所有节点信息
```
cat domains/${USER}.serv00.net/am-nodejs-proxy/node/.env
```

***NODE.JS 和 XRAY 不能同时处于活动状态。一次只能运行其中一个。***

## 检查会话

要检查特定组件的状态，您可以附加到其 tmux 会话：

```
tmux attach -t <session>
```

将 `<session>` 替换为：

- `cf` for Cloudflared
- `node` for Node.js
- `xray` for Xray

例如，要检查 Cloudflared 会话：

```
tmux attach -t cf
```

要从 tmux 会话分离而不关闭它，请按：

```
Ctrl + b, 然后是 d
```

此组合键允许您退出会话，同时使其在后台运行。

## Notes

- 该脚本使用 tmux 来管理每个组件的会话。
- 设置 Cron 作业用于定期维护 Node.js 和 Xray。
- Cloudflared、Node.js 和 Xray 配置自动生成。
- 该脚本包括端口管理和清理功能。

# 
<center>
<details><summary><strong> [点击展开] 赞赏支持 ~🧧</strong></summary>
*我非常感谢您的赞赏和支持，它们将极大地激励我继续创新，持续产生有价值的工作。*

- **USDT-TRC20:** `TWTxUyay6QJN3K4fs4kvJTT8Zfa2mWTwDD`
- **TRX-TRC20:** `TWTxUyay6QJN3K4fs4kvJTT8Zfa2mWTwDD`

<div align="center"> 
  <img src="https://github.com/user-attachments/assets/e6cdc42a-6374-4722-b833-601738f72196" width="200"></br> 
  TRC10/TRC20扫码支付 
</div> 
</details>
</center>

 #
 免责声明:
 - 1、该项目设计和开发仅供学习、研究和安全测试目的。请于下载后 24 小时内删除, 不得用作任何商业用途, 文字、数据及图片均有所属版权, 如转载须注明来源。
 - 2、使用本程序必循遵守部署服务器所在地区的法律、所在国家和用户所在国家的法律法规。对任何人或团体使用该项目时产生的任何后果由使用者承担。
 - 3、作者不对使用该项目可能引起的任何直接或间接损害负责。作者保留随时更新免责声明的权利，且不另行通知。
 
