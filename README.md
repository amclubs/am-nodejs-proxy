# [am-nodejs-proxy](https://github.com/amclubs/am-nodejs-proxy)
基于 Node.js 的 vless 实现包。它在各种 Node.js 环境中都能运行，包括但不限于：Windows、Linux、MacOS、Android、iOS、树莓派等。同时，它也适用于各种 PaaS 平台，如：replit、heroku 等。

#
▶️ **新人[YouTube](https://youtube.com/@am_clubs?sub_confirmation=1)** 需要您的支持，请务必帮我**点赞**、**关注**、**打开小铃铛**，***十分感谢！！！*** ✅
</br>🎁请 **follow** 我的[GitHub](https://github.com/amclubs)、给我所有项目一个 **Star** 星星（拜托了）！你的支持是我不断前进的动力！ 💖
</br>✅**解锁更多技能** [加入TG群【am_clubs】](https://t.me/am_clubs)、[YouTube频道【@am_clubs】](https://youtube.com/@am_clubs?sub_confirmation=1)、[【博客(国内)】](https://amclubss.com)、[【博客(国际)】](https://amclubs.blogspot.com) 
</br>✅点击观看教程[CLoudflare免费节点](https://www.youtube.com/playlist?list=PLGVQi7TjHKXbrY0Pk8gm3T7m8MZ-InquF) | [VPS搭建节点](https://www.youtube.com/playlist?list=PLGVQi7TjHKXaVlrHP9Du61CaEThYCQaiY) | [获取免费域名](https://www.youtube.com/playlist?list=PLGVQi7TjHKXZGODTvB8DEervrmHANQ1AR) | [免费VPN](https://www.youtube.com/playlist?list=PLGVQi7TjHKXY7V2JF-ShRSVwGANlZULdk) | [IPTV源](https://www.youtube.com/playlist?list=PLGVQi7TjHKXbkozDYVsDRJhbnNaEOC76w) | [Mac和Win工具](https://www.youtube.com/playlist?list=PLGVQi7TjHKXYBWu65yP8E08HxAu9LbCWm) | [AI分享](https://www.youtube.com/playlist?list=PLGVQi7TjHKXaodkM-mS-2Nwggwc5wRjqY)

- [中文文档](./README_CN.md) 
- [视频教程](https://youtu.be/tj9uD575R80)

This README explains how to set up and use the `start.sh` script to manage the project components.

## Initial Setup

1. Connect to your host using SSH:

```
ssh <username>@<panel>.serv00.com
```

Use the information emailed to you by serv00.

2. Enable management permissions:

```
devil binexec on
```

***AFTER THIS STEP, EXIT FROM SSH AND LOG IN AGAIN.***

3. Clone the repository:

```
cd domains/${USER}.serv00.net
```
```
git clone https://github.com/ansoncloud8/am-nodejs-proxy.git
```
```
cd am-nodejs-proxy
```

## Usage

To use the script, run:

```
./start.sh <action> <sub-action>
```

| Action |  Sub-Action   |         Command         |                  Description                   |
| :----: | :-----------: | :---------------------: | :--------------------------------------------: |
| setup  |  node/xray/cf   | `./start.sh setup node` |       Setup services in a single command       |
| check  |  node/xray/cf   | `./start.sh check node` |     Checks Cloudflared and other services      |
|  show  | node/xray/all | `./start.sh show node`  | Displays VLESS connection links from node/.env |

View all node information
```
cat domains/${USER}.serv00.net/am-nodejs-proxy/node/.env
```

***NODE.JS AND XRAY CANNOT BE ACTIVE SIMULTANEOUSLY. ONLY ONE OF THEM SHOULD BE RUNNING AT A TIME.***

## Checking Sessions

To check the status of a specific component, you can attach to its tmux session:

```
tmux attach -t <session>
```

Replace `<session>` with:

- `cf` for Cloudflared
- `node` for Node.js
- `xray` for Xray

For example, to check the Cloudflared session:

```
tmux attach -t cf
```

To detach from a tmux session without closing it, press:

```
Ctrl + b, then d
```

This key combination allows you to exit the session while leaving it running in the background.

## Notes

- The script uses tmux to manage sessions for each component.
- Cron jobs are set up for periodic maintenance of Node.js and Xray.
- Cloudflared, Node.js, and Xray configurations are generated automatically.
- The script includes functions for port management and cleanup.

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
 
