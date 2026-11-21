# 移动 Atlas

[English](README.md)

把两项移动 Web 增强装到插件页的同一张卡上，每行都可以独立开关。

- [左缘滑动返回](../dsh-swipe-back/README.md)在手机宽度下从屏幕左缘向右滑。
  主屏幕应用或无历史记录的标签页可以这样收起当前面板，或打开会话抽屉。
  抽屉已经打开时，普通标签页也可双向滑动关闭。
- [iOS 顶部留白](../dsh-ios-top-clearance/README.zh.md)在 iOS 主屏幕应用的手机宽度下为整个界面留出顶部空间。

通过 `dsh-mobile` 启动时，请从 `web` profile 的插件页安装。

## 安装

需要 DeepSeek Harness 0.2.2-rc.3 或更新版本 及 Web 客户端。

1. 在本目录运行 `pnpm install`，链接工作区中的源插件。
2. 如果目标 profile 已安装成员的独立 bundle，先记下开关状态并移除这些 bundle。
   只关掉插件行仍会留下重复的行 ID。
3. 在 **插件 → 添加插件** 选择本目录。
   确认卡内有两行，再恢复各行的开关状态。

[项目文档](docs/README.md)
