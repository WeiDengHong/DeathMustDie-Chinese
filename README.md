# Death Must Die 简体中文汉化

Death Must Die 非官方简体中文汉化，当前版本 **2.9.0**。提供 Windows 终端安装包，包含汉化插件、中文字体和所需加载器。

## 下载与安装

请在本仓库的 **Releases** 页面下载 `DeathMustDie-Chinese-2.9.0-Terminal.zip`，不要下载 GitHub 自动生成的 Source code 压缩包。

1. 完整解压安装包。
2. 退出游戏，双击 `Install.cmd`。
3. 安装程序会查找 Steam 游戏目录；找不到时，输入包含 `Death Must Die.exe` 的文件夹路径。
4. 提示安装成功后，从 Steam 正常启动游戏。

也可以在解压目录打开 PowerShell，指定游戏路径：

```powershell
.\Install.cmd -GamePath "D:\SteamLibrary\steamapps\common\Death Must Die"
```

仅检查，不写入文件：

```powershell
.\Install.cmd -GamePath "D:\SteamLibrary\steamapps\common\Death Must Die" -Action Check
```

## 备份与恢复

安装前会自动备份需要覆盖的汉化文件，备份位于游戏目录的 `DMD-Chinese-Backups` 文件夹。请保留备份。

退出游戏后，双击 `Restore.cmd`，可以撤销最近一次尚未恢复的安装。

```powershell
.\Restore.cmd -GamePath "D:\SteamLibrary\steamapps\common\Death Must Die"
```

如果安装后修改了词库、配置或游戏更新了相关文件，恢复程序会停止，避免覆盖修改。如果后来安装了依赖 BepInEx 的其他 MOD，可先将 `BepInEx/config/dmd.zhcn.cfg` 中的 `Enabled` 改为 `false` 停用汉化。

## 包含内容

- 简体中文汉化插件 2.9.0，以及游戏文本、对话和原文映射词库。
- Noto Serif SC 中文字体。
- BepInEx 5.4.23.6、Unity Doorstop 4.6.0 及依赖。
- 安装、完整性校验、备份与恢复脚本。

不包含游戏本体、存档、日志或其他 MOD。检测到不同版本的现有加载器时，安装会停止，请先协调加载器版本。

## 兼容与反馈

适用于 Windows 64 位、Unity Mono 版 Death Must Die。已通过 12 项隔离安装流程测试和 ZIP 校验；尚未验证所有游戏版本、第三方电脑及其他 MOD 组合。

遇到问题可以提交 Issue，并说明游戏版本、安装步骤、报错和是否使用其他 MOD。如需提供 `BepInEx/LogOutput.log`，请先检查并删除个人信息。

## 第三方组件

本项目是社区汉化，与游戏开发商或发行商无隶属关系。需要自行拥有游戏。

安装包 `licenses` 目录包含第三方加载器、依赖和字体的许可证，以及 Doorstop 对应上游源码。各许可证适用于各自组件。
