# Rig downloads

Rig Windows 桌面端的安装包与更新清单分发仓库。
本仓库的 Git 历史只包含下载说明；应用安装包以 Release 附件提供。

## 安装

打开 [最新版本](https://github.com/FUDAHA99/rig-downloads/releases/latest)，
下载 `Rig-<version>-x64.exe` 并安装。当前提供 Windows x64 NSIS 安装包。
安装器尚未签名，Windows SmartScreen 可能显示未知发布者提示。

## 更新源

固定更新清单入口：

```text
https://github.com/FUDAHA99/rig-downloads/releases/latest/download/update-feed.json
```

已有桌面客户端可通过 `RIG_UPDATE_FEED_URL` 或用户数据目录中的
`update-feed.txt` 指定该地址。清单中的安装包 URL 固定到具体版本；
客户端在安装前校验 SHA-256。

当前 0.1.6 安装包是原发行文件的镜像，二进制内容未改动；内置默认更新源
将随后续桌面客户端版本提供。后台自动安装仍需显式设置
`RIG_UPDATE_AUTO_INSTALL=1`。

## 校验与维护

各版本 Release 说明列出安装包与 blockmap 的大小和 SHA-256。
每个正式版本均携带 `update-feed.json`，并显式设置为 Latest。
已发布的版本安装包不覆盖；新版使用新的版本 tag。

下载需要访问 GitHub 及其 Release 附件域名。网络可达性和下载速度取决于用户网络。
