# al-skill-packs

一组打包好的 Agent 技能包，可直接用于 WorkBuddy（插件市场）、Claude Code、Cursor、Codex 等支持 `SKILL.md` 的客户端。

## 包一览

| 包 | 技能数 | 用途 | 依赖 | 许可 |
|---|---|---|---|---|
| `chatcut` | 13 | ChatCut 桌面端 AI 剪辑：素材导入、转写、配音、动效、字幕、导出 | ChatCut 桌面版 + MCP | Apache-2.0 |
| `hyperframes` | 9 | HyperFrames 视频生产：CLI、组件注册表、Figma 导入、幻灯片、反向拆解视频 | Node 22+、FFmpeg、hyperframes CLI | Apache-2.0 |
| `agent-desktop` | 6 | 通过无障碍树操作本机应用（Win/macOS/Linux） | agent-desktop CLI | Apache-2.0 |
| `craft` | 6 | Computer Use、Deep Research、cangjie-skill（拆书/视频蒸馏）、Impeccable、Hallmark | 视技能而定 | MIT / Apache-2.0 |

## 装法一：WorkBuddy 插件市场

> 需要客户端左侧有「插件」入口（部分版本未开放）。没有的话直接用装法二。

1. 左侧「插件」→ 右上 `+` → 添加插件市场
2. 地址填：`https://github.com/shuijinlens-cpu/al-skill-packs`
3. 在市场里选中要的包 → 安装（整包一次装完）

## 装法二：Claude Code / 其他客户端

```bash
git clone https://github.com/shuijinlens-cpu/al-skill-packs.git
cp -r al-skill-packs/plugins/chatcut/skills/* ~/.claude/skills/
```
或直接解压 `dist/<包名>-skillpack.zip`，把里面的 `skills/*` 拷到对应客户端的技能目录。

## 装法三：只要单个技能

```bash
npx skills add <本仓库地址>
```

## 目录结构

```
.codebuddy-plugin/marketplace.json   # 市场清单
plugins/<包名>/.codebuddy-plugin/plugin.json
plugins/<包名>/skills/<技能>/SKILL.md
dist/<包名>-skillpack.zip            # 单包 zip，给不支持市场的客户端
licenses/                            # 各上游许可证原文
```

## 来源与许可

各包内容均来自上游开源仓库，仅做目录重组，未修改技能正文。每个包目录内附 `NOTICE.md` 与 `LICENSE`。
上游：ChatCut-Inc/agent-plugin（Apache-2.0）、heygen-com/hyperframes（Apache-2.0）、
vercel-labs/agent-desktop（Apache-2.0）、stablyai/orca（MIT）、affaan-m/ECC（MIT）、
kangarooking/cangjie-skill（MIT）、pbakaus/impeccable（Apache-2.0）、Nutlope/hallmark（MIT）。

> VoiceStudio（AGPL-3.0）未包含在本仓库中。
