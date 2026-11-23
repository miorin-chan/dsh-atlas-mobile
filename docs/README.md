# 项目文档

## 使用

- [左缘滑动返回](../../dsh-swipe-back/README.md)。
  在主屏幕应用或无浏览历史的标签页，从左缘右滑即可返回或打开会话抽屉。
  抽屉打开时，向任一方向滑动都可关闭，普通标签页也适用。
- [iOS 顶部留白](../../dsh-ios-top-clearance/README.zh.md)。
  为 iOS 主屏幕应用的界面顶部留出空间。

## 兼容条件

需要 DeepSeek Harness `0.2.2-rc.3` 或更新版本的 Web 客户端。

## 安装

通过 `dsh-mobile` 启动时，在 `web` profile 中安装。

1. 在聚合包目录运行 `pnpm install`。
2. 如果目标 profile 已单独安装任何成员，记下开关状态，再移除独立安装的包，避免行 ID 重复。
3. 在 **插件 → 添加插件** 选择聚合包目录，然后在新卡片恢复各成员的开关状态。

[聚合清单](../aggregate.yml)声明源插件的顺序和版本范围。
生成器复制源插件的行 ID 与初始配置。
卡片的启停由 profile 的 bundle 选择管理，卡内开关按行 ID 管理。

## 维护

在本目录运行 `pnpm run aggregate` 更新产物，再运行 `pnpm run check`。
成员有变动时重新运行 `pnpm install`。
本包通过工作区相邻目录的 `link:` 依赖安装。

在一次性 Web profile 中核对整卡、逐行启停和各功能的独立使用。
迁移现有 profile 时，先记下各成员的开关状态，移除独立 bundle，再安装聚合卡并核对各行。
如果要改回独立安装，先移除聚合卡。

## 验证记录

2026-11-21 在 DSH `0.2.2-rc.5` 上与 Session Atlas 同装至一次性 Web profile，隔离服务器成功监听回环端口。
合成配置中的两个成员行各出现一次，行 ID 和初始配置与源插件一致。
通过 `--patch` 逐行覆盖停用和启用状态，并用一次性 profile 的 CLI 移除及恢复整包。
每次操作后核对其他成员行。骨架检查、清单漂移检查和打包内容检查均通过。

`--dump-config-schema` 在没有安装聚合包的同版本 Web profile 中也会报告四处 `unrecognized Loader tree carrier`，
本次使用能成功导出的 `--dump-config` 核对加载配置。
浏览器插件页的视觉和点击结果尚未验证。
iPhone 上的系统返回手势和顶部模糊带仍需实机验证。

## Usage

- [Left-edge swipe](../../dsh-swipe-back/README.en.md) goes back or opens the session drawer
  in a Home Screen app or a tab with no history.
  Swipe either way to close an open drawer, including in a regular tab.
- [iOS top clearance](../../dsh-ios-top-clearance/README.md) adds space above the interface in the iOS Home Screen app.

## Compatibility

Requires the Web client on DeepSeek Harness `0.2.2-rc.3` or later.

## Install

When using `dsh-mobile`, install in the `web` profile.

1. Run `pnpm install` from the bundle directory.
2. If any member is installed separately in the target profile, note its switch state and remove its bundle
   to avoid duplicate row IDs.
3. In **Plugins → Add plugin**, select the bundle directory.
   Restore the saved switch states on the new card.
