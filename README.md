# 高校招聘信息导航桌面版发布

本仓库仅分发 macOS Apple Silicon 桌面版安装镜像和签名更新清单；应用源代码位于私有源码仓库。

## 安装与手动更新

1. 下载最新 Release 中的 `University-Recruitment-<版本>-arm64.dmg` 和同名 `.sha256` 文件。
2. 在终端进入下载目录，执行 `shasum -c University-Recruitment-<版本>-arm64.dmg.sha256` 校验文件。
3. 打开 DMG，将“高校招聘信息导航.app”拖入“应用程序”文件夹。
4. 首次打开时，macOS 可能要求在“系统设置 → 隐私与安全性”中确认打开 ad-hoc 签名应用。

应用内更新会验证由本项目 Ed25519 公钥签名的清单和 DMG 摘要。应用只下载并校验 DMG，不会自动替换已安装应用；安装仍由用户手动完成。更新不会迁移或删除现有 profile 与数据库。
