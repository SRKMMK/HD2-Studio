# HD2 摄影台 r8 使用说明

1. 安装 Windows 版 Blender 与《绝地潜兵 2》。本版既有验收使用 Blender 5.3.0 和游戏 Build 26568081，预留约 30 GiB 本地生成空间。
2. 下载 `HD2-Studio-Windows-Setup-r8.zip`，完整解压到短路径，例如 `C:\HD2Studio`。不要在压缩包预览窗口中运行。
3. 打开解压后的 `HD2-Test`，双击 `启动摄影台.cmd`。
4. 选择游戏安装目录，即包含 `data` 文件夹的那一层；必要时选择 Blender 的 `blender.exe`。
5. 等待工具展开、装备生成、检查和自动试拍完成。首次准备时间取决于电脑和磁盘，尚无从零全量提取耗时承诺。
6. 摄影台打开后，选择角色和装备、动作、背景及灯光，先使用默认的 1080p 快速档出图。之后可使用桌面 `HD2 摄影台` 入口启动。

## 文件与恢复

试拍图为生成目录下的 `salute-preview.png`，试拍工程为 `salute-studio.blend`，自动验证为 `verification.json`。常规生成目录是 `HD2-Test\staging\test-data\studio`；失败重试时可能是 `studio-编号`，以控制台为准。

生成失败时保留日志，修正原因后重新启动，可以复用已成功的归档。移动整份解压目录后，在新位置双击 `创建桌面入口.cmd` 重建快捷方式。

`一键清空.cmd` 会移除本包 `staging\test-data` 下生成的资源、试拍工程、图片、日志、路径记录和 Blender 配置。使用前关闭本包的 Blender，并将需要保留的工程与图片复制到该目录以外；清空后首次准备需要重新进行。它不是正常启动的必需步骤。

## 下载校验

在 PowerShell 中切换到下载目录，执行：

```powershell
Get-FileHash -LiteralPath '.\HD2-Studio-Windows-Setup-r8.zip' -Algorithm SHA256
```

结果应为 `69b8b81ac81dff508e34b38f8d07564ce1c10d50a4070598ff782048f7f53439`。完整功能和已知问题见同页发布说明。
