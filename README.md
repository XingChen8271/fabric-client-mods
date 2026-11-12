# Minecraft 客户端小模组集 · Fabric Client Mods

一组面向 Minecraft **1.20.1 / Fabric** 的纯客户端小模组。全部以 MIT 协议发布，可自由使用、修改、分发。
A collection of small **client-side** Fabric mods for Minecraft 1.20.1.

[![Minecraft](https://img.shields.io/badge/Minecraft-1.20.1-62B47A)](#)
[![Loader](https://img.shields.io/badge/Loader-Fabric-DBB69A)](#)
[![License](https://img.shields.io/badge/License-MIT-blue)](#)
[![Side](https://img.shields.io/badge/Environment-Client--only-lightgrey)](#)

> 全部模组均为**仅客户端**运行，服务端无需安装。装上就能用，卸掉不留痕。
> All mods are **client-side only**. Nothing is required on the server.

---

## 模组列表

| 模组 | 版本 | 功能 | 前置 |
|---|---|---|---|
| **[Quick Backpack](#quick-backpack)** | 3.2.0 | 一键汇总身上所有旅行背包里的物品，按品类合并显示，并可原路取回 | Traveler's Backpack |
| **[Stardew Auto Fish](#stardew-auto-fish)** | 1.0.4 | 自动完成星露谷钓鱼小游戏 | Stardew Fishing |
| **[AutoFish Speed](#autofish-speed)** | 1.0.0 | 把钓鱼小游戏加速到约 1 秒完成 | Stardew Fishing |
| **[Moon Phase](#moon-phase)** | 1.0.0 | HUD 显示当前月相，按 `M` 开关 | 无 |
| **[No Blind & Darkness](#no-blind--darkness)** | 1.0.0 | 自动清除失明与黑暗效果 | 无 |

---

## 环境要求

| 项目 | 要求 |
|---|---|
| Minecraft | 1.20.1 |
| 加载器 | Fabric Loader ≥ 0.16.9（Moon Phase / No Blind 为 ≥ 0.15.0） |
| Java | 17 及以上 |
| 必装前置 | [Fabric API](https://modrinth.com/mod/fabric-api) |

---

## 安装

1. 安装 **Fabric Loader**（对应 Minecraft 1.20.1）
2. 把 [Fabric API](https://modrinth.com/mod/fabric-api) 和需要的模组 jar 一起放进 `.minecraft/mods/`
3. 若有前置模组（见上表），一并放入
4. 启动游戏，确认模组列表中出现对应条目

---

## Quick Backpack

> 前置：[Traveler's Backpack](https://modrinth.com/mod/travelers-backpack)

按下绑定按键，列出随身所有旅行背包内的物品，**按物品合并统计**，并给出每个背包的分项明细；可以直接从汇总界面把物品取回，走的是正常容器逻辑，不需要先打开背包。

在物品栏中**右键点击背包**也能直接打开它。

- 纯客户端实现，服务器不用装
- 取物走原版容器交互，不会与服务端校验冲突
- 支持多背包叠加统计

## Stardew Auto Fish

> 前置：[Stardew Fishing](https://modrinth.com/mod/stardew-fishing)

自动完成 Stardew Fishing 的钓鱼小游戏，适合挂机刷鱼或不想手动点的时候。1.0.4 为功能基础版。

- 客户端自动化，不改动服务端逻辑
- 保留原模组的掉落与判定规则

## AutoFish Speed

把钓鱼小游戏的时间压缩到约 1 秒完成，适合想快速过钓鱼流程的场合。
与 Stardew Auto Fish 功能可叠加；如果两个都想要，直接用合并版 `autofish-plus`。

## Moon Phase

在 HUD 上显示当前月相，按 `M` 键查询并开关显示。

- 无前置依赖（仅需 Fabric API）
- HUD 位置可配置（配置文件见 `config/moonphase.json`）〔按实际填写〕

## No Blind & Darkness

自动移除失明（Blindness）与黑暗（Darkness）状态效果，客户端每 tick 清除一次。

- 仅影响客户端显示
- 适用于洞穴、深层探索、下界等场景

---

## 下载

所有版本见 **[Releases](../../releases)** 页面，选择与你的 Minecraft 版本对应的 jar。

> 请从本仓库 Releases 或 MC百科 页面下载，其他渠道的二次打包版本不做保证。

---

## 兼容性说明

- 全部模组为客户端模组，**不改变服务端行为**，可用于大多数服务器与整合包
- 与 OptiFine / Iris 等渲染模组无已知冲突〔按实际测试情况修改〕
- 与同类功能的模组可能重复响应同一个按键，遇到冲突请在按键设置里改绑定

---

## 关于源码

| 模组 | 源码 |
|---|---|
| Quick Backpack | ✅ 完整源码在 [`quickbackpack/`](quickbackpack/) 目录 |
| Stardew Auto Fish / AutoFish Speed | ⚠️ 早期开发未保留源码，仓库仅提供构建产物 |
| Moon Phase | ⚠️ 早期开发未保留源码，仓库仅提供构建产物 |
| No Blind & Darkness | ⚠️ 早期开发未保留源码，仓库仅提供构建产物 |

未提供源码的模组以 MIT 协议发布构建产物，你可以在协议允许范围内自由使用、修改、再分发。
如需自行修改，可对 jar 进行反编译后二次开发。

## 从源码构建

> 仅适用于仓库内含源码的模组（当前为 Quick Backpack）。

```bash
git clone https://github.com/XingChen8271/fabric-client-mods.git
cd fabric-client-mods
./gradlew build
# 产物在 build/libs/
```

---

## 许可

本项目基于 **MIT License** 发布，详见 [LICENSE](LICENSE)。
你可以自由使用、修改、分发，保留版权声明即可。

## 免责声明

本项目为个人开发的非官方模组，与 Mojang Studios、Microsoft 及任何第三方模组作者均无隶属关系。
Minecraft 是 Mojang Studios 的商标。

## 反馈

- 遇到 Bug 或想提建议：请开 [Issue](../../issues)
- 提交时请附上：游戏版本、Fabric Loader 版本、完整日志（`logs/latest.log`）、复现步骤
