## 玩赚AI设计工作台 v1.0.3（无内置渠道版）正式发布

玩赚 AI 设计工作台（无限画布无内置渠道版）1.0.3 正式发布，全平台支持 Windows / Linux / macOS（x64 与 arm64）。

### 主要更新

- **彻底修复升级安装完成后仍重复提示「安装新版本」Bug**：在 `restore()` 启动恢复及 `check()` 检测阶段增加与当前安装版本号（`app.getVersion()`）的比对；升级重启后自动销毁遗留的 `updates/state.json` 及旧安装包并释放磁盘空间，顶部「安装新版本」角标即刻消退，不再陷入重复更新提示死循环。
- **支持已就绪更新跨代发现**：若本地曾下载过安装包尚未安装，仓库发布新版本时点击「检查更新」仍能识别最新版本。
- **包含 v1.0.1 / v1.0.2 全部核心能力与修复**：
  - 独立仓库 `pazmulroneyv-alt/wzai-design-noplugin` 更新源完全隔离；
  - 多模态连线同侪依赖隔离、`gpt-image-2.5/2.6` 自动防重复扣费路由、主进程直读模型列表与免 Key 本地端点兼容。

### 安装包

| 系统 | 安装包 |
| --- | --- |
| Windows x64 | `Wanzhuan-AI-Design-Setup-1.0.3-noplugin-x64.exe` |
| Linux x64 | `Wanzhuan-AI-Design-1.0.3-noplugin-linux-amd64.deb`、`Wanzhuan-AI-Design-1.0.3-noplugin-linux-x86_64.AppImage` |
| Linux arm64 | `Wanzhuan-AI-Design-1.0.3-noplugin-linux-arm64.deb`、`Wanzhuan-AI-Design-1.0.3-noplugin-linux-arm64.AppImage` |
| macOS Intel | `Wanzhuan-AI-Design-1.0.3-noplugin-macos-x64.dmg` |
| macOS Apple Silicon | `Wanzhuan-AI-Design-1.0.3-noplugin-macos-arm64.dmg` |

### 校验值（SHA-256）

```
b1b1ce4aad84541b6f6567e93cc213dca4aa207223e5db2b65a25ad695b63245  Wanzhuan-AI-Design-Setup-1.0.3-noplugin-x64.exe
c74f6ae12edf7733e2554ddc7112833ae92289c04e39c13b2cda6aad227c7711  Wanzhuan-AI-Design-1.0.3-noplugin-linux-amd64.deb
90fc1fb9de3eabfbab74eadba56a00744e7b2e2bd850dec667da86eefa392fe2  Wanzhuan-AI-Design-1.0.3-noplugin-linux-x86_64.AppImage
57a262ebae675464e0bcbc53a7841aee36634b794dd18bf4b051a143afeaa75a  Wanzhuan-AI-Design-1.0.3-noplugin-linux-arm64.deb
c0a182c4626f3ab3d9c3004be30fa591adb45ee14e1f84171eba6decf572cbf5  Wanzhuan-AI-Design-1.0.3-noplugin-linux-arm64.AppImage
77ffcea83bbdd790b9a8aed15f68d5eca86cfdfba4ee14e8d7a37b6d71b1c301  Wanzhuan-AI-Design-1.0.3-noplugin-macos-x64.dmg
ea1ac9eacd4b7ac006b63587a32dfa75a5c01be456394a9ca4a7ac48c54d425f  Wanzhuan-AI-Design-1.0.3-noplugin-macos-arm64.dmg
```

每个安装包同时附有 `.sha256` 文件，供升级入口自动校验使用。

### 局域网归档

- NAS 发布目录：`\\192.168.88.8\wz\无限画布二开\wzai-design-v1.0.3-noplugin\`
