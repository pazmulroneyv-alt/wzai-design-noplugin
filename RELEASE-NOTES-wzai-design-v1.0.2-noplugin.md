## 玩赚AI设计工作台 v1.0.2（无内置渠道版）正式发布

玩赚 AI 设计工作台（无限画布无内置渠道版）1.0.2 正式发布，全平台支持 Windows / Linux / macOS（x64 与 arm64）。

### 主要更新

- **独立仓库与自动更新源完全隔离**：自动更新检测迁移至独立专属仓库 `pazmulroneyv-alt/wzai-design-noplugin`，彻底消除与内置渠道版之间的跨版本更新串包风险。
- **包含 v1.0.1 全部核心修复**：
  - 多模态连线同侪依赖隔离（防止下游 Config 兄弟节点污染上游独立生成）；
  - `gpt-image-2.5` / `gpt-image-2.6` 自动走 `/v1/images/generations` 协议，彻底防止 New-API 网关工具重复扣费；
  - 桌面主进程直读 `/models` 绕过跨域（CORS）预检，兼容本地免 Key 接口；
  - 完整 73 项自动化测试套件验证通过（含端到端自动更新验证）。

### 安装包

| 系统 | 安装包 |
| --- | --- |
| Windows x64 | `Wanzhuan-AI-Design-Setup-1.0.2-noplugin-x64.exe` |
| Linux x64 | `Wanzhuan-AI-Design-1.0.2-noplugin-linux-amd64.deb`、`Wanzhuan-AI-Design-1.0.2-noplugin-linux-x86_64.AppImage` |
| Linux arm64 | `Wanzhuan-AI-Design-1.0.2-noplugin-linux-arm64.deb`、`Wanzhuan-AI-Design-1.0.2-noplugin-linux-arm64.AppImage` |
| macOS Intel | `Wanzhuan-AI-Design-1.0.2-noplugin-macos-x64.dmg` |
| macOS Apple Silicon | `Wanzhuan-AI-Design-1.0.2-noplugin-macos-arm64.dmg` |

### 校验值（SHA-256）

```
92a20c02659afbef37d3010f398384791119c8157a27f0db4b8711aebe1257c1  Wanzhuan-AI-Design-Setup-1.0.2-noplugin-x64.exe
c81091fd37f27b2d6ef2d5a84a2324fcfabe84aa0dd1768a645a5a99b276cb6b  Wanzhuan-AI-Design-1.0.2-noplugin-linux-amd64.deb
8f82d1d0228dc3073493bb5729dfc69f4d5ff2ab95925ca21c8fcdec2e6ffb2a  Wanzhuan-AI-Design-1.0.2-noplugin-linux-x86_64.AppImage
cb9ae85b77f1fd76fccd2e74c548e45f543ac53be771806d95241bd91cf51477  Wanzhuan-AI-Design-1.0.2-noplugin-linux-arm64.deb
4113782c3176ca294b82549a15139d97d207e58effbfbdec7b3db12399bf0e4a  Wanzhuan-AI-Design-1.0.2-noplugin-linux-arm64.AppImage
0e204a7540001bffa250a0d30dafaf5e418bbf14d16f07a110857d6cf842d69c  Wanzhuan-AI-Design-1.0.2-noplugin-macos-x64.dmg
f3ab34ed8724b52ded42895a39d1e4051b52a605e1f4fc95f1c70456c6ea802e  Wanzhuan-AI-Design-1.0.2-noplugin-macos-arm64.dmg
```

每个安装包同时附有 `.sha256` 文件，供升级入口自动校验使用。

### 局域网归档

- NAS 发布目录：`\\192.168.88.8\wz\无限画布二开\wzai-design-v1.0.2-noplugin\`
