## 玩赚AI设计工作台 v1.0.4（无内置渠道版）正式发布

玩赚 AI 设计工作台（无限画布无内置渠道版）1.0.4 正式发布，全平台支持 Windows / Linux / macOS（x64 与 arm64）。

### 主要更新

- **优化 StepAudio 3 Music 交互与前置校验（方案 A）**：
  - 明确区分「音乐风格描述（caption）」与「歌词（lyrics）」输入框职责，在画布节点与独立音频页提供按任务类型切换的提示说明（纯音乐 / 歌曲 / 翻唱 / 人声配乐）及输出时长特性提示；
  - 纯音乐模式下若主输入框为空则只读防误填，若存在已输入文本或已连接上游文本节点，在点击生成前即给出明确可操作提示并阻止提交；
  - 对「歌曲」误接参考音频及「翻唱 / 人声配乐」缺少歌词或参考音频的情况增加前置校验。
- **包含 v1.0.1 / v1.0.2 / v1.0.3 全部核心能力与修复**：
  - 独立仓库 `pazmulroneyv-alt/wzai-design-noplugin` 更新源完全隔离；
  - 升级重启自动清理遗留安装包与 `updates/state.json` 彻底消除重复提示；
  - 多模态连线同侪依赖隔离、`gpt-image-2.5/2.6` 自动防重复扣费路由、主进程直读模型列表与免 Key 本地端点兼容。

### 安装包

| 系统 | 安装包 |
| --- | --- |
| Windows x64 | `Wanzhuan-AI-Design-Setup-1.0.4-noplugin-x64.exe` |
| Linux x64 | `Wanzhuan-AI-Design-1.0.4-noplugin-linux-amd64.deb`、`Wanzhuan-AI-Design-1.0.4-noplugin-linux-x86_64.AppImage` |
| Linux arm64 | `Wanzhuan-AI-Design-1.0.4-noplugin-linux-arm64.deb`、`Wanzhuan-AI-Design-1.0.4-noplugin-linux-arm64.AppImage` |
| macOS Intel | `Wanzhuan-AI-Design-1.0.4-noplugin-macos-x64.dmg` |
| macOS Apple Silicon | `Wanzhuan-AI-Design-1.0.4-noplugin-macos-arm64.dmg` |

### 校验值（SHA-256）

```
0b4841a302cddabc733b2a89854e316a3789f067842b607829a5f0f9b6a8d4cc  Wanzhuan-AI-Design-Setup-1.0.4-noplugin-x64.exe
77c728d41fb6eee24c5b4c82f68987927cb075c1aad882f57f35e4fd938cd5db  Wanzhuan-AI-Design-1.0.4-noplugin-linux-amd64.deb
fee1c2ae38fcbf8cd341847f046094e996243d00f6293643639f0f9882943bcb  Wanzhuan-AI-Design-1.0.4-noplugin-linux-x86_64.AppImage
8ddf30fc00a511d552f22ff192d0db0a7998107f5607c30fb17f046629b6a0ff  Wanzhuan-AI-Design-1.0.4-noplugin-linux-arm64.deb
c787324c09e6a17a1c5e866d85c9bc5459e66aca73816ee2a64bffd1c4e3c264  Wanzhuan-AI-Design-1.0.4-noplugin-linux-arm64.AppImage
7d9349e605dfa5e96b62aabf2432edd994a90392a7f586271d0298e69cb549c2  Wanzhuan-AI-Design-1.0.4-noplugin-macos-x64.dmg
8ceab9325347fa34aabf908ccd50de8ffdbd0f3912ed9af72f1995b7f3cf81e1  Wanzhuan-AI-Design-1.0.4-noplugin-macos-arm64.dmg
```

每个安装包同时附有 `.sha256` 文件，供升级入口自动校验使用。

### 局域网归档

- NAS 发布目录：`\\192.168.88.8\wz\无限画布二开\wzai-design-v1.0.4-noplugin\`
