# 移动端模块化改良计划

[English](README.md)

在手机上使用 DSH 时，可分别开启两项改进。

- [左缘滑动返回](../dsh-swipe-back/README.md)。
  在主屏幕应用或无浏览历史的标签页，从左缘右滑即可返回或打开会话抽屉。
  抽屉打开时，向任一方向滑动都可关闭，普通标签页也适用。
- [iOS 顶部留白](../dsh-ios-top-clearance/README.zh.md)。
  为 iOS 主屏幕应用的界面顶部留出空间。

## 安装

需要 DeepSeek Harness `0.2.2-rc.3` 或更新版本的 Web 客户端。
经 `dsh-mobile` 启动时使用 `web` profile。

1. 在本目录运行 `pnpm install`。
2. 如果当前 profile 已单独安装其中的插件，先记下开关状态，再移除独立安装的包，避免插件 ID 重复。
3. 在 **插件 → 添加插件** 选择本目录，再到新卡片恢复已记下的开关状态。

[维护与验证](docs/README.md)
