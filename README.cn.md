<div align="center">

<img src="assets/icon-256.png" alt="Home Assistant Control 图标" width="96" height="96" />

# Home Assistant Control

### 把智能家居，留在自己的局域网。

**一个本地优先的控制中心，统一管理兼容的米家设备与向日葵插座，支持 Windows、macOS 和浏览器客户端。**

[![Release](https://img.shields.io/badge/release-latest-blue)](https://github.com/yuan-xin-9997/HomeAssistantControl/releases/latest)
[![平台](https://img.shields.io/badge/platform-Windows%2010%2F11%20%7C%20macOS%2013%2B-lightgrey)](#下载安装)
[![下载](https://img.shields.io/badge/download-安装包-0078D4)](https://github.com/yuan-xin-9997/HomeAssistantControl/releases/latest/download/HomeAssistantControl-Setup.exe)
[![免费试用](https://img.shields.io/badge/free%20trial-免费试用%2030%20天-16a34a)](https://hacontrol.yuan-xin.top/download)

[English](README.md) | 简体中文 | [更新日志](CHANGELOG.md)

**[下载](#下载安装) · [功能](#功能) · [免费试用](#免费试用) · [激活与购买](#激活与购买) · [兼容性](#兼容性) · [常见问题](#常见问题) · [支持](#支持)**

</div>

> **关于本仓库**
>
> 这是 Home Assistant Control 的官方发布与文档仓库。源代码维护在私有仓库。请从 [Releases](https://github.com/yuan-xin-9997/HomeAssistantControl/releases/latest) 下载安装包；每个安装包都包含 **30 天免费试用**，开始试用不需要邮箱、账号或信用卡。

## 项目简介

Home Assistant Control 在一台常开的家用电脑上运行小型控制中心。它登录小米账号导入兼容的米家设备，通过局域网发送真实 miIO/MIoT 指令，也可以扫描和控制向日葵插座。其他电脑使用配对码连接控制中心，在 Windows、macOS 或浏览器里共享同一套设备与场景。

- **全部功能免费试用 30 天**，只统计实际打开软件的天数，没打开的日子不消耗。
- 试用记录保存在服务端并绑定机器码，改系统时间、卸载重装或清除本地数据都不会重置；剩余天数在启动器和授权面板可见。
- 不需要端口映射、云端中转或订阅。
- 设备凭据使用 AES-GCM 加密落盘。
- 试用结束后，激活码绑定机器，日常使用不会连接授权服务器。

## 界面预览

<div align="center">
<img src="screenshots/app-zh.png" alt="Home Assistant Control 控制面板（演示数据）" width="860" />
</div>

## 功能

| 功能 | 说明 |
| --- | --- |
| 米家账号导入 | 扫码或账号密码登录，选择与米家 App 相同的地区，导入兼容 IP 设备的名称、房间和凭据。 |
| 局域网 miIO / MIoT | 读取属性、发送真实局域网指令；控件由型号规格生成，不硬编码属性编号。 |
| 向日葵插座 | 扫描 6767/5767 端口的 C1/C2/P1 系列，支持逐孔开关和功率读取；C2-BLE-V3 等仅云端型号通过向日葵账号控制。 |
| 智能场景 | 把米家属性和向日葵插孔编排成多步场景，在活动记录中查看每一步结果。 |
| 多端控制中心 | 一台电脑运行中心，其他 Windows/macOS/浏览器使用配对码连接；账号和设备状态由中心统一管理。 |
| 本地优先隐私 | 没有遥测、没有云端中转；断网时局域网控制仍然可用。 |
| 演示模式 | 用示例数据体验界面，不需要授权，也不会控制真实设备。 |

## 1.1.0 新变化

- **30 天免费试用**，包含全部功能，只按实际打开软件的天数计算。
- 启动器、顶部栏和授权面板都会显示剩余试用天数。
- 试用状态由服务端保存并绑定机器码：卸载重装、清除本地数据或修改系统时间都不会重置。
- 支持离线试用；离线打开的天数会在联网后补报。
- Windows 卸载时提供可跳过、不阻塞的卸载调研。
- 支持用下单邮箱 + 机器码找回激活码，不再强制订单号。

## 下载安装

| 下载 | 说明 |
| --- | --- |
| **[HomeAssistantControl-Setup.exe](https://github.com/yuan-xin-9997/HomeAssistantControl/releases/latest/download/HomeAssistantControl-Setup.exe)** | 推荐：Windows 10/11 安装包。 |
| [全部版本](https://github.com/yuan-xin-9997/HomeAssistantControl/releases) | 版本历史、更新说明和旧安装包。 |
| [SHA256SUMS.txt](https://github.com/yuan-xin-9997/HomeAssistantControl/releases/latest/download/SHA256SUMS.txt) | 最新安装包的 SHA-256 校验值。 |
| **[免费试用](https://hacontrol.yuan-xin.top/download)** | 下载完整软件，30 天内使用全部功能。 |

**系统要求：** Windows 10/11（64 位）或 macOS 13+。网页面板由同一个程序提供。控制中心与设备必须在同一 IPv4 子网。miIO 使用 UDP 54321；向日葵本地插座使用 TCP 6767/5767。

> 当前 GitHub Release 提供 Windows 安装包。macOS 安装包需要在 macOS 上构建并完成开发者签名/公证后再公开分发；需要 macOS 版本请联系支持。

1. 下载并运行安装包。
2. 启动程序，30 天免费试用自动开始；启动器会显示剩余天数和本机机器码。
3. 选择“作为控制中心”，选择家庭网卡并启动。
4. 登录小米账号并导入设备。
5. 试用结束后如果想继续控制真实设备，再在商店购买授权，用机器码领取 `HAC-...` 激活码并点击“激活”。

## 免费试用

- 每个安装包都包含完整软件，首次启动自动开始 **30 天免费试用**，不需要邮箱、账号或信用卡。
- 只有当天打开软件才消耗一天；没打开软件的日子不消耗。
- 试用记录保存在服务端并绑定软件中显示的机器码。改系统时间、卸载重装或清除本地数据都不会重置。
- 启动器和“授权与购买”面板会一直显示剩余天数。
- 首次确认试用需要联网；之后可以离线使用，离线打开的天数会在下次联网时补报。
- 30 个打开日后，可以继续免费使用演示模式，或购买授权继续控制真实设备。

## 激活与购买

试用结束后，Home Assistant Control 使用**离线激活**：

- 软件会显示类似 `ABCD-EFGH-IJKL-MNOP` 的机器码。
- 在[商店购买页](https://hacontrol.yuan-xin.top/purchase)购买授权并提交机器码。
- 商店返回绑定该机器的 `HAC-...` 激活码。
- 把激活码粘贴回程序。程序使用内置 P-256 公钥在本地验签，不连接授权服务器。
- 每份订单可激活 **2 台电脑**；重复提交同一机器码返回同一激活码，不重复占名额。
- 一次买断，含 1 年更新。当前价格只在商店购买页和结账页显示。
- 激活码或邮件丢了？用[找回授权](https://hacontrol.yuan-xin.top/retrieve)输入下单邮箱和软件中的机器码即可找回；已经签发过激活码的机器不需要订单号和邮件。

> 已经签发的离线激活码无法远程失效。退款或争议会阻止该订单后续补发和换机。详见[退款政策](https://hacontrol.yuan-xin.top/refund)。

## 兼容性

| 范围 | 支持情况 |
| --- | --- |
| 开放局域网 miIO/MIoT 的米家 Wi-Fi/以太网设备 | 型号和固件允许本地指令时支持 |
| 仅云端米家设备 | 可导入记录，但本程序不做云端远程控制 |
| 蓝牙 / BLE Mesh / Zigbee / Matter | 未实现 |
| 摄像头、门锁、扫地机地图 | 未实现 |
| 向日葵 C1/C2/P1 系列（本地 HTTP） | 支持开关、分孔和用电读取 |
| 向日葵 C2-BLE-V3 等仅云端型号 | 通过向日葵账号和 Oray 云端控制 |
| 跨子网 / 其他家庭 | 不支持；控制中心只控制所选 IPv4 子网 |

设备具备 MIoT 规格不代表固件允许本地控制；请按型号、固件和属性验证。详见[兼容性说明](https://hacontrol.yuan-xin.top/compatibility)。

## 常见问题

### 这是小米或 Home Assistant 官方产品吗？

不是。本产品由独立开发者开发，与小米、米家、向日葵/Oray 及 Home Assistant 项目均无隶属关系。

### 需要联网吗？

局域网控制不需要。登录小米账号、导入设备、同步型号规格和控制仅云端向日葵插座需要联网。拿到激活码后，激活过程完全离线。

### 可以激活几台电脑？

每个订单最多为 2 台不同电脑签发激活码。在每台电脑上打开程序，用该机器的机器码分别领取。

### 有免费试用吗？

有。每个安装包都包含全部功能，可免费试用 30 天；只统计实际打开软件的天数，剩余天数在软件内显示。试用绑定机器码并保存在服务端，卸载重装不会重置。试用结束后，控制真实设备需要一次性授权；演示模式仍然免费。

### 1 年更新期结束后还能用吗？

可以继续使用已安装的版本；新版本更新可能需要有效授权。

### 我的数据存在哪里？

设备凭据、场景和设置保存在程序自己的本地数据目录；凭据使用 AES-GCM 加密。程序没有遥测。试用期间，商店会接收机器码、实际打开软件的本地日期、程序版本和平台；领取激活码时还会接收你提交的机器码及其哈希。

### 如何卸载？

Windows 在“设置 → 应用”中卸载；卸载器会在浏览器中打开一个可选的 10 秒卸载调研页面，直接关闭即可跳过，且不会阻塞卸载。macOS 把应用拖到废纸篓，或在菜单中打开卸载反馈。本地数据目录会保留，以便重装后继续使用；如需彻底清理可手动删除。

## 隐私

程序不会把小米/向日葵密码、会话、设备 Token、设备名称、场景、活动记录或网络扫描上传到商店。商店只从 Creem 获取订单数据，并保存你提交的机器码。详见[隐私政策](https://hacontrol.yuan-xin.top/privacy)。

## 支持

- 商店与激活码：<https://hacontrol.yuan-xin.top/>
- 支持邮箱：<support@yuan-xin.top>
- 问题反馈：在本仓库提交 Issue
- 源代码：私有仓库；本仓库只用于发布和文档

## 更新日志

见 [CHANGELOG.md](CHANGELOG.md)。

---

Home Assistant Control 是专有软件。当前条款和隐私政策以商店页面为准。
