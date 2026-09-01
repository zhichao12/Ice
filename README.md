<div align="center">
  <img src="Ice/Assets.xcassets/AppIcon.appiconset/icon_256x256.png" width="160" alt="Ice 图标">
  <h1>Ice 简体中文</h1>
  <p>macOS 菜单栏项目管理工具</p>

  <a href="https://github.com/zhichao12/Ice/releases/latest">下载最新版本</a>
  &nbsp;|&nbsp;
  <a href="https://github.com/zhichao12/Ice">项目主页</a>
  &nbsp;|&nbsp;
  <a href="https://github.com/jordanbaird/Ice">上游项目</a>
</div>

## 简介

这是 [Ice](https://github.com/jordanbaird/Ice) 的简体中文 fork。它用于整理、隐藏、显示和搜索 macOS 菜单栏项目，适用于菜单栏图标较多的场景。

本 fork 以 [`main`](https://github.com/zhichao12/Ice/tree/main) 作为发布源，所有中文资源、构建工作流和发布改动均在该分支维护。

## 安装

1. 从[最新 Release](https://github.com/zhichao12/Ice/releases/latest)下载 `Ice-zh-Hans-*.zip`。
2. 解压后，将 `Ice.app` 移至“应用程序”文件夹。
3. 首次启动时，按应用内提示授予所需权限。

当前 Release 使用 ad-hoc 签名，未进行 Apple Developer ID 签名或公证。若 macOS 阻止启动，请在“系统设置 -> 隐私与安全性”中选择“仍要打开”。

系统要求：macOS 14 或更高版本。

## 主要功能

- 将菜单栏项目分为显示、隐藏和始终隐藏区域。
- 通过点击、悬停、滚动或快捷键显示隐藏项目。
- 在菜单栏下方使用 Ice Bar 显示隐藏项目。
- 在设置中拖放排列菜单栏项目。
- 搜索菜单栏项目。
- 自定义菜单栏颜色、边框、阴影与形状。
- 设置项目自动重新隐藏和开机登录启动。
- 提供菜单栏项目间距调节功能，当前为 beta。

## 菜单栏间距

Ice 的“菜单栏项目间距”使用 macOS 的全局 `NSStatusItemSpacing` 与 `NSStatusItemSelectionPadding` 设置。应用该设置会重启拥有菜单栏项目的应用；少数应用可能需要手动重新启动，必要时注销并重新登录。

该设置只能统一调整状态项外框的间距，不能修改第三方应用图标自身的透明边缘、文字宽度或内部留白。因此，不同应用的图标在视觉上仍可能显得疏密不同。这是各应用状态项窗口的实现差异，Ice 不会通过改变单项点击区域来强行对齐。

## 权限

Ice 会在需要时请求 macOS 权限。请在“系统设置 -> 隐私与安全性”中允许 Ice 使用应用内提示所需的权限；未授予权限时，隐藏、布局或图像预览等功能可能不可用。

## 构建与发布

GitHub Actions 在 macOS 15 / Xcode 16 上构建 `main` 分支，并对输出应用进行 ad-hoc 签名校验。构建工件会打包为 `Ice-zh-Hans.zip`，Release 附带 ZIP 与 SHA-256 校验文件。

## 与上游的关系

本仓库保留上游 Ice 的 GPL-3.0 许可证，并感谢上游作者和贡献者。功能性问题、上游演进和英文文档请参考 [jordanbaird/Ice](https://github.com/jordanbaird/Ice)。

## 许可证

本项目基于 [GPL-3.0](LICENSE) 发布。
