# Mono-BPS Releases

Mono-BPS（结构光 BPS 系统）Windows x64 安装程序与运行环境发布仓库。

> 安装包体积较大，统一通过 [Releases](../../releases) 发布，不放进 Git 历史。

## 最新版本

| 版本 | 安装包 | 大小 | 构建时间 |
|------|--------|------|----------|
| v1.13.1 | [MonoBPS_Setup_1.13.1_x64.exe](../../releases/download/v1.13.1/MonoBPS_Setup_1.13.1_x64.exe) | 103.7 MiB | 2026-10-24 |

SHA-256：`4343ec33044cc06540a48bb417aa8ea69c311e935eb610f776cecb134fc83ebe`

## 安装步骤

1. 从 Releases 下载 `MonoBPS_Setup_1.13.1_x64.exe`。
2. 双击运行安装程序，默认安装目录为 `D:\LinaTech\x64\BPS\monobps-1.13.1`。
3. 安装完成后通过开始菜单或桌面快捷方式启动 **Mono-BPS**。
4. 按现场硬件修改安装目录下的 `config.ini`（相机序列号、触发边沿、投影仪等）。
5. Copilot 对话功能需在 `config.ini` 的 `[Copilot]` 节自行填写 `Endpoint` / `ApiKey` / `Model`，安装包不预置任何密钥。

## 内置运行环境

安装包已包含程序运行所需的全部运行库，目标机器无需另外安装：

| 组件 | 说明 |
|------|------|
| 操作系统 | Windows 10 / 11 x64 |
| Qt | 6.7.3（含 Qt6Charts、Qt6Concurrent 等） |
| OpenCV | 4.5.5 |
| PCL | 1.15 |
| VTK | 随 PCL 分发的 Qt6 版本 |
| FFTW | 3.x |
| 相机 SDK 运行库 | IMV 微视 MicroView（`MVSDKmd.dll` 等） |
| 相机 SDK 运行库 | 海康威视 MVS（`MvCameraControl.dll` 等） |
| C++ 运行库 | VC++ 2015-2022 x64（`vcredist_x64.exe`） |
| OpenMP 运行库 | `vcomp140.dll` |

## 硬件要求

- 结构光投影仪：DLP4500 / DLPC350（USB HID）
- 工业相机：IMV 微视或海康威视（USB3 / GigE）

## 随包文档

- `docs/Mono-BPS-系统标定操作文档-v2.3.0.pdf`
- `docs/Mono-BPS-System-Calibration-Operation-Manual-v2.3.0.pdf`

## 版本记录

| 版本 | 说明 |
|------|------|
| v1.13.1 | 当前发布版本 |
