# oktetoy
# 

## 

## 概述

### 注册地址：https://okteto.com/
本专案用于在 Okteto上部署 ，

部署完成后，每次启动应用时，运行的 将始终为最新版本

## 首先声明一下

### 本项目为  大佬的项目修改，因为有人反映同时fork二者会有冲突，我才将此重新上传改为本人的项目
### 不是剽窃，感谢大佬的付出，谢谢！

## 部署

### 步骤

 1. Fork 本专案到自己的 GitHub 账户（用户名以 `example` 为例）
 2. 如果有需要，修改UUID  在  `entrypoint.sh` 这个文件里修改
 

 

### 变量

对部署时需设定的变量名称做如下说明。

| 变量 | 默认值 | 说明 |
| :--- | :--- | :--- |
| `ID` | `ad806487-2d26-4636-98b6-ab85cc8521f7` | VMess 用户主 ID，用于身份验证，为 UUID 格式 |
| `AID` | `64` | 为进一步防止被探测所设额外 ID，即 AlterID，范围为 0 至 65535 |
| `WSPATH` | `/` | WebSocket 所使用的 HTTP 协议路径 |

## 接入 CloudFlare

以下两种方式均可以将应用接入 CloudFlare，从而在一定程度上提升速度。

 1. 为应用绑定域名，并将该域名接入 CloudFlare
 2. 通过 CloudFlare Workers 反向代理


