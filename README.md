# DeskMate 桌面小黄条

Windows 桌面小组件：日历（法定节假日与调休标识）、待办、便签、时钟天气。

本仓库只做**发行与下载**，源码不在此公开。

## 下载

- 安装包（推荐）：[最新版本 Releases](https://github.com/Aelisa/deskmate-release/releases/latest)
  下载 `DeskMate-Setup.exe`
- 免安装便携版：同一 Release 里的 `DeskMate-Portable.exe`，双击即用
- 校验值：同一 Release 里的 `SHA256SUMS.txt`

国内访问更稳的镜像：<https://gitee.com/LZTZT/deskmate-release/releases>

### 校验

PowerShell：

```powershell
Get-FileHash .\DeskMate-Setup.exe -Algorithm SHA256
```

与 `SHA256SUMS.txt` 对应行比对，一致后再运行。

## 说明

- exe 未做代码签名，SmartScreen / Defender / 第三方杀软可能提示「未知发布者」，属常见误报；
  请先核对 SHA256 与来源，再决定是否继续。
- 安装包默认装到当前用户目录，不弹 UAC；程序数据在 `%APPDATA%\DeskMate`，与安装目录解耦，
  升级不丢数据。
- 命令行支持 `--import <json>` 导入待办/便签/日程、`--export <path>` 只读导出快照、
  `--version` 查看版本。

## 技能联动

WorkBuddy 市场内的免费技能 **`deskmate-todo`（DeskMate 待办助手）** 可在对话里把会议记录、
任务清单、带时间段的表格直接写进已安装的小黄条。装技能再用本仓库的程序即可联动。

## 许可

MIT，见 [LICENSE](LICENSE)。Copyright (c) 2026 帝一
